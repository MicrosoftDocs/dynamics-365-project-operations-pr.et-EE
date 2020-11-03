---
title: Üldiste broneeritavate ressursside määramine tööülesande ja projekti meeskonna jaoks
description: See teema pakub teavet tööülesannetele ja projekti meeskondadele üldressursside broneerimise kohta.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074971"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="783b7-103">Üldiste broneeritavate ressursside määramine tööülesande jaoks ressursi nõuete loomine</span><span class="sxs-lookup"><span data-stu-id="783b7-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="783b7-104">Peale broneerimise ja projektile nime või tegeliku ressurssi määramise, saate projekti tööülesannetele üldressursid määrata.</span><span class="sxs-lookup"><span data-stu-id="783b7-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="783b7-105">Need ressursid võivad olla nimega ressursside kohatäited, kuni olete valmis oma projekti nimega ressurssidega täitma.</span><span class="sxs-lookup"><span data-stu-id="783b7-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="783b7-106">Avage rakenduses Project Service Automation (PSA) lehel **Projekt** ja sisestage vahekaardil **Ajakava** üldressursi positsiooni nimi ajakava lahtrisse **Ressurss**.</span><span class="sxs-lookup"><span data-stu-id="783b7-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="783b7-107">Või klõpsake ressursivalija avamiseks lahtris ikooni **Ressurss** ja seejärel sisestage selle üldressursi nimi, mida soovite luua.</span><span class="sxs-lookup"><span data-stu-id="783b7-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Üldise meeskonnaliikme loomine ja määramine](media/RM-how-to-9.png)

<span data-ttu-id="783b7-109">See avab paneeli **Kiirloomine: projekti meeskonnaliige**.</span><span class="sxs-lookup"><span data-stu-id="783b7-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="783b7-110">Sisestage üldressursi meeskonnaliikme roll ja organisatsiooniüksus ning klõpsake siis käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="783b7-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Üldise meeskonnaliikme kiirloomine](media/RM-how-to-10.png)

3. <span data-ttu-id="783b7-112">Kui olete loonud uue üldressursi meeskonnaliikme, määratakse talle tööülesanne.</span><span class="sxs-lookup"><span data-stu-id="783b7-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="783b7-113">Saate jätkata selle üldressursi määramist tööülesannete ajakava muudele toimingutele.</span><span class="sxs-lookup"><span data-stu-id="783b7-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Olemasoleva üldise meeskonnaliikme määramine tööülesannetele](media/RM-how-to-11.png)

4. <span data-ttu-id="783b7-115">Pärast seda, kui olete määranud üldressursi, saate ressursi nõude genereerida ja selle täita otse ressursihaldurisse ressursi taotluse broneerimisel või esitamisel.</span><span class="sxs-lookup"><span data-stu-id="783b7-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Üldise meeskonnaliikme jaoks nõude loomine](media/RM-how-to-12.png)

<span data-ttu-id="783b7-117">Meeskonnaliikme ruudustikul saate peale ülalmainitud ressursivalija kasutamist lisada üldisi ressursse otse.</span><span class="sxs-lookup"><span data-stu-id="783b7-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="783b7-118">Ressursid lisatakse ressursi nõudele, mis põhineb paanil **Kiirloomine: projekti meeskonnaliige** määratud algus- ja lõppkuupäevadel ning eraldamise meetodil.</span><span class="sxs-lookup"><span data-stu-id="783b7-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="783b7-119">Erinevust näete juhul, kui lisate otse üldise meeskonnaliikme ja määrate üldressursile rohkem tööülesandeid, kui nad on tundide katmiseks taotlenud.</span><span class="sxs-lookup"><span data-stu-id="783b7-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="783b7-120">Kui soovite taastada vajalike tundide ja määrangute vahelise tasakaalu klõpsake **Loo nõue**.</span><span class="sxs-lookup"><span data-stu-id="783b7-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="783b7-121">Nõude avamiseks ja oskuste, eelistatud ressursside jms lisamiseks võite klõpsata ka meeskonna ruudustikus linki **Ressursinõue**.</span><span class="sxs-lookup"><span data-stu-id="783b7-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Ressursinõue](media/RM-how-to-13.png)

