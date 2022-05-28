---
title: Projekti ajakava API-de kasutamine koos Power Automate
description: See teema pakub näidisvoogu, mis kasutab Projecti ajakava rakenduste programmeerimisliidesi (API-sid).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597701"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projekti ajakava API-de kasutamine koos Power Automate

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Selles teemas kirjeldatakse näidisvoogu, mis näitab, kuidas luua täielik projektiplaan toimingukomplekti loomise ja olemi värskendamise abil Microsoft Power Automate. Näites kirjeldatakse, kuidas luua projekt, projektimeeskonna liige, operatsioonikomplektid, projektiülesanded ja ressursimäärangud. Selles teemas selgitatakse ka olemi värskendamist ja toimingukomplekti käivitamist.

Järgnevalt on toodud täielik loend toimingutest, mis on dokumenteeritud selle teema näidisvoos.

1. [Päästiku loomine PowerApps](#1)
2. [Projekti loomine](#2)
3. [Meeskonnaliikme muutuja lähtestamine](#3)
4. [Üldise meeskonnaliikme loomine](#4)
5. [Toimingukomplekti loomine](#5)
6. [Projekti ämbri loomine](#6)
7. [Lingi oleku muutuja lähtestamine](#7)
8. [Ülesannete arvu muutuja lähtestamine](#8)
9. [Projektiülesande ID muutuja lähtestamine](#9)
10. [Tee, kuni](#10)
11. [Projektiülesande seadmine](#11)
12. [Projektiülesande loomine](#12)
13. [Ressursimäärangu loomine](#13)
14. [Muutuja vähendamine](#14)
15. [Projektiülesande ümbernimetamine](#15)
16. [Toimingukomplekti käivitamine](#16)

## <a name="assumptions"></a>Eeldused

See teema eeldab, et teil on põhiteadmised Dataverse platvormist, pilvevoogudest ja projekti ajakava rakenduse programmeerimisliidest (API). Lisateavet leiate selle teema hilisemast jaotisest [Viited](#references).

## <a name="create-a-flow"></a>Voo loomine

### <a name="select-an-environment"></a>Valige keskkond

Saate luua Power Automate voolu oma keskkonnas.

1. <https://flow.microsoft.com> Avage väärtus ja kasutage sisselogimiseks administraatori mandaati.
2. Valige paremas ülanurgas **Keskkonnad**.
3. Valige loendist keskkond, kuhu Dynamics 365 Project Operations on installitud.

### <a name="create-a-solution"></a>Lahenduse loomine

Lahenduseteadliku voo loomiseks [järgige neid juhiseid](/power-automate/overview-solution-flows). Lahenduseteadliku voo loomisega saate voo hõlpsamini eksportida, et seda hiljem kasutada.

1. Valige navigeerimispaanil **Lahendused**.
2. **Valige lehel Lahendused** suvand **Uus lahendus**.
3. Seadke dialoogiboksis **Uus lahendus** vajalikud väljad ja seejärel valige **Loo**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. samm: päästiku loomine PowerApps

1. **Valige lehel Lahendused** loodud lahendus ja seejärel valige **Uus**.
2. Valige vasakpoolsel paanil **Pilvevoogude** \> **automatiseerimise** \> **pilvevoog** \> **Kohene.**
3. Sisestage väljale **Voo nimi** väärtus Aja API demovoog **.**
4. **Valige loendis Vali, kuidas seda voo** käivitada, suvand **Power Apps**. Päästiku loomisel Power Apps sõltub loogika sinust kui autorist. Selles teemas jätke sisendparameetrid testimiseks tühjaks.
5. Valige käsk **Loo**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. etapp: looge projekt

Näidisprojekti loomiseks järgige neid juhiseid.

1. Valige loodud **voos Uus samm**.

    ![Uue sammu lisamine.](media/newstep.png)

2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.

    ![Operatsiooni valimine.](media/chooseactiontab.png)

3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.

![Nimetan sammu ümber.](media/renamestep.png)

4. Nimetage samm **Projekti loomine ümber**.
5. Valige väljal **Tegevuse** nimi **väärtus msdyn\_ CreateProjectV1**.
6. Valige väljal **msdyn\_ teema** **käsk Lisa dünaamiline sisu**.
7. Sisestage **vahekaardi Avaldis** funktsiooniväljale **projekti nimi - utcNow()**.
8. Valige **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. samm: meeskonnaliikme muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale lähtestamismuutuja**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Ümber Initi meeskonna liige**.
5. Sisestage väljale **Nimi** **väärtus TeamMemberAction**.
6. Valige väljal **Liik** **nupp String**.
7. Sisestage väljale **Väärtus** väärtus **väärtus msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. samm: üldise meeskonnaliikme loomine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Meeskonna liikme** loomine ümber.
5. Väljal **Tegevuse nimi** valige **dialoogiboksis** Dünaamiline sisu **käsk TeamMemberAction**.
6. Sisestage väljale **Toiminguparameetrid** järgmine parameetriteave.

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

    - **\@\@ odata.type** – olemi nimi. Näiteks sisestage **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – projektimeeskonna ID peamine võti. Väärtus on globaalse ainuidentifikaatori (GUID) avaldis.   ID luuakse avaldise vahekaardilt.

    - **msdyn\_ projekt\@ odata.bind** – Omamisprojekti projekti ID. Väärtus on dünaamiline sisu, mis tuleneb sammu "Loo projekt" vastusest. Veenduge, et sisestate kogu tee ja lisate sulgude vahele dünaamilise sisu. Jutumärgid on vajalikud. Näiteks sisestage **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyni\_ nimi** – Meeskonnaliikme nimi. Näiteks sisestage **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. samm: toimingukomplekti loomine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Toimingukomplekti** loomine ümber.
5. Valige väljal **Tegevuse** nimi **kohandatud toiming msdyn\_ CreateOperationSetV1** Dataverse.
6. Sisestage väljale **Kirjeldus** **väärtus ScheduleAPIDemoOperationSet**.
7. Sisestage väljale **Projekt** /msdyn **projektid(\_.**
8. Valige dialoogiboksis **Dünaamiline sisu** suvand **msdyn\_ CreateProjectV1Response ProjectId**.
9. Sisestage **väljale** Projekt **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. samm: projekti ämbri loomine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale lisa uus rida**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Ümber Loo kopp**.
5. Valige väljal **Tabeli nimi** suvand **Projektiämbrid**.
6. Sisestage väljale **Nimi** **väärtus ScheduleAPIDemoBucket1**.
7. Valige väljal **Projekt** **dialoogiboksis Dünaamiline sisu\_ käsk msdyn** **CreateProjectV1Response ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. samm: lingi oleku muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale lähtestamismuutuja**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Ümber Init linkstatus**.
5. Sisestage **väljale** Nimi **linktatus**.
6. Valige väljal **Liik** suvand **Täisarv**.
7. Sisestage **väljale** Väärtus **väärtus 192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. samm: ülesannete arvu muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale lähtestamismuutuja**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Ümber Init Ülesannete** arv.
5. Sisestage **väljale** Nimi **ülesannete** arv.
6. Valige väljal **Liik** suvand **Täisarv**.
7. Sisestage **väljale** Väärtus **väärtus väärtus 5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. samm: projektiülesande ID muutuja lähtestamine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale lähtestamismuutuja**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **ümber Init ProjectTaskID**.
5. Sisestage **väljale** Nimi **ülesannete** arv.
6. Valige väljal **Liik** **nupp String**.
7. Sisestage väljale **Väärtus** **avaldisekoosturisse guid().**

## <a name="step-10-do-until"></a><a id="10"></a> 10. samm: tehke kuni

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale käsk Tee kuni**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Määrake tingimusvälja **sätte esimene väärtus dialoogiboksi Dünaamiline** sisu **muutujaks muutuvate ülesannete** arvule.
4. Määrake tingimus väiksemaks **kui** võrdne.
5. Määrake tingimusväljavõtte teise väärtuse väärtuseks **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. samm: projektiülesande seadmine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale käsk Sea muutuja**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Projektiülesande seadmine** ümber.
5. Valige väljal **Nimi** **väärtus msdyn\_ projecttaskid**.
6. Sisestage väljale **Väärtus** **avaldisekoosturisse guid().**

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. samm: projektiülesande loomine

Järgige neid juhiseid, et luua projektiülesanne, millel on kordumatu ID, mis kuulub praegusesse projekti ja teie loodud projektiämbrisse.

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige juhises kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Projektiülesande** loomine ümber.
5. Valige väljal **Tegevuse** nimi **väärtus msdyn\_ PssCreateV1**.
6. Sisestage väljale **Olem** järgmine parameetriteave.

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

    - **\@\@ odata.type** – olemi nimi. Näiteks sisestage **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – ülesande unikaalne ID. Väärtus tuleks seada dünaamilisele muutujale **msdyn\_ projecttaskidist**.
    - **msdyn\_ projekt\@ odata.bind** – Omamisprojekti projekti ID. Väärtus on dünaamiline sisu, mis tuleneb sammu "Loo projekt" vastusest. Veenduge, et sisestate kogu tee ja lisate sulgude vahele dünaamilise sisu. Jutumärgid on vajalikud. Näiteks sisestage **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ subjekt** – iga ülesande nimi.
    - **msdyn\_ projectbucket\@ odata.bind** – Projekti ämber, mis sisaldab ülesandeid. Väärtus on dünaamiline sisu, mis tuleneb sammu "Loo ämber" vastusest. Veenduge, et sisestate kogu tee ja lisate sulgude vahele dünaamilise sisu. Jutumärgid on vajalikud. Näiteks sisestage **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – dünaamiline sisu alguskuupäevaks. Näiteks homme on esindatud kui **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – planeeritud alguskuupäev. Näiteks homme on esindatud kui **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – planeeritud lõppkuupäev. Valige tulevikus kuupäev. Näiteks määrake **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – lingi olek. Näiteks sisestage **"192350000"**.

7. Valige väljal **OperationSetId** **dialoogiboksis Dünaamiline sisu\_ käsk msdyn** **CreateOperationSetV1Response**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. samm: ressursimäärangu loomine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige juhises kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Loo määramine** ümber.
5. Valige väljal **Tegevuse** nimi **väärtus msdyn\_ PssCreateV1**.
6. Sisestage väljale **Olem** järgmine parameetriteave.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Valige väljal **OperationSetId** **dialoogiboksis Dünaamiline sisu\_ käsk msdyn** **CreateOperationSetV1Response**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. samm: muutuja vähendamine

1. Valige voos **Uus samm**.
2. **Sisestage** dialoogiboksi Toimingu **valimine otsinguväljale kulumismuutuja**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige väljal **Nimi** **ülesannete** arv.
4. Sisestage **väljale** Väärtus **väärtus väärtus 1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. samm: projektiülesande ümbernimetamine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige juhises kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Projektiülesande ümbernimetamiseks**.
5. Valige väljal **Tegevuse** nimi **väärtus msdyn\_ PssUpdateV1**.
6. Sisestage väljale **Olem** järgmine parameetriteave.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Valige väljal **OperationSetId** **dialoogiboksis Dünaamiline sisu\_ käsk msdyn** **CreateOperationSetV1Response**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. samm: toimingukomplekti käivitamine

1. Valige voos **Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. Seejärel valige vahekaardil **Toimingud** tulemite loendis toiming.
3. Valige juhises kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **Käivita toimingukomplekt** ümber.
5. Valige väljal **Tegevuse nimi** käsk **msdyn\_ ExecuteOperationSetV1**.
6. Valige väljal **OperationSetId** **dialoogiboksis Dynamidi sisu\_ msdyn** CreateOperationSetV1Response **OperationSetId**.

## <a name="references"></a>Viited

- [Ülevaade sellest, kuidas vooge Dataverse integreerida - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](schedule-api-preview.md)
- [Ülevaade pilvevoogudest - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Ülevaade lahenduseteadlikest voogudest - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
