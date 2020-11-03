---
title: Projekti tegelike näitajate sünkroonimine otse Project Service Automationist projekti integreerimise töölehele rakendusse Finance and Operations sisestamiseks
description: Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075088"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekti tegelike näitajate sünkroonimine otse Project Service Automationist projekti integreerimise töölehele rakendusse Finance and Operations sisestamiseks

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.

Malliga sünkroonitakse tehingud rakendusest Project Service Automation koondtabelisse rakenduses Finance. Kui sünkroonimine on lõpule jõudnud, **peate** andmed koondtabelist integratsiooni töölehele importima.

> [!NOTE]
> - Projekti tegelike näitajate integreerimine on saadaval alates versioonist 8.0.1.
> - Kui kasutate rakendust Enterprise Edition 7.3.0 pärast KB 4132657 ja KB 4132660 installimist, on teil võimalik kasutada malle, et integreerida projekti tööülesanded, kuluarvestuse kategooriad, tunnihinnangud, kuluhinnangud ja tegelikud näitajad ning konfigureerida funktsioonide lukustamist. Kui te peate arvestuse jaotuse lähtestama, soovitame installida ka KB 4131710.
> - Kui kasutate versiooni 7.3.0 ja toote tasulised tehingud Project Service Automationist üle, peate installima KB 4345320, et kaasata need tasud projekti arvesse.
> - Kui sisestate rakendusse Project Service Autimation käibemaksu summasid aja- või kuluarvestuse kaudu, peate installima rakenduse Project Service Automation Update 7. Muul juhul ei lingita maksude tegelikke näitajaid seotud aja ega kulu tegelike näitajatega ja neid ei sünkroonita rakendusega Finance. Lisateabe saamiseks pöörduge tugimeeskonna poole.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Andmevoog rakendusest Project Service Automation rakendusse Finance

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt. Andmete integreerimise funktsiooniga saadaolevad integreerimismallid võimaldavad projekti tegelike andmete voogu Project Service Automationist Finance’i.

Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekti tegelikud näitajad rakendusest Project Service Automation

### <a name="template-and-tasks"></a>Mall ja ülesanded

Saadaolevatele mallidele Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt** , et valida avalikud mallid.

Projekti tegelike näitajate sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete migreerimise malli nimi:** projekti tegelike näitajate prognoosid (PSA-st Fini ja Opsi)
- **Ülesannete nimi projektis:**

    - Tegelikud näitajad
    - TransactionConnections

### <a name="entity-set"></a>Olemikogum

| Project Service Automation | Finantsid                                   |
|----------------------------|----------------------------------------------------------|
| Tegelikud näitajad                    | Integratsiooniolem projekti tegelike näitajate jaoks                   |
| Kande ühendused    | Projekti kande seoste integratsiooni olem |

### <a name="entity-flow"></a>Olemi voog

Projekti tegellikke näitajaid hallatakse rakenduses Project Service Automation ja need sünkroonitakse projekti integratsiooni töölehtedega rakenduses Finance. Raamatupidamist rakendatakse vaikefinantsdimensioonide ja sisestusseadistuste põhjal.

### <a name="prerequisites"></a>Eeltingimused

Enne, kui tegelike näitajate sünkroonimine võib ilmneda, peate konfigureerima rakenduse Project Service Automation integratsiooniparameetrid ja sünkroonima projektid, projekti tööülesanded ja projekti kulukannete kategooriad.

### <a name="power-query"></a>Power Query

Projekti tegelike näitajate mallil peate kasutama lisandmoodulit Microsoft Power Query for Excel, et lõpetada järgmised ülesanded.

- Teisendage kandetüüp rakenduses Project Service Automation sobivaks kandetüübiks rakenduses Finance. See teisendus on juba määratletud projekti tegelike näitajate (PSA kuni FIN ja Ops) mallis.
- Teisendage arvetüüp rakenduses Project Service Automation sobivaks arvetüübiks rakenduses Finance. See teisendus on juba määratletud projekti tegelike näitajate (PSA kuni FIN ja Ops) mallis. Arve tüüp vastendatakse seejärel reaatribuudiga, mis põhineb lehe **Rakenduse Project Service Automation integratsiooniparameetrid** konfiguratsioonil.
- Filtreerige kindla ressursi organisatsiooniliste üksustega, mis tuleb selle malliga sünkroonida.
- Kui kontsernisisene aeg või kontsernisisene kulu sünkroonitakse rakendusega Finance, peate muutma lepingu organisatsiooniüksuse rakenduses Finance sobivaks olemiks. Projekti tegelike näitajate (PSA to FIN ja Ops) mallis määratletakse tingimuslik veerg, mis põhineb demo andmetel. Peate viimati lisatud tingimusliku veeru värskendama õigetele juriidilistele olemitele. Vastasel juhul võib juhtuda, et integratsioon võib ilmneda või valed tegelikud tehingud saab importida rakendusse Finance.
- Kui kontsernisisest aega või kontsernisisest kulu ei sünkroonita rakendusega Finance, peate kustutama viimati lisatud tingimusliku veeru oma mallist. Vastasel juhul võib juhtuda, et integratsioon võib ilmneda või valed tegelikud tehingud saab importida rakendusse Finance.

#### <a name="contract-organizational-unit"></a>Lepingu organisatsiooniüksus
Mallis sisestatud tingimusliku veeru värskendamiseks klõpsake noolt **Vastenda** , et avada vastendamine. Valige link **Täpsem päring ja filtreerimine** , et avada Power Query.

- Kui kasutate vaikimisi projekti tegelikke näitajate (PSA-st Finile ja Opsile) malli, siis valige Power Querys jaotisest **Rakendatud sammud** viimane suvand **Sisestatud tingimus**. Kirjes **Funktsioon** asendage **USSI** juriidilise üksuse nimega, mida peaks kasutama koos integratsiooniga. Lisage **Funktsiooni** kirjele soovitud täiendavad tingimused ja värskendage **else** tingimus **USMF** -ilt õigele juriidilisele olemile.
- Kui loote uue malli, peate kontsernisisese aja ja kulude toetamiseks lisama veeru. Valige **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **LegalEntity**. Sisestage veeru jaoks tingimus, et kui **msdyn\_contractorganizationalunitid.msdyn\_nimi** on \<organizational unit\>, siis \<enter the legal entity\>; muu on tühi.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on toodud andmete integratsioonis malli ülesande vastendamise näide. Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine - tegelikud näitajad](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Malli vastendamine - kande seosed](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Koondtabelist pärast integreerimist rakendusest Project Service Automation importimine

Koondtabelist importimise perioodiline protsess tuleb käivitada pärast tegelike näitajate sünkroonimist rakendusest Project Service Automation rakendusse Finance. Selle toiminguga imporditakse projektitehingud koondtabelist projekti rakenduse Project Service Automation töölehele, kus rakendatakse raamatupidamist ja imporditud kandeid saab sisestada. Soovitame seda protsessi käivitada pakettrežiimis; soovi korral saab seadistada korduva pakett-töötluse.

## <a name="update-actuals-from-finance"></a>Tegelike näitajate värskendamine rakendusest Finance

### <a name="template-and-tasks"></a>Mall ja ülesanded

Järgmist malli ja aluseks olevaid tööülesandeid kasutatakse selleks, et sünkroonida sisestatud projektitehingutega seotud kannete arvu ja käibemaksu rakendusest Finance rakendusse Project Service Automation.

- **Andmete migreerimise malli nimi:** projekti tegelike näitajate värskendused (Fin-itt Ops-ist PSA-sse)
- **Ülesannete nimi projektis:**

    - Tegelikud näitajad 
    - TransactionConnections

### <a name="entity-set"></a>Olemikogum

| Finantsid                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integratsiooniolem projekti tegelike näitajate jaoks                   | Tegelikud näitajad                    |
| Projekti kande seoste integratsiooni olem | Kande ühendused    |

### <a name="entity-flow"></a>Olemi voog

Projekti tegellikke näitajaid hallatakse rakenduses Project Service Automation ja need sünkroonitakse projekti integratsiooni töölehtedega rakenduses Finance. Pärast tegelike näitajate sisestamist rakendusse Finance uuendatakse need rakenduses Project Service Automation koos kandenumbriga rakendusest Finance. Kui käibemaksud on lisatud rakendusse Finance, luuakse Project Service Automationis uued maksude tegelikud näitajad.

### <a name="power-query"></a>Power Query

Projekti tegelike näitajate cärskendatud mallil peate kasutama lisandmoodulit Power Query, et lõpetada järgmised ülesanded.

- Teisendage kandetüüp rakenduses Finance sobivaks kandetüübiks Project Service Automationis. See teisendus on juba määratletud projekti tegelike näitajate värskendatud (Fin Ops -ilt PSA-le) mallis.
- Teisendage arvetüüp rakenduses Finance sobivaks arvetüübiks rakenduses Project Service Automation. See teisendus on juba määratletud projekti tegelike näitajate värskendatud (Fin Ops -ilt PSA-le) mallis.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näited. Vastendus näitab välja teavet, mis sünkroonitakse Finance'ist Project Service Automationisse.

[![Malli vastendamine - tegelike näitajate värskendus](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Malli vastendamine - kane värskendus](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)