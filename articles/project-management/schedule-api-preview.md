---
title: Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks
description: Selles teemas on toodud teave ja näited projekti ajakava API-de kasutamise kohta.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293222"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="762cf-103">Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks</span><span class="sxs-lookup"><span data-stu-id="762cf-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="762cf-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="762cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="762cf-105">Osad või kõik selles teemas märgitud funktsioonid on saadaval suunatud kasutajatele osana eelversiooni väljaandest.</span><span class="sxs-lookup"><span data-stu-id="762cf-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="762cf-106">Sisu ja funktsioonid võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="762cf-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="762cf-107">Olemite ajastamine</span><span class="sxs-lookup"><span data-stu-id="762cf-107">Scheduling entities</span></span>

<span data-ttu-id="762cf-108">Projekti ajakava API-d annavad võimaluse teha **ajastamise olemitega** loomise, värskendamise ja kustutamise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="762cf-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="762cf-109">Neid olemeid hallatakse veebirakenduse Project ajastamise mootori kaudu.</span><span class="sxs-lookup"><span data-stu-id="762cf-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="762cf-110">Suvandiga **Olemite ajastamine** toimingute loomine, värskendamine ja kustutamine oli rakenduse Dynamics 365 Project Operations varasemates väljaannetes piiratud.</span><span class="sxs-lookup"><span data-stu-id="762cf-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="762cf-111">Järgmises tabelid on toodud projekti ajakava olemite täielik loend.</span><span class="sxs-lookup"><span data-stu-id="762cf-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="762cf-112">Olemi nimi</span><span class="sxs-lookup"><span data-stu-id="762cf-112">Entity name</span></span>  | <span data-ttu-id="762cf-113">Olemi loogiline nimi</span><span class="sxs-lookup"><span data-stu-id="762cf-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="762cf-114">Project</span><span class="sxs-lookup"><span data-stu-id="762cf-114">Project</span></span> | <span data-ttu-id="762cf-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="762cf-115">msdyn_project</span></span> |
| <span data-ttu-id="762cf-116">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="762cf-116">Project Task</span></span>  | <span data-ttu-id="762cf-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="762cf-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="762cf-118">Projekti ülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="762cf-118">Project Task Dependency</span></span>  | <span data-ttu-id="762cf-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="762cf-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="762cf-120">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="762cf-120">Resource Assignment</span></span> | <span data-ttu-id="762cf-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="762cf-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="762cf-122">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="762cf-122">Project Bucket</span></span>  | <span data-ttu-id="762cf-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="762cf-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="762cf-124">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="762cf-124">Project Team Member</span></span> | <span data-ttu-id="762cf-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="762cf-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="762cf-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="762cf-126">OperationSet</span></span>

<span data-ttu-id="762cf-127">OperationSet on tööühiku muster, mida saab kasutada juhul, kui kandes tuleb töödelda mitut ajakava mõjutavat taotlust.</span><span class="sxs-lookup"><span data-stu-id="762cf-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="762cf-128">Projekti ajakava API-d</span><span class="sxs-lookup"><span data-stu-id="762cf-128">Project schedule APIs</span></span>

<span data-ttu-id="762cf-129">Järgnev on praeguste projekti ajakava API-de loend.</span><span class="sxs-lookup"><span data-stu-id="762cf-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="762cf-130">**msdyn_CreateProjectV1**: seda API-d saab kasutada projekti loomiseks.</span><span class="sxs-lookup"><span data-stu-id="762cf-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="762cf-131">Projekt ja vaikimisi projektisalv luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="762cf-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="762cf-132">**msdyn_CreateTeamMemberV1**: seda API-d saab kasutada projektimeeskonna liikme loomiseks.</span><span class="sxs-lookup"><span data-stu-id="762cf-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="762cf-133">Meeskonnaliikme kirje luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="762cf-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="762cf-134">**msdyn_CreateOperationSetV1**: seda API-d saab kasutada mitme taotluse ajastamiseks, mis tuleb kande sees teha.</span><span class="sxs-lookup"><span data-stu-id="762cf-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="762cf-135">**msdyn_PSSCreateV1**: seda API-d saab kasutada olemi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="762cf-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="762cf-136">Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab loomistoimingut.</span><span class="sxs-lookup"><span data-stu-id="762cf-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="762cf-137">**msdyn_PSSUpdateV1**: seda API-d saab kasutada olemi uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="762cf-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="762cf-138">Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab värskendamistoimingut.</span><span class="sxs-lookup"><span data-stu-id="762cf-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="762cf-139">**msdyn_PSSDeleteV1**: seda API-d saab kasutada olemi kustutamiseks.</span><span class="sxs-lookup"><span data-stu-id="762cf-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="762cf-140">Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab kustutamistoimingut.</span><span class="sxs-lookup"><span data-stu-id="762cf-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="762cf-141">**msdyn_ExecuteOperationSetV1**: seda API-d kasutatakse antud toimingute komplektis kõikide toimingute täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="762cf-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="762cf-142">Projekti ajakava API-de kasutamine väärtusega OperationSet</span><span class="sxs-lookup"><span data-stu-id="762cf-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="762cf-143">Kuna nii API **CreateProjectV1** kui ka **CreateTeamMemberV1** kirjed luuakse kohe, ei saa neid API-sid olemis **OperationSet** otse kasutada.</span><span class="sxs-lookup"><span data-stu-id="762cf-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="762cf-144">Samas saate kasutada API-d, et luua vajalikke kirjeid, luua üksuse **OperationSet** ja kasutada seejärel neid eelnevalt loodud kirjeid üksuses **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="762cf-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="762cf-145">Toetatud toimingud</span><span class="sxs-lookup"><span data-stu-id="762cf-145">Supported operations</span></span>

| <span data-ttu-id="762cf-146">Olemi ajastamine</span><span class="sxs-lookup"><span data-stu-id="762cf-146">Scheduling entity</span></span> | <span data-ttu-id="762cf-147">Koosta</span><span class="sxs-lookup"><span data-stu-id="762cf-147">Create</span></span> | <span data-ttu-id="762cf-148">Värskendus</span><span class="sxs-lookup"><span data-stu-id="762cf-148">Update</span></span> | <span data-ttu-id="762cf-149">Kustutusklahv (Delete)</span><span class="sxs-lookup"><span data-stu-id="762cf-149">Delete</span></span> | <span data-ttu-id="762cf-150">Olulised kaalutlused</span><span class="sxs-lookup"><span data-stu-id="762cf-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="762cf-151">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="762cf-151">Project task</span></span> | <span data-ttu-id="762cf-152">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-152">Yes</span></span> | <span data-ttu-id="762cf-153">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-153">Yes</span></span> | <span data-ttu-id="762cf-154">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-154">Yes</span></span> | <span data-ttu-id="762cf-155">Pole</span><span class="sxs-lookup"><span data-stu-id="762cf-155">None</span></span> |
| <span data-ttu-id="762cf-156">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="762cf-156">Project task dependency</span></span> | <span data-ttu-id="762cf-157">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-157">Yes</span></span> | <span data-ttu-id="762cf-158">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-158">Yes</span></span> | | <span data-ttu-id="762cf-159">Projektiülesande sõltuvuskirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="762cf-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="762cf-160">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="762cf-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="762cf-161">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="762cf-161">Resource assignment</span></span> | <span data-ttu-id="762cf-162">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-162">Yes</span></span> | <span data-ttu-id="762cf-163">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-163">Yes</span></span> | | <span data-ttu-id="762cf-164">Järgmiste väljadega toiminguid ei toetata: **BookableResourceID** (Broneeritava ressursi ID), **Effort** (Panus), **EffortCompleted** (Lõpule viidud panus), **EffortRemaining** (Järelejäänud panus) ja **PlannedWork** (Planeeritud töö).</span><span class="sxs-lookup"><span data-stu-id="762cf-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="762cf-165">Ressursi määramise kirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="762cf-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="762cf-166">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="762cf-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="762cf-167">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="762cf-167">Project bucket</span></span> | <span data-ttu-id="762cf-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="762cf-168">N/A</span></span> | <span data-ttu-id="762cf-169">Puudub</span><span class="sxs-lookup"><span data-stu-id="762cf-169">N/A</span></span> | <span data-ttu-id="762cf-170">Puudub</span><span class="sxs-lookup"><span data-stu-id="762cf-170">N/A</span></span> | <span data-ttu-id="762cf-171">Vaikesalv luuakse API-d **CreateProjectV1** kasutades.</span><span class="sxs-lookup"><span data-stu-id="762cf-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="762cf-172">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="762cf-172">Project team member</span></span> | <span data-ttu-id="762cf-173">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-173">Yes</span></span> | <span data-ttu-id="762cf-174">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-174">Yes</span></span> | <span data-ttu-id="762cf-175">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-175">Yes</span></span> | <span data-ttu-id="762cf-176">Kasutage loomistoiminguks API-d **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="762cf-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="762cf-177">Project</span><span class="sxs-lookup"><span data-stu-id="762cf-177">Project</span></span> | <span data-ttu-id="762cf-178">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-178">Yes</span></span> | <span data-ttu-id="762cf-179">Ja</span><span class="sxs-lookup"><span data-stu-id="762cf-179">Yes</span></span> | <span data-ttu-id="762cf-180">Puudub</span><span class="sxs-lookup"><span data-stu-id="762cf-180">N/A</span></span> | <span data-ttu-id="762cf-181">Järgmiste väljadega toiminguid ei toetata: **StateCode** (Olekukood), **BulkGenerationStatus** (Hulgiloomise olek), **GlobalRevisionToken** (Üldine redaktsioonitõend), **CalendarID** (Kalendri ID), **Effort** (Panus), **EffortCompleted** (Lõpule jõudnud panus), **EffortRemaining** (Järelejäänud panus), **Progress** (Edenemine), **Finish** (Lõpp), **TaskEarliestStart** (Ülesande varajaseim algus) ja **Duration** (Kestus).</span><span class="sxs-lookup"><span data-stu-id="762cf-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="762cf-182">Neid API-sid saab kutsuda olemiobjektidega, mis sisaldavad kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="762cf-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="762cf-183">ID atribuut on valikuline.</span><span class="sxs-lookup"><span data-stu-id="762cf-183">The ID property is optional.</span></span> <span data-ttu-id="762cf-184">Kui see on antud, proovib süsteem seda kasutada ja loob erandi, kui seda ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="762cf-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="762cf-185">Kui seda ei ole antud, loob süsteem selle.</span><span class="sxs-lookup"><span data-stu-id="762cf-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="762cf-186">Piiratud väljad</span><span class="sxs-lookup"><span data-stu-id="762cf-186">Restricted fields</span></span>

<span data-ttu-id="762cf-187">Järgmistes tabelites määratletakse väljad, mille **loomine** ja **redigeerimine** on piiratud.</span><span class="sxs-lookup"><span data-stu-id="762cf-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="762cf-188">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="762cf-188">Project task</span></span>

| <span data-ttu-id="762cf-189">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="762cf-189">**Logical name**</span></span>                       | <span data-ttu-id="762cf-190">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="762cf-190">**Can create**</span></span> | <span data-ttu-id="762cf-191">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="762cf-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="762cf-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="762cf-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="762cf-193">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-193">no</span></span>             | <span data-ttu-id="762cf-194">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-194">no</span></span>               |
| <span data-ttu-id="762cf-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="762cf-196">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-196">no</span></span>             | <span data-ttu-id="762cf-197">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-197">no</span></span>               |
| <span data-ttu-id="762cf-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="762cf-198">msdyn_actualend</span></span>                        | <span data-ttu-id="762cf-199">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-199">no</span></span>             | <span data-ttu-id="762cf-200">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-200">no</span></span>               |
| <span data-ttu-id="762cf-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="762cf-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="762cf-202">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-202">no</span></span>             | <span data-ttu-id="762cf-203">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-203">no</span></span>               |
| <span data-ttu-id="762cf-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="762cf-205">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-205">no</span></span>             | <span data-ttu-id="762cf-206">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-206">no</span></span>               |
| <span data-ttu-id="762cf-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="762cf-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="762cf-208">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-208">no</span></span>             | <span data-ttu-id="762cf-209">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-209">no</span></span>               |
| <span data-ttu-id="762cf-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="762cf-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="762cf-211">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-211">no</span></span>             | <span data-ttu-id="762cf-212">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-212">no</span></span>               |
| <span data-ttu-id="762cf-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="762cf-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="762cf-214">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-214">no</span></span>             | <span data-ttu-id="762cf-215">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-215">no</span></span>               |
| <span data-ttu-id="762cf-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="762cf-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="762cf-217">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-217">no</span></span>             | <span data-ttu-id="762cf-218">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-218">no</span></span>               |
| <span data-ttu-id="762cf-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="762cf-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="762cf-220">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-220">no</span></span>             | <span data-ttu-id="762cf-221">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-221">no</span></span>               |
| <span data-ttu-id="762cf-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="762cf-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="762cf-223">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-223">no</span></span>             | <span data-ttu-id="762cf-224">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-224">no</span></span>               |
| <span data-ttu-id="762cf-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="762cf-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="762cf-226">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-226">no</span></span>             | <span data-ttu-id="762cf-227">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-227">no</span></span>               |
| <span data-ttu-id="762cf-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="762cf-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="762cf-229">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-229">no</span></span>             | <span data-ttu-id="762cf-230">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-230">no</span></span>               |
| <span data-ttu-id="762cf-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="762cf-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="762cf-232">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-232">no</span></span>             | <span data-ttu-id="762cf-233">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-233">no</span></span>               |
| <span data-ttu-id="762cf-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="762cf-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="762cf-235">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-235">no</span></span>             | <span data-ttu-id="762cf-236">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-236">no</span></span>               |
| <span data-ttu-id="762cf-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="762cf-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="762cf-238">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-238">no</span></span>             | <span data-ttu-id="762cf-239">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-239">no</span></span>               |
| <span data-ttu-id="762cf-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="762cf-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="762cf-241">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-241">no</span></span>             | <span data-ttu-id="762cf-242">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-242">no</span></span>               |
| <span data-ttu-id="762cf-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="762cf-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="762cf-244">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-244">no</span></span>             | <span data-ttu-id="762cf-245">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-245">no</span></span>               |
| <span data-ttu-id="762cf-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="762cf-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="762cf-247">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-247">no</span></span>             | <span data-ttu-id="762cf-248">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-248">no</span></span>               |
| <span data-ttu-id="762cf-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="762cf-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="762cf-250">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-250">no</span></span>             | <span data-ttu-id="762cf-251">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-251">no</span></span>               |
| <span data-ttu-id="762cf-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="762cf-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="762cf-253">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-253">no</span></span>             | <span data-ttu-id="762cf-254">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-254">no</span></span>               |
| <span data-ttu-id="762cf-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="762cf-256">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-256">no</span></span>             | <span data-ttu-id="762cf-257">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-257">no</span></span>               |
| <span data-ttu-id="762cf-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="762cf-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="762cf-259">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-259">no</span></span>             | <span data-ttu-id="762cf-260">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-260">no</span></span>               |
| <span data-ttu-id="762cf-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="762cf-262">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-262">no</span></span>             | <span data-ttu-id="762cf-263">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-263">no</span></span>               |
| <span data-ttu-id="762cf-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="762cf-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="762cf-265">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-265">no</span></span>             | <span data-ttu-id="762cf-266">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-266">no</span></span>               |
| <span data-ttu-id="762cf-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="762cf-267">msdyn_progress</span></span>                         | <span data-ttu-id="762cf-268">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-268">no</span></span>             | <span data-ttu-id="762cf-269">ei (jah P4W jaoks)</span><span class="sxs-lookup"><span data-stu-id="762cf-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="762cf-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="762cf-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="762cf-271">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-271">no</span></span>             | <span data-ttu-id="762cf-272">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-272">no</span></span>               |
| <span data-ttu-id="762cf-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="762cf-274">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-274">no</span></span>             | <span data-ttu-id="762cf-275">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-275">no</span></span>               |
| <span data-ttu-id="762cf-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="762cf-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="762cf-277">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-277">no</span></span>             | <span data-ttu-id="762cf-278">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-278">no</span></span>               |
| <span data-ttu-id="762cf-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="762cf-280">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-280">no</span></span>             | <span data-ttu-id="762cf-281">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-281">no</span></span>               |
| <span data-ttu-id="762cf-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="762cf-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="762cf-283">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-283">no</span></span>             | <span data-ttu-id="762cf-284">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-284">no</span></span>               |
| <span data-ttu-id="762cf-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="762cf-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="762cf-286">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-286">no</span></span>             | <span data-ttu-id="762cf-287">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-287">no</span></span>               |
| <span data-ttu-id="762cf-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="762cf-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="762cf-289">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-289">no</span></span>             | <span data-ttu-id="762cf-290">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-290">no</span></span>               |
| <span data-ttu-id="762cf-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="762cf-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="762cf-292">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-292">no</span></span>             | <span data-ttu-id="762cf-293">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-293">no</span></span>               |
| <span data-ttu-id="762cf-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="762cf-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="762cf-295">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-295">no</span></span>             | <span data-ttu-id="762cf-296">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-296">no</span></span>               |
| <span data-ttu-id="762cf-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="762cf-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="762cf-298">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-298">no</span></span>             | <span data-ttu-id="762cf-299">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-299">no</span></span>               |
| <span data-ttu-id="762cf-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="762cf-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="762cf-301">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-301">no</span></span>             | <span data-ttu-id="762cf-302">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-302">no</span></span>               |
| <span data-ttu-id="762cf-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="762cf-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="762cf-304">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-304">no</span></span>             | <span data-ttu-id="762cf-305">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-305">no</span></span>               |
| <span data-ttu-id="762cf-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="762cf-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="762cf-307">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-307">no</span></span>             | <span data-ttu-id="762cf-308">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-308">no</span></span>               |
| <span data-ttu-id="762cf-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="762cf-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="762cf-310">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-310">no</span></span>             | <span data-ttu-id="762cf-311">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-311">no</span></span>               |
| <span data-ttu-id="762cf-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="762cf-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="762cf-313">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-313">no</span></span>             | <span data-ttu-id="762cf-314">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-314">no</span></span>               |
| <span data-ttu-id="762cf-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="762cf-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="762cf-316">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-316">no</span></span>             | <span data-ttu-id="762cf-317">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-317">no</span></span>               |
| <span data-ttu-id="762cf-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="762cf-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="762cf-319">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-319">no</span></span>             | <span data-ttu-id="762cf-320">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-320">no</span></span>               |
| <span data-ttu-id="762cf-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="762cf-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="762cf-322">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-322">no</span></span>             | <span data-ttu-id="762cf-323">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-323">no</span></span>               |
| <span data-ttu-id="762cf-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="762cf-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="762cf-325">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-325">no</span></span>             | <span data-ttu-id="762cf-326">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-326">no</span></span>               |
| <span data-ttu-id="762cf-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="762cf-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="762cf-328">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-328">no</span></span>             | <span data-ttu-id="762cf-329">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-329">no</span></span>               |
| <span data-ttu-id="762cf-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="762cf-330">msdyn_summary</span></span>                          | <span data-ttu-id="762cf-331">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-331">no</span></span>             | <span data-ttu-id="762cf-332">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-332">no</span></span>               |
| <span data-ttu-id="762cf-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="762cf-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="762cf-334">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-334">no</span></span>             | <span data-ttu-id="762cf-335">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-335">no</span></span>               |
| <span data-ttu-id="762cf-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="762cf-337">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-337">no</span></span>             | <span data-ttu-id="762cf-338">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="762cf-339">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="762cf-339">Project task dependency</span></span>

| <span data-ttu-id="762cf-340">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="762cf-340">**Logical name**</span></span>              | <span data-ttu-id="762cf-341">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="762cf-341">**Can create**</span></span> | <span data-ttu-id="762cf-342">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="762cf-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="762cf-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="762cf-343">msdyn_linktype</span></span>                | <span data-ttu-id="762cf-344">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-344">no</span></span>             | <span data-ttu-id="762cf-345">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-345">no</span></span>           |
| <span data-ttu-id="762cf-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="762cf-346">msdyn_linktypename</span></span>            | <span data-ttu-id="762cf-347">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-347">no</span></span>             | <span data-ttu-id="762cf-348">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-348">no</span></span>           |
| <span data-ttu-id="762cf-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="762cf-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="762cf-350">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-350">yes</span></span>            | <span data-ttu-id="762cf-351">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-351">no</span></span>           |
| <span data-ttu-id="762cf-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="762cf-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="762cf-353">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-353">yes</span></span>            | <span data-ttu-id="762cf-354">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-354">no</span></span>           |
| <span data-ttu-id="762cf-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="762cf-355">msdyn_project</span></span>                 | <span data-ttu-id="762cf-356">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-356">yes</span></span>            | <span data-ttu-id="762cf-357">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-357">no</span></span>           |
| <span data-ttu-id="762cf-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="762cf-358">msdyn_projectname</span></span>             | <span data-ttu-id="762cf-359">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-359">yes</span></span>            | <span data-ttu-id="762cf-360">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-360">no</span></span>           |
| <span data-ttu-id="762cf-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="762cf-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="762cf-362">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-362">yes</span></span>            | <span data-ttu-id="762cf-363">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-363">no</span></span>           |
| <span data-ttu-id="762cf-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="762cf-364">msdyn_successortask</span></span>           | <span data-ttu-id="762cf-365">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-365">yes</span></span>            | <span data-ttu-id="762cf-366">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-366">no</span></span>           |
| <span data-ttu-id="762cf-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="762cf-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="762cf-368">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-368">yes</span></span>            | <span data-ttu-id="762cf-369">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="762cf-370">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="762cf-370">Resource assignment</span></span>

| <span data-ttu-id="762cf-371">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="762cf-371">**Logical name**</span></span>             | <span data-ttu-id="762cf-372">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="762cf-372">**Can create**</span></span> | <span data-ttu-id="762cf-373">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="762cf-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="762cf-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="762cf-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="762cf-375">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-375">yes</span></span>            | <span data-ttu-id="762cf-376">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-376">no</span></span>           |
| <span data-ttu-id="762cf-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="762cf-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="762cf-378">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-378">yes</span></span>            | <span data-ttu-id="762cf-379">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-379">no</span></span>           |
| <span data-ttu-id="762cf-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="762cf-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="762cf-381">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-381">no</span></span>             | <span data-ttu-id="762cf-382">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-382">no</span></span>           |
| <span data-ttu-id="762cf-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="762cf-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="762cf-384">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-384">no</span></span>             | <span data-ttu-id="762cf-385">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-385">no</span></span>           |
| <span data-ttu-id="762cf-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="762cf-386">msdyn_committype</span></span>             | <span data-ttu-id="762cf-387">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-387">no</span></span>             | <span data-ttu-id="762cf-388">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-388">no</span></span>           |
| <span data-ttu-id="762cf-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="762cf-389">msdyn_committypename</span></span>         | <span data-ttu-id="762cf-390">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-390">no</span></span>             | <span data-ttu-id="762cf-391">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-391">no</span></span>           |
| <span data-ttu-id="762cf-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="762cf-392">msdyn_effort</span></span>                 | <span data-ttu-id="762cf-393">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-393">no</span></span>             | <span data-ttu-id="762cf-394">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-394">no</span></span>           |
| <span data-ttu-id="762cf-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="762cf-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="762cf-396">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-396">no</span></span>             | <span data-ttu-id="762cf-397">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-397">no</span></span>           |
| <span data-ttu-id="762cf-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="762cf-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="762cf-399">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-399">no</span></span>             | <span data-ttu-id="762cf-400">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-400">no</span></span>           |
| <span data-ttu-id="762cf-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="762cf-401">msdyn_finish</span></span>                 | <span data-ttu-id="762cf-402">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-402">no</span></span>             | <span data-ttu-id="762cf-403">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-403">no</span></span>           |
| <span data-ttu-id="762cf-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="762cf-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="762cf-405">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-405">no</span></span>             | <span data-ttu-id="762cf-406">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-406">no</span></span>           |
| <span data-ttu-id="762cf-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="762cf-408">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-408">no</span></span>             | <span data-ttu-id="762cf-409">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-409">no</span></span>           |
| <span data-ttu-id="762cf-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="762cf-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="762cf-411">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-411">no</span></span>             | <span data-ttu-id="762cf-412">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-412">no</span></span>           |
| <span data-ttu-id="762cf-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="762cf-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="762cf-414">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-414">no</span></span>             | <span data-ttu-id="762cf-415">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-415">no</span></span>           |
| <span data-ttu-id="762cf-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="762cf-417">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-417">no</span></span>             | <span data-ttu-id="762cf-418">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-418">no</span></span>           |
| <span data-ttu-id="762cf-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="762cf-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="762cf-420">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-420">no</span></span>             | <span data-ttu-id="762cf-421">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-421">no</span></span>           |
| <span data-ttu-id="762cf-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="762cf-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="762cf-423">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-423">no</span></span>             | <span data-ttu-id="762cf-424">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-424">no</span></span>           |
| <span data-ttu-id="762cf-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="762cf-425">msdyn_projectid</span></span>              | <span data-ttu-id="762cf-426">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-426">yes</span></span>            | <span data-ttu-id="762cf-427">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-427">no</span></span>           |
| <span data-ttu-id="762cf-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="762cf-428">msdyn_projectidname</span></span>          | <span data-ttu-id="762cf-429">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-429">no</span></span>             | <span data-ttu-id="762cf-430">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-430">no</span></span>           |
| <span data-ttu-id="762cf-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="762cf-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="762cf-432">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-432">no</span></span>             | <span data-ttu-id="762cf-433">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-433">no</span></span>           |
| <span data-ttu-id="762cf-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="762cf-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="762cf-435">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-435">no</span></span>             | <span data-ttu-id="762cf-436">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-436">no</span></span>           |
| <span data-ttu-id="762cf-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="762cf-437">msdyn_start</span></span>                  | <span data-ttu-id="762cf-438">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-438">no</span></span>             | <span data-ttu-id="762cf-439">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-439">no</span></span>           |
| <span data-ttu-id="762cf-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="762cf-440">msdyn_taskid</span></span>                 | <span data-ttu-id="762cf-441">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-441">no</span></span>             | <span data-ttu-id="762cf-442">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-442">no</span></span>           |
| <span data-ttu-id="762cf-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="762cf-443">msdyn_taskidname</span></span>             | <span data-ttu-id="762cf-444">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-444">no</span></span>             | <span data-ttu-id="762cf-445">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-445">no</span></span>           |
| <span data-ttu-id="762cf-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="762cf-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="762cf-447">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-447">no</span></span>             | <span data-ttu-id="762cf-448">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="762cf-449">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="762cf-449">Project team member</span></span>

| <span data-ttu-id="762cf-450">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="762cf-450">**Logical name**</span></span>                                 | <span data-ttu-id="762cf-451">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="762cf-451">**Can create**</span></span> | <span data-ttu-id="762cf-452">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="762cf-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="762cf-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="762cf-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="762cf-454">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-454">no</span></span>             | <span data-ttu-id="762cf-455">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-455">no</span></span>           |
| <span data-ttu-id="762cf-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="762cf-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="762cf-457">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-457">no</span></span>             | <span data-ttu-id="762cf-458">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-458">no</span></span>           |
| <span data-ttu-id="762cf-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="762cf-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="762cf-460">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-460">no</span></span>             | <span data-ttu-id="762cf-461">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-461">no</span></span>           |
| <span data-ttu-id="762cf-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="762cf-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="762cf-463">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-463">no</span></span>             | <span data-ttu-id="762cf-464">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-464">no</span></span>           |
| <span data-ttu-id="762cf-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="762cf-465">msdyn_effort</span></span>                                     | <span data-ttu-id="762cf-466">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-466">no</span></span>             | <span data-ttu-id="762cf-467">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-467">no</span></span>           |
| <span data-ttu-id="762cf-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="762cf-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="762cf-469">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-469">no</span></span>             | <span data-ttu-id="762cf-470">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-470">no</span></span>           |
| <span data-ttu-id="762cf-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="762cf-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="762cf-472">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-472">no</span></span>             | <span data-ttu-id="762cf-473">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-473">no</span></span>           |
| <span data-ttu-id="762cf-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="762cf-474">msdyn_finish</span></span>                                     | <span data-ttu-id="762cf-475">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-475">no</span></span>             | <span data-ttu-id="762cf-476">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-476">no</span></span>           |
| <span data-ttu-id="762cf-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="762cf-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="762cf-478">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-478">no</span></span>             | <span data-ttu-id="762cf-479">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-479">no</span></span>           |
| <span data-ttu-id="762cf-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="762cf-480">msdyn_hours</span></span>                                      | <span data-ttu-id="762cf-481">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-481">no</span></span>             | <span data-ttu-id="762cf-482">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-482">no</span></span>           |
| <span data-ttu-id="762cf-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="762cf-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="762cf-484">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-484">no</span></span>             | <span data-ttu-id="762cf-485">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-485">no</span></span>           |
| <span data-ttu-id="762cf-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="762cf-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="762cf-487">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-487">no</span></span>             | <span data-ttu-id="762cf-488">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-488">no</span></span>           |
| <span data-ttu-id="762cf-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="762cf-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="762cf-490">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-490">no</span></span>             | <span data-ttu-id="762cf-491">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-491">no</span></span>           |
| <span data-ttu-id="762cf-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="762cf-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="762cf-493">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-493">no</span></span>             | <span data-ttu-id="762cf-494">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-494">no</span></span>           |
| <span data-ttu-id="762cf-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="762cf-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="762cf-496">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-496">no</span></span>             | <span data-ttu-id="762cf-497">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-497">no</span></span>           |
| <span data-ttu-id="762cf-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="762cf-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="762cf-499">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-499">no</span></span>             | <span data-ttu-id="762cf-500">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-500">no</span></span>           |
| <span data-ttu-id="762cf-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="762cf-501">msdyn_start</span></span>                                      | <span data-ttu-id="762cf-502">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-502">no</span></span>             | <span data-ttu-id="762cf-503">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="762cf-504">Project</span><span class="sxs-lookup"><span data-stu-id="762cf-504">Project</span></span>

| <span data-ttu-id="762cf-505">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="762cf-505">**Logical name**</span></span>                       | <span data-ttu-id="762cf-506">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="762cf-506">**Can create**</span></span> | <span data-ttu-id="762cf-507">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="762cf-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="762cf-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="762cf-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="762cf-509">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-509">no</span></span>             | <span data-ttu-id="762cf-510">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-510">no</span></span>           |
| <span data-ttu-id="762cf-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="762cf-512">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-512">no</span></span>             | <span data-ttu-id="762cf-513">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-513">no</span></span>           |
| <span data-ttu-id="762cf-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="762cf-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="762cf-515">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-515">no</span></span>             | <span data-ttu-id="762cf-516">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-516">no</span></span>           |
| <span data-ttu-id="762cf-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="762cf-518">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-518">no</span></span>             | <span data-ttu-id="762cf-519">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-519">no</span></span>           |
| <span data-ttu-id="762cf-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="762cf-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="762cf-521">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-521">no</span></span>             | <span data-ttu-id="762cf-522">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-522">no</span></span>           |
| <span data-ttu-id="762cf-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="762cf-524">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-524">no</span></span>             | <span data-ttu-id="762cf-525">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-525">no</span></span>           |
| <span data-ttu-id="762cf-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="762cf-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="762cf-527">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-527">yes</span></span>            | <span data-ttu-id="762cf-528">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-528">no</span></span>           |
| <span data-ttu-id="762cf-529">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="762cf-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="762cf-530">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-530">yes</span></span>            | <span data-ttu-id="762cf-531">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-531">no</span></span>           |
| <span data-ttu-id="762cf-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="762cf-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="762cf-533">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-533">yes</span></span>            | <span data-ttu-id="762cf-534">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-534">no</span></span>           |
| <span data-ttu-id="762cf-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="762cf-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="762cf-536">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-536">no</span></span>             | <span data-ttu-id="762cf-537">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-537">no</span></span>           |
| <span data-ttu-id="762cf-538">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="762cf-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="762cf-539">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-539">no</span></span>             | <span data-ttu-id="762cf-540">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-540">no</span></span>           |
| <span data-ttu-id="762cf-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="762cf-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="762cf-542">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-542">no</span></span>             | <span data-ttu-id="762cf-543">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-543">no</span></span>           |
| <span data-ttu-id="762cf-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="762cf-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="762cf-545">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-545">no</span></span>             | <span data-ttu-id="762cf-546">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-546">no</span></span>           |
| <span data-ttu-id="762cf-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="762cf-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="762cf-548">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-548">no</span></span>             | <span data-ttu-id="762cf-549">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-549">no</span></span>           |
| <span data-ttu-id="762cf-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="762cf-550">msdyn_duration</span></span>                         | <span data-ttu-id="762cf-551">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-551">no</span></span>             | <span data-ttu-id="762cf-552">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-552">no</span></span>           |
| <span data-ttu-id="762cf-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="762cf-553">msdyn_effort</span></span>                           | <span data-ttu-id="762cf-554">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-554">no</span></span>             | <span data-ttu-id="762cf-555">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-555">no</span></span>           |
| <span data-ttu-id="762cf-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="762cf-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="762cf-557">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-557">no</span></span>             | <span data-ttu-id="762cf-558">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-558">no</span></span>           |
| <span data-ttu-id="762cf-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="762cf-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="762cf-560">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-560">no</span></span>             | <span data-ttu-id="762cf-561">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-561">no</span></span>           |
| <span data-ttu-id="762cf-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="762cf-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="762cf-563">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-563">no</span></span>             | <span data-ttu-id="762cf-564">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-564">no</span></span>           |
| <span data-ttu-id="762cf-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="762cf-565">msdyn_finish</span></span>                           | <span data-ttu-id="762cf-566">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-566">yes</span></span>            | <span data-ttu-id="762cf-567">jah</span><span class="sxs-lookup"><span data-stu-id="762cf-567">yes</span></span>          |
| <span data-ttu-id="762cf-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="762cf-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="762cf-569">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-569">no</span></span>             | <span data-ttu-id="762cf-570">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-570">no</span></span>           |
| <span data-ttu-id="762cf-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="762cf-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="762cf-572">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-572">no</span></span>             | <span data-ttu-id="762cf-573">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-573">no</span></span>           |
| <span data-ttu-id="762cf-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="762cf-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="762cf-575">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-575">no</span></span>             | <span data-ttu-id="762cf-576">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-576">no</span></span>           |
| <span data-ttu-id="762cf-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="762cf-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="762cf-578">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-578">no</span></span>             | <span data-ttu-id="762cf-579">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-579">no</span></span>           |
| <span data-ttu-id="762cf-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="762cf-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="762cf-581">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-581">no</span></span>             | <span data-ttu-id="762cf-582">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-582">no</span></span>           |
| <span data-ttu-id="762cf-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="762cf-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="762cf-584">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-584">no</span></span>             | <span data-ttu-id="762cf-585">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-585">no</span></span>           |
| <span data-ttu-id="762cf-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="762cf-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="762cf-587">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-587">no</span></span>             | <span data-ttu-id="762cf-588">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-588">no</span></span>           |
| <span data-ttu-id="762cf-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="762cf-590">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-590">no</span></span>             | <span data-ttu-id="762cf-591">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-591">no</span></span>           |
| <span data-ttu-id="762cf-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="762cf-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="762cf-593">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-593">no</span></span>             | <span data-ttu-id="762cf-594">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-594">no</span></span>           |
| <span data-ttu-id="762cf-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="762cf-596">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-596">no</span></span>             | <span data-ttu-id="762cf-597">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-597">no</span></span>           |
| <span data-ttu-id="762cf-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="762cf-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="762cf-599">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-599">no</span></span>             | <span data-ttu-id="762cf-600">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-600">no</span></span>           |
| <span data-ttu-id="762cf-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="762cf-602">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-602">no</span></span>             | <span data-ttu-id="762cf-603">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-603">no</span></span>           |
| <span data-ttu-id="762cf-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="762cf-604">msdyn_progress</span></span>                         | <span data-ttu-id="762cf-605">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-605">no</span></span>             | <span data-ttu-id="762cf-606">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-606">no</span></span>           |
| <span data-ttu-id="762cf-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="762cf-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="762cf-608">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-608">no</span></span>             | <span data-ttu-id="762cf-609">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-609">no</span></span>           |
| <span data-ttu-id="762cf-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="762cf-611">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-611">no</span></span>             | <span data-ttu-id="762cf-612">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-612">no</span></span>           |
| <span data-ttu-id="762cf-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="762cf-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="762cf-614">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-614">no</span></span>             | <span data-ttu-id="762cf-615">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-615">no</span></span>           |
| <span data-ttu-id="762cf-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="762cf-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="762cf-617">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-617">no</span></span>             | <span data-ttu-id="762cf-618">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-618">no</span></span>           |
| <span data-ttu-id="762cf-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="762cf-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="762cf-620">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-620">no</span></span>             | <span data-ttu-id="762cf-621">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-621">no</span></span>           |
| <span data-ttu-id="762cf-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="762cf-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="762cf-623">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-623">no</span></span>             | <span data-ttu-id="762cf-624">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-624">no</span></span>           |
| <span data-ttu-id="762cf-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="762cf-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="762cf-626">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-626">no</span></span>             | <span data-ttu-id="762cf-627">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-627">no</span></span>           |
| <span data-ttu-id="762cf-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="762cf-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="762cf-629">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-629">no</span></span>             | <span data-ttu-id="762cf-630">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-630">no</span></span>           |
| <span data-ttu-id="762cf-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="762cf-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="762cf-632">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-632">no</span></span>             | <span data-ttu-id="762cf-633">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-633">no</span></span>           |
| <span data-ttu-id="762cf-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="762cf-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="762cf-635">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-635">no</span></span>             | <span data-ttu-id="762cf-636">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-636">no</span></span>           |
| <span data-ttu-id="762cf-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="762cf-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="762cf-638">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-638">no</span></span>             | <span data-ttu-id="762cf-639">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-639">no</span></span>           |
| <span data-ttu-id="762cf-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="762cf-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="762cf-641">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-641">no</span></span>             | <span data-ttu-id="762cf-642">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-642">no</span></span>           |
| <span data-ttu-id="762cf-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="762cf-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="762cf-644">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-644">no</span></span>             | <span data-ttu-id="762cf-645">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-645">no</span></span>           |
| <span data-ttu-id="762cf-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="762cf-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="762cf-647">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-647">no</span></span>             | <span data-ttu-id="762cf-648">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-648">no</span></span>           |
| <span data-ttu-id="762cf-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="762cf-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="762cf-650">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-650">no</span></span>             | <span data-ttu-id="762cf-651">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-651">no</span></span>           |
| <span data-ttu-id="762cf-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="762cf-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="762cf-653">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-653">no</span></span>             | <span data-ttu-id="762cf-654">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-654">no</span></span>           |
| <span data-ttu-id="762cf-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="762cf-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="762cf-656">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-656">no</span></span>             | <span data-ttu-id="762cf-657">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-657">no</span></span>           |
| <span data-ttu-id="762cf-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="762cf-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="762cf-659">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-659">no</span></span>             | <span data-ttu-id="762cf-660">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-660">no</span></span>           |
| <span data-ttu-id="762cf-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="762cf-662">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-662">no</span></span>             | <span data-ttu-id="762cf-663">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-663">no</span></span>           |
| <span data-ttu-id="762cf-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="762cf-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="762cf-665">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-665">no</span></span>             | <span data-ttu-id="762cf-666">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-666">no</span></span>           |
| <span data-ttu-id="762cf-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="762cf-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="762cf-668">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-668">no</span></span>             | <span data-ttu-id="762cf-669">ei</span><span class="sxs-lookup"><span data-stu-id="762cf-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="762cf-670">Piirangud ja teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="762cf-670">Limitations and known issues</span></span>
<span data-ttu-id="762cf-671">Järgnevalt on toodud piirangute ja teadaolevate probleemide loend.</span><span class="sxs-lookup"><span data-stu-id="762cf-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="762cf-672">Projekti ajakava API-sid saavad kasutada ainult **Microsoft Projecti litsentsiga kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="762cf-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="762cf-673">Neid ei saa kasutada järgnevad.</span><span class="sxs-lookup"><span data-stu-id="762cf-673">They can't be used by:</span></span>
    - <span data-ttu-id="762cf-674">Rakenduse kasutajad</span><span class="sxs-lookup"><span data-stu-id="762cf-674">Application users</span></span>
    - <span data-ttu-id="762cf-675">Süsteemi kasutajad</span><span class="sxs-lookup"><span data-stu-id="762cf-675">System users</span></span>
    - <span data-ttu-id="762cf-676">Integratsiooni kasutajad</span><span class="sxs-lookup"><span data-stu-id="762cf-676">Integration users</span></span>
    - <span data-ttu-id="762cf-677">Teised kasutajad, kes ei oma nõutavat litsentsi</span><span class="sxs-lookup"><span data-stu-id="762cf-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="762cf-678">Igal suvandil **OperationSet** saab olla maksimaalselt 100 toimingut.</span><span class="sxs-lookup"><span data-stu-id="762cf-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="762cf-679">Igal kasutajal saab maksimaalselt olla 10 avatud suvandit **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="762cf-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="762cf-680">Project Operations toetab praegu projektil kokku maksimaalselt 500 ülesannet.</span><span class="sxs-lookup"><span data-stu-id="762cf-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="762cf-681">Suvandi **OperationSet** tõrkeolek ja tõrkelogid pole hetkel saadaval.</span><span class="sxs-lookup"><span data-stu-id="762cf-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="762cf-682">Projektide ja tööülesannete piirangud ja piirid</span><span class="sxs-lookup"><span data-stu-id="762cf-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="762cf-683">Tõrketöötlus</span><span class="sxs-lookup"><span data-stu-id="762cf-683">Error handling</span></span>

   - <span data-ttu-id="762cf-684">Toimingukomplektide põhjal loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **Toimingutekomplekt**.</span><span class="sxs-lookup"><span data-stu-id="762cf-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="762cf-685">Projekti ajastamisteenuses loodud tõrgete läbivaatamiseks minge jaotisse **Sätted** \> **Ajakava integreerimine** \> **PSS-i tõrkelogid**.</span><span class="sxs-lookup"><span data-stu-id="762cf-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="762cf-686">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="762cf-686">Sample scenario</span></span>

<span data-ttu-id="762cf-687">Selles stsenaariumis loote projekti, meeskonnaliikme, neli ülesannet ja kaks ressursi määramist.</span><span class="sxs-lookup"><span data-stu-id="762cf-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="762cf-688">Järgmisena värskendate ühte ülesannet, värskendate projekti, kustutate ühe ülesande, kustutate ühe ressursi määramise ja loote ülesande sõltuvuse.</span><span class="sxs-lookup"><span data-stu-id="762cf-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="762cf-689">Täiendavad näited</span><span class="sxs-lookup"><span data-stu-id="762cf-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
