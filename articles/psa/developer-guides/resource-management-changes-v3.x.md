---
title: Ressursihalduse muudatused (Project Service Automation 3.x)
description: Selles teemas antakse teavet ressursihalduse alas tehtud muudatuste kohta.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148638"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Ressursihalduse muudatused (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Selle teema jaotised annavad teavet rakenduse Dynamics 365 Project Service Automation versioon 3.x ressursihalduse alas tehtud muudatuste kohta.

## <a name="project-estimates"></a>Projekti prognoosid

Selle asemel, et võtta aluseks olem **msdyn\_projecttask** (**Projekti ülesanne**), põhinevad projekti prognoosid olemil **msdyn\_resourceassignment** (**Ressursi määramine**). Ressursi määramised on muutunud ülesannete kavandamise ja hinnakujunduse juures nö tõe allikaks.

## <a name="line-tasks"></a>Reaülesanded

Rakenduses PSA 3.x on reaülesanded aegunud (iganenud). Määramised viitavad nüüd kogu ülesandele, mitte reaülesannetele.

Järgmises näites kirjeldatakse, kuidas ülesanne, mille nimi on „Testülesanne”, määratakse meeskonnaliikmetele A ja B PSA varasemates versioonides ja PSA versioonis 3.x.

- **Enne PSA versiooni 3.x.**

    - Testülesanne

        - Testülesanne – reaülesanne 1

            - Määramine liikmele A

        - Testülesanne – reaülesanne 2

            - Määramine liikmele B

- **Versioonis PSA 3.x.**

    - Testülesanne

        - Määramine liikmele A
        - Määramine liikmele B

## <a name="unassigned-assignment"></a>Määramata määramine

PSA versioonis 3.x on määramata määramine selline määramine, mis on määratud meeskonnaliikmele **NULL** ja ressursile **NULL**. Määramata määramised võivad ilmneda paari stsenaariumi korral.

- Kui ülesanne on loodud, kuid see pole veel ühelegi meeskonnaliikmele määratud, luuakse alati määramata määramine. 
- Kui kõik ülesandele määratud isikud eemaldatakse, luuakse selle ülesande jaoks määramata määramine uuesti.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Väljade ajastamine olemis Projekti ülesanne

Olemi **msdyn\_projecttask** väljad on aegunud või teisaldatud olemisse **msdyn\_resourceassignment** või viidatakse neile nüüd olemist **msdyn\_projectteam** (**Projektimeeskonna liige**).

| Aegunud väli olemis msdyn\_projecttask (Projekti ülesanne) | Uus väli olemis msdyn\_resourceassignment (Ressursi määramine) | Kommentaar |
|---|---|---|
| msdyn\_assignedresources | Pole | |
| msdyn\_assignedteammembers | Pole | |
| msdyn\_numberofresources | Pole | |
| msdyn\_scheduledhours | Pole | |
| msdyn\_effortcontour | msdyn\_plannedwork | Väljal talletatud JavaScript objektiesituse (JSON) andmestruktuuri vormingut on muudetud. |

## <a name="schedule-contour"></a>Ajakava kontuur

Ajakava kontuuri talletatakse iga olemi **Ressursi määramine** (**msdyn\_resourceassignment**) puhul väljal **Plaanitud töö** (**msdyn\_plannedwork**).

### <a name="structure"></a>Struktuur

Ajakava kontuuri uus struktuur koosneb paindlikest ajasektoritest, mis on määratletud ajakava iga päeva jaoks. Igal ajasektoril on järgmised atribuudid.

- **Algus** – päeva töötundide algus projektikalendri järgi.
- **Lõpp** – päeva töötundide lõpp projektikalendri järgi.
- **Tunnid** – päevale määratud tundide arv.

**Näide**

Selles näites kasutatakse projektikalendrit, kus tööpäev kestab 9–17ni ajavööndis UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automaatne plaanimine ja käsitsi plaanimine

Kui ülesanne ajastatakse automaatselt, on tunnid langevalt ja ülesande kestust võidakse vähendada.

**Näide**

Järgmine ülesanne plaaniti automaatselt 18 tunniks kolme päeva jooksul (3. detsembrist 2018 kuni 5. detsembrini 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Kui ülesanne plaanitakse käsitsi, jaotatakse tunnid ühtlaselt kõigile kuupäevadele.

**Näide**

Järgmine ülesanne plaaniti käsitsi 18 tunniks kolme päeva jooksul (3. detsembrist 2018 kuni 5. detsembrini 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Määramise ühik

Määramise ühik on PSA versioonis 3.x kasutuselt kõrvaldatud. Ülesande panusetunnid on nüüd võrdselt päeva kaupa jaotatud kõigi määratud ressursside vahel.

**Näide**

Selles näites on ülesanne määratud kahele ressursile ja see on automaatselt ajastatud 36 tunniks kolme päeva jooksul (3. detsembrist 2018 kuni 5. detsembrini 2018).

- Määramine 1

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Määramine 2

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Hinnadimensioonid

PSA versioonis 3.x on ressursikohased hinnadimensiooni väljad (nt **Roll** ja **Organisatsiooniüksus**) olemist **msdyn\_projecttask** eemaldatud. Neid välju saab nüüd projekti prognooside loomisel tuua vastavast ressursi määramise (**msdyn\_resourceassignment**) projektimeeskonna liikmest (**msdyn\_projectteam**). Olemisse **msdyn\_projectteam** on lisatud uus väli **msdyn\_organizationalunit**.

| Aegunud väli olemis msdyn\_projecttask (Projekti ülesanne) | Väi olemist msdyn\_projectteam (Projektimeeskonna liige), mida selle asemel kasutatakse |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontuurid

Hinnakujunduse ja hindamise kontuuriväljad on olemis **msdyn\_projecttask** kasutuselt kõrvaldatud. Need on teisaldatud olemisse **msdyn\_resourceassignment**.

| Aegunud väli olemis msdyn\_projecttask (Projekti ülesanne) | Uus väli olemis msdyn\_resourceassignment (Ressursi määramine) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Järgmised väljad on lisatud olemisse **msdyn\_resourceassignment**.

* msdyn\_plannedcost
* msdyn\_plannedsales

Järgmised plaanitud, tegelike ja ülejäänud kulude ja müügi väljad on olemis **msdyn\_projecttask** muutmata.

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]