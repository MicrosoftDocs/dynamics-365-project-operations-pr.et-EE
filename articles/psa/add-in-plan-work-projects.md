---
title: Microsoft Projecti töö kavandamine Project Service'i lisandmooduliga
description: Selles teemas kirjeldatakse, kuidas kasutada Microsoft Projecti lisandmoodulit teenuse Microsoft Project Service jaoks.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145938"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Microsoft Projecti töö kavandamine Project Service'i lisandmooduliga

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lihtsustab projektide plaanimist ja hinnanguid. Saate tööd määratleda, nii et lõplikus ettepanekus on konkreetsed kulud, töö hulk ja müügiväärtus.  

Saate installida tarkvara [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ja plaanida tööd tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] tuttavas keskkonnas. Kasutage tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] töökindlaid plaanimis- ja haldusvõimalusi ning seejärel värskendage projektiplaani lisandmoodulis Project Service Automation.  

> [!IMPORTANT]
> - Selleks, et rakenduse SharePoint dokumendihalduse abil salvestada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faile rakenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektidele, peab teie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administraator dokumendihalduse sisse lülitama. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ühildub ainult tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Lisandmooduli allalaadimine ja installimine  
 Veenduge, et teil oleks käepärast [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sisselogimisteave. Seda teavet on vaja tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] teenusega [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ühenduse loomiseks.  

1.  Allalaadimiskeskuses laadige alla lisandmoodul, mida teie Project Service’i versioon toetab, nt [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) või [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Valige allalaadimise link.  

3.  Kui allalaadimine on lõppenud, valige lisandmooduli installimiseks **Jah**.  

## <a name="configure-the-add-in"></a>Lisandmooduli konfigureerimine  

1. Avage tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja valige vahekaart **Project Service**.  

2. Valige käsk **Ühenda**.  

3. Sisestage sisselogimisteave ja valige **Logi sisse**.  

   Nüüd saate lisandmoodulit kasutada.  

## <a name="read-from-a-template"></a>Mallist lugemine  
 Projekti plaanimise alustamiseks lugege andmed mallist, mille lõite rakenduses [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ja kopeerisite rakendusse [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projektimalli loomine (Project Service Automation)](../psa/create-project-template.md)  

1.  Valige vahekaardil **Project Service** jaotis **Loe** > **Project Service Automationi projektimall**.  

2.  Valige loendist projektimall ja seejärel valige **Ava**.  

    > [!NOTE]
    >  Ülesanded, mis kopeeritakse mallist projekti tuleb vaikeseadistuses käsitsi ajastada.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Rakenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rollide määramine projekti ressurssidele  

1.  Avage projekt ja valige ribal **Ülesanne**.  

2. Valige menüü **Gantti diagramm** ja valige **Ressursileht**.  

3. Ressursilehel valige ripploend **Project Service’i ressursi roll** ja valige Project Service Automationi roll.  

## <a name="staff-your-project-with-resources"></a>Projektile ressursside lisamine  

1.  Valige rida vahekaardil Project Service ja valige **Leia ressursse**.  

2.  Kuval **Book Resource** (Reserveeri ressurss) valige ressurss, mida soovite selles projektis kasutada.  

3.  Valige **Broneeri** ja seejärel **OK**.  

## <a name="publish-your-project"></a>Projekti avaldamine  
Kui projekti plaanimine on lõppenud, on järgmiseks etapiks projekti importimine ja avaldamine lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt imporditakse lisandmoodulisse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Rakendatakse hinnakujunduse ja meeskonnaloomise protsessid. Ava projekt lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], et näha, kas on loodud meeskond, projekti eelarvestused ja tööjaotuse struktuur. Järgmine tabel näitab, kust leida tulemusi.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantti diagramm**   | Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Tööjaotuse struktuur**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressursileht** |   Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Projektimeeskonna liikmed**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**Kasutamine**    |    Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Projekti prognoosid**.     |

**Projekti importimine ja avaldamine**  
1. Avage vahekaardil **Project Service** jaotis **Avalda** > **Uus Project Service Automationi projekt**.  

2. Sisestage dialoogiboksi **Avalda teenuse Project Service uues projektis** **Projekti nimi** ja valige **Klient**.  

3. Võite ka valida ruudu **Seo projekti plaan lisandmooduliga Project Service Automation**, et seostada projekti plaani fail lisandmooduliga Project Service Automation.  

4. Valige **Avalda**.  

   Projekti faili seostamine lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teeb Projekti failist juhteksemplari ning seadistab tööjaotuse struktuuri lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kirjutuskaitstuks.  Projekti plaani muutmiseks tuleb muudatusi teha tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Project ning avaldada need värskendusena lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Imporditud projekti redigeerimine  
 Lisandmoodulisse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imporditud projekti plaani muutmiseks on kaks võimalust.  

- Avage põhifail ning redigeerige seda tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Eemaldage faili seos lisandmooduliga ning redigeerige Project Service’is. Tarkvarast [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] imporditud projekt on vaikimisi lukus ning seda saab redigeerida ainult Projectis. Faili redigeerimiseks lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tuleb faili seos lisandmooduliga eemaldada.  

### <a name="edit-in-pn_microsoft_project"></a>Redigeeri [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]is  

1. Avage peamenüüs **Project Service** > **Projektid**.  

2. Avage projektide loendist projekt, mille lõite tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Valige ribalt **Ava tarkvaras MS Project**. See avab seostatud põhifaili tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Faili seose eemaldamine ja faili redigeerimine [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service’is  

1. Avage peamenüüs **Project Service** > **Projektid**.  

2. Avage projektide loendist projekt, mille lõite tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Valige ribalt **Eemalda seos MS Projectiga**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Projektifaili laadimine rakendusse SharePoint või Office Groups  
 Võite projektifaili rakendusse SharePoint üles laadida, seejärel leiate selle lisandmooduli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektide valikust Seotud dokumendid.  Administraator peab konfigureerima teenuse SharePoint dokumendihalduse ja selle projekti üksuse jaoks sisse lülitama. 

 Kui olete seadistanud rakenduse Office Groups, võite projekti laadida ka rakendusse [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)].

### <a name="upload-a-file-for-sharepoint"></a>Faili üleslaadimine rakenduse SharePoint jaoks  

1. Avage peamenüüs **Project Service** > **Laadi üles**.  

2. Valige **Lisandmooduli Project Service Automation projekti dokumentidesse**.  

3. Dialoogiboksis **Luba avamine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** valige **Jah** või **Ei**.  

   - Kui valite **Jah**, saate valida lisandmoodulis Project Service Automation nuppu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ning käivitada tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja laadida projektifaili SharePoint dokumenditeegist.  

   - Kui valite **Ei**, siis link **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ei tööta.  

4. Tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faili leiate lisandmoodulist [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] konkreetse projekti jaotisest **Dokumendid**.  

### <a name="upload-a-file-for-office-groups"></a>Faili laadimine rakendusse Office Groups  

1. Avage peamenüüs **Project Service** > **Laadi üles**.  

2. Valige **Lisandmooduli Project Service Automation projekti dokumentidesse**.  

3. Dialoogiboksis **Luba avamine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** valige **Jah** või **Ei**.  

   - Kui valite **Jah**, saate valida lisandmoodulis Project Service Automation nuppu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ning käivitada tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja laadida projektifaili SharePoint dokumenditeegist.  

   - Kui valite **Ei**, siis link **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ei tööta.  

4. Tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faili leiate lisandmoodulist [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] konkreetse projekti jaotisest **Dokumendid**.  

## <a name="publish--your-project-as-a-template"></a>Projekti avaldamine mallina  
 Võite projekti salvestada ning seda taaskasutada, salvestades see projektimallina lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projektimallid on taaskasutatavad projektiplaanid lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Lisateavet leiate teemast [Projektimalli loomine (Project Service Automation)](../psa/create-project-template.md). 

1. Avage vahekaardil **Project Service** jaotis **Avalda** > **Uus Project Service Automationi mall**.  

2. Dialoogiboksi **Avalda uues projektis Project Service mall** sisestage **Projektimalli nimi**.  

3. Võite ka valida suvandi **Seosta projektiplaan lisandmooduliga Project Service Automation**, et seostada projektiplaani fail lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Valige **Avalda**.  

Projekti faili seostamine lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teeb projekti failist juhteksemplari ning seadistab tööjaotuse struktuuri lisandmooduli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] mallis kirjutuskaitstuks.:  Projekti plaani muutmiseks tuleb muudatusi teha tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Project ning avaldada need värskendusena lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Ressursi laaditud ajakava lugemine

Projekti lugemisel rakendusest Project Service Automation ei sünkroonita ressursi kalendrit töölaua kliendiga. Kui tööülesande kestustes, pingutustes või lõpus on erinevusi, on ilmselt põhjuseks see, et ressurssidel ja töölaua kliendil ei ole projektile rakendatud sama töötunni malli kalendrit.


## <a name="data-synchronization"></a>Andmete sünkroonimine
Selles jaotises asuvad tabelid pakuvad teavet olemiandmete sünkroonimise kohta Project Service Automationi ja Microsoft Projecti töölaua lisandmooduli vahel.

### <a name="project-task-entity-table"></a>Projekti tööülesande olemi tabel
Järgmine tabel kirjeldab, kuidas projekti tööülesande andmeid Project Service Automationi ja Microsoft Projecti töölaua lisandmooduli vahel sünkroonitakse.

| **Olem** | **Väli** | **Microsoft Projecti sünkroonimine Project Service Automationiga** | **Project Service Automationi sünkroonimine Microsoft Projectiga** |
| --- | --- | --- | --- |
| Projekti ülesanne | Tähtaeg | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Prognoositud panus | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | MS Projecti kliendi ID | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Emaülesanne | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Project | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Projekti ülesanne | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Projekti ülesande nimi | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Ressursiühik (aegunud versioonis 3.0) | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Kavandatud kestus | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | Alguskuupäev | Sünkroonitud | Sünkroonimata |
| Projekti ülesanne | WBS-i ID | Sünkroonitud | Sünkroonimata |

### <a name="team-member-entity-table"></a>Meeskonnaliikme olemi tabel
Järgmine tabel kirjeldab, kuidas meeskonnaliikme olemi andmeid Project Service Automationi ja Microsoft Projecti töölaua lisandmooduli vahel sünkroonitakse.

| **Olem** | **Väli** | **Microsoft Projecti sünkroonimine Project Service Automationiga** | **Project Service Automationi sünkroonimine Microsoft Projectiga** |
| --- | --- | --- | --- |
| Meeskonnaliige | MS Projecti kliendi ID | Sünkroonitud | Sünkroonimata |
| Meeskonnaliige | Ametikoha nimi | Sünkroonitud | Sünkroonimata |
| Meeskonnaliige | projekt | Sünkroonitud | Sünkroonitud |
| Meeskonnaliige | Projektimeeskond | Sünkroonitud | Sünkroonitud |
| Meeskonnaliige | Ressursi üksus | Sünkroonimata | Sünkroonitud |
| Meeskonnaliige | Roll | Sünkroonimata | Sünkroonitud |
| Meeskonnaliige | Töötunnid | Sünkroonimata | Sünkroonimata |

### <a name="resource-assignment-entity-table"></a>Ressursi määramise olemi tabel
Järgmine tabel kirjeldab, kuidas ressursi määramise olemi andmeid Project Service Automationi ja Microsoft Projecti töölaua lisandmooduli vahel sünkroonitakse.

| **Olem** | **Väli** | **Microsoft Projecti sünkroonimine Project Service Automationiga** | **Project Service Automationi sünkroonimine Microsoft Projectiga** |
| --- | --- | --- | --- |
| Ressursi määramine | Kuupäevast | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | tundi | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | MS Projecti kliendi ID | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | Plaanitud töö | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | Project | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | Projektimeeskond | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | Ressursi määramine | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | Toiming | Sünkroonitud | Sünkroonimata |
| Ressursi määramine | Kuupäevani | Sünkroonitud | Sünkroonimata |

### <a name="project-task-dependencies-entity-table"></a>Projekti tööülesande sõltuvuste olemi tabel
Järgmine tabel kirjeldab, kuidas projekti tööülesande sõltuvuste olemi andmeid Project Service Automationi ja Microsoft Projecti töölaua lisandmooduli vahel sünkroonitakse.

| **Olem** | **Väli** | **Microsoft Projecti sünkroonimine Project Service Automationiga** | **Project Service Automationi sünkroonimine Microsoft Projectiga** |
| --- | --- | --- | --- |
| Projekti ülesande sõltuvused | Projekti ülesande sõltuvus | Sünkroonitud | Sünkroonimata |
| Projekti ülesande sõltuvused | Lingi tüüp | Sünkroonitud | Sünkroonimata |
| Projekti ülesande sõltuvused | Eelkäijast ülesanne | Sünkroonitud | Sünkroonimata |
| Projekti ülesande sõltuvused | Project | Sünkroonitud | Sünkroonimata |
| Projekti ülesande sõltuvused | Järglasest ülesanne | Sünkroonitud | Sünkroonimata |

### <a name="additional-resources"></a>Lisaressursid
 [Projektijuhi juhend](../psa/project-manager-guide.md)
