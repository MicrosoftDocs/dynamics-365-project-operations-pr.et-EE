---
title: Projekti ajakava API-de kasutamine tarkvaraga Power Automate
description: Selles artiklis on näidisvoog, mis kasutab Projecti ajakava rakenduse programmeerimisliideseid (API-sid).
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

Selles artiklis kirjeldatakse näidisvoogu, mis näitab, kuidas luua projekti täielikku plaani, kasutades Microsoft Power Automate seda, kuidas luua operatsioonikomplekti ja kuidas värskendada olemit. Näide demonstreerib, kuidas luua projekti, projektimeeskonna liiget, operatsioonikomplekte, projektiülesandeid ja ressursimääranguid. Selles artiklis selgitatakse ka seda, kuidas olemit värskendada ja operatsioonikomplekti käivitada.

Järgmine on täielik loetelu sammudest, mis on dokumenteeritud selle artikli proovivoos:

1. [Päästiku loomine PowerApps](#1)
2. [Projekti loomine](#2)
3. [Meeskonnaliikme muutuja lähtestamine](#3)
4. [Üldise meeskonnaliikme loomine](#4)
5. [Operatsioonikomplekti loomine](#5)
6. [Projektisalve loomine](#6)
7. [Lingi oleku muutuja lähtestamine](#7)
8. [Muutuja lähtestamine ülesannete arvu jaoks](#8)
9. [Projekti ülesande ID muutuja lähtestamine](#9)
10. [Tehke seni, kuni](#10)
11. [Projektiülesande määramine](#11)
12. [Projektiülesande loomine](#12)
13. [Ressursimäärangu loomine](#13)
14. [Muutuja dekrementeerimine](#14)
15. [Projektiülesande ümbernimetamine](#15)
16. [Operatsioonikomplekti käivitamine](#16)

## <a name="assumptions"></a>Eeldused

Selles artiklis eeldatakse, et teil on põhiteadmised platvormist, pilvevoogudest Dataverse ja projekti ajakava rakenduse programmeerimisliidesest (API). Lisateavet leiate selle artikli allpool olevast jaotisest [Viited](#references).

## <a name="create-a-flow"></a>Voo loomine

### <a name="select-an-environment"></a>Valige keskkond

Saate luua Power Automate voolu oma keskkonnas.

1. Avage <https://flow.microsoft.com> jaotis ja kasutage sisselogimiseks oma administraatori mandaati.
2. Tehke paremas ülanurgas valik **Keskkonnad**.
3. Valige loendist keskkond, kuhu Dynamics 365 Project Operations on installitud.

### <a name="create-a-solution"></a>Lahenduse loomine

Lahenduseteadliku voo [loomiseks toimige järgmiselt](/power-automate/overview-solution-flows). Luues lahendusteadliku voo, saate voolu hõlpsamini eksportida, et seda hiljem kasutada.

1. Valige **navigeerimispaanil Lahendused**.
2. **Valige lehel Lahendused** suvand **Uus lahendus**.
3. **Määrake dialoogiboksis Uus lahendus** soovitud väljad ja seejärel valige **Loo**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. samm: looge PowerApps päästik

1. **Valige lehel Lahendused** loodud lahendus ja seejärel valige **Uus**.
2. Valige **vasakpoolsel paanil Pilvevoogude** \> **automatiseerimise** \> **pilvevoog** \> **Instant.**
3. Sisestage väljale **Voo nimi** tekst **Schedule API Demo Flow**.
4. **Valige loendist Valige, kuidas seda voogu** käivitada.**Power Apps** Päästiku loomisel Power Apps on loogika teie kui autori otsustada. Selles artiklis jätke sisendparameetrid testimise eesmärgil tühjaks.
5. Valige käsk **Loo**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. etapp: looge projekt

Näidisprojekti loomiseks tehke järgmist.

1. Valige **loodud voos Uus etapp**.

    ![Uue sammu lisamine.](media/newstep.png)

2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.

    ![Operatsiooni valimine.](media/chooseactiontab.png)

3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.

![Sammu ümbernimetamine.](media/renamestep.png)

4. Nimetage etapp **projekti loomine ümber**.
5. Valige **väljal** Toimingu nimi **msdyn\_ CreateProjectV1**.
6. **Valige msdyn-teemaväljal\_** Käsk Lisa dünaamiline **sisu**.
7. Sisestage **vahekaardil** Expression **funktsiooniväljale Projekti nimi - utcNow()**.
8. Valige **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. samm: lähtestage meeskonnaliikme jaoks muutuja

1. Valige **voos Uus samm**.
2. **Sisestage** dialoogiboksi Toimingu **valimine otsinguväljale muutuja** lähtestamine. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage samm **init meeskonnaliikmeks**.
5. Sisestage väljale **Nimi** väärtus **TeamMemberAction**.
6. Valige väljal **Tüüp** string **·**.
7. Sisestage väljale **Väärtus** väärtus msdyn **CreateTeamMemberV1\_.**

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. toiming: looge üldine meeskonnaliige

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage juhis **Meeskonnaliikme** loomine ümber.
5. Välja Toimingu **nimi jaoks valige** dünaamilise sisu **dialoogiboksis TeamMemberAction** **.**
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

    - **\@\@ odata.type** – olemi nimi. Näiteks sisestage **"Microsoft.Dynamics.CRM.msdyn\_ projectteam".**
    - **msdyn\_ projectteamid** – projektimeeskonna ID esmane võti. Väärtus on globaalselt kordumatu identifikaatori (GUID) avaldis.   ID luuakse avaldise vahekaardilt.

    - **msdyn\_ project\@ odata.bind** – omaniku projekti ID. Väärtus on dünaamiline sisu, mis tuleneb sammu "Loo projekt" vastusest. Sisestage kindlasti kogu tee ja lisage sulgudesse dünaamiline sisu. Jutumärgid on kohustuslikud. Näiteks sisestage **"/msdyn\_ projects(ADD DYNAMIC CONTENT)".**"
    - **msdyn\_ nimi** – meeskonnaliikme nimi. Näiteks sisestage **"ScheduleAPIDemoTM1".**

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. toiming: looge operatsioonikomplekt

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage samm **ümber Toimingukomplekti loomine**.
5. Valige väljal **Toimingu nimi** kohandatud toiming msdyn **CreateOperationSetV1\_**.Dataverse
6. Sisestage väljale **Kirjeldus** tekst **ScheduleAPIDemoOperationSet**.
7. Sisestage väljale **Projekt** väärtus **/msdyn\_ projects(**.
8. **Valige** dialoogiboksis Dünaamiline sisu **msdyn\_ CreateProjectV1Response ProjectId**.
9. Sisestage **väljale** Projekt **).**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. toiming: looge projekti salve

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale tekst Lisa uus rida**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage juhisämber **ümber**.
5. Valige väljal **Tabeli nimi** suvand **Projektisalved**.
6. Sisestage väljale **Nimi** tekst **ScheduleAPIDemoBucket1**.
7. **Välja Projekt** puhul valige **dialoogiboksis Dünaamiline sisu\_ suvand msdyn** CreateProjectV1Response **ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. samm: lähtestage lingi oleku muutuja

1. Valige **voos Uus samm**.
2. **Sisestage** dialoogiboksi Toimingu **valimine otsinguväljale muutuja** lähtestamine. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage samm **ümber Init linkstatus**.
5. Sisestage väljale **Nimi** **lingid**.
6. Valige väljal **Tüüp** väärtus **Täisarv**.
7. Sisestage **väljale** Väärtus **väärtus 192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. samm: lähtestage muutuja ülesannete arvu jaoks

1. Valige **voos Uus samm**.
2. **Sisestage** dialoogiboksi Toimingu **valimine otsinguväljale muutuja** lähtestamine. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage samm **ümber Init Ülesannete** arv.
5. Sisestage **väljale** Nimi **ülesannete** arv.
6. Valige väljal **Tüüp** väärtus **Täisarv**.
7. Sisestage **väljale** Väärtus **väärtus 5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. samm: lähtestage muutuja projekti ülesande ID jaoks

1. Valige **voos Uus samm**.
2. **Sisestage** dialoogiboksi Toimingu **valimine otsinguväljale muutuja** lähtestamine. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage samm **ümber Init ProjectTaskID**.
5. Sisestage **väljale** Nimi **ülesannete** arv.
6. Valige väljal **Tüüp** string **·**.
7. Sisestage väljale **Väärtus** avaldisekoosturisse **tekst guid(**).

## <a name="step-10-do-until"></a><a id="10"></a> 10. samm: tehke seni, kuni

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi Toimingu** valimine otsinguväljale tekst **tee kuni**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Määrake tingimuslause esimene väärtus ülesannete **arvule**, mis muutub **dialoogiboksis Dünaamiline sisu**.
4. Seadke tingimus väärtuseks **väiksem kui võrdne**.
5. Määrake tingimuslause teine väärtus väärtuseks **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. toiming: määrake projekti ülesanne

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale set variable**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige uues etapis kolmikpunkt (**...**) ja seejärel valige Nimeta **ümber**.
4. Nimetage juhis **Sea projektiülesanne ümber**.
5. Valige väljal **Nimi** väärtus **msdyn\_ projecttaskid**.
6. Sisestage väljale **Väärtus** avaldisekoosturisse **tekst guid(**).

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. toiming: looge projektiülesanne

Järgige neid juhiseid, et luua projektiülesanne, millel on kordumatu ID, mis kuulub praegusele projektile ja teie loodud projektisalvele.

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige selles etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **ümber Projektiülesande** loomine.
5. Valige väljal **Toimingu nimi** väärtus **msdyn\_ PssCreateV1**.
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

    - **\@\@ odata.type** – olemi nimi. Näiteks sisestage **"Microsoft.Dynamics.CRM.msdyn\_ projecttask".**
    - **msdyn\_ projecttaskid** – ülesande kordumatu ID. Väärtuseks tuleks seada dünaamiline muutuja **msdyn\_ projecttaskidist**.
    - **msdyn\_ project\@ odata.bind** – omaniku projekti ID. Väärtus on dünaamiline sisu, mis tuleneb sammu "Loo projekt" vastusest. Sisestage kindlasti kogu tee ja lisage sulgudesse dünaamiline sisu. Jutumärgid on kohustuslikud. Näiteks sisestage **"/msdyn\_ projects(ADD DYNAMIC CONTENT)".**"
    - **msdyn\_ subjekt** – mis tahes ülesande nimi.
    - **msdyn\_ projectbucket\@ odata.bind** – projekti ämber, mis sisaldab ülesandeid. Väärtus on dünaamiline sisu, mis tuleneb sammu "Loo ämber" vastusest. Sisestage kindlasti kogu tee ja lisage sulgudesse dünaamiline sisu. Jutumärgid on kohustuslikud. Näiteks sisestage **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)".**"
    - **msdyn\_ start** – alguskuupäeva dünaamiline sisu. Näiteks homme on kujutatud kui **"addDays(utcNow(), 1)".**
    - **msdyn\_ scheduledstart** – plaanitud alguskuupäev. Näiteks homme on kujutatud kui **"addDays(utcNow(), 1)".**
    - **msdyn\_ scheduleend** – plaanitud lõppkuupäev. Valige kuupäev tulevikus. Näiteks määrake **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – lingi olek. Näiteks sisestage **"192350000".**

7. **Välja OperationSetId** jaoks valige **dialoogiboksis Dünaamiline sisu\_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. toiming: ressursimäärangu loomine

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige selles etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **ülesande** loomine ümber.
5. Valige väljal **Toimingu nimi** väärtus **msdyn\_ PssCreateV1**.
6. Sisestage väljale **Olem** järgmine parameetriteave.

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

7. **Välja OperationSetId** jaoks valige **dialoogiboksis Dünaamiline sisu\_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. samm: muutuja dekrementeerimine

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale dekrementmuutuja**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige **väljal** Nimi **ülesannete** arv.
4. Sisestage **väljale** Väärtus **väärtus 1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. toiming: nimetage projektiülesanne ümber

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige selles etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage etapp **ümber Project Taski ümbernimetamiseks**.
5. Valige väljal **Toimingu nimi** väärtus msdyn **PssUpdateV1\_.**
6. Sisestage väljale **Olem** järgmine parameetriteave.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Välja OperationSetId** jaoks valige **dialoogiboksis Dünaamiline sisu\_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. samm: käivitage operatsioonikomplekt

1. Valige **voos Uus samm**.
2. Sisestage **dialoogiboksi** Toimingu **valimine otsinguväljale sidumata toiming**. **Seejärel valige vahekaardil Toimingud** tulemite loendist toiming.
3. Valige selles etapis kolmikpunkt (**...**) ja seejärel valige **Nimeta ümber**.
4. Nimetage samm **ümber käivitage toimingukomplekt**.
5. Valige väljal **Toimingu nimi** väärtus **msdyn\_ ExecuteOperationSetV1**.
6. **Välja OperationSetId** jaoks valige **dialoogiboksis Dynamid content\_ msdyn** CreateOperationSetV1Response **OperationSetId**.

## <a name="references"></a>Viited

- [Ülevaade sellest, kuidas integreerida vooge Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](schedule-api-preview.md)
- [Pilvevoogude ülevaade - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Ülevaade lahendusteadlikest voogudest - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
