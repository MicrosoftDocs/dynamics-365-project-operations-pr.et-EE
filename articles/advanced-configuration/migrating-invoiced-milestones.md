---
title: Täielikult arveldatud arvelduse etappide migreerimine ülemineku ajal
description: See artikkel selgitab, kuidas migreerida fikseeritud hinnaga arveldamise vahekokkuvõtteid, mis on kliendile avatud projektilepingute eest enne käivituskuupäeva arvele pandud.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Täielikult arveldatud arvelduse etappide migreerimine ülemineku ajal

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

## <a name="scenario"></a>Stsenaarium

Contoso hakkab kasutama rakendust Microsoft Dynamics 365 Project Operations ressurssi-/mittelaopõhiste stsenaariumide jaoks. Osana üleminekutegevusest peab rakendusmeeskond migreerima avatud projektilepingud vanast süsteemist. Mõned projektilepingud sisaldavad lepinguridu, mille puhul kasutatakse fikseeritud hinnaga arveldusmeetodit ja mille kohta on lõpptarbijale juba osaliselt arve esitatud. Rakendusmeeskond peab need arveldamise vahekokkuvõtted üle viima kui **Kliendiarve postitatud**, sest need tuleb tulude kajastamiseks lisada lepingu koguväärtusesse. See ei tohi aga mõjutada klientide saldosid müügireskontros ja pearaamatus.

## <a name="solution"></a>Lahendus

### <a name="prerequisites"></a>eeltingimused

- Paigaldatud peab olema rakendus Dynamics 365 Finance 10.0.24 või uuem versioon.
- Keskkond, kus migratsioonietapid viiakse lõpule, peab olema hooldusrežiimis. Vahekokkuvõtete migreerimise ajal ei tohi teha muid tegevusi.
- Migratsioonietappe tuleb järgida täpselt nii, nagu siin kirjeldatud, ja neid saab kasutada ainult üleminekutoimingu puhul. Microsoft ei toeta selle võimaluse muud kasutamist.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Looge rakenduse Project Operations integratsioonilepingu rea vahekokkuvõtete topeltkirjutuse kaart. 

1. Veenduge, et olemi **Project Operationsi integratsioonilepingu rea vahekokkuvõtted** sihtmärkide kaardistamine on ajakohane. 

    1. Minge finantssüsteemis **Andmehaldus** \> **Andmeolemid** ja valige olem **Project Operationsi integreerimislepingu rea vahekokkuvõtted**. 
    2. Valige **Muuda sihtmärgi vastendusi**. 
    3. Lehel **Sihtmärgi vastendamine** valige **Vastenduse loomine** ja seejärel kinnitage, et soovite vastenduse luua.

2. Peatage ja värskendage topeltkirjutuse kaarti **Project Operationsi integreerimislepingu rea vahekokkuvõtted** (**msdyn\_contractlinescheduleofvalues**). 

    1. Minge loendisse **Andmehaldus** \> **Topeltkirjutus**, valige kaart ja avage selle üksikasjad. 
    2. Valige **Stop** ja oodake, kuni süsteem kaardi peatab. 
    3. Valige **Tabelite värskendamine**.

3. Tehingu oleku vastenduse lisamine.

    1. Valige **Vastendamise lisamine**.
    2. Valige uuel real veerus **Finants- ja äritoimingute rakendused** väli **TRANSSTATUS \[TRANSSTATUS\]** field.
    3. Veerus **Microsoft Dataverse** valige **msdyn\_invoicestatus \[Arve olek\]**.
    4. Valige veerus **Kaardi tüüp** parempoolne nool (**\>**).
    5. Ilmuvas dialoogiboksis valige väljal **Sünkroniseerimise suund** valik **Dataverse Finants- ja äritoimingute rakendustele**.
    6. Valige suvand **Transformeerimise lisamine**.
    7. Valige väljal **Transformeerimise tüüp** väärtus **ValueMap**.
    8. Valige **Väärtuste vastendamise lisamine**.
    9. Sisestage vasakpoolsele väärtusväljale **4**. Sisestage parempoolsele väärtusväljale **192350001**. 
    10. Valige nupp **Salvesta** ja seejärel sulgege dialoogiboks.

4. Valige **Salvesta kui**, et salvestada topeltkirjutuskaardi versioon. 
5. Paanis **Tabeli lisamine** valige **Väljaandja** väljal **Vaikeväljaandja**.
6. Sisestage väljale **Versioon** versioon.
7. Väljale **Kirjeldus** sisestage märkus selle vastendamise lõikeversiooni kohta. 
8. Valige **Salvesta**.
9. Vastendamise alustamine.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Arveldatud vahekokkuvõtete migreerimine Dataverse keskkonda

1. Looge rakenduse Project Operations Dataverse keskkonnas vahekokkuvõtted, mille arvete olek on **Valmis arvete esitamiseks**. Sel hetkel ärge migreerige ühtegi vahekokkuvõtet, mille eest ei ole arvet esitatud.

    > [!NOTE]
    > Enne arvete vahekokkuvõtete migreerimist veenduge, et projekti lepingureaga seotud finantsdimensioonid on seatud ootuspäraselt. Finantsdimensioone ei saa pärast migratsiooni lõpuleviimist muuta.

2. Kui kõik vahekokkuvõtted on migreeritud, lõpetage järgmised topeltkirjutuskaardid:

    - Project Operationsi integratsiooni lepingurea vahekokkuvõtted (msdyn\_contractlinescheduleofvalues)
    - Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals)
    - Projektiarve ettepanek V2 (arved)

    Vastendamiste peatamiseks järgige järgmisi samme:

    1. Rahanduses minge **Andmehaldus** \> **Topeltkirjutus**, valige kaart ja avage selle üksikasjad.
    2. Valige **Stop** ja oodake, kuni süsteem kaardi peatab.

3. Looge ja kinnitage Project Operations Dataverse keskkonnas näidisarveid arvete vahekokkuvõtete kohta. 

    1. Minge saidikaardil projekti lepingutesse, valige lepingud ja seejärel **Arvete loomine**.
    2. Kui arved on loodud, avage need saidikaardil menüüst **Arved** ja valige seejärel **Kinnita**.

    See etapp loob vajalikud kirjed Dataverse keskkonnas. See ei mõjuta siiski finantse ja müügireskontrot, sest varem loetletud topeltkirjutuskaardid peatati.

4. Pärast seda, kui kõik näidisarved on kinnitatud, tagastage kõik topeltkirjutuskaardid algsesse olekusse.

    1. Värskendage rakenduse **Project Operations integratsiooni lepinguridade vahekokkuvõtete** (**msdyn\_contractlinescheduleofvalues**) topeltkirjutuskaardi versioon tagasi originaalile. 
    2. Valige kaardiloendis topeltkirjutuskaart, valige **Tabelikaardi versioon**, ja seejärel valige tabelikaardi originaalversioon.
    3. Valige **Salvesta**.
    4. Taaskäivitage järgmised topeltkirjutuskaardid:

        - Project Operationsi integratsiooni lepingurea vahekokkuvõtted (msdyn\_contractlinescheduleofvalues)
        - Project Operationsi integreerimise tegelikud andmed (msdyn\_actuals)
        - Projektiarve ettepanek V2 (arved)

Vahekokkuvõtted on nüüdseks migreeritud ja süsteem on valmis üleminekutegevuse järgmisteks etappideks.
