---
title: Tööjaotuse struktuuri täiendamise kaalutlused
description: Selles teemas kirjeldatakse, kuidas täiendada tööjaotuse struktuuri Project Service Automation versioonilt 2.x versioonile 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005606"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="55717-103">Tööjaotuse struktuuri täiendamise kaalutlused</span><span class="sxs-lookup"><span data-stu-id="55717-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="55717-104">Selles teemas kirjeldatakse, kuidas täiendada tööjaotuse struktuuri Project Service Automation versioonilt 2.x versioonile 3.x.</span><span class="sxs-lookup"><span data-stu-id="55717-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="55717-105">Selles teemas määratletakse projekti töökorras olek Project Service Automation (PSA), mis on vajalik edukaks täienduseks.</span><span class="sxs-lookup"><span data-stu-id="55717-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="55717-106">Samuti leiate sellest teemast teavet levinud blokeerimistingimuste kohta, mis põhjustavad täienduse nurjumist.</span><span class="sxs-lookup"><span data-stu-id="55717-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="55717-107">Lisateavet projekti ülesannete ja nende funktsioonide määratlemise kohta projekti ajakava raames leiate jaotisest [Projekti ajakavad](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="55717-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="55717-108">Põhiolemid</span><span class="sxs-lookup"><span data-stu-id="55717-108">Key entities</span></span>
<span data-ttu-id="55717-109">Täpse tööjaotuse struktuuri jaoks, mis on juba ressurssidega laaditud, on nõutavad järgmised olemid.</span><span class="sxs-lookup"><span data-stu-id="55717-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="55717-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="55717-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="55717-111">Projektimeeskond</span><span class="sxs-lookup"><span data-stu-id="55717-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="55717-112">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="55717-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="55717-113">Ressursimääramised</span><span class="sxs-lookup"><span data-stu-id="55717-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="55717-114">Projekti ülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="55717-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="55717-115">Reserveeritavad ressursid</span><span class="sxs-lookup"><span data-stu-id="55717-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="55717-116">Ressursiga laaditud tööjaotuse struktuuri määratlemiseks peate läbi tegema järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="55717-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="55717-117">Uue projekti loomine.</span><span class="sxs-lookup"><span data-stu-id="55717-117">Create a new project.</span></span> <span data-ttu-id="55717-118">Lisateavet uue projekti loomise kohta leiate jaotisest [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="55717-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="55717-119">Ühe või mitme ülesande loomine.</span><span class="sxs-lookup"><span data-stu-id="55717-119">Create one or more tasks.</span></span> <span data-ttu-id="55717-120">Lisateavet ülesande loomise kohta leiate jaotisest [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="55717-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="55717-121">Ülesannete sõltuvuste määramine.</span><span class="sxs-lookup"><span data-stu-id="55717-121">Define the task dependencies.</span></span> <span data-ttu-id="55717-122">Lisateavet leiate teemast [Projekti tööülesande sõltuvus](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="55717-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="55717-123">Projekti meeskonnaliikmete määramine projektile.</span><span class="sxs-lookup"><span data-stu-id="55717-123">Assign project team members to the project.</span></span> <span data-ttu-id="55717-124">Lisateavet leiate jaotisest [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="55717-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="55717-125">Projekti meeskonnaliikmete määramine ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="55717-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="55717-126">Lisateavet leiate jaotisest [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="55717-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="55717-127">Projekti meeskonna seosed</span><span class="sxs-lookup"><span data-stu-id="55717-127">Project team relationships</span></span>

<span data-ttu-id="55717-128">Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.</span><span class="sxs-lookup"><span data-stu-id="55717-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="55717-129">Kõik projekti meeskonnaliikmed peavad olema seostatud broneeritava ressursiga.</span><span class="sxs-lookup"><span data-stu-id="55717-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="55717-130">Kõik projekti meeskonnaliikmed peavad olema seostatud sama projektiga.</span><span class="sxs-lookup"><span data-stu-id="55717-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="55717-131">Projekti ülesande seosed</span><span class="sxs-lookup"><span data-stu-id="55717-131">Project task relationships</span></span>
<span data-ttu-id="55717-132">Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.</span><span class="sxs-lookup"><span data-stu-id="55717-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="55717-133">Kõik seostuvad ülesanded tuleb seostada sama projektiga.</span><span class="sxs-lookup"><span data-stu-id="55717-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="55717-134">Iga rea ülesandel peab olema emaülesanne.</span><span class="sxs-lookup"><span data-stu-id="55717-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="55717-135">Igal ülesandel peab olema emaprojekt.</span><span class="sxs-lookup"><span data-stu-id="55717-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="55717-136">Sobivad tingimused</span><span class="sxs-lookup"><span data-stu-id="55717-136">Valid conditions</span></span>

- <span data-ttu-id="55717-137">Kõik ülesannete kestused peavad olema suuremad kui üks tund või sellega võrdsed (> =) ja väiksemad kui 1 800 000 minutit (1250 päeva).\*</span><span class="sxs-lookup"><span data-stu-id="55717-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="55717-138">Kõigi ülesannete varaseim alguskuupäev tohib olla 01.01.2000.\*</span><span class="sxs-lookup"><span data-stu-id="55717-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="55717-139">Kõigi ülesannete hiliseim alguskuupäev tohib olla 17 aastast praegusest päevast.\*</span><span class="sxs-lookup"><span data-stu-id="55717-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="55717-140">Kõigi ülesannete alguskuupäev peab olema lõppkuupäevast varasem või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="55717-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="55717-141">Kõigil liigituste (kulu, materjal, maks ja aeg) all olevatel kandetüüpidel peavad olema seatud väärtused väljade **Vaikeühik** ja **Ühikurühm** jaoks.</span><span class="sxs-lookup"><span data-stu-id="55717-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="55717-142">Tähti sisaldavaid kuupäevavorminguid tuleb vältida.</span><span class="sxs-lookup"><span data-stu-id="55717-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="55717-143">Potentsiaalsed lahendusetapid</span><span class="sxs-lookup"><span data-stu-id="55717-143">Potential mitigation steps</span></span>
- <span data-ttu-id="55717-144">Täpsema otsingu abil saate tuvastada projekti tööülesanded, mis ei sisalda projekti ID-d.</span><span class="sxs-lookup"><span data-stu-id="55717-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="55717-145">Täpsema otsingu abil saate tuvastada projekti tööülesanded, mille kavandatav kestus on suurem kui > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="55717-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="55717-146">Enne andmete muutmist peaksite uurima, millised kohandused on seostatud olemiga, mis võis viia andmete halba olekusse sattumiseni.</span><span class="sxs-lookup"><span data-stu-id="55717-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="55717-147">Need kohandused tuleks lahendada enne mis tahes andmetega seotud värskenduste jätkamist.</span><span class="sxs-lookup"><span data-stu-id="55717-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="55717-148">Tuvastatud orvustunud ülesannete korral kaaluge nende tööülesannete kustutamist, kui neid pole vaja või need tuleks seostada õige peamise projektiga.</span><span class="sxs-lookup"><span data-stu-id="55717-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="55717-149">Mis tahes toimingute korral, mille kestus on pikem kui 1 250 päeva, kaaluge vajadusel lisada mitu tööülesannet, et tähistada kogu kestust.</span><span class="sxs-lookup"><span data-stu-id="55717-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="55717-150">Tärniga (\*) märgitud üksustel on piirangud, sest kliendisuhete haldus (CRM) toetab ainult 7320 korduvuse laiendamist.</span><span class="sxs-lookup"><span data-stu-id="55717-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="55717-151">Peate jääma sellest piirist allapoole.</span><span class="sxs-lookup"><span data-stu-id="55717-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="55717-152">Ressursi määramise seosed</span><span class="sxs-lookup"><span data-stu-id="55717-152">Resource Assignment relationships</span></span>
<span data-ttu-id="55717-153">Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.</span><span class="sxs-lookup"><span data-stu-id="55717-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="55717-154">Kõik tööjaotuse struktuuris olevad ressursi määramised peavad olema seotud sama projektiga.</span><span class="sxs-lookup"><span data-stu-id="55717-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="55717-155">Kõik tööjaotuse struktuuris olevad ressursi määramised peavad olema seostatud sama projekti meeskonnaliikmetega.</span><span class="sxs-lookup"><span data-stu-id="55717-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="55717-156">Potentsiaalsed lahendusetapid</span><span class="sxs-lookup"><span data-stu-id="55717-156">Potential mitigation steps</span></span>
- <span data-ttu-id="55717-157">Saate tuvastada kõik tööülesanded, mis jäävad eespool kirjeldatud tingimustest välja.</span><span class="sxs-lookup"><span data-stu-id="55717-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="55717-158">Kõik ressursi määramised, mis enam ei kehti, peaks kustutatama.</span><span class="sxs-lookup"><span data-stu-id="55717-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="55717-159">Projekti ülesande sõltuvuse seosed</span><span class="sxs-lookup"><span data-stu-id="55717-159">Project task dependency relationships</span></span>
<span data-ttu-id="55717-160">Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.</span><span class="sxs-lookup"><span data-stu-id="55717-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="55717-161">Kõik projekti ülesande sõltuvused peavad olema seotud sama projektiga.</span><span class="sxs-lookup"><span data-stu-id="55717-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="55717-162">Ülesandel ei saa samale sõltuvusele viidata rohkem kui üks kord.</span><span class="sxs-lookup"><span data-stu-id="55717-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]