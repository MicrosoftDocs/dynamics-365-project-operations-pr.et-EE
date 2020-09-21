---
title: Tööjaotuse struktuuriga projekti ajastamine
description: Tööjaotuse struktuuriga projekti plaanimine Project Service'is
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751013"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="4ae4f-103">Tööjaotuse struktuuriga projekti plaanimine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4ae4f-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4ae4f-104">Projekti ajakavas on andmed selle kohta, millist tööd on vaja teha, millised ressursid töö teevad ja ajapiirid, milles töö tuleb ära teha.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="4ae4f-105">Projekti ajakava kajastab kogu tööd, mis on seotud projekti õigeaegse valmimisega.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="4ae4f-106">Üks esimesi toiminguid projekti algatamise faasis on koostada projekti ajakava.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="4ae4f-107">Projekti ajakava loomiseks peate koostama tööjaotuse struktuuri.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="4ae4f-108">Koostage tööjaotuse struktuuriga projekti struktuur, mis aitab teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="4ae4f-109">Jagada tööd hallatavateks ülesanneteks</span><span class="sxs-lookup"><span data-stu-id="4ae4f-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="4ae4f-110">Hinnata ülesande täitmiseks vajalikku aega</span><span class="sxs-lookup"><span data-stu-id="4ae4f-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="4ae4f-111">Määrata ülesande sõltuvusi ja kestust</span><span class="sxs-lookup"><span data-stu-id="4ae4f-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="4ae4f-112">Määrata iga ülesande täitmiseks vajalikke rolle</span><span class="sxs-lookup"><span data-stu-id="4ae4f-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="4ae4f-113">Projekti ajakava tööjaotuse struktuuris näeb tuttav välja ning sellel on interaktiivne Gantti diagramm.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="4ae4f-114">Projektile tööjaotuse struktuuri loomine</span><span class="sxs-lookup"><span data-stu-id="4ae4f-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="4ae4f-115">Saate luua tööjaotuse struktuuri, mis kajastab projekti ülesannete järjekorda.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="4ae4f-116">Tööjaotuse struktuur sisaldab ülesandeid, iga ülesande nõudmisi ja tulu ning kulu andmeid.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="4ae4f-117">Tööjaotuse struktuuri saate lisada järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="4ae4f-118">Ülesannete järjestus hierarhias</span><span class="sxs-lookup"><span data-stu-id="4ae4f-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="4ae4f-119">Muud ülesanded (kui on), mis tuleb enne ülesande alustamist täita</span><span class="sxs-lookup"><span data-stu-id="4ae4f-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="4ae4f-120">Ülesande alguskuupäev, lõppkuupäev ja kestus</span><span class="sxs-lookup"><span data-stu-id="4ae4f-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="4ae4f-121">Ülesande jaoks vajalik tundide arv</span><span class="sxs-lookup"><span data-stu-id="4ae4f-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="4ae4f-122">Vajalikud töötaja oskused ja haridus</span><span class="sxs-lookup"><span data-stu-id="4ae4f-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="4ae4f-123">Töötajad, kes on tööülesandele määratud</span><span class="sxs-lookup"><span data-stu-id="4ae4f-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="4ae4f-124">Eeldatav tulu ja kulud</span><span class="sxs-lookup"><span data-stu-id="4ae4f-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="4ae4f-125">Ülesannete tüübid</span><span class="sxs-lookup"><span data-stu-id="4ae4f-125">Task types</span></span>  
<span data-ttu-id="4ae4f-126">Tööjaotuse struktuuri koostamisel kasutatakse järgmisi ülesannete tüüpe.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="4ae4f-127">**Projekti juursõlm**</span><span class="sxs-lookup"><span data-stu-id="4ae4f-127">**Project root node**</span></span> | <span data-ttu-id="4ae4f-128">Projekti ülataseme kokkuvõtteülesanne.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-128">The top-level summary task for the project.</span></span> <span data-ttu-id="4ae4f-129">Kõik muud projekti ülesanded luuakse selle alla.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-129">All other project tasks are created under it.</span></span> <span data-ttu-id="4ae4f-130">Juurülesande nimi on projekti nimi.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-130">The name of the root task is the project name.</span></span> <span data-ttu-id="4ae4f-131">Juursõlme panus, kuupäevad ja kestus põhinevad selle all oleva hierarhia väärtustel.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="4ae4f-132">Juursõlme atribuute saab muuta või juursõlme saab kustutada.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="4ae4f-133">**Kokkuvõtvad ehk konteinerülesanded**</span><span class="sxs-lookup"><span data-stu-id="4ae4f-133">**Summary or container tasks**</span></span> | <span data-ttu-id="4ae4f-134">Kokkuvõttev ülesanne on alamülesannetega ülesanne.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="4ae4f-135">Kokkuvõtval ülesandel pole oma tööpanust ega maksumust.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="4ae4f-136">Selle tööpanus ja maksumus koosneb alamülesannete koondväärtusest.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="4ae4f-137">Kokkuvõtva ülesande nime saab muuta, kuid panust, kuupäevi ega kestust ei saa muuta, kuna need arvutatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="4ae4f-138">Kokkuvõtva ülesande kustutamisel kustutatakse ülesanne ja kõik selle alamülesanded.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="4ae4f-139">**Lehesõlme ülesanded**</span><span class="sxs-lookup"><span data-stu-id="4ae4f-139">**Leaf node tasks**</span></span> | <span data-ttu-id="4ae4f-140">Lehesõlme ülesanne kajastab projekti kõige üksikasjalikumat tööd.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="4ae4f-141">Sellel on arvestuslik panus, plaanitud hulk ressursse, plaanitud algus- ja lõppkuupäevad ning kestus.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="4ae4f-142">Ülesannete hierarhia</span><span class="sxs-lookup"><span data-stu-id="4ae4f-142">Task hierarchy</span></span>  
 <span data-ttu-id="4ae4f-143">Ülesannete hierarhia loomisel on teil järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="4ae4f-144">**Ülesande lisamine**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-144">**Add task**.</span></span>   <span data-ttu-id="4ae4f-145">Saate lisada ülesande ülesannete hierarhias valitud kohta.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="4ae4f-146">Kui te kohta ei vali, kuvatakse teie uus ülesanne lõpus.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="4ae4f-147">**Ülesande taandamine**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-147">**Indent task**.</span></span>   <span data-ttu-id="4ae4f-148">Saate ülesande taandada, muutes selle otse ülesande kohal oleva ülesande alamülesandeks.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="4ae4f-149">**Ülesande eendamine**</span><span class="sxs-lookup"><span data-stu-id="4ae4f-149">**Outdent task**.</span></span>   <span data-ttu-id="4ae4f-150">Saate ülesande eendada, et see poleks enam algse põhiülesande alamülesanne.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="4ae4f-151">**Nihuta üles ja Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-151">**Move up and Move down**.</span></span>   <span data-ttu-id="4ae4f-152">Saate nihutada ülesandeid peamise ülesande hierarhias üles ja alla.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="4ae4f-153">Ülesande üles või alla nihutamisel puudub mõju selle panusele, maksumusele, kuupäevadele või kestusele.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="4ae4f-154">Ülesande atribuudid</span><span class="sxs-lookup"><span data-stu-id="4ae4f-154">Task attributes</span></span>  
 <span data-ttu-id="4ae4f-155">Ülesande nimi kirjeldab tööd, mida on vaja teha.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="4ae4f-156">Mitmesuguste ülesande atribuutide abil saab kirjeldada ülesande ajakava ja personalinõudeid.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="4ae4f-157">Atribuutide plaanimine</span><span class="sxs-lookup"><span data-stu-id="4ae4f-157">Schedule attributes</span></span>

 - <span data-ttu-id="4ae4f-158">Saate määrata väärtusi valikutele **Panuse tunnid**, **Ressursside arv**, **Alguskuupäev**, **Lõppkuupäev** ja **Kestus** ülesande ajakava määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="4ae4f-159">**Panus** on ülesande lõpuleviimiseks eeldatavalt kuluv tundide arv.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="4ae4f-160">**Ressursside arv** on hinnanguline väärtus, mille projektijuht ülesandele lisab, et saada parim võimalik ajakava.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="4ae4f-161">**Kestus** (päevades) näitab ülesande täitmiseks vajalikku tööpäevade arvu.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="4ae4f-162">Personaliatribuudid</span><span class="sxs-lookup"><span data-stu-id="4ae4f-162">Staffing attributes</span></span>

 - <span data-ttu-id="4ae4f-163">**Roll**, **Ressursi organisatsiooniüksus**, **Ressursside arv** ja **Ressursid** kirjeldavad ülesande personalivajadusi.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="4ae4f-164">**Roll** kirjeldab ülesande sooritamiseks vajalikku ressursi tüüpi.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="4ae4f-165">**Ressursi organisatsiooniüksus** tähistab organisatsiooniüksust, millest selle ülesande jaoks ressursid tuleks võtta; see mõjutab ka ülesande eeldatavat maksumust ja müügihinda, kuna seda arvestatakse ühiku müügihinna määramisel ressursile.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="4ae4f-166">**Ressursid** sisaldavad üldist ressurssi või nimelist ressurssi, kui see leitakse.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="4ae4f-167">Ülesande sõltuvused</span><span class="sxs-lookup"><span data-stu-id="4ae4f-167">Task dependencies</span></span>  
 <span data-ttu-id="4ae4f-168">Saate luua eelkäija seoseid tööjaotuse struktuuri ülesannete vahel.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="4ae4f-169">Saate määrata ülesannete eelkäija väljale vähemalt ühe väärtuse, et näidata ülesandeid, millest see sõltub.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="4ae4f-170">Eelkäija väärtuse määramisel ülesandele saab ülesanne alata alles siis, kui eelkäijatest ülesanded on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="4ae4f-171">Selle sõltuvuse määramisel ülesandele arvutatakse ülesande plaanitav alguskuupäev ümber kõigi selle eelkäijate hiliseimaks lõppkuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="4ae4f-172">Eelkäijaga seotud mõju ajakavale pole ülesandele määratletud ajakavarežiimiga piiratud.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="4ae4f-173">Ülesande režiim</span><span class="sxs-lookup"><span data-stu-id="4ae4f-173">Task mode</span></span>  
 <span data-ttu-id="4ae4f-174">Ülesande režiim on üks olulistest teguritest, mis määravad ajakava lehesõlme ülesanded.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="4ae4f-175">Igal ülesandel on kaks režiimi: automaatne plaanimisrežiim ja käsitsi plaanimisrežiim.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="4ae4f-176">**Automaatne plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-176">**Auto scheduling**.</span></span>   <span data-ttu-id="4ae4f-177">Kui määrate ülesande režiimiks automaatse plaanimise, kasutab ülesande plaanimismootor plaanimisreegleid järgmistel ülesande atribuutidel ülesande ajakava määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="4ae4f-178">Eelkäijad</span><span class="sxs-lookup"><span data-stu-id="4ae4f-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="4ae4f-179">Panus</span><span class="sxs-lookup"><span data-stu-id="4ae4f-179">Effort</span></span>  
  
    -   <span data-ttu-id="4ae4f-180">Ressursside arv</span><span class="sxs-lookup"><span data-stu-id="4ae4f-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="4ae4f-181">algus- ja lõppkuupäevad;</span><span class="sxs-lookup"><span data-stu-id="4ae4f-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="4ae4f-182">**Plaanimise reeglid**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-182">**Scheduling rules**.</span></span>   <span data-ttu-id="4ae4f-183">Eelkäijateta lehesõlme ülesande alguskuupäev on vaikimisi projekti ajakava alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="4ae4f-184">Lehesõlme ülesande kestuseks arvutatakse alati algus- ja lõppkuupäeva vaheline päevade arv.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="4ae4f-185">Kui ülesanne on automaatselt ajastatud, järgib plaanimismootor järgmisi reegleid.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="4ae4f-186">Ülesande algus- ja lõppkuupäev peavad alati olema projekti plaanimiskalendrile vastavad tööpäevad</span><span class="sxs-lookup"><span data-stu-id="4ae4f-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="4ae4f-187">Eelkäijatega ülesande alguskuupäev on vaikimisi selle eelkäijate hiliseim lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="4ae4f-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="4ae4f-188">Panus = inimeste arv \* kestus \* projektikalendri standardtööpäeva tundide arv</span><span class="sxs-lookup"><span data-stu-id="4ae4f-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="4ae4f-189">**Käsitsi plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-189">**Manual scheduling**.</span></span>   <span data-ttu-id="4ae4f-190">Mõnikord võib olla vaja neist reeglitest erinevalt tegutseda.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="4ae4f-191">Sellisel juhul saate määrata ülesande režiimi käsitsi plaanimise.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="4ae4f-192">Sellega lõpetab plaanimismootor teiste plaanimisatribuutide väärtuste arvutamise.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="4ae4f-193">Ülesannete eelkäijate seadistamine mõjutab alati sõltuva ülesande alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="4ae4f-194">Tööjaotuse struktuuri loomine</span><span class="sxs-lookup"><span data-stu-id="4ae4f-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="4ae4f-195">Minge jaotisse **Project Service > Projektid**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="4ae4f-196">Klõpsake projekti, millega soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="4ae4f-197">Valige kuva ülaosas asuvalt ribalt projekti nime kõrval olev allanool ja seejärel klõpsake valikut Tööjaotuse struktuur.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="4ae4f-198">Ülesande lisamiseks klõpsake käsku **Lisa ülesanne**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="4ae4f-199">Täitke ülesande väljad ja klõpsake siis käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="4ae4f-200">Jätkake ülesannete lisamist, kuni tööjaotuse struktuur on valmis.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="4ae4f-201">Tööjaotuse struktuuri loomisel saate ülesannete korraldamiseks teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="4ae4f-202">Valige ülesanne ja klõpsake käsku **Taanda**, et nihutada see teise ülesande alla, või käsku Eenda, et nihutada see taseme võrra üles.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="4ae4f-203">Valige ülesanne ja klõpsake käsku **Nihuta üles** või **Nihuta alla**, et nihutada seda loendis üles või alla.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="4ae4f-204">Gantti diagrammi peitmiseks klõpsake valikut **Peida Gantt**, selle uuesti kuvamiseks klõpsake valikut **Kuva Gantt**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="4ae4f-205">Saate valida Gantti diagrammi jaoks muu ajavahemiku jaotises **Ajaskaala**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="4ae4f-206">Tööjaotuse struktuuris määratud rollide lisamiseks projekti meeskonnaliikmetele klõpsake käsku **Loo projektimeeskond**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="4ae4f-207">Kui olete muudatuste tegemise lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4ae4f-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4ae4f-208">Vt ka</span><span class="sxs-lookup"><span data-stu-id="4ae4f-208">See Also</span></span>  
 [<span data-ttu-id="4ae4f-209">Projektijuhi juhend</span><span class="sxs-lookup"><span data-stu-id="4ae4f-209">Project manager guide</span></span>](../project-service/project-manager-guide.md)
