---
title: Project Service’i lisandmooduli kasutamine töö planeerimiseks tarkvaras Microsoft Project | MicrosoftDocs
description: Selles teemas kirjeldatakse, kuidas lisada, konfigureerida ja kasutada Microsoft Projecti lisandmooduleid teenuse Microsoft Project Service jaoks.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129673"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Lisandmooduli Project Service Automation kasutamine töö planeerimiseks tarkvaras Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lihtsustab projektide plaanimist ja hinnanguid. Saate tööd määratleda, nii et lõplikus ettepanekus on konkreetsed kulud, töö hulk ja müügiväärtus.  

 Nüüd saate installida tarkvara [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ja plaanida tööd tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] tuttavas keskkonnas. Kasutage tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] töökindlaid plaanimis- ja haldusvõimalusi ning seejärel värskendage projektiplaani lisandmoodulis Project Service Automation.  

> [!IMPORTANT]
> - Selleks, et rakenduse SharePoint dokumendihalduse abil salvestada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faile rakenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektidele, peab teie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administraator dokumendihalduse sisse lülitama. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ühildub ainult tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Lisandmooduli allalaadimine ja installimine  
 Veenduge, et teil oleks käepärast [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sisselogimisteave. Seda teavet on vaja tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] teenusega [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ühenduse loomiseks.  

1.  Allalaadimiskeskuses laadige alla lisandmoodul, mida teie Project Service’i versioon toetab, nt [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) või [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Klõpsake allalaadimise lingil.  

3.  Kui allalaadimine on lõppenud, klõpsake lisandmooduli installimiseks **Jah**.  

## <a name="configure-the-add-in"></a>Lisandmooduli konfigureerimine  

1. Avage tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja klõpsake vahekaarti **Project Service**.  

2. Klõpsake **Ühenda**.  

3. Sisestage sisselogimisteave ja klõpsake **Logi sisse**.  

   Nüüd saate lisandmoodulit kasutada.  

## <a name="read-from-a-template"></a>Mallist lugemine  
 Projekti plaanimise alustamiseks lugege andmed mallist, mille lõite rakenduses [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ja kopeerisite rakendusse [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projektimalli loomine (Project Service Automation)](../psa/create-project-template.md)  

1.  Vahekaardil **Project Service** klõpsake suvandeid **Loe** > **Project Service Automation projektimall**.  

2.  Valige loendist projektimall ja klõpsake **Ava**.  

    > [!NOTE]
    >  Ülesanded, mis kopeeritakse mallist projekti tuleb vaikeseadistuses käsitsi ajastada.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Rakenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rollide määramine projekti ressurssidele  

1.  Avage projekt ja klõpsake lindil **Ülesanne**.  

2.  Klõpsake menüül **Gantti diagramm** ja valige **Ressursileht**.  

3.  Ressursilehel klõpsake ripploendil **Project Service’i ressursi roll** ja valige Project Service Automation roll.  

## <a name="staff-your-project-with-resources"></a>Projektile ressursside lisamine  

1.  Valige rida vahekaardil Project Service ja klõpsake **Leia ressursse**.  

2.  Kuval **Book Resource** (Reserveeri ressurss) valige ressurss, mida soovite selles projektis kasutada.  

3.  Klõpsake **Book** (Reserveeri) ja seejärel **OK**.  

## <a name="publish-your-project"></a>Projekti avaldamine  
Kui projekti plaanimine on lõppenud, on järgmiseks etapiks projekti importimine ja avaldamine lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt imporditakse lisandmoodulisse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Rakendatakse hinnakujunduse ja meeskonnaloomise protsessid. Ava projekt lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], et näha, kas on loodud meeskond, projekti eelarvestused ja tööjaotuse struktuur. Järgmine tabel näitab, kust leida tulemusi.


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantti diagramm**   | Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Tööjaotuse struktuur**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressursileht** |   Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Projektimeeskonna liikmed**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**Kasutamine**    |    Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Projekti prognoosid**.     |

**Projekti importimine ja avaldamine**  
1. Klõpsake vahekaarti **Project Service** ja seejärel suvandeid **Avalda** > **Uus Project Service Automation projekt**.  

2. Dialoogiboksis **Avalda teenuse Project Service uues projektis** sisestage **Projekti nimi** ja valige **Klient**.  

3. Võite ka märkida ruudu **Seo projekti plaan lisandmooduliga Project Service Automation**, et seostada projekti plaani fail lisandmooduliga Project Service Automation.  

4. Klõpsake nuppu **Avalda**.  

   Projekti faili seostamine lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teeb Projekti failist juhteksemplari ning seadistab tööjaotuse struktuuri lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kirjutuskaitstuks.  Projekti plaani muutmiseks tuleb muudatusi teha tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Project ning avaldada need värskendusena lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Imporditud projekti redigeerimine  
 Lisandmoodulisse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imporditud projekti plaani muutmiseks on kaks võimalust.  

- Avage põhifail ning redigeerige seda tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Eemaldage faili seos lisandmooduliga ning redigeerige Project Service’is. Tarkvarast [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] imporditud projekt on vaikimisi lukus ning seda saab redigeerida ainult Projectis. Faili redigeerimiseks lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tuleb faili seos lisandmooduliga eemaldada.  

### <a name="edit-in-pn_microsoft_project"></a>Redigeerimine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Klõpsake peamenüüs suvandeid **Project Service** > **Projektid**.  

2. Avage projektide loendist projekt, mille lõite tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klõpsake lindil **Ava tarkvaras MS Project**. See avab seostatud põhifaili tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Faili seose eemaldamine ja faili redigeerimine [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service’is  

1. Klõpsake peamenüüs suvandeid **Project Service** > **Projektid**.  

2. Avage projektide loendist projekt, mille lõite tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klõpsake lindil **Eemalda seos MS Projectiga**  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Projektifaili laadimine rakendusse SharePoint või Office Groups  
 Võite projektifaili rakendusse SharePoint üles laadida, seejärel leiate selle lisandmooduli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektide valikust Seotud dokumendid.  Administraator peab konfigureerima teenuse SharePoint dokumendihalduse ja selle projekti üksuse jaoks sisse lülitama. 

 Kui olete seadistanud rakenduse Office Groups, võite projekti laadida ka rakendusse [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)].

### <a name="upload-a-file-for-sharepoint"></a>Faili üleslaadimine rakenduse SharePoint jaoks  

1. Klõpsake peamenüüs **Project Service** > **Laadi üles**.  

2. Valige **Lisandmooduli Project Service Automation projekti dokumentidesse**.  

3. Dialoogiboksis **Luba avamine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** valige **Jah** või **Ei**.  

   - Kui klõpsate **Jah**, saate valida lisandmoodulis Project Service Automation nuppu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ning käivitada tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja laadida projektifaili SharePoint dokumenditeegist.  

   - Kui klõpsate **Ei**, ei tööta nupu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** link.  

4. Tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faili leiate lisandmoodulist [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] konkreetse projekti jaotisest **Dokumendid**.  

### <a name="upload-a-file-for-office-groups"></a>Faili laadimine rakendusse Office Groups  

1. Klõpsake peamenüüs **Project Service** > **Laadi üles**.  

2. Valige **Lisandmooduli Project Service Automation projekti dokumentidesse**.  

3. Dialoogiboksis **Luba avamine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** valige **Jah** või **Ei**.  

   - Kui klõpsate **Jah**, saate valida lisandmoodulis Project Service Automation nuppu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ning käivitada tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja laadida projektifaili SharePoint dokumenditeegist.  

   - Kui klõpsate **Ei**, ei tööta nupu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** link.  

4. Tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faili leiate lisandmoodulist [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] konkreetse projekti jaotisest **Dokumendid**.  

## <a name="publish--your-project-as-a-template"></a>Projekti avaldamine mallina  
 Võite projekti salvestada ning seda taaskasutada, salvestades see projektimallina lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Projektimallid on taaskasutatavad projektiplaanid lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projektimalli loomine (Project Service Automation)](../psa/create-project-template.md)  

1. Klõpsake vahekaarti **Project Service** ja seejärel **Avalda** > **Uus lisandmooduli Project Service Automation projektimall**.  

2. Dialoogiboksi **Avalda uues projektis Project Service mall** sisestage **Projektimalli nimi**.  

3. Võite ka märgistada märkeruudu **Seosta projektiplaan lisandmooduliga Project Service Automation**, et seostada projekti fail lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Klõpsake nuppu **Avalda**.  

Projekti faili seostamine lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teeb projekti failist juhteksemplari ning seadistab tööjaotuse struktuuri lisandmooduli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] mallis kirjutuskaitstuks.:  Projekti plaani muutmiseks tuleb muudatusi teha tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Project ning avaldada need värskendusena lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Vt ka  
 [Projektijuhi juhend](../psa/project-manager-guide.md)
