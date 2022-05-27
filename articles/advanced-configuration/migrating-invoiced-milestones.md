---
title: Täielikult arveldatud arvelduse vahe-eesmärkide migreerimine üleehitamisel
description: Selles teemas selgitatakse, kuidas migreerida fikseeritud hinnaga arvelduse vahe-eesmärgid, mis on kliendile arveldatud avatud projektilepingute eest enne kasutusaja loomise kuupäeva.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576265"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Täielikult arveldatud arvelduse vahe-eesmärkide migreerimine üleehitamisel

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="scenario"></a>Stsenaarium

Contoso läheb Microsoftiga Dynamics 365 Project Operations ressursi- ja ladustamata stsenaariumide jaoks otseülekandena. Ülelõiketegevuse raames peab rakendusmeeskond migreerima avatud projektilepingud vanast süsteemist. Mõned projektilepingud sisaldavad lepinguridu, mis kasutavad fikseeritud hinnaga arveldusmeetodit ja mis on juba osaliselt arveldatud lõpptarbijale. Juurutusmeeskond peab need arvelduse verstapostid migreerima konteeritud **kliendiarvena**, kuna need tuleb tulude kajastamise eesmärgil kaasata lepingu koguväärtusesse. Siiski ei tohi mõjutada klientide saldosid müügireskontros ja pearaamatus.

## <a name="solution"></a>Lahendus

### <a name="prerequisites"></a>eeltingimused

- Dynamics 365 Finance 10.0.24 või uuem tuleb paigaldada.
- Keskkond, kus migreerimisetapid lõpetatakse, peab olema hooldusrežiimis. Vahe-eesmärkide migreerimise ajal ei tohiks teha muid tegevusi.
- Rändesamme tuleb järgida täpselt nii, nagu siin kirjeldatud, ja neid saab kasutada ainult ülelõiketegevuseks. Microsoft ei toeta selle funktsiooni muud kasutamist.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Project Operationsi integratsioonilepingu rea vahe-eesmärkide kahe kirjutamise kaardi ülelõikeversiooni loomine 

1. Veenduge, et olemi Project Operations integration contract line milestones sihtvastendus **oleks** ajakohane. 

    1. Avage jaotises Finance **andmehaldusolemid** \> **ja** valige **olem Project Operationsi integratsioonilepingu rea vahe-eesmärgid.** 
    2. Valige **Muuda sihtvastendusi**. 
    3. **Valige lehel** Vastendamine sihtgrupini **käsk Loo vastendamine** ja seejärel kinnitage, et soovite vastenduse luua.

2. Projektitoimingute integreerimise lepingurea vahe-eesmärkide **(msdyn** contractlinelineschedule ofvalues **) kahe kirjutamiskaardi peatamine ja värskendamine\_**. 

    1. **Avage jaotis Andmehaldus** \> **Dual-write**, valige kaart ja avage selle üksikasjad. 
    2. Valige **Stopp** ja oodake, kuni süsteem kaardi peatab. 
    3. Valige **Värskenda tabeleid**.

3. Lisage kande oleku vastendus.

    1. Valige **Lisa vastendamine**.
    2. Valige uuel real veerus **Finance and Operations rakenduste** veerg **väli TRANSSTATUS \[TRANSSTATUS\]**.
    3. Valige veerus **Microsoft Dataverse** **msdyn\_ invoicestatus \[Invoice olek\]**.
    4. Valige veerus **Kaardi tüüp** paremnool (**\>**).
    5. Valige kuvatavas dialoogiboksis väljal **Sünkrooni** suund **Dataverse väärtus Finance and Operations (rakendused** Finance and Operations).
    6. Valige **Lisa teisendus**.
    7. Valige väljal **Teisenduse** tüüp **väärtusmap**.
    8. Valige **Lisa väärtuse vastendus**.
    9. Sisestage **vasakul väljal väärtus 4**. Sisestage õigele väljale **192350001**. 
    10. Valige **Salvesta** ja seejärel sulgege dialoogiboks.

4. Topeltkirjutuskaardi versiooni salvestamiseks valige **Salvesta**. 
5. Valige tabelipaani **Lisamine väljal** Avaldaja **väärtus Vaikeväljaandja** **.**
6. Sisestage väljale **Versioon** versioon.
7. Sisestage väljale **Kirjeldus** märkme selle kaardi üleehitamise versiooni kohta. 
8. Valige **Salvesta**.
9. Käivita kaart.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Arveldatud vahe-eesmärkide Dataverse migreerimine keskkonda

1. Looge keskkonnas Project Operations Dataverse vahe-eesmärgid, mille arve olek **on arveldamiseks** valmis. Sel hetkel ärge migreerige ühtegi verstaposti, mida pole arveldatud.

    > [!NOTE]
    > Enne arvelduse vahe-eesmärkide migreerimist veenduge, et projektilepingu reaga seotud finantsdimensioonid oleksid seatud ootuspäraselt. Finantsdimensioone ei saa pärast migreerimise lõpuleviimist redigeerida.

2. Kui kõik verstapostid on migreeritud, peatage järgmised topeltkirjutamise kaardid.

    - Project Operationsi integreerimise lepingurea verstapostid (msdyn\_ lepingulineschedule ofvalues)
    - Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals)
    - Projektiarve ettepanek V2 (arved)

    Kaartide peatamiseks tehke järgmist.

    1. Avage jaotises Finance **jaotis Andmehaldus** \> **Dual-write**, valige kaart ja avage selle üksikasjad.
    2. Valige **Stopp** ja oodake, kuni süsteem kaardi peatab.

3. Looge ja kinnitage keskkonnas Project Operations Dataverse arvelduse vahe-eesmärkide jaoks pro forma arved. 

    1. Avage saidikaardil projektilepingud, valige lepingud ja seejärel valige **Loo arved**.
    2. Pärast arvete loomist avage need saidikaardi menüüst **Arved** ja seejärel valige **Kinnita**.

    See samm loob keskkonnas nõutavad kirjed Dataverse. Kuid see ei mõjuta saadaolevaid finantse ja kontosid, kuna varem loetletud topeltkirjutamise kaardid peatati.

4. Kui kõik pro forma arved on kinnitatud, tagastage kõik topeltkirjutatud kaardid algsesse olekusse.

    1. **Värskendage project operationsi integratsioonilepingu rea vahe-eesmärkide** (**msdyn\_ contractlinelinescheduleofvalues**) versiooni topeltkirjutuskaardiga tagasi originaali. 
    2. Valige kaardiloendist kahe kirjutamise kaart, valige **Tabelikaardi versioon** ja seejärel valige tabelikaardi algne versioon.
    3. Valige **Salvesta**.
    4. Taaskäivitage järgmised topeltkirjutamise kaardid.

        - Project Operationsi integreerimise lepingurea verstapostid (msdyn\_ lepingulineschedule ofvalues)
        - Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals)
        - Projektiarve ettepanek V2 (arved)

Verstapostid on nüüd migreeritud ja süsteem on valmis järgmisteks sammudeks ülelõiketegevuses.
