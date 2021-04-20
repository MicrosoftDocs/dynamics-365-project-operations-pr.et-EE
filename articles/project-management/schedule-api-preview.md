---
title: Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks
description: Selles teemas on toodud teave ja näited ajakava API-de kasutamise kohta.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868124"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="644e0-103">Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks</span><span class="sxs-lookup"><span data-stu-id="644e0-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="644e0-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="644e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="644e0-105">Osad või kõik selles teemas märgitud funktsioonid on saadaval suunatud kasutajatele osana eelversiooni väljaandest.</span><span class="sxs-lookup"><span data-stu-id="644e0-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="644e0-106">Sisu ja funktsioonid võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="644e0-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="644e0-107">Olemite ajastamine</span><span class="sxs-lookup"><span data-stu-id="644e0-107">Scheduling entities</span></span>

<span data-ttu-id="644e0-108">Ajakava API-d annavad võimaluse teha suvandiga **Olemite ajastamine** loomise, värskendamise ja kustutamise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="644e0-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="644e0-109">Neid olemeid hallatakse veebirakenduse Project ajastamise mootori kaudu.</span><span class="sxs-lookup"><span data-stu-id="644e0-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="644e0-110">Suvandiga **Olemite ajastamine** toimingute loomine, värskendamine ja kustutamine oli rakenduse Dynamics 365 Project Operations varasemates väljaannetes piiratud.</span><span class="sxs-lookup"><span data-stu-id="644e0-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="644e0-111">Järgmises tabelis on toodud suvandi **Olemite kavandamine** täielik loend.</span><span class="sxs-lookup"><span data-stu-id="644e0-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="644e0-112">Olemi nimi</span><span class="sxs-lookup"><span data-stu-id="644e0-112">Entity name</span></span>  | <span data-ttu-id="644e0-113">Olemi loogiline nimi</span><span class="sxs-lookup"><span data-stu-id="644e0-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="644e0-114">Project</span><span class="sxs-lookup"><span data-stu-id="644e0-114">Project</span></span> | <span data-ttu-id="644e0-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="644e0-115">msdyn_project</span></span> |
| <span data-ttu-id="644e0-116">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="644e0-116">Project Task</span></span>  | <span data-ttu-id="644e0-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="644e0-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="644e0-118">Projekti ülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="644e0-118">Project Task Dependency</span></span>  | <span data-ttu-id="644e0-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="644e0-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="644e0-120">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="644e0-120">Resource Assignment</span></span> | <span data-ttu-id="644e0-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="644e0-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="644e0-122">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="644e0-122">Project Bucket</span></span>  | <span data-ttu-id="644e0-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="644e0-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="644e0-124">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="644e0-124">Project Team Member</span></span> | <span data-ttu-id="644e0-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="644e0-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="644e0-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="644e0-126">OperationSet</span></span>

<span data-ttu-id="644e0-127">OperationSet on tööühiku muster, mida saab kasutada juhul, kui kandes tuleb töödelda mitut ajakava mõjutavat taotlust.</span><span class="sxs-lookup"><span data-stu-id="644e0-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="644e0-128">API-de kavandamine</span><span class="sxs-lookup"><span data-stu-id="644e0-128">Schedule APIs</span></span>

<span data-ttu-id="644e0-129">Järgnev on praeguste API-de ajastamise loend.</span><span class="sxs-lookup"><span data-stu-id="644e0-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="644e0-130">**msdyn_CreateProjectV1**: seda API-d saab kasutada projekti loomiseks.</span><span class="sxs-lookup"><span data-stu-id="644e0-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="644e0-131">Projekt ja vaikimisi projektisalv luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="644e0-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="644e0-132">**msdyn_CreateTeamMemberV1**: seda API-d saab kasutada projektimeeskonna liikme loomiseks.</span><span class="sxs-lookup"><span data-stu-id="644e0-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="644e0-133">Meeskonnaliikme kirje luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="644e0-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="644e0-134">**msdyn_CreateOperationSetV1**: seda API-d saab kasutada mitme taotluse ajastamiseks, mis tuleb kande sees teha.</span><span class="sxs-lookup"><span data-stu-id="644e0-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="644e0-135">**msdyn_PSSCreateV1**: seda API-d saab kasutada olemi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="644e0-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="644e0-136">Olem võib olla mis tahes ajastamise olem, mis toetab loomise toimingut.</span><span class="sxs-lookup"><span data-stu-id="644e0-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="644e0-137">**msdyn_PSSUpdateV1**: seda API-d saab kasutada olemi uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="644e0-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="644e0-138">Olem võib olla mis tahes ajastamise olem, mis toetab värskendamise toimingut.</span><span class="sxs-lookup"><span data-stu-id="644e0-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="644e0-139">**msdyn_PSSDeleteV1**: seda API-d saab kasutada olemi kustutamiseks.</span><span class="sxs-lookup"><span data-stu-id="644e0-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="644e0-140">Olem võib olla mis tahes ajastamise olem, mis toetab kustutamise toimingut.</span><span class="sxs-lookup"><span data-stu-id="644e0-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="644e0-141">**msdyn_ExecuteOperationSetV1**: seda API-d kasutatakse antud toimingute komplektis kõikide toimingute täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="644e0-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="644e0-142">Ajakava API-de kasutamine üksusega OperationSet</span><span class="sxs-lookup"><span data-stu-id="644e0-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="644e0-143">Kuna nii API **CreateProjectV1** kui ka **CreateTeamMemberV1** kirjed luuakse kohe, ei saa neid API-sid olemis **OperationSet** otse kasutada.</span><span class="sxs-lookup"><span data-stu-id="644e0-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="644e0-144">Samas saate kasutada API-d, et luua vajalikke kirjeid, luua üksuse **OperationSet** ja kasutada seejärel neid eelnevalt loodud kirjeid üksuses **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="644e0-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="644e0-145">Toetatud toimingud</span><span class="sxs-lookup"><span data-stu-id="644e0-145">Supported operations</span></span>

| <span data-ttu-id="644e0-146">Olemi ajastamine</span><span class="sxs-lookup"><span data-stu-id="644e0-146">Scheduling entity</span></span> | <span data-ttu-id="644e0-147">Koosta</span><span class="sxs-lookup"><span data-stu-id="644e0-147">Create</span></span> | <span data-ttu-id="644e0-148">Värskendus</span><span class="sxs-lookup"><span data-stu-id="644e0-148">Update</span></span> | <span data-ttu-id="644e0-149">Kustutusklahv (Delete)</span><span class="sxs-lookup"><span data-stu-id="644e0-149">Delete</span></span> | <span data-ttu-id="644e0-150">Olulised kaalutlused</span><span class="sxs-lookup"><span data-stu-id="644e0-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="644e0-151">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="644e0-151">Project task</span></span> | <span data-ttu-id="644e0-152">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-152">Yes</span></span> | <span data-ttu-id="644e0-153">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-153">Yes</span></span> | <span data-ttu-id="644e0-154">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-154">Yes</span></span> | <span data-ttu-id="644e0-155">Pole</span><span class="sxs-lookup"><span data-stu-id="644e0-155">None</span></span> |
| <span data-ttu-id="644e0-156">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="644e0-156">Project task dependency</span></span> | <span data-ttu-id="644e0-157">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-157">Yes</span></span> | <span data-ttu-id="644e0-158">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-158">Yes</span></span> | | <span data-ttu-id="644e0-159">Projektiülesande sõltuvuskirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="644e0-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="644e0-160">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="644e0-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="644e0-161">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="644e0-161">Resource assignment</span></span> | <span data-ttu-id="644e0-162">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-162">Yes</span></span> | <span data-ttu-id="644e0-163">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-163">Yes</span></span> | | <span data-ttu-id="644e0-164">Järgmiste väljadega toiminguid ei toetata: **BookableResourceID** (Broneeritava ressursi ID), **Effort** (Panus), **EffortCompleted** (Lõpule viidud panus), **EffortRemaining** (Järelejäänud panus) ja **PlannedWork** (Planeeritud töö).</span><span class="sxs-lookup"><span data-stu-id="644e0-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="644e0-165">Ressursi määramise kirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="644e0-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="644e0-166">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="644e0-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="644e0-167">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="644e0-167">Project bucket</span></span> | <span data-ttu-id="644e0-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="644e0-168">N/A</span></span> | <span data-ttu-id="644e0-169">Puudub</span><span class="sxs-lookup"><span data-stu-id="644e0-169">N/A</span></span> | <span data-ttu-id="644e0-170">Puudub</span><span class="sxs-lookup"><span data-stu-id="644e0-170">N/A</span></span> | <span data-ttu-id="644e0-171">Vaikesalv luuakse API-d **CreateProjectV1** kasutades.</span><span class="sxs-lookup"><span data-stu-id="644e0-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="644e0-172">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="644e0-172">Project team member</span></span> | <span data-ttu-id="644e0-173">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-173">Yes</span></span> | <span data-ttu-id="644e0-174">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-174">Yes</span></span> | <span data-ttu-id="644e0-175">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-175">Yes</span></span> | <span data-ttu-id="644e0-176">Kasutage loomistoiminguks API-d **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="644e0-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="644e0-177">Project</span><span class="sxs-lookup"><span data-stu-id="644e0-177">Project</span></span> | <span data-ttu-id="644e0-178">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-178">Yes</span></span> | <span data-ttu-id="644e0-179">Ja</span><span class="sxs-lookup"><span data-stu-id="644e0-179">Yes</span></span> | <span data-ttu-id="644e0-180">Puudub</span><span class="sxs-lookup"><span data-stu-id="644e0-180">N/A</span></span> | <span data-ttu-id="644e0-181">Järgmiste väljadega toiminguid ei toetata: **StateCode** (Olekukood), **BulkGenerationStatus** (Hulgiloomise olek), **GlobalRevisionToken** (Üldine redaktsioonitõend), **CalendarID** (Kalendri ID), **Effort** (Panus), **EffortCompleted** (Lõpule jõudnud panus), **EffortRemaining** (Järelejäänud panus), **Progress** (Edenemine), **Finish** (Lõpp), **TaskEarliestStart** (Ülesande varajaseim algus) ja **Duration** (Kestus).</span><span class="sxs-lookup"><span data-stu-id="644e0-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="644e0-182">Neid API-sid saab kutsuda olemiobjektidega, mis sisaldavad kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="644e0-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="644e0-183">ID atribuut on valikuline.</span><span class="sxs-lookup"><span data-stu-id="644e0-183">The ID property is optional.</span></span> <span data-ttu-id="644e0-184">Kui see on antud, proovib süsteem seda kasutada ja loob erandi, kui seda ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="644e0-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="644e0-185">Kui seda ei ole antud, loob süsteem selle.</span><span class="sxs-lookup"><span data-stu-id="644e0-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="644e0-186">Piirangud ja teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="644e0-186">Limitations and known issues</span></span>
<span data-ttu-id="644e0-187">Järgnevalt on toodud piirangute ja teadaolevate probleemide loend.</span><span class="sxs-lookup"><span data-stu-id="644e0-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="644e0-188">Ajakava API-sid saavad kasutada ainult **Microsoft Projecti litsentsiga kasutajad.**</span><span class="sxs-lookup"><span data-stu-id="644e0-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="644e0-189">Neid ei saa kasutada järgnevad.</span><span class="sxs-lookup"><span data-stu-id="644e0-189">They can't be used by:</span></span>
    - <span data-ttu-id="644e0-190">Rakenduse kasutajad</span><span class="sxs-lookup"><span data-stu-id="644e0-190">Application users</span></span>
    - <span data-ttu-id="644e0-191">Süsteemi kasutajad</span><span class="sxs-lookup"><span data-stu-id="644e0-191">System users</span></span>
    - <span data-ttu-id="644e0-192">Integratsiooni kasutajad</span><span class="sxs-lookup"><span data-stu-id="644e0-192">Integration users</span></span>
    - <span data-ttu-id="644e0-193">Teised kasutajad, kes ei oma nõutavat litsentsi</span><span class="sxs-lookup"><span data-stu-id="644e0-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="644e0-194">Igal suvandil **OperationSet** saab olla maksimaalselt 100 toimingut.</span><span class="sxs-lookup"><span data-stu-id="644e0-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="644e0-195">Igal kasutajal saab maksimaalselt olla 10 avatud suvandit **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="644e0-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="644e0-196">Project Operations toetab praegu projektil kokku maksimaalselt 500 ülesannet.</span><span class="sxs-lookup"><span data-stu-id="644e0-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="644e0-197">Suvandi **OperationSet** tõrkeolek ja tõrkelogid pole hetkel saadaval.</span><span class="sxs-lookup"><span data-stu-id="644e0-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="644e0-198">Ajakava API-d on avalikus eelversioonis.</span><span class="sxs-lookup"><span data-stu-id="644e0-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="644e0-199">Microsoft ei toeta nende API-de kasutamist töökeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="644e0-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="644e0-200">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="644e0-200">Sample scenario</span></span>

<span data-ttu-id="644e0-201">Selles stsenaariumis loote projekti, meeskonnaliikme, neli ülesannet ja kaks ressursi määramist.</span><span class="sxs-lookup"><span data-stu-id="644e0-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="644e0-202">Järgmisena värskendate ühte ülesannet, värskendate projekti, kustutate ühe ülesande, kustutate ühe ressursi määramise ja loote ülesande sõltuvuse.</span><span class="sxs-lookup"><span data-stu-id="644e0-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="644e0-203">Täiendavad näited</span><span class="sxs-lookup"><span data-stu-id="644e0-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
