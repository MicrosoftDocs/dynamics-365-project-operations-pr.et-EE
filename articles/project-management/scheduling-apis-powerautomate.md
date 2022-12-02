---
title: Projekti ajakava API-de kasutamine tarkvaraga Power Automate
description: See artikkel kirjeldab näidisvoogu, mis kasutab projekti ajakava rakenduse programmeerimisliidest (API-d).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404453"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projekti ajakava API-de kasutamine tarkvaraga Power Automate

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

See artikkel kirjeldab näidisvoogu, mis näitab, kuidas luua rakenduse Microsoft Power Automate abil täielikku projektiplaani, kuidas luua Toimingukomplekti ja kuidas värskendada olemit. Näide näitab, kuidas luua projekti, projektimeeskonna liiget, toimingukomplekte, projekti tööülesandeid ja ressursi määramist. See artikkel kirjeldab ka olemi värskendamist ja Toimingukomplekti käivitamist.

Järgmine on täielik loetelu etappidest, mis on dokumenteeritud käesoleva artikli näidisvoos.

1. [Looge PowerApps päästik](#1)
2. [Projekti loomine](#2)
3. [Meeskonnaliikme muutuja lähtestamine](#3)
4. [Üldise meeskonnaliikme loomine.](#4)
5. [Toimingukomplekti loomine](#5)
6. [Projekti salve loomine](#6)
7. [Lingi oleku muutuja lähtestamine](#7)
8. [Ülesannete arvu muutuja lähtestamine](#8)
9. [Projekti ülesande ID muutuja lähtestamine](#9)
10. [Tehke kuni](#10)
11. [Projekti ülesande määramine](#11)
12. [Projekti ülesande loomine](#12)
13. [Ressursimääramise loomine](#13)
14. [Muutuja vähendamine](#14)
15. [Projekti ülesande ümbernimetamine](#15)
16. [Toimingukomplekti käivitamine](#16)

## <a name="assumptions"></a>Oletused

See artikkel eeldab, et teil on põhiteadmised Dataverse platvormi, pilvevoogude ja projekti ajakava rakendusliidese (API) kohta. Lisateabe saamiseks vaadake selle artikli hilisemat jaotist [Viited](#references).

## <a name="create-a-flow"></a>Voo loomine

### <a name="select-an-environment"></a>Valige keskkond

Saate luua oma keskkonnas Power Automate voo.

1. Minge aadressile <https://flow.microsoft.com> ja kasutage sisselogimiseks oma administraatori identimisteavet.
2. Valige paremas ülanurgas **Keskkonnad**.
3. Valige loendist keskkond, kuhu rakendus Dynamics 365 Project Operations on installitud.

### <a name="create-a-solution"></a>Lahenduse loomine

Järgige neid etappe, et luua [lahendusteadlik voog](/power-automate/overview-solution-flows). Lahendusteadliku voo loomisega saate voo hõlpsamini eksportida, et seda hiljem kasutada.

1. Valige navigeerimispaanil **Lahendused**.
2. Lehel **Lahendused** valige **Uus lahendus**.
3. Dialoogiboksis **Uus lahendus** määrake nõutud väljad ja seejärel valige **Loo**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1. etapp: PowerAppsi käivitaja loomine

1. Valige lehel **Lahendused** loodud lahendus ja seejärel **Uus**.
2. Valige vasakpoolsel paanil **Pilvevood** \> **Automatiseerimine** \> **Pilvevoog** \> **Vahetu**.
3. Sisestage väljale **Voo nimi** field, enter **API demo voo ajastamine**.
4. Loendis **Kuidas selle voo käivitamist valida** valige **Power Apps**. Kui loote Power Appsi päästiku, on loogika teie kui autori otsustada. Selles artiklis jätke testimise eesmärgil sisendparameetrid tühjaks.
5. Valige käsk **Loo**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. etapp: looge projekt

Näidisprojekti loomiseks järgige neid etappe.

1. Valige loodud voos **Uus etapp**.

    ![Uue etapi lisamine.](media/newstep.png)

2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.

    ![Toimingu valimine.](media/chooseactiontab.png)

3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.

![Etapi ümbernimetamine.](media/renamestep.png)

4. Nimetage etapp **Projekti loomine** ümber.
5. Valige väljal **Tegevuse nimi** **msdyn\_CreateProjectV1**.
6. Tehke väljal **msdyn\_subject** valik **Dünaamilise sisu lisamine**.
7. Sisestage vahekaardi **Avaldis** funktsiooniväljale **Projekti nimi - utcNow()**.
8. Valige **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3. etapp: Meeskonnaliikme muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Tehingu valimine** otsinguväljale **muutuja lähtestamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Initi meeskonnaliige** ümber.
5. Sisestage väljale **Nimi** **TeamMemberAction**.
6. Valige väljal **Tüüp** **String**.
7. Sisestage väljale **Väärtus** **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. etapp: Üldise meeskonnaliikme loomine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Meeskonnaliikme loomine** ümber.
5. Valige välja **Tegevuse nimi** jaoks **TeamMemberAction** dialoogiboksis **Dünaamiline sisu**.
6. Sisestage väljale **Tegevuse parameetrid** järgmine parameetriteave.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Siin on parameetrite selgitus:

    - **\@\@odata.type** – Olemi nimi. Näiteks sisestage **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Projektimeeskonna ID primaarvõti. Väärtus on globaalse ainuidentifikaatori (GUID) avaldis.   ID genereeritakse avaldise vahekaardilt.

    - **msdyn\_project\@odata.bind** – Omanikprojekti projekti ID. Väärtus on dünaamiline sisu, mis tuleneb etapi „Projekti loomine“ vastusest. Sisestage kindlasti kogu tee ja lisage sulgude vahele dünaamiline sisu. Jutumärgid on nõutud. Näiteks sisestage **"/msdyn\_projects(DÜNAAMILISE SISU LISAMINE)"**.
    - **msdyn\_name** – kasutatud meeskonnaliikme nimi. Näiteks sisestage **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5. etapp: Toimingukomplekti loomine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Toimingukomplekti loomine** ümber.
5. Valige väljal **Tegevuse nimi** kohandatud tegevus **msdyn\_CreateOperationSetV1** Dataverse.
6. Sisestage väljale **Kirjeldus** **ScheduleAPIDemoOperationSet**.
7. Sisestage väljale **Projekt** **/msdyn\_projects(**.
8. Dialoogiboksis **Dünaamiline sisu** valige **msdyn\_CreateProjectV1Response ProjectId**.
9. Sisestage väljale **Projekt** **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. etapp: Projekti salve loomine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Tehingu valimine** otsinguväljale **uue rea lisamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Salve loomine** ümber.
5. Valige väljal **Tabeli nimi** **Projekti salved**.
6. Sisestage väljale **Nimi** **ScheduleAPIDemoBucket1**.
7. Välja **Projekt** jaoks valige **msdyn\_CreateProjectV1Response ProjectId** dialoogiboksis **Dünaamiline sisu**. 

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7. etapp: lingi oleku muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Tehingu valimine** otsinguväljale **muutuja lähtestamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Init linkstatus** ümber.
5. Sisestage väljale **Nimi** **linkstatus**.
6. Valige väljal **Tüüp** **Täisarv**.
7. Sisestage väljale **Väärtus** **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8. etapp: Ülesannete arvu muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Tehingu valimine** otsinguväljale **muutuja lähtestamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Init tööülesannete arv** ümber.
5. Sisestage väljale **Nimi** **ülesannete arv**.
6. Valige väljal **Tüüp** **Täisarv**.
7. Sisestage väljale **Väärtus** **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9. etapp: Projekti ülesande ID muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Tehingu valimine** otsinguväljale **muutuja lähtestamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Init ProjectTaskID** ümber.
5. Sisestage väljale **Nimi** **ülesannete arv**.
6. Valige väljal **Tüüp** **String**.
7. Sisestage avaldise koostaja väljale **Väärtus** **guid()**.

## <a name="step-10-do-until"></a><a id="10"></a>10. etapp: Tehke kuni

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **tehke kuni**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Määrake tingimuslause esimeseks väärtuseks muutuja **ülesannete arv** dialoogiboksis **Dünaamiline sisu**.
4. Määrake tingimuseks **vähem kui võrdne**.
5. Seadke tingimuslause teiseks väärtuseks **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11. etapp: Projekti ülesande määramine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **muutuja määramine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Uues etapis valige kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **Projekti ülesande määramine** ümber.
5. Valige väljal **Nimi** **msdyn\_projecttaskid**.
6. Sisestage avaldise koostaja väljale **Väärtus** **guid()**.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. etapp: Projekti ülesande loomine

Järgige neid etappe, et luua projektiülesanne, millel on praegusele projektile ja teie loodud projektisalvele kuuluv kordumatu ID.

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Selles etapis valige kolmikpunkt (**...**) ja seejärel **Nimeta ümber**.
4. Nimetage etapp **Projekti ülesande loomine** ümber.
5. Valige väljal **Tegevuse nimi** **msdyn\_PssCreateV1**.
6. Sisestage paneelil **Olem** järgmine parameetri teave.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Siin on parameetrite selgitus:

    - **\@\@odata.type** – Olemi nimi. Näiteks sisestage **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Ülesande kordumatu ID. Väärtuseks tuleks määrata dünaamiline muutuja alates **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – Omanikprojekti projekti ID. Väärtus on dünaamiline sisu, mis tuleneb etapi „Projekti loomine“ vastusest. Sisestage kindlasti kogu tee ja lisage sulgude vahele dünaamiline sisu. Jutumärgid on nõutud. Näiteks sisestage **"/msdyn\_projects(DÜNAAMILISE SISU LISAMINE)"**.
    - **msdyn\_teema** – Mis tahes ülesande nimi.
    - **msdyn\_projectbucket\@odata.bind** – Projektisalv, mis sisaldab ülesandeid. Väärtus on dünaamiline sisu, mis tuleneb etapi „Salve loomine“ vastusest. Sisestage kindlasti kogu tee ja lisage sulgude vahele dünaamiline sisu. Jutumärgid on nõutud. Näiteks sisestage **"/msdyn\_projectbuckets(DÜNAAMILISE SISU LISAMINE)"**.
    - **msdyn\_start** – Alguskuupäeva dünaamiline sisu. Näiteks homset tähistatakse kui **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Ajastatud alguskuupäev. Näiteks homset tähistatakse kui **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Ajastatud lõppkuupäev. Valige kuupäev tulevikus. Näiteks määrake **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Lingi olek. Näiteks sisestage **"192350000"**.

7. Välja **OperationSetId** jaoks valige **msdyn\_CreateOperationSetV1Response** dialoogiboksis **Dünaamiline sisu**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13. etapp: Ressursi määramise loomine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Selles etapis valige kolmikpunkt (**...**) ja seejärel **Nimeta ümber**.
4. Nimetage etapp **Ülesande loomine** ümber.
5. Valige väljal **Tegevuse nimi** **msdyn\_PssCreateV1**.
6. Sisestage paneelil **Olem** järgmine parameetri teave.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Välja **OperationSetId** jaoks valige **msdyn\_CreateOperationSetV1Response** dialoogiboksis **Dünaamiline sisu**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14. etapp: Muutuja vähendamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu eemaldamine** otsinguväljale **muutuja vähenemine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Valige väljale **Nimi** **ülesannete arv**.
4. Sisestage väljale **Väärtus** **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. etapp: Projekti ülesande ümbernimetamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Selles etapis valige kolmikpunkt (**...**) ja seejärel **Nimeta ümber**.
4. Nimetage etapp **Projekti ülesande ümbernimetamine** ümber.
5. Valige väljal **Tegevuse nimi** **msdyn\_PssUpdateV1**.
6. Sisestage paneelil **Olem** järgmine parameetri teave.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Välja **OperationSetId** jaoks valige **msdyn\_CreateOperationSetV1Response** dialoogiboksis **Dünaamiline sisu**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16. etapp: Toimingukomplekti käivitamine

1. Valige voos **Uus samm**.
2. Sisestage dialoogiboksi **Toimingu valimine** otsinguväljale **sidumata toimingu sooritamine**. Seejärel valige vahekaardil **Toimingud** tulemuste loendist toiming.
3. Selles etapis valige kolmikpunkt (**...**) ja seejärel **Nimeta ümber**.
4. Nimetage etapp **Toimingukomplekti täitmine** ümber.
5. Valige väljal **Tegevuse nimi** **msdyn\_ExecuteOperationSetV1**.
6. Välja **OperationSetId** jaoks valige **msdyn\_CreateOperationSetV1Response OperationSetId** dialoogiboksis **Dünaamiline sisu**.

## <a name="references"></a>Viited

- [Ülevaade voogude integreerimisest Dataverse’iga - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](schedule-api-preview.md)
- [Pilvevoogude ülevaade – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Lahenduseteadlike voogude ülevaade – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
