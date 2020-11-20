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
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="af8c9-103">Lisandmooduli Project Service Automation kasutamine töö planeerimiseks tarkvaras Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="af8c9-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="af8c9-104">lihtsustab projektide plaanimist ja hinnanguid.</span><span class="sxs-lookup"><span data-stu-id="af8c9-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="af8c9-105">Saate tööd määratleda, nii et lõplikus ettepanekus on konkreetsed kulud, töö hulk ja müügiväärtus.</span><span class="sxs-lookup"><span data-stu-id="af8c9-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="af8c9-106">Nüüd saate installida tarkvara [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ja plaanida tööd tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] tuttavas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="af8c9-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="af8c9-107">Kasutage tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] töökindlaid plaanimis- ja haldusvõimalusi ning seejärel värskendage projektiplaani lisandmoodulis Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="af8c9-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="af8c9-108">Selleks, et rakenduse SharePoint dokumendihalduse abil salvestada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faile rakenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektidele, peab teie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administraator dokumendihalduse sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="af8c9-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="af8c9-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ühildub ainult tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="af8c9-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="af8c9-110">Lisandmooduli allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="af8c9-110">Download and install the add-in</span></span>  
 <span data-ttu-id="af8c9-111">Veenduge, et teil oleks käepärast [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sisselogimisteave.</span><span class="sxs-lookup"><span data-stu-id="af8c9-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="af8c9-112">Seda teavet on vaja tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] teenusega [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ühenduse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="af8c9-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="af8c9-113">Allalaadimiskeskuses laadige alla lisandmoodul, mida teie Project Service’i versioon toetab, nt [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) või [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="af8c9-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="af8c9-114">Klõpsake allalaadimise lingil.</span><span class="sxs-lookup"><span data-stu-id="af8c9-114">Click the download link.</span></span>  

3.  <span data-ttu-id="af8c9-115">Kui allalaadimine on lõppenud, klõpsake lisandmooduli installimiseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="af8c9-116">Lisandmooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="af8c9-116">Configure the add-in</span></span>  

1. <span data-ttu-id="af8c9-117">Avage tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja klõpsake vahekaarti **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="af8c9-118">Klõpsake **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="af8c9-119">Sisestage sisselogimisteave ja klõpsake **Logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="af8c9-120">Nüüd saate lisandmoodulit kasutada.</span><span class="sxs-lookup"><span data-stu-id="af8c9-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="af8c9-121">Mallist lugemine</span><span class="sxs-lookup"><span data-stu-id="af8c9-121">Read from a template</span></span>  
 <span data-ttu-id="af8c9-122">Projekti plaanimise alustamiseks lugege andmed mallist, mille lõite rakenduses [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ja kopeerisite rakendusse [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="af8c9-123">[Projektimalli loomine (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="af8c9-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="af8c9-124">Vahekaardil **Project Service** klõpsake suvandeid **Loe** > **Project Service Automation projektimall**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="af8c9-125">Valige loendist projektimall ja klõpsake **Ava**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="af8c9-126">Ülesanded, mis kopeeritakse mallist projekti tuleb vaikeseadistuses käsitsi ajastada.</span><span class="sxs-lookup"><span data-stu-id="af8c9-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="af8c9-127">Rakenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rollide määramine projekti ressurssidele</span><span class="sxs-lookup"><span data-stu-id="af8c9-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="af8c9-128">Avage projekt ja klõpsake lindil **Ülesanne**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="af8c9-129">Klõpsake menüül **Gantti diagramm** ja valige **Ressursileht**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="af8c9-130">Ressursilehel klõpsake ripploendil **Project Service’i ressursi roll** ja valige Project Service Automation roll.</span><span class="sxs-lookup"><span data-stu-id="af8c9-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="af8c9-131">Projektile ressursside lisamine</span><span class="sxs-lookup"><span data-stu-id="af8c9-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="af8c9-132">Valige rida vahekaardil Project Service ja klõpsake **Leia ressursse**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="af8c9-133">Kuval **Book Resource** (Reserveeri ressurss) valige ressurss, mida soovite selles projektis kasutada.</span><span class="sxs-lookup"><span data-stu-id="af8c9-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="af8c9-134">Klõpsake **Book** (Reserveeri) ja seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="af8c9-135">Projekti avaldamine</span><span class="sxs-lookup"><span data-stu-id="af8c9-135">Publish your project</span></span>  
<span data-ttu-id="af8c9-136">Kui projekti plaanimine on lõppenud, on järgmiseks etapiks projekti importimine ja avaldamine lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="af8c9-137">Projekt imporditakse lisandmoodulisse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="af8c9-138">Rakendatakse hinnakujunduse ja meeskonnaloomise protsessid.</span><span class="sxs-lookup"><span data-stu-id="af8c9-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="af8c9-139">Ava projekt lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], et näha, kas on loodud meeskond, projekti eelarvestused ja tööjaotuse struktuur.</span><span class="sxs-lookup"><span data-stu-id="af8c9-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="af8c9-140">Järgmine tabel näitab, kust leida tulemusi.</span><span class="sxs-lookup"><span data-stu-id="af8c9-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="af8c9-141">**Gantti diagramm**</span><span class="sxs-lookup"><span data-stu-id="af8c9-141">**Gantt Chart**</span></span>   | <span data-ttu-id="af8c9-142">Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Tööjaotuse struktuur**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="af8c9-143">**Ressursileht**</span><span class="sxs-lookup"><span data-stu-id="af8c9-143">**Resource Sheet**</span></span> |   <span data-ttu-id="af8c9-144">Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Projektimeeskonna liikmed**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]<span data-ttu-id="af8c9-145">**Kasutamine**</span><span class="sxs-lookup"><span data-stu-id="af8c9-145">**Use Usage**</span></span>    |    <span data-ttu-id="af8c9-146">Impordib teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuvale **Projekti prognoosid**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="af8c9-147">**Projekti importimine ja avaldamine**</span><span class="sxs-lookup"><span data-stu-id="af8c9-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="af8c9-148">Klõpsake vahekaarti **Project Service** ja seejärel suvandeid **Avalda** > **Uus Project Service Automation projekt**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="af8c9-149">Dialoogiboksis **Avalda teenuse Project Service uues projektis** sisestage **Projekti nimi** ja valige **Klient**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="af8c9-150">Võite ka märkida ruudu **Seo projekti plaan lisandmooduliga Project Service Automation**, et seostada projekti plaani fail lisandmooduliga Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="af8c9-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="af8c9-151">Klõpsake nuppu **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-151">Click **Publish**.</span></span>  

   <span data-ttu-id="af8c9-152">Projekti faili seostamine lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teeb Projekti failist juhteksemplari ning seadistab tööjaotuse struktuuri lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="af8c9-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="af8c9-153">Projekti plaani muutmiseks tuleb muudatusi teha tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Project ning avaldada need värskendusena lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="af8c9-154">Imporditud projekti redigeerimine</span><span class="sxs-lookup"><span data-stu-id="af8c9-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="af8c9-155">Lisandmoodulisse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] imporditud projekti plaani muutmiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="af8c9-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="af8c9-156">Avage põhifail ning redigeerige seda tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="af8c9-157">Eemaldage faili seos lisandmooduliga ning redigeerige Project Service’is.</span><span class="sxs-lookup"><span data-stu-id="af8c9-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="af8c9-158">Tarkvarast [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] imporditud projekt on vaikimisi lukus ning seda saab redigeerida ainult Projectis.</span><span class="sxs-lookup"><span data-stu-id="af8c9-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="af8c9-159">Faili redigeerimiseks lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tuleb faili seos lisandmooduliga eemaldada.</span><span class="sxs-lookup"><span data-stu-id="af8c9-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="af8c9-160">Redigeerimine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="af8c9-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="af8c9-161">Klõpsake peamenüüs suvandeid **Project Service** > **Projektid**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="af8c9-162">Avage projektide loendist projekt, mille lõite tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="af8c9-163">Klõpsake lindil **Ava tarkvaras MS Project**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="af8c9-164">See avab seostatud põhifaili tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="af8c9-165">Faili seose eemaldamine ja faili redigeerimine [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service’is</span><span class="sxs-lookup"><span data-stu-id="af8c9-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="af8c9-166">Klõpsake peamenüüs suvandeid **Project Service** > **Projektid**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="af8c9-167">Avage projektide loendist projekt, mille lõite tarkvaraga [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="af8c9-168">Klõpsake lindil **Eemalda seos MS Projectiga**</span><span class="sxs-lookup"><span data-stu-id="af8c9-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="af8c9-169">Projektifaili laadimine rakendusse SharePoint või Office Groups</span><span class="sxs-lookup"><span data-stu-id="af8c9-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="af8c9-170">Võite projektifaili rakendusse SharePoint üles laadida, seejärel leiate selle lisandmooduli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektide valikust Seotud dokumendid.</span><span class="sxs-lookup"><span data-stu-id="af8c9-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="af8c9-171">Administraator peab konfigureerima teenuse SharePoint dokumendihalduse ja selle projekti üksuse jaoks sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="af8c9-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="af8c9-172">Kui olete seadistanud rakenduse Office Groups, võite projekti laadida ka rakendusse [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="af8c9-173">Faili üleslaadimine rakenduse SharePoint jaoks</span><span class="sxs-lookup"><span data-stu-id="af8c9-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="af8c9-174">Klõpsake peamenüüs **Project Service** > **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="af8c9-175">Valige **Lisandmooduli Project Service Automation projekti dokumentidesse**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="af8c9-176">Dialoogiboksis **Luba avamine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** valige **Jah** või **Ei**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="af8c9-177">Kui klõpsate **Jah**, saate valida lisandmoodulis Project Service Automation nuppu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ning käivitada tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja laadida projektifaili SharePoint dokumenditeegist.</span><span class="sxs-lookup"><span data-stu-id="af8c9-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="af8c9-178">Kui klõpsate **Ei**, ei tööta nupu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** link.</span><span class="sxs-lookup"><span data-stu-id="af8c9-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="af8c9-179">Tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faili leiate lisandmoodulist [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] konkreetse projekti jaotisest **Dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="af8c9-180">Faili laadimine rakendusse Office Groups</span><span class="sxs-lookup"><span data-stu-id="af8c9-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="af8c9-181">Klõpsake peamenüüs **Project Service** > **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="af8c9-182">Valige **Lisandmooduli Project Service Automation projekti dokumentidesse**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="af8c9-183">Dialoogiboksis **Luba avamine tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** valige **Jah** või **Ei**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="af8c9-184">Kui klõpsate **Jah**, saate valida lisandmoodulis Project Service Automation nuppu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ning käivitada tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ja laadida projektifaili SharePoint dokumenditeegist.</span><span class="sxs-lookup"><span data-stu-id="af8c9-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="af8c9-185">Kui klõpsate **Ei**, ei tööta nupu **Ava tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** link.</span><span class="sxs-lookup"><span data-stu-id="af8c9-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="af8c9-186">Tarkvara [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] faili leiate lisandmoodulist [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teenuse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] konkreetse projekti jaotisest **Dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="af8c9-187">Projekti avaldamine mallina</span><span class="sxs-lookup"><span data-stu-id="af8c9-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="af8c9-188">Võite projekti salvestada ning seda taaskasutada, salvestades see projektimallina lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="af8c9-189">Projektimallid on taaskasutatavad projektiplaanid lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="af8c9-190">[Projektimalli loomine (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="af8c9-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="af8c9-191">Klõpsake vahekaarti **Project Service** ja seejärel **Avalda** > **Uus lisandmooduli Project Service Automation projektimall**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="af8c9-192">Dialoogiboksi **Avalda uues projektis Project Service mall** sisestage **Projektimalli nimi**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="af8c9-193">Võite ka märgistada märkeruudu **Seosta projektiplaan lisandmooduliga Project Service Automation**, et seostada projekti fail lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="af8c9-194">Klõpsake nuppu **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="af8c9-194">Click **Publish**.</span></span>  

<span data-ttu-id="af8c9-195">Projekti faili seostamine lisandmooduliga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] teeb projekti failist juhteksemplari ning seadistab tööjaotuse struktuuri lisandmooduli [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] mallis kirjutuskaitstuks.:</span><span class="sxs-lookup"><span data-stu-id="af8c9-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="af8c9-196">Projekti plaani muutmiseks tuleb muudatusi teha tarkvaras [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Project ning avaldada need värskendusena lisandmoodulis [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af8c9-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="af8c9-197">Vt ka</span><span class="sxs-lookup"><span data-stu-id="af8c9-197">See Also</span></span>  
 [<span data-ttu-id="af8c9-198">Projektijuhi juhend</span><span class="sxs-lookup"><span data-stu-id="af8c9-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
