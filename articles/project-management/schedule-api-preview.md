---
title: Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks
description: Selles teemas on toodud teave ja näited ajakava API-de kasutamise kohta.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950799"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="47015-103">Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks</span><span class="sxs-lookup"><span data-stu-id="47015-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="47015-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="47015-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="47015-105">Osad või kõik selles teemas märgitud funktsioonid on saadaval suunatud kasutajatele osana eelversiooni väljaandest.</span><span class="sxs-lookup"><span data-stu-id="47015-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="47015-106">Sisu ja funktsioonid võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="47015-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="47015-107">Olemite ajastamine</span><span class="sxs-lookup"><span data-stu-id="47015-107">Scheduling entities</span></span>

<span data-ttu-id="47015-108">Ajakava API-d annavad võimaluse teha suvandiga **Olemite ajastamine** loomise, värskendamise ja kustutamise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="47015-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="47015-109">Neid olemeid hallatakse veebirakenduse Project ajastamise mootori kaudu.</span><span class="sxs-lookup"><span data-stu-id="47015-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="47015-110">Suvandiga **Olemite ajastamine** toimingute loomine, värskendamine ja kustutamine oli rakenduse Dynamics 365 Project Operations varasemates väljaannetes piiratud.</span><span class="sxs-lookup"><span data-stu-id="47015-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="47015-111">Järgmises tabelis on toodud suvandi **Olemite kavandamine** täielik loend.</span><span class="sxs-lookup"><span data-stu-id="47015-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="47015-112">Olemi nimi</span><span class="sxs-lookup"><span data-stu-id="47015-112">Entity name</span></span>  | <span data-ttu-id="47015-113">Olemi loogiline nimi</span><span class="sxs-lookup"><span data-stu-id="47015-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="47015-114">Project</span><span class="sxs-lookup"><span data-stu-id="47015-114">Project</span></span> | <span data-ttu-id="47015-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="47015-115">msdyn_project</span></span> |
| <span data-ttu-id="47015-116">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="47015-116">Project Task</span></span>  | <span data-ttu-id="47015-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="47015-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="47015-118">Projekti ülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="47015-118">Project Task Dependency</span></span>  | <span data-ttu-id="47015-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="47015-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="47015-120">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="47015-120">Resource Assignment</span></span> | <span data-ttu-id="47015-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="47015-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="47015-122">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="47015-122">Project Bucket</span></span>  | <span data-ttu-id="47015-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="47015-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="47015-124">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="47015-124">Project Team Member</span></span> | <span data-ttu-id="47015-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="47015-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="47015-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="47015-126">OperationSet</span></span>

<span data-ttu-id="47015-127">OperationSet on tööühiku muster, mida saab kasutada juhul, kui kandes tuleb töödelda mitut ajakava mõjutavat taotlust.</span><span class="sxs-lookup"><span data-stu-id="47015-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="47015-128">API-de kavandamine</span><span class="sxs-lookup"><span data-stu-id="47015-128">Schedule APIs</span></span>

<span data-ttu-id="47015-129">Järgnev on praeguste API-de ajastamise loend.</span><span class="sxs-lookup"><span data-stu-id="47015-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="47015-130">**msdyn_CreateProjectV1**: seda API-d saab kasutada projekti loomiseks.</span><span class="sxs-lookup"><span data-stu-id="47015-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="47015-131">Projekt ja vaikimisi projektisalv luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="47015-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="47015-132">**msdyn_CreateTeamMemberV1**: seda API-d saab kasutada projektimeeskonna liikme loomiseks.</span><span class="sxs-lookup"><span data-stu-id="47015-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="47015-133">Meeskonnaliikme kirje luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="47015-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="47015-134">**msdyn_CreateOperationSetV1**: seda API-d saab kasutada mitme taotluse ajastamiseks, mis tuleb kande sees teha.</span><span class="sxs-lookup"><span data-stu-id="47015-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="47015-135">**msdyn_PSSCreateV1**: seda API-d saab kasutada olemi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="47015-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="47015-136">Olem võib olla mis tahes ajastamise olem, mis toetab loomise toimingut.</span><span class="sxs-lookup"><span data-stu-id="47015-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="47015-137">**msdyn_PSSUpdateV1**: seda API-d saab kasutada olemi uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="47015-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="47015-138">Olem võib olla mis tahes ajastamise olem, mis toetab värskendamise toimingut.</span><span class="sxs-lookup"><span data-stu-id="47015-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="47015-139">**msdyn_PSSDeleteV1**: seda API-d saab kasutada olemi kustutamiseks.</span><span class="sxs-lookup"><span data-stu-id="47015-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="47015-140">Olem võib olla mis tahes ajastamise olem, mis toetab kustutamise toimingut.</span><span class="sxs-lookup"><span data-stu-id="47015-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="47015-141">**msdyn_ExecuteOperationSetV1**: seda API-d kasutatakse antud toimingute komplektis kõikide toimingute täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="47015-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="47015-142">Ajakava API-de kasutamine üksusega OperationSet</span><span class="sxs-lookup"><span data-stu-id="47015-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="47015-143">Kuna nii API **CreateProjectV1** kui ka **CreateTeamMemberV1** kirjed luuakse kohe, ei saa neid API-sid olemis **OperationSet** otse kasutada.</span><span class="sxs-lookup"><span data-stu-id="47015-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="47015-144">Samas saate kasutada API-d, et luua vajalikke kirjeid, luua üksuse **OperationSet** ja kasutada seejärel neid eelnevalt loodud kirjeid üksuses **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="47015-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="47015-145">Toetatud toimingud</span><span class="sxs-lookup"><span data-stu-id="47015-145">Supported operations</span></span>

| <span data-ttu-id="47015-146">Olemi ajastamine</span><span class="sxs-lookup"><span data-stu-id="47015-146">Scheduling entity</span></span> | <span data-ttu-id="47015-147">Koosta</span><span class="sxs-lookup"><span data-stu-id="47015-147">Create</span></span> | <span data-ttu-id="47015-148">Värskendus</span><span class="sxs-lookup"><span data-stu-id="47015-148">Update</span></span> | <span data-ttu-id="47015-149">Kustutusklahv (Delete)</span><span class="sxs-lookup"><span data-stu-id="47015-149">Delete</span></span> | <span data-ttu-id="47015-150">Olulised kaalutlused</span><span class="sxs-lookup"><span data-stu-id="47015-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="47015-151">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="47015-151">Project task</span></span> | <span data-ttu-id="47015-152">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-152">Yes</span></span> | <span data-ttu-id="47015-153">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-153">Yes</span></span> | <span data-ttu-id="47015-154">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-154">Yes</span></span> | <span data-ttu-id="47015-155">Pole</span><span class="sxs-lookup"><span data-stu-id="47015-155">None</span></span> |
| <span data-ttu-id="47015-156">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="47015-156">Project task dependency</span></span> | <span data-ttu-id="47015-157">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-157">Yes</span></span> | <span data-ttu-id="47015-158">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-158">Yes</span></span> | | <span data-ttu-id="47015-159">Projektiülesande sõltuvuskirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="47015-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="47015-160">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="47015-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="47015-161">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="47015-161">Resource assignment</span></span> | <span data-ttu-id="47015-162">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-162">Yes</span></span> | <span data-ttu-id="47015-163">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-163">Yes</span></span> | | <span data-ttu-id="47015-164">Järgmiste väljadega toiminguid ei toetata: **BookableResourceID** (Broneeritava ressursi ID), **Effort** (Panus), **EffortCompleted** (Lõpule viidud panus), **EffortRemaining** (Järelejäänud panus) ja **PlannedWork** (Planeeritud töö).</span><span class="sxs-lookup"><span data-stu-id="47015-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="47015-165">Ressursi määramise kirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="47015-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="47015-166">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="47015-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="47015-167">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="47015-167">Project bucket</span></span> | <span data-ttu-id="47015-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="47015-168">N/A</span></span> | <span data-ttu-id="47015-169">Puudub</span><span class="sxs-lookup"><span data-stu-id="47015-169">N/A</span></span> | <span data-ttu-id="47015-170">Puudub</span><span class="sxs-lookup"><span data-stu-id="47015-170">N/A</span></span> | <span data-ttu-id="47015-171">Vaikesalv luuakse API-d **CreateProjectV1** kasutades.</span><span class="sxs-lookup"><span data-stu-id="47015-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="47015-172">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="47015-172">Project team member</span></span> | <span data-ttu-id="47015-173">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-173">Yes</span></span> | <span data-ttu-id="47015-174">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-174">Yes</span></span> | <span data-ttu-id="47015-175">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-175">Yes</span></span> | <span data-ttu-id="47015-176">Kasutage loomistoiminguks API-d **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="47015-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="47015-177">Project</span><span class="sxs-lookup"><span data-stu-id="47015-177">Project</span></span> | <span data-ttu-id="47015-178">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-178">Yes</span></span> | <span data-ttu-id="47015-179">Ja</span><span class="sxs-lookup"><span data-stu-id="47015-179">Yes</span></span> | <span data-ttu-id="47015-180">Puudub</span><span class="sxs-lookup"><span data-stu-id="47015-180">N/A</span></span> | <span data-ttu-id="47015-181">Järgmiste väljadega toiminguid ei toetata: **StateCode** (Olekukood), **BulkGenerationStatus** (Hulgiloomise olek), **GlobalRevisionToken** (Üldine redaktsioonitõend), **CalendarID** (Kalendri ID), **Effort** (Panus), **EffortCompleted** (Lõpule jõudnud panus), **EffortRemaining** (Järelejäänud panus), **Progress** (Edenemine), **Finish** (Lõpp), **TaskEarliestStart** (Ülesande varajaseim algus) ja **Duration** (Kestus).</span><span class="sxs-lookup"><span data-stu-id="47015-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="47015-182">Neid API-sid saab kutsuda olemiobjektidega, mis sisaldavad kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="47015-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="47015-183">ID atribuut on valikuline.</span><span class="sxs-lookup"><span data-stu-id="47015-183">The ID property is optional.</span></span> <span data-ttu-id="47015-184">Kui see on antud, proovib süsteem seda kasutada ja loob erandi, kui seda ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="47015-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="47015-185">Kui seda ei ole antud, loob süsteem selle.</span><span class="sxs-lookup"><span data-stu-id="47015-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="47015-186">Piiratud väljad</span><span class="sxs-lookup"><span data-stu-id="47015-186">Restricted fields</span></span>

<span data-ttu-id="47015-187">Järgmistes tabelites määratletakse väljad, mille **loomine** ja **redigeerimine** on piiratud.</span><span class="sxs-lookup"><span data-stu-id="47015-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="47015-188">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="47015-188">Project task</span></span>

| <span data-ttu-id="47015-189">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="47015-189">**Logical name**</span></span>                       | <span data-ttu-id="47015-190">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="47015-190">**Can create**</span></span> | <span data-ttu-id="47015-191">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="47015-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="47015-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="47015-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="47015-193">ei</span><span class="sxs-lookup"><span data-stu-id="47015-193">no</span></span>             | <span data-ttu-id="47015-194">ei</span><span class="sxs-lookup"><span data-stu-id="47015-194">no</span></span>               |
| <span data-ttu-id="47015-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="47015-196">ei</span><span class="sxs-lookup"><span data-stu-id="47015-196">no</span></span>             | <span data-ttu-id="47015-197">ei</span><span class="sxs-lookup"><span data-stu-id="47015-197">no</span></span>               |
| <span data-ttu-id="47015-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="47015-198">msdyn_actualend</span></span>                        | <span data-ttu-id="47015-199">ei</span><span class="sxs-lookup"><span data-stu-id="47015-199">no</span></span>             | <span data-ttu-id="47015-200">ei</span><span class="sxs-lookup"><span data-stu-id="47015-200">no</span></span>               |
| <span data-ttu-id="47015-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="47015-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="47015-202">ei</span><span class="sxs-lookup"><span data-stu-id="47015-202">no</span></span>             | <span data-ttu-id="47015-203">ei</span><span class="sxs-lookup"><span data-stu-id="47015-203">no</span></span>               |
| <span data-ttu-id="47015-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="47015-205">ei</span><span class="sxs-lookup"><span data-stu-id="47015-205">no</span></span>             | <span data-ttu-id="47015-206">ei</span><span class="sxs-lookup"><span data-stu-id="47015-206">no</span></span>               |
| <span data-ttu-id="47015-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="47015-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="47015-208">ei</span><span class="sxs-lookup"><span data-stu-id="47015-208">no</span></span>             | <span data-ttu-id="47015-209">ei</span><span class="sxs-lookup"><span data-stu-id="47015-209">no</span></span>               |
| <span data-ttu-id="47015-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="47015-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="47015-211">ei</span><span class="sxs-lookup"><span data-stu-id="47015-211">no</span></span>             | <span data-ttu-id="47015-212">ei</span><span class="sxs-lookup"><span data-stu-id="47015-212">no</span></span>               |
| <span data-ttu-id="47015-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="47015-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="47015-214">ei</span><span class="sxs-lookup"><span data-stu-id="47015-214">no</span></span>             | <span data-ttu-id="47015-215">ei</span><span class="sxs-lookup"><span data-stu-id="47015-215">no</span></span>               |
| <span data-ttu-id="47015-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="47015-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="47015-217">ei</span><span class="sxs-lookup"><span data-stu-id="47015-217">no</span></span>             | <span data-ttu-id="47015-218">ei</span><span class="sxs-lookup"><span data-stu-id="47015-218">no</span></span>               |
| <span data-ttu-id="47015-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="47015-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="47015-220">ei</span><span class="sxs-lookup"><span data-stu-id="47015-220">no</span></span>             | <span data-ttu-id="47015-221">ei</span><span class="sxs-lookup"><span data-stu-id="47015-221">no</span></span>               |
| <span data-ttu-id="47015-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="47015-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="47015-223">ei</span><span class="sxs-lookup"><span data-stu-id="47015-223">no</span></span>             | <span data-ttu-id="47015-224">ei</span><span class="sxs-lookup"><span data-stu-id="47015-224">no</span></span>               |
| <span data-ttu-id="47015-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="47015-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="47015-226">ei</span><span class="sxs-lookup"><span data-stu-id="47015-226">no</span></span>             | <span data-ttu-id="47015-227">ei</span><span class="sxs-lookup"><span data-stu-id="47015-227">no</span></span>               |
| <span data-ttu-id="47015-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="47015-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="47015-229">ei</span><span class="sxs-lookup"><span data-stu-id="47015-229">no</span></span>             | <span data-ttu-id="47015-230">ei</span><span class="sxs-lookup"><span data-stu-id="47015-230">no</span></span>               |
| <span data-ttu-id="47015-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="47015-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="47015-232">ei</span><span class="sxs-lookup"><span data-stu-id="47015-232">no</span></span>             | <span data-ttu-id="47015-233">ei</span><span class="sxs-lookup"><span data-stu-id="47015-233">no</span></span>               |
| <span data-ttu-id="47015-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="47015-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="47015-235">ei</span><span class="sxs-lookup"><span data-stu-id="47015-235">no</span></span>             | <span data-ttu-id="47015-236">ei</span><span class="sxs-lookup"><span data-stu-id="47015-236">no</span></span>               |
| <span data-ttu-id="47015-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="47015-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="47015-238">ei</span><span class="sxs-lookup"><span data-stu-id="47015-238">no</span></span>             | <span data-ttu-id="47015-239">ei</span><span class="sxs-lookup"><span data-stu-id="47015-239">no</span></span>               |
| <span data-ttu-id="47015-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="47015-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="47015-241">ei</span><span class="sxs-lookup"><span data-stu-id="47015-241">no</span></span>             | <span data-ttu-id="47015-242">ei</span><span class="sxs-lookup"><span data-stu-id="47015-242">no</span></span>               |
| <span data-ttu-id="47015-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="47015-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="47015-244">ei</span><span class="sxs-lookup"><span data-stu-id="47015-244">no</span></span>             | <span data-ttu-id="47015-245">ei</span><span class="sxs-lookup"><span data-stu-id="47015-245">no</span></span>               |
| <span data-ttu-id="47015-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="47015-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="47015-247">ei</span><span class="sxs-lookup"><span data-stu-id="47015-247">no</span></span>             | <span data-ttu-id="47015-248">ei</span><span class="sxs-lookup"><span data-stu-id="47015-248">no</span></span>               |
| <span data-ttu-id="47015-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="47015-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="47015-250">ei</span><span class="sxs-lookup"><span data-stu-id="47015-250">no</span></span>             | <span data-ttu-id="47015-251">ei</span><span class="sxs-lookup"><span data-stu-id="47015-251">no</span></span>               |
| <span data-ttu-id="47015-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="47015-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="47015-253">ei</span><span class="sxs-lookup"><span data-stu-id="47015-253">no</span></span>             | <span data-ttu-id="47015-254">ei</span><span class="sxs-lookup"><span data-stu-id="47015-254">no</span></span>               |
| <span data-ttu-id="47015-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="47015-256">ei</span><span class="sxs-lookup"><span data-stu-id="47015-256">no</span></span>             | <span data-ttu-id="47015-257">ei</span><span class="sxs-lookup"><span data-stu-id="47015-257">no</span></span>               |
| <span data-ttu-id="47015-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="47015-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="47015-259">ei</span><span class="sxs-lookup"><span data-stu-id="47015-259">no</span></span>             | <span data-ttu-id="47015-260">ei</span><span class="sxs-lookup"><span data-stu-id="47015-260">no</span></span>               |
| <span data-ttu-id="47015-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="47015-262">ei</span><span class="sxs-lookup"><span data-stu-id="47015-262">no</span></span>             | <span data-ttu-id="47015-263">ei</span><span class="sxs-lookup"><span data-stu-id="47015-263">no</span></span>               |
| <span data-ttu-id="47015-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="47015-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="47015-265">ei</span><span class="sxs-lookup"><span data-stu-id="47015-265">no</span></span>             | <span data-ttu-id="47015-266">ei</span><span class="sxs-lookup"><span data-stu-id="47015-266">no</span></span>               |
| <span data-ttu-id="47015-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="47015-267">msdyn_progress</span></span>                         | <span data-ttu-id="47015-268">ei</span><span class="sxs-lookup"><span data-stu-id="47015-268">no</span></span>             | <span data-ttu-id="47015-269">ei (jah P4W jaoks)</span><span class="sxs-lookup"><span data-stu-id="47015-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="47015-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="47015-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="47015-271">ei</span><span class="sxs-lookup"><span data-stu-id="47015-271">no</span></span>             | <span data-ttu-id="47015-272">ei</span><span class="sxs-lookup"><span data-stu-id="47015-272">no</span></span>               |
| <span data-ttu-id="47015-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="47015-274">ei</span><span class="sxs-lookup"><span data-stu-id="47015-274">no</span></span>             | <span data-ttu-id="47015-275">ei</span><span class="sxs-lookup"><span data-stu-id="47015-275">no</span></span>               |
| <span data-ttu-id="47015-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="47015-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="47015-277">ei</span><span class="sxs-lookup"><span data-stu-id="47015-277">no</span></span>             | <span data-ttu-id="47015-278">ei</span><span class="sxs-lookup"><span data-stu-id="47015-278">no</span></span>               |
| <span data-ttu-id="47015-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="47015-280">ei</span><span class="sxs-lookup"><span data-stu-id="47015-280">no</span></span>             | <span data-ttu-id="47015-281">ei</span><span class="sxs-lookup"><span data-stu-id="47015-281">no</span></span>               |
| <span data-ttu-id="47015-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="47015-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="47015-283">ei</span><span class="sxs-lookup"><span data-stu-id="47015-283">no</span></span>             | <span data-ttu-id="47015-284">ei</span><span class="sxs-lookup"><span data-stu-id="47015-284">no</span></span>               |
| <span data-ttu-id="47015-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="47015-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="47015-286">ei</span><span class="sxs-lookup"><span data-stu-id="47015-286">no</span></span>             | <span data-ttu-id="47015-287">ei</span><span class="sxs-lookup"><span data-stu-id="47015-287">no</span></span>               |
| <span data-ttu-id="47015-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="47015-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="47015-289">ei</span><span class="sxs-lookup"><span data-stu-id="47015-289">no</span></span>             | <span data-ttu-id="47015-290">ei</span><span class="sxs-lookup"><span data-stu-id="47015-290">no</span></span>               |
| <span data-ttu-id="47015-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="47015-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="47015-292">ei</span><span class="sxs-lookup"><span data-stu-id="47015-292">no</span></span>             | <span data-ttu-id="47015-293">ei</span><span class="sxs-lookup"><span data-stu-id="47015-293">no</span></span>               |
| <span data-ttu-id="47015-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="47015-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="47015-295">ei</span><span class="sxs-lookup"><span data-stu-id="47015-295">no</span></span>             | <span data-ttu-id="47015-296">ei</span><span class="sxs-lookup"><span data-stu-id="47015-296">no</span></span>               |
| <span data-ttu-id="47015-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="47015-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="47015-298">ei</span><span class="sxs-lookup"><span data-stu-id="47015-298">no</span></span>             | <span data-ttu-id="47015-299">ei</span><span class="sxs-lookup"><span data-stu-id="47015-299">no</span></span>               |
| <span data-ttu-id="47015-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="47015-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="47015-301">ei</span><span class="sxs-lookup"><span data-stu-id="47015-301">no</span></span>             | <span data-ttu-id="47015-302">ei</span><span class="sxs-lookup"><span data-stu-id="47015-302">no</span></span>               |
| <span data-ttu-id="47015-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="47015-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="47015-304">ei</span><span class="sxs-lookup"><span data-stu-id="47015-304">no</span></span>             | <span data-ttu-id="47015-305">ei</span><span class="sxs-lookup"><span data-stu-id="47015-305">no</span></span>               |
| <span data-ttu-id="47015-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="47015-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="47015-307">ei</span><span class="sxs-lookup"><span data-stu-id="47015-307">no</span></span>             | <span data-ttu-id="47015-308">ei</span><span class="sxs-lookup"><span data-stu-id="47015-308">no</span></span>               |
| <span data-ttu-id="47015-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="47015-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="47015-310">ei</span><span class="sxs-lookup"><span data-stu-id="47015-310">no</span></span>             | <span data-ttu-id="47015-311">ei</span><span class="sxs-lookup"><span data-stu-id="47015-311">no</span></span>               |
| <span data-ttu-id="47015-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="47015-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="47015-313">ei</span><span class="sxs-lookup"><span data-stu-id="47015-313">no</span></span>             | <span data-ttu-id="47015-314">ei</span><span class="sxs-lookup"><span data-stu-id="47015-314">no</span></span>               |
| <span data-ttu-id="47015-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="47015-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="47015-316">ei</span><span class="sxs-lookup"><span data-stu-id="47015-316">no</span></span>             | <span data-ttu-id="47015-317">ei</span><span class="sxs-lookup"><span data-stu-id="47015-317">no</span></span>               |
| <span data-ttu-id="47015-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="47015-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="47015-319">ei</span><span class="sxs-lookup"><span data-stu-id="47015-319">no</span></span>             | <span data-ttu-id="47015-320">ei</span><span class="sxs-lookup"><span data-stu-id="47015-320">no</span></span>               |
| <span data-ttu-id="47015-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="47015-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="47015-322">ei</span><span class="sxs-lookup"><span data-stu-id="47015-322">no</span></span>             | <span data-ttu-id="47015-323">ei</span><span class="sxs-lookup"><span data-stu-id="47015-323">no</span></span>               |
| <span data-ttu-id="47015-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="47015-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="47015-325">ei</span><span class="sxs-lookup"><span data-stu-id="47015-325">no</span></span>             | <span data-ttu-id="47015-326">ei</span><span class="sxs-lookup"><span data-stu-id="47015-326">no</span></span>               |
| <span data-ttu-id="47015-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="47015-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="47015-328">ei</span><span class="sxs-lookup"><span data-stu-id="47015-328">no</span></span>             | <span data-ttu-id="47015-329">ei</span><span class="sxs-lookup"><span data-stu-id="47015-329">no</span></span>               |
| <span data-ttu-id="47015-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="47015-330">msdyn_summary</span></span>                          | <span data-ttu-id="47015-331">ei</span><span class="sxs-lookup"><span data-stu-id="47015-331">no</span></span>             | <span data-ttu-id="47015-332">ei</span><span class="sxs-lookup"><span data-stu-id="47015-332">no</span></span>               |
| <span data-ttu-id="47015-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="47015-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="47015-334">ei</span><span class="sxs-lookup"><span data-stu-id="47015-334">no</span></span>             | <span data-ttu-id="47015-335">ei</span><span class="sxs-lookup"><span data-stu-id="47015-335">no</span></span>               |
| <span data-ttu-id="47015-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="47015-337">ei</span><span class="sxs-lookup"><span data-stu-id="47015-337">no</span></span>             | <span data-ttu-id="47015-338">ei</span><span class="sxs-lookup"><span data-stu-id="47015-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="47015-339">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="47015-339">Project task dependency</span></span>

| <span data-ttu-id="47015-340">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="47015-340">**Logical name**</span></span>              | <span data-ttu-id="47015-341">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="47015-341">**Can create**</span></span> | <span data-ttu-id="47015-342">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="47015-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="47015-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="47015-343">msdyn_linktype</span></span>                | <span data-ttu-id="47015-344">ei</span><span class="sxs-lookup"><span data-stu-id="47015-344">no</span></span>             | <span data-ttu-id="47015-345">ei</span><span class="sxs-lookup"><span data-stu-id="47015-345">no</span></span>           |
| <span data-ttu-id="47015-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="47015-346">msdyn_linktypename</span></span>            | <span data-ttu-id="47015-347">ei</span><span class="sxs-lookup"><span data-stu-id="47015-347">no</span></span>             | <span data-ttu-id="47015-348">ei</span><span class="sxs-lookup"><span data-stu-id="47015-348">no</span></span>           |
| <span data-ttu-id="47015-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="47015-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="47015-350">jah</span><span class="sxs-lookup"><span data-stu-id="47015-350">yes</span></span>            | <span data-ttu-id="47015-351">ei</span><span class="sxs-lookup"><span data-stu-id="47015-351">no</span></span>           |
| <span data-ttu-id="47015-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="47015-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="47015-353">jah</span><span class="sxs-lookup"><span data-stu-id="47015-353">yes</span></span>            | <span data-ttu-id="47015-354">ei</span><span class="sxs-lookup"><span data-stu-id="47015-354">no</span></span>           |
| <span data-ttu-id="47015-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="47015-355">msdyn_project</span></span>                 | <span data-ttu-id="47015-356">jah</span><span class="sxs-lookup"><span data-stu-id="47015-356">yes</span></span>            | <span data-ttu-id="47015-357">ei</span><span class="sxs-lookup"><span data-stu-id="47015-357">no</span></span>           |
| <span data-ttu-id="47015-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="47015-358">msdyn_projectname</span></span>             | <span data-ttu-id="47015-359">jah</span><span class="sxs-lookup"><span data-stu-id="47015-359">yes</span></span>            | <span data-ttu-id="47015-360">ei</span><span class="sxs-lookup"><span data-stu-id="47015-360">no</span></span>           |
| <span data-ttu-id="47015-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="47015-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="47015-362">jah</span><span class="sxs-lookup"><span data-stu-id="47015-362">yes</span></span>            | <span data-ttu-id="47015-363">ei</span><span class="sxs-lookup"><span data-stu-id="47015-363">no</span></span>           |
| <span data-ttu-id="47015-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="47015-364">msdyn_successortask</span></span>           | <span data-ttu-id="47015-365">jah</span><span class="sxs-lookup"><span data-stu-id="47015-365">yes</span></span>            | <span data-ttu-id="47015-366">ei</span><span class="sxs-lookup"><span data-stu-id="47015-366">no</span></span>           |
| <span data-ttu-id="47015-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="47015-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="47015-368">jah</span><span class="sxs-lookup"><span data-stu-id="47015-368">yes</span></span>            | <span data-ttu-id="47015-369">ei</span><span class="sxs-lookup"><span data-stu-id="47015-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="47015-370">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="47015-370">Resource assignment</span></span>

| <span data-ttu-id="47015-371">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="47015-371">**Logical name**</span></span>             | <span data-ttu-id="47015-372">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="47015-372">**Can create**</span></span> | <span data-ttu-id="47015-373">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="47015-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="47015-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="47015-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="47015-375">jah</span><span class="sxs-lookup"><span data-stu-id="47015-375">yes</span></span>            | <span data-ttu-id="47015-376">ei</span><span class="sxs-lookup"><span data-stu-id="47015-376">no</span></span>           |
| <span data-ttu-id="47015-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="47015-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="47015-378">jah</span><span class="sxs-lookup"><span data-stu-id="47015-378">yes</span></span>            | <span data-ttu-id="47015-379">ei</span><span class="sxs-lookup"><span data-stu-id="47015-379">no</span></span>           |
| <span data-ttu-id="47015-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="47015-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="47015-381">ei</span><span class="sxs-lookup"><span data-stu-id="47015-381">no</span></span>             | <span data-ttu-id="47015-382">ei</span><span class="sxs-lookup"><span data-stu-id="47015-382">no</span></span>           |
| <span data-ttu-id="47015-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="47015-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="47015-384">ei</span><span class="sxs-lookup"><span data-stu-id="47015-384">no</span></span>             | <span data-ttu-id="47015-385">ei</span><span class="sxs-lookup"><span data-stu-id="47015-385">no</span></span>           |
| <span data-ttu-id="47015-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="47015-386">msdyn_committype</span></span>             | <span data-ttu-id="47015-387">ei</span><span class="sxs-lookup"><span data-stu-id="47015-387">no</span></span>             | <span data-ttu-id="47015-388">ei</span><span class="sxs-lookup"><span data-stu-id="47015-388">no</span></span>           |
| <span data-ttu-id="47015-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="47015-389">msdyn_committypename</span></span>         | <span data-ttu-id="47015-390">ei</span><span class="sxs-lookup"><span data-stu-id="47015-390">no</span></span>             | <span data-ttu-id="47015-391">ei</span><span class="sxs-lookup"><span data-stu-id="47015-391">no</span></span>           |
| <span data-ttu-id="47015-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="47015-392">msdyn_effort</span></span>                 | <span data-ttu-id="47015-393">ei</span><span class="sxs-lookup"><span data-stu-id="47015-393">no</span></span>             | <span data-ttu-id="47015-394">ei</span><span class="sxs-lookup"><span data-stu-id="47015-394">no</span></span>           |
| <span data-ttu-id="47015-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="47015-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="47015-396">ei</span><span class="sxs-lookup"><span data-stu-id="47015-396">no</span></span>             | <span data-ttu-id="47015-397">ei</span><span class="sxs-lookup"><span data-stu-id="47015-397">no</span></span>           |
| <span data-ttu-id="47015-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="47015-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="47015-399">ei</span><span class="sxs-lookup"><span data-stu-id="47015-399">no</span></span>             | <span data-ttu-id="47015-400">ei</span><span class="sxs-lookup"><span data-stu-id="47015-400">no</span></span>           |
| <span data-ttu-id="47015-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="47015-401">msdyn_finish</span></span>                 | <span data-ttu-id="47015-402">ei</span><span class="sxs-lookup"><span data-stu-id="47015-402">no</span></span>             | <span data-ttu-id="47015-403">ei</span><span class="sxs-lookup"><span data-stu-id="47015-403">no</span></span>           |
| <span data-ttu-id="47015-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="47015-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="47015-405">ei</span><span class="sxs-lookup"><span data-stu-id="47015-405">no</span></span>             | <span data-ttu-id="47015-406">ei</span><span class="sxs-lookup"><span data-stu-id="47015-406">no</span></span>           |
| <span data-ttu-id="47015-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="47015-408">ei</span><span class="sxs-lookup"><span data-stu-id="47015-408">no</span></span>             | <span data-ttu-id="47015-409">ei</span><span class="sxs-lookup"><span data-stu-id="47015-409">no</span></span>           |
| <span data-ttu-id="47015-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="47015-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="47015-411">ei</span><span class="sxs-lookup"><span data-stu-id="47015-411">no</span></span>             | <span data-ttu-id="47015-412">ei</span><span class="sxs-lookup"><span data-stu-id="47015-412">no</span></span>           |
| <span data-ttu-id="47015-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="47015-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="47015-414">ei</span><span class="sxs-lookup"><span data-stu-id="47015-414">no</span></span>             | <span data-ttu-id="47015-415">ei</span><span class="sxs-lookup"><span data-stu-id="47015-415">no</span></span>           |
| <span data-ttu-id="47015-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="47015-417">ei</span><span class="sxs-lookup"><span data-stu-id="47015-417">no</span></span>             | <span data-ttu-id="47015-418">ei</span><span class="sxs-lookup"><span data-stu-id="47015-418">no</span></span>           |
| <span data-ttu-id="47015-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="47015-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="47015-420">ei</span><span class="sxs-lookup"><span data-stu-id="47015-420">no</span></span>             | <span data-ttu-id="47015-421">ei</span><span class="sxs-lookup"><span data-stu-id="47015-421">no</span></span>           |
| <span data-ttu-id="47015-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="47015-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="47015-423">ei</span><span class="sxs-lookup"><span data-stu-id="47015-423">no</span></span>             | <span data-ttu-id="47015-424">ei</span><span class="sxs-lookup"><span data-stu-id="47015-424">no</span></span>           |
| <span data-ttu-id="47015-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="47015-425">msdyn_projectid</span></span>              | <span data-ttu-id="47015-426">jah</span><span class="sxs-lookup"><span data-stu-id="47015-426">yes</span></span>            | <span data-ttu-id="47015-427">ei</span><span class="sxs-lookup"><span data-stu-id="47015-427">no</span></span>           |
| <span data-ttu-id="47015-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="47015-428">msdyn_projectidname</span></span>          | <span data-ttu-id="47015-429">ei</span><span class="sxs-lookup"><span data-stu-id="47015-429">no</span></span>             | <span data-ttu-id="47015-430">ei</span><span class="sxs-lookup"><span data-stu-id="47015-430">no</span></span>           |
| <span data-ttu-id="47015-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="47015-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="47015-432">ei</span><span class="sxs-lookup"><span data-stu-id="47015-432">no</span></span>             | <span data-ttu-id="47015-433">ei</span><span class="sxs-lookup"><span data-stu-id="47015-433">no</span></span>           |
| <span data-ttu-id="47015-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="47015-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="47015-435">ei</span><span class="sxs-lookup"><span data-stu-id="47015-435">no</span></span>             | <span data-ttu-id="47015-436">ei</span><span class="sxs-lookup"><span data-stu-id="47015-436">no</span></span>           |
| <span data-ttu-id="47015-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="47015-437">msdyn_start</span></span>                  | <span data-ttu-id="47015-438">ei</span><span class="sxs-lookup"><span data-stu-id="47015-438">no</span></span>             | <span data-ttu-id="47015-439">ei</span><span class="sxs-lookup"><span data-stu-id="47015-439">no</span></span>           |
| <span data-ttu-id="47015-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="47015-440">msdyn_taskid</span></span>                 | <span data-ttu-id="47015-441">ei</span><span class="sxs-lookup"><span data-stu-id="47015-441">no</span></span>             | <span data-ttu-id="47015-442">ei</span><span class="sxs-lookup"><span data-stu-id="47015-442">no</span></span>           |
| <span data-ttu-id="47015-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="47015-443">msdyn_taskidname</span></span>             | <span data-ttu-id="47015-444">ei</span><span class="sxs-lookup"><span data-stu-id="47015-444">no</span></span>             | <span data-ttu-id="47015-445">ei</span><span class="sxs-lookup"><span data-stu-id="47015-445">no</span></span>           |
| <span data-ttu-id="47015-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="47015-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="47015-447">ei</span><span class="sxs-lookup"><span data-stu-id="47015-447">no</span></span>             | <span data-ttu-id="47015-448">ei</span><span class="sxs-lookup"><span data-stu-id="47015-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="47015-449">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="47015-449">Project team member</span></span>

| <span data-ttu-id="47015-450">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="47015-450">**Logical name**</span></span>                                 | <span data-ttu-id="47015-451">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="47015-451">**Can create**</span></span> | <span data-ttu-id="47015-452">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="47015-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="47015-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="47015-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="47015-454">ei</span><span class="sxs-lookup"><span data-stu-id="47015-454">no</span></span>             | <span data-ttu-id="47015-455">ei</span><span class="sxs-lookup"><span data-stu-id="47015-455">no</span></span>           |
| <span data-ttu-id="47015-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="47015-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="47015-457">ei</span><span class="sxs-lookup"><span data-stu-id="47015-457">no</span></span>             | <span data-ttu-id="47015-458">ei</span><span class="sxs-lookup"><span data-stu-id="47015-458">no</span></span>           |
| <span data-ttu-id="47015-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="47015-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="47015-460">ei</span><span class="sxs-lookup"><span data-stu-id="47015-460">no</span></span>             | <span data-ttu-id="47015-461">ei</span><span class="sxs-lookup"><span data-stu-id="47015-461">no</span></span>           |
| <span data-ttu-id="47015-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="47015-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="47015-463">ei</span><span class="sxs-lookup"><span data-stu-id="47015-463">no</span></span>             | <span data-ttu-id="47015-464">ei</span><span class="sxs-lookup"><span data-stu-id="47015-464">no</span></span>           |
| <span data-ttu-id="47015-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="47015-465">msdyn_effort</span></span>                                     | <span data-ttu-id="47015-466">ei</span><span class="sxs-lookup"><span data-stu-id="47015-466">no</span></span>             | <span data-ttu-id="47015-467">ei</span><span class="sxs-lookup"><span data-stu-id="47015-467">no</span></span>           |
| <span data-ttu-id="47015-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="47015-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="47015-469">ei</span><span class="sxs-lookup"><span data-stu-id="47015-469">no</span></span>             | <span data-ttu-id="47015-470">ei</span><span class="sxs-lookup"><span data-stu-id="47015-470">no</span></span>           |
| <span data-ttu-id="47015-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="47015-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="47015-472">ei</span><span class="sxs-lookup"><span data-stu-id="47015-472">no</span></span>             | <span data-ttu-id="47015-473">ei</span><span class="sxs-lookup"><span data-stu-id="47015-473">no</span></span>           |
| <span data-ttu-id="47015-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="47015-474">msdyn_finish</span></span>                                     | <span data-ttu-id="47015-475">ei</span><span class="sxs-lookup"><span data-stu-id="47015-475">no</span></span>             | <span data-ttu-id="47015-476">ei</span><span class="sxs-lookup"><span data-stu-id="47015-476">no</span></span>           |
| <span data-ttu-id="47015-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="47015-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="47015-478">ei</span><span class="sxs-lookup"><span data-stu-id="47015-478">no</span></span>             | <span data-ttu-id="47015-479">ei</span><span class="sxs-lookup"><span data-stu-id="47015-479">no</span></span>           |
| <span data-ttu-id="47015-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="47015-480">msdyn_hours</span></span>                                      | <span data-ttu-id="47015-481">ei</span><span class="sxs-lookup"><span data-stu-id="47015-481">no</span></span>             | <span data-ttu-id="47015-482">ei</span><span class="sxs-lookup"><span data-stu-id="47015-482">no</span></span>           |
| <span data-ttu-id="47015-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="47015-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="47015-484">ei</span><span class="sxs-lookup"><span data-stu-id="47015-484">no</span></span>             | <span data-ttu-id="47015-485">ei</span><span class="sxs-lookup"><span data-stu-id="47015-485">no</span></span>           |
| <span data-ttu-id="47015-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="47015-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="47015-487">ei</span><span class="sxs-lookup"><span data-stu-id="47015-487">no</span></span>             | <span data-ttu-id="47015-488">ei</span><span class="sxs-lookup"><span data-stu-id="47015-488">no</span></span>           |
| <span data-ttu-id="47015-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="47015-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="47015-490">ei</span><span class="sxs-lookup"><span data-stu-id="47015-490">no</span></span>             | <span data-ttu-id="47015-491">ei</span><span class="sxs-lookup"><span data-stu-id="47015-491">no</span></span>           |
| <span data-ttu-id="47015-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="47015-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="47015-493">ei</span><span class="sxs-lookup"><span data-stu-id="47015-493">no</span></span>             | <span data-ttu-id="47015-494">ei</span><span class="sxs-lookup"><span data-stu-id="47015-494">no</span></span>           |
| <span data-ttu-id="47015-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="47015-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="47015-496">ei</span><span class="sxs-lookup"><span data-stu-id="47015-496">no</span></span>             | <span data-ttu-id="47015-497">ei</span><span class="sxs-lookup"><span data-stu-id="47015-497">no</span></span>           |
| <span data-ttu-id="47015-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="47015-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="47015-499">ei</span><span class="sxs-lookup"><span data-stu-id="47015-499">no</span></span>             | <span data-ttu-id="47015-500">ei</span><span class="sxs-lookup"><span data-stu-id="47015-500">no</span></span>           |
| <span data-ttu-id="47015-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="47015-501">msdyn_start</span></span>                                      | <span data-ttu-id="47015-502">ei</span><span class="sxs-lookup"><span data-stu-id="47015-502">no</span></span>             | <span data-ttu-id="47015-503">ei</span><span class="sxs-lookup"><span data-stu-id="47015-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="47015-504">Project</span><span class="sxs-lookup"><span data-stu-id="47015-504">Project</span></span>

| <span data-ttu-id="47015-505">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="47015-505">**Logical name**</span></span>                       | <span data-ttu-id="47015-506">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="47015-506">**Can create**</span></span> | <span data-ttu-id="47015-507">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="47015-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="47015-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="47015-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="47015-509">ei</span><span class="sxs-lookup"><span data-stu-id="47015-509">no</span></span>             | <span data-ttu-id="47015-510">ei</span><span class="sxs-lookup"><span data-stu-id="47015-510">no</span></span>           |
| <span data-ttu-id="47015-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="47015-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="47015-512">ei</span><span class="sxs-lookup"><span data-stu-id="47015-512">no</span></span>             | <span data-ttu-id="47015-513">ei</span><span class="sxs-lookup"><span data-stu-id="47015-513">no</span></span>           |
| <span data-ttu-id="47015-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="47015-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="47015-515">ei</span><span class="sxs-lookup"><span data-stu-id="47015-515">no</span></span>             | <span data-ttu-id="47015-516">ei</span><span class="sxs-lookup"><span data-stu-id="47015-516">no</span></span>           |
| <span data-ttu-id="47015-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="47015-518">ei</span><span class="sxs-lookup"><span data-stu-id="47015-518">no</span></span>             | <span data-ttu-id="47015-519">ei</span><span class="sxs-lookup"><span data-stu-id="47015-519">no</span></span>           |
| <span data-ttu-id="47015-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="47015-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="47015-521">ei</span><span class="sxs-lookup"><span data-stu-id="47015-521">no</span></span>             | <span data-ttu-id="47015-522">ei</span><span class="sxs-lookup"><span data-stu-id="47015-522">no</span></span>           |
| <span data-ttu-id="47015-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="47015-524">ei</span><span class="sxs-lookup"><span data-stu-id="47015-524">no</span></span>             | <span data-ttu-id="47015-525">ei</span><span class="sxs-lookup"><span data-stu-id="47015-525">no</span></span>           |
| <span data-ttu-id="47015-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="47015-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="47015-527">jah</span><span class="sxs-lookup"><span data-stu-id="47015-527">yes</span></span>            | <span data-ttu-id="47015-528">ei</span><span class="sxs-lookup"><span data-stu-id="47015-528">no</span></span>           |
| <span data-ttu-id="47015-529">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="47015-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="47015-530">jah</span><span class="sxs-lookup"><span data-stu-id="47015-530">yes</span></span>            | <span data-ttu-id="47015-531">ei</span><span class="sxs-lookup"><span data-stu-id="47015-531">no</span></span>           |
| <span data-ttu-id="47015-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="47015-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="47015-533">jah</span><span class="sxs-lookup"><span data-stu-id="47015-533">yes</span></span>            | <span data-ttu-id="47015-534">ei</span><span class="sxs-lookup"><span data-stu-id="47015-534">no</span></span>           |
| <span data-ttu-id="47015-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="47015-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="47015-536">ei</span><span class="sxs-lookup"><span data-stu-id="47015-536">no</span></span>             | <span data-ttu-id="47015-537">ei</span><span class="sxs-lookup"><span data-stu-id="47015-537">no</span></span>           |
| <span data-ttu-id="47015-538">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="47015-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="47015-539">ei</span><span class="sxs-lookup"><span data-stu-id="47015-539">no</span></span>             | <span data-ttu-id="47015-540">ei</span><span class="sxs-lookup"><span data-stu-id="47015-540">no</span></span>           |
| <span data-ttu-id="47015-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="47015-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="47015-542">ei</span><span class="sxs-lookup"><span data-stu-id="47015-542">no</span></span>             | <span data-ttu-id="47015-543">ei</span><span class="sxs-lookup"><span data-stu-id="47015-543">no</span></span>           |
| <span data-ttu-id="47015-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="47015-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="47015-545">ei</span><span class="sxs-lookup"><span data-stu-id="47015-545">no</span></span>             | <span data-ttu-id="47015-546">ei</span><span class="sxs-lookup"><span data-stu-id="47015-546">no</span></span>           |
| <span data-ttu-id="47015-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="47015-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="47015-548">ei</span><span class="sxs-lookup"><span data-stu-id="47015-548">no</span></span>             | <span data-ttu-id="47015-549">ei</span><span class="sxs-lookup"><span data-stu-id="47015-549">no</span></span>           |
| <span data-ttu-id="47015-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="47015-550">msdyn_duration</span></span>                         | <span data-ttu-id="47015-551">ei</span><span class="sxs-lookup"><span data-stu-id="47015-551">no</span></span>             | <span data-ttu-id="47015-552">ei</span><span class="sxs-lookup"><span data-stu-id="47015-552">no</span></span>           |
| <span data-ttu-id="47015-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="47015-553">msdyn_effort</span></span>                           | <span data-ttu-id="47015-554">ei</span><span class="sxs-lookup"><span data-stu-id="47015-554">no</span></span>             | <span data-ttu-id="47015-555">ei</span><span class="sxs-lookup"><span data-stu-id="47015-555">no</span></span>           |
| <span data-ttu-id="47015-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="47015-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="47015-557">ei</span><span class="sxs-lookup"><span data-stu-id="47015-557">no</span></span>             | <span data-ttu-id="47015-558">ei</span><span class="sxs-lookup"><span data-stu-id="47015-558">no</span></span>           |
| <span data-ttu-id="47015-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="47015-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="47015-560">ei</span><span class="sxs-lookup"><span data-stu-id="47015-560">no</span></span>             | <span data-ttu-id="47015-561">ei</span><span class="sxs-lookup"><span data-stu-id="47015-561">no</span></span>           |
| <span data-ttu-id="47015-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="47015-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="47015-563">ei</span><span class="sxs-lookup"><span data-stu-id="47015-563">no</span></span>             | <span data-ttu-id="47015-564">ei</span><span class="sxs-lookup"><span data-stu-id="47015-564">no</span></span>           |
| <span data-ttu-id="47015-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="47015-565">msdyn_finish</span></span>                           | <span data-ttu-id="47015-566">jah</span><span class="sxs-lookup"><span data-stu-id="47015-566">yes</span></span>            | <span data-ttu-id="47015-567">jah</span><span class="sxs-lookup"><span data-stu-id="47015-567">yes</span></span>          |
| <span data-ttu-id="47015-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="47015-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="47015-569">ei</span><span class="sxs-lookup"><span data-stu-id="47015-569">no</span></span>             | <span data-ttu-id="47015-570">ei</span><span class="sxs-lookup"><span data-stu-id="47015-570">no</span></span>           |
| <span data-ttu-id="47015-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="47015-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="47015-572">ei</span><span class="sxs-lookup"><span data-stu-id="47015-572">no</span></span>             | <span data-ttu-id="47015-573">ei</span><span class="sxs-lookup"><span data-stu-id="47015-573">no</span></span>           |
| <span data-ttu-id="47015-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="47015-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="47015-575">ei</span><span class="sxs-lookup"><span data-stu-id="47015-575">no</span></span>             | <span data-ttu-id="47015-576">ei</span><span class="sxs-lookup"><span data-stu-id="47015-576">no</span></span>           |
| <span data-ttu-id="47015-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="47015-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="47015-578">ei</span><span class="sxs-lookup"><span data-stu-id="47015-578">no</span></span>             | <span data-ttu-id="47015-579">ei</span><span class="sxs-lookup"><span data-stu-id="47015-579">no</span></span>           |
| <span data-ttu-id="47015-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="47015-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="47015-581">ei</span><span class="sxs-lookup"><span data-stu-id="47015-581">no</span></span>             | <span data-ttu-id="47015-582">ei</span><span class="sxs-lookup"><span data-stu-id="47015-582">no</span></span>           |
| <span data-ttu-id="47015-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="47015-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="47015-584">ei</span><span class="sxs-lookup"><span data-stu-id="47015-584">no</span></span>             | <span data-ttu-id="47015-585">ei</span><span class="sxs-lookup"><span data-stu-id="47015-585">no</span></span>           |
| <span data-ttu-id="47015-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="47015-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="47015-587">ei</span><span class="sxs-lookup"><span data-stu-id="47015-587">no</span></span>             | <span data-ttu-id="47015-588">ei</span><span class="sxs-lookup"><span data-stu-id="47015-588">no</span></span>           |
| <span data-ttu-id="47015-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="47015-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="47015-590">ei</span><span class="sxs-lookup"><span data-stu-id="47015-590">no</span></span>             | <span data-ttu-id="47015-591">ei</span><span class="sxs-lookup"><span data-stu-id="47015-591">no</span></span>           |
| <span data-ttu-id="47015-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="47015-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="47015-593">ei</span><span class="sxs-lookup"><span data-stu-id="47015-593">no</span></span>             | <span data-ttu-id="47015-594">ei</span><span class="sxs-lookup"><span data-stu-id="47015-594">no</span></span>           |
| <span data-ttu-id="47015-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="47015-596">ei</span><span class="sxs-lookup"><span data-stu-id="47015-596">no</span></span>             | <span data-ttu-id="47015-597">ei</span><span class="sxs-lookup"><span data-stu-id="47015-597">no</span></span>           |
| <span data-ttu-id="47015-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="47015-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="47015-599">ei</span><span class="sxs-lookup"><span data-stu-id="47015-599">no</span></span>             | <span data-ttu-id="47015-600">ei</span><span class="sxs-lookup"><span data-stu-id="47015-600">no</span></span>           |
| <span data-ttu-id="47015-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="47015-602">ei</span><span class="sxs-lookup"><span data-stu-id="47015-602">no</span></span>             | <span data-ttu-id="47015-603">ei</span><span class="sxs-lookup"><span data-stu-id="47015-603">no</span></span>           |
| <span data-ttu-id="47015-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="47015-604">msdyn_progress</span></span>                         | <span data-ttu-id="47015-605">ei</span><span class="sxs-lookup"><span data-stu-id="47015-605">no</span></span>             | <span data-ttu-id="47015-606">ei</span><span class="sxs-lookup"><span data-stu-id="47015-606">no</span></span>           |
| <span data-ttu-id="47015-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="47015-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="47015-608">ei</span><span class="sxs-lookup"><span data-stu-id="47015-608">no</span></span>             | <span data-ttu-id="47015-609">ei</span><span class="sxs-lookup"><span data-stu-id="47015-609">no</span></span>           |
| <span data-ttu-id="47015-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="47015-611">ei</span><span class="sxs-lookup"><span data-stu-id="47015-611">no</span></span>             | <span data-ttu-id="47015-612">ei</span><span class="sxs-lookup"><span data-stu-id="47015-612">no</span></span>           |
| <span data-ttu-id="47015-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="47015-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="47015-614">ei</span><span class="sxs-lookup"><span data-stu-id="47015-614">no</span></span>             | <span data-ttu-id="47015-615">ei</span><span class="sxs-lookup"><span data-stu-id="47015-615">no</span></span>           |
| <span data-ttu-id="47015-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="47015-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="47015-617">ei</span><span class="sxs-lookup"><span data-stu-id="47015-617">no</span></span>             | <span data-ttu-id="47015-618">ei</span><span class="sxs-lookup"><span data-stu-id="47015-618">no</span></span>           |
| <span data-ttu-id="47015-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="47015-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="47015-620">ei</span><span class="sxs-lookup"><span data-stu-id="47015-620">no</span></span>             | <span data-ttu-id="47015-621">ei</span><span class="sxs-lookup"><span data-stu-id="47015-621">no</span></span>           |
| <span data-ttu-id="47015-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="47015-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="47015-623">ei</span><span class="sxs-lookup"><span data-stu-id="47015-623">no</span></span>             | <span data-ttu-id="47015-624">ei</span><span class="sxs-lookup"><span data-stu-id="47015-624">no</span></span>           |
| <span data-ttu-id="47015-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="47015-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="47015-626">ei</span><span class="sxs-lookup"><span data-stu-id="47015-626">no</span></span>             | <span data-ttu-id="47015-627">ei</span><span class="sxs-lookup"><span data-stu-id="47015-627">no</span></span>           |
| <span data-ttu-id="47015-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="47015-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="47015-629">ei</span><span class="sxs-lookup"><span data-stu-id="47015-629">no</span></span>             | <span data-ttu-id="47015-630">ei</span><span class="sxs-lookup"><span data-stu-id="47015-630">no</span></span>           |
| <span data-ttu-id="47015-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="47015-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="47015-632">ei</span><span class="sxs-lookup"><span data-stu-id="47015-632">no</span></span>             | <span data-ttu-id="47015-633">ei</span><span class="sxs-lookup"><span data-stu-id="47015-633">no</span></span>           |
| <span data-ttu-id="47015-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="47015-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="47015-635">ei</span><span class="sxs-lookup"><span data-stu-id="47015-635">no</span></span>             | <span data-ttu-id="47015-636">ei</span><span class="sxs-lookup"><span data-stu-id="47015-636">no</span></span>           |
| <span data-ttu-id="47015-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="47015-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="47015-638">ei</span><span class="sxs-lookup"><span data-stu-id="47015-638">no</span></span>             | <span data-ttu-id="47015-639">ei</span><span class="sxs-lookup"><span data-stu-id="47015-639">no</span></span>           |
| <span data-ttu-id="47015-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="47015-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="47015-641">ei</span><span class="sxs-lookup"><span data-stu-id="47015-641">no</span></span>             | <span data-ttu-id="47015-642">ei</span><span class="sxs-lookup"><span data-stu-id="47015-642">no</span></span>           |
| <span data-ttu-id="47015-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="47015-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="47015-644">ei</span><span class="sxs-lookup"><span data-stu-id="47015-644">no</span></span>             | <span data-ttu-id="47015-645">ei</span><span class="sxs-lookup"><span data-stu-id="47015-645">no</span></span>           |
| <span data-ttu-id="47015-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="47015-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="47015-647">ei</span><span class="sxs-lookup"><span data-stu-id="47015-647">no</span></span>             | <span data-ttu-id="47015-648">ei</span><span class="sxs-lookup"><span data-stu-id="47015-648">no</span></span>           |
| <span data-ttu-id="47015-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="47015-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="47015-650">ei</span><span class="sxs-lookup"><span data-stu-id="47015-650">no</span></span>             | <span data-ttu-id="47015-651">ei</span><span class="sxs-lookup"><span data-stu-id="47015-651">no</span></span>           |
| <span data-ttu-id="47015-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="47015-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="47015-653">ei</span><span class="sxs-lookup"><span data-stu-id="47015-653">no</span></span>             | <span data-ttu-id="47015-654">ei</span><span class="sxs-lookup"><span data-stu-id="47015-654">no</span></span>           |
| <span data-ttu-id="47015-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="47015-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="47015-656">ei</span><span class="sxs-lookup"><span data-stu-id="47015-656">no</span></span>             | <span data-ttu-id="47015-657">ei</span><span class="sxs-lookup"><span data-stu-id="47015-657">no</span></span>           |
| <span data-ttu-id="47015-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="47015-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="47015-659">ei</span><span class="sxs-lookup"><span data-stu-id="47015-659">no</span></span>             | <span data-ttu-id="47015-660">ei</span><span class="sxs-lookup"><span data-stu-id="47015-660">no</span></span>           |
| <span data-ttu-id="47015-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="47015-662">ei</span><span class="sxs-lookup"><span data-stu-id="47015-662">no</span></span>             | <span data-ttu-id="47015-663">ei</span><span class="sxs-lookup"><span data-stu-id="47015-663">no</span></span>           |
| <span data-ttu-id="47015-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="47015-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="47015-665">ei</span><span class="sxs-lookup"><span data-stu-id="47015-665">no</span></span>             | <span data-ttu-id="47015-666">ei</span><span class="sxs-lookup"><span data-stu-id="47015-666">no</span></span>           |
| <span data-ttu-id="47015-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="47015-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="47015-668">ei</span><span class="sxs-lookup"><span data-stu-id="47015-668">no</span></span>             | <span data-ttu-id="47015-669">ei</span><span class="sxs-lookup"><span data-stu-id="47015-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="47015-670">Piirangud ja teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="47015-670">Limitations and known issues</span></span>
<span data-ttu-id="47015-671">Järgnevalt on toodud piirangute ja teadaolevate probleemide loend.</span><span class="sxs-lookup"><span data-stu-id="47015-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="47015-672">Ajakava API-sid saavad kasutada ainult **Microsoft Projecti litsentsiga kasutajad.**</span><span class="sxs-lookup"><span data-stu-id="47015-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="47015-673">Neid ei saa kasutada järgnevad.</span><span class="sxs-lookup"><span data-stu-id="47015-673">They can't be used by:</span></span>
    - <span data-ttu-id="47015-674">Rakenduse kasutajad</span><span class="sxs-lookup"><span data-stu-id="47015-674">Application users</span></span>
    - <span data-ttu-id="47015-675">Süsteemi kasutajad</span><span class="sxs-lookup"><span data-stu-id="47015-675">System users</span></span>
    - <span data-ttu-id="47015-676">Integratsiooni kasutajad</span><span class="sxs-lookup"><span data-stu-id="47015-676">Integration users</span></span>
    - <span data-ttu-id="47015-677">Teised kasutajad, kes ei oma nõutavat litsentsi</span><span class="sxs-lookup"><span data-stu-id="47015-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="47015-678">Igal suvandil **OperationSet** saab olla maksimaalselt 100 toimingut.</span><span class="sxs-lookup"><span data-stu-id="47015-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="47015-679">Igal kasutajal saab maksimaalselt olla 10 avatud suvandit **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="47015-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="47015-680">Project Operations toetab praegu projektil kokku maksimaalselt 500 ülesannet.</span><span class="sxs-lookup"><span data-stu-id="47015-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="47015-681">Suvandi **OperationSet** tõrkeolek ja tõrkelogid pole hetkel saadaval.</span><span class="sxs-lookup"><span data-stu-id="47015-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="47015-682">Ajakava API-d on avalikus eelversioonis.</span><span class="sxs-lookup"><span data-stu-id="47015-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="47015-683">Microsoft ei toeta nende API-de kasutamist töökeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="47015-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="47015-684">Projektide ja tööülesannete piirangud ja piirid</span><span class="sxs-lookup"><span data-stu-id="47015-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="47015-685">Tõrketöötlus</span><span class="sxs-lookup"><span data-stu-id="47015-685">Error handling</span></span>

   - <span data-ttu-id="47015-686">Toimingukomplektide põhjal loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **Toimingutekomplekt**.</span><span class="sxs-lookup"><span data-stu-id="47015-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="47015-687">Projekti kavandamise teenuse kaudu loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **PSS-i vealogi**.</span><span class="sxs-lookup"><span data-stu-id="47015-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="47015-688">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="47015-688">Sample scenario</span></span>

<span data-ttu-id="47015-689">Selles stsenaariumis loote projekti, meeskonnaliikme, neli ülesannet ja kaks ressursi määramist.</span><span class="sxs-lookup"><span data-stu-id="47015-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="47015-690">Järgmisena värskendate ühte ülesannet, värskendate projekti, kustutate ühe ülesande, kustutate ühe ressursi määramise ja loote ülesande sõltuvuse.</span><span class="sxs-lookup"><span data-stu-id="47015-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="47015-691">Täiendavad näited</span><span class="sxs-lookup"><span data-stu-id="47015-691">Additional samples</span></span>

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
