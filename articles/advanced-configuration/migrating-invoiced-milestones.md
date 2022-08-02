---
title: Täielikult arveldatud arvelduse verstapostide migreerimine ületõstmisel
description: Selles artiklis selgitatakse, kuidas migreerida fikseeritud hinnaga arvelduse verstaposte, mis on kliendile avatud projektilepingute eest arve esitatud enne kasutuselevõtu kuupäeva.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028697"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Täielikult arveldatud arvelduse verstapostide migreerimine ületõstmisel

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="scenario"></a>Stsenaarium

Contoso läheb Microsoftiga Dynamics 365 Project Operations otseülekandesse ressursside / varudeta stsenaariumide jaoks. Osana kärpetegevustest peab rakendusmeeskond avatud projektilepingud vanast süsteemist üle viima. Mõned projektilepingud sisaldavad lepinguridu, mis kasutavad fikseeritud hinnaga arveldusmeetodit ja mille eest on lõppkliendile juba osaliselt arve esitatud. Juurutusmeeskond peab need arvelduse verstapostid kliendiarve sisestamisena **üle** viima, kuna need tuleb tulu kajastamise eesmärgil kaasata lepingu koguväärtusse. Klientide saldosid müügireskontros ja pearaamatus ei tohi see siiski mõjutada.

## <a name="solution"></a>Lahendus

### <a name="prerequisites"></a>eeltingimused

- Dynamics 365 Finance 10.0.24 või uuem versioon.
- Keskkond, kus migreerimisetapid lõpule viiakse, peab olema hooldusrežiimis. Verstapostide ületamise ajal ei tohiks teha muid tegevusi.
- Migreerimisetappe tuleb järgida täpselt nii, nagu siin kirjeldatud, ja neid saab kasutada ainult ületõstetegevuse jaoks. Microsoft ei toeta selle võimaluse muud kasutamist.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Project Operationsi integratsioonilepingu rea verstapostide ületõsteversiooni loomine kahekordse kirjutamisega kaardil 

1. Veenduge, et üksus Project Operations integration contract rea verstapostide üksus target vastendus **oleks** ajakohane. 

    1. Avage finance jaotises **Andmehalduse** \> **andmeüksused** ja valige **üksus Project Operationsi integratsioonilepingu rea verstapostid.** 
    2. Valige **Käsk Muuda sihtvastendusi**. 
    3. **Valige lehel Kaardi koondamine sihtimiseks** suvand **Loo vastendus** ja seejärel kinnitage, et soovite vastenduse luua.

2. Peatage ja värskendage **Project Operationsi integratsiooni lepingurea verstaposte** (**msdyn\_ contractlinescheduleofvalues**) kahekordse kirjutamisega kaarti. 

    1. Avage **Andmehaldus** \> **Kahekordne kirjutamine**, valige kaart ja avage selle üksikasjad. 
    2. Valige **Stopp** ja oodake, kuni süsteem kaardi peatab. 
    3. Valige **Värskenda tabeleid**.

3. Lisage kande oleku vastendus.

    1. Valige **Lisa vastendus**.
    2. Valige uuel real **veerus** Finance and operations apps (Finants- ja operatsioonirakendused **) väli TRANSSTATUS \[TRANSSTATUS\]**.
    3. Veerus valige **Microsoft Dataverse** **msdyn\_ invoicestatus \[Arve olek\]**.
    4. **Valige veerus Kaardi tüüp** paremnool (**\>**).
    5. Valige kuvatavas dialoogiboksis väljal **Sünkroonimissuund** väärtus **Dataverse Finance and Operationsi rakendused**.
    6. Valige **Lisa teisendus**.
    7. Väljal **Teisenduse tüüp** valige **Väärtusmap**.
    8. Valige **Lisa väärtuse vastendus**.
    9. Sisestage **vasakpoolsele väljale 4**. Sisestage **parempoolsele väljale 192350001**. 
    10. Valige **Salvesta** ja seejärel sulgege dialoogiboks.

4. Topeltkirjutusega **kaardi versiooni salvestamiseks valige** Salvesta nimega. 
5. **Valige tabeli** lisamise paanil väljal **Publisher** suvand **Vaikimisi väljaandja**.
6. Sisestage **versioon väljale Versioon**.
7. Sisestage väljale **Kirjeldus** märkus kaardi selle ülelõikeversiooni kohta. 
8. Valige **Salvesta**.
9. Käivitage kaart.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Arveldatud verstapostide migreerimine Dataverse keskkonda

1. Looge keskkonnas Project Operations Dataverse verstapostid, mille arve olek **on arveldamiseks** valmis. Siinkohal ärge migreerige verstaposte, mille eest pole arvet esitatud.

    > [!NOTE]
    > Enne arvelduse verstapostide migreerimist veenduge, et projekti lepingureaga seotud finantsdimensioonid oleksid seatud ootuspäraselt. Finantsdimensioone ei saa pärast migreerimise lõpuleviimist redigeerida.

2. Kui kõik verstapostid on migreeritud, peatage järgmised kahekordselt kirjutatud kaardid:

    - Project Operations integration contract rea verstapostid (msdyn\_ contractlinescheduleofvalues)
    - Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals)
    - Projektiarve ettepanek V2 (arved)

    Kaartide peatamiseks toimige järgmiselt.

    1. Avage Finance'is **andmehaldus** \> **Topeltkirjutus**, valige kaart ja avage selle üksikasjad.
    2. Valige **Stopp** ja oodake, kuni süsteem kaardi peatab.

3. Looge ja kinnitage keskkonnas Project Operations Dataverse arvelduse verstapostide jaoks pro forma arved. 

    1. Minge saidikaardil projekti lepingute juurde, valige lepingud ja seejärel valige **Loo arved**.
    2. Pärast arvete loomist avage need saidikaardi menüüst **Arved** ja seejärel valige **Kinnita**.

    See etapp loob keskkonnas nõutavad kirjed Dataverse. Kuid see ei mõjuta finantse ja saadaolevaid arveid, kuna varem loetletud topeltkirjutusega kaardid peatati.

4. Kui kõik pro-forma arved on kinnitatud, tagastage kõik topeltkirjutusega kaardid nende algsesse olekusse.

    1. Värskendage Project Operationsi integratsioonilepingu rea verstapostide **versiooni**(**msdyn\_ contractlinescheduleofvalues**) topeltkirjutusega kaart tagasi originaalile. 
    2. Valige kaardiloendist topeltkirjutusega kaart, valige **Tabelikaardi versioon** ja seejärel valige tabelikaardi algne versioon.
    3. Valige **Salvesta**.
    4. Taaskäivitage järgmised topeltkirjutuskaardid:

        - Project Operations integration contract rea verstapostid (msdyn\_ contractlinescheduleofvalues)
        - Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals)
        - Projektiarve ettepanek V2 (arved)

Verstapostid on nüüd migreeritud ja süsteem on valmis järgmisteks sammudeks ülelõikamistegevuses.
