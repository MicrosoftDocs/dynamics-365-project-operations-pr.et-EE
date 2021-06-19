---
title: Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks
description: Selles teemas on toodud teave ja näited ajakava API-de kasutamise kohta.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116792"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="6b728-103">Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks</span><span class="sxs-lookup"><span data-stu-id="6b728-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="6b728-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="6b728-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="6b728-105">Osad või kõik selles teemas märgitud funktsioonid on saadaval suunatud kasutajatele osana eelversiooni väljaandest.</span><span class="sxs-lookup"><span data-stu-id="6b728-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="6b728-106">Sisu ja funktsioonid võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="6b728-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="6b728-107">Olemite ajastamine</span><span class="sxs-lookup"><span data-stu-id="6b728-107">Scheduling entities</span></span>

<span data-ttu-id="6b728-108">Ajakava API-d annavad võimaluse teha suvandiga **Olemite ajastamine** loomise, värskendamise ja kustutamise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="6b728-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="6b728-109">Neid olemeid hallatakse veebirakenduse Project ajastamise mootori kaudu.</span><span class="sxs-lookup"><span data-stu-id="6b728-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="6b728-110">Suvandiga **Olemite ajastamine** toimingute loomine, värskendamine ja kustutamine oli rakenduse Dynamics 365 Project Operations varasemates väljaannetes piiratud.</span><span class="sxs-lookup"><span data-stu-id="6b728-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="6b728-111">Järgmises tabelis on toodud suvandi **Olemite kavandamine** täielik loend.</span><span class="sxs-lookup"><span data-stu-id="6b728-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="6b728-112">Olemi nimi</span><span class="sxs-lookup"><span data-stu-id="6b728-112">Entity name</span></span>  | <span data-ttu-id="6b728-113">Olemi loogiline nimi</span><span class="sxs-lookup"><span data-stu-id="6b728-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="6b728-114">Project</span><span class="sxs-lookup"><span data-stu-id="6b728-114">Project</span></span> | <span data-ttu-id="6b728-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="6b728-115">msdyn_project</span></span> |
| <span data-ttu-id="6b728-116">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="6b728-116">Project Task</span></span>  | <span data-ttu-id="6b728-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="6b728-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="6b728-118">Projekti ülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="6b728-118">Project Task Dependency</span></span>  | <span data-ttu-id="6b728-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="6b728-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="6b728-120">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="6b728-120">Resource Assignment</span></span> | <span data-ttu-id="6b728-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="6b728-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="6b728-122">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="6b728-122">Project Bucket</span></span>  | <span data-ttu-id="6b728-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="6b728-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="6b728-124">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="6b728-124">Project Team Member</span></span> | <span data-ttu-id="6b728-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="6b728-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="6b728-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="6b728-126">OperationSet</span></span>

<span data-ttu-id="6b728-127">OperationSet on tööühiku muster, mida saab kasutada juhul, kui kandes tuleb töödelda mitut ajakava mõjutavat taotlust.</span><span class="sxs-lookup"><span data-stu-id="6b728-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="6b728-128">API-de kavandamine</span><span class="sxs-lookup"><span data-stu-id="6b728-128">Schedule APIs</span></span>

<span data-ttu-id="6b728-129">Järgnev on praeguste API-de ajastamise loend.</span><span class="sxs-lookup"><span data-stu-id="6b728-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="6b728-130">**msdyn_CreateProjectV1**: seda API-d saab kasutada projekti loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6b728-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="6b728-131">Projekt ja vaikimisi projektisalv luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="6b728-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="6b728-132">**msdyn_CreateTeamMemberV1**: seda API-d saab kasutada projektimeeskonna liikme loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6b728-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="6b728-133">Meeskonnaliikme kirje luuakse kohe.</span><span class="sxs-lookup"><span data-stu-id="6b728-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="6b728-134">**msdyn_CreateOperationSetV1**: seda API-d saab kasutada mitme taotluse ajastamiseks, mis tuleb kande sees teha.</span><span class="sxs-lookup"><span data-stu-id="6b728-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="6b728-135">**msdyn_PSSCreateV1**: seda API-d saab kasutada olemi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6b728-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="6b728-136">Olem võib olla mis tahes ajastamise olem, mis toetab loomise toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b728-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="6b728-137">**msdyn_PSSUpdateV1**: seda API-d saab kasutada olemi uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="6b728-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="6b728-138">Olem võib olla mis tahes ajastamise olem, mis toetab värskendamise toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b728-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="6b728-139">**msdyn_PSSDeleteV1**: seda API-d saab kasutada olemi kustutamiseks.</span><span class="sxs-lookup"><span data-stu-id="6b728-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="6b728-140">Olem võib olla mis tahes ajastamise olem, mis toetab kustutamise toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b728-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="6b728-141">**msdyn_ExecuteOperationSetV1**: seda API-d kasutatakse antud toimingute komplektis kõikide toimingute täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="6b728-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="6b728-142">Ajakava API-de kasutamine üksusega OperationSet</span><span class="sxs-lookup"><span data-stu-id="6b728-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="6b728-143">Kuna nii API **CreateProjectV1** kui ka **CreateTeamMemberV1** kirjed luuakse kohe, ei saa neid API-sid olemis **OperationSet** otse kasutada.</span><span class="sxs-lookup"><span data-stu-id="6b728-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="6b728-144">Samas saate kasutada API-d, et luua vajalikke kirjeid, luua üksuse **OperationSet** ja kasutada seejärel neid eelnevalt loodud kirjeid üksuses **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6b728-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="6b728-145">Toetatud toimingud</span><span class="sxs-lookup"><span data-stu-id="6b728-145">Supported operations</span></span>

| <span data-ttu-id="6b728-146">Olemi ajastamine</span><span class="sxs-lookup"><span data-stu-id="6b728-146">Scheduling entity</span></span> | <span data-ttu-id="6b728-147">Koosta</span><span class="sxs-lookup"><span data-stu-id="6b728-147">Create</span></span> | <span data-ttu-id="6b728-148">Värskendus</span><span class="sxs-lookup"><span data-stu-id="6b728-148">Update</span></span> | <span data-ttu-id="6b728-149">Kustutusklahv (Delete)</span><span class="sxs-lookup"><span data-stu-id="6b728-149">Delete</span></span> | <span data-ttu-id="6b728-150">Olulised kaalutlused</span><span class="sxs-lookup"><span data-stu-id="6b728-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="6b728-151">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="6b728-151">Project task</span></span> | <span data-ttu-id="6b728-152">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-152">Yes</span></span> | <span data-ttu-id="6b728-153">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-153">Yes</span></span> | <span data-ttu-id="6b728-154">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-154">Yes</span></span> | <span data-ttu-id="6b728-155">Pole</span><span class="sxs-lookup"><span data-stu-id="6b728-155">None</span></span> |
| <span data-ttu-id="6b728-156">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="6b728-156">Project task dependency</span></span> | <span data-ttu-id="6b728-157">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-157">Yes</span></span> | <span data-ttu-id="6b728-158">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-158">Yes</span></span> | | <span data-ttu-id="6b728-159">Projektiülesande sõltuvuskirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="6b728-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="6b728-160">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="6b728-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="6b728-161">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="6b728-161">Resource assignment</span></span> | <span data-ttu-id="6b728-162">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-162">Yes</span></span> | <span data-ttu-id="6b728-163">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-163">Yes</span></span> | | <span data-ttu-id="6b728-164">Järgmiste väljadega toiminguid ei toetata: **BookableResourceID** (Broneeritava ressursi ID), **Effort** (Panus), **EffortCompleted** (Lõpule viidud panus), **EffortRemaining** (Järelejäänud panus) ja **PlannedWork** (Planeeritud töö).</span><span class="sxs-lookup"><span data-stu-id="6b728-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="6b728-165">Ressursi määramise kirjeid ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="6b728-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="6b728-166">Selle asemel saab vana kirje kustutada ja luua uue kirje.</span><span class="sxs-lookup"><span data-stu-id="6b728-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="6b728-167">Projektisalv</span><span class="sxs-lookup"><span data-stu-id="6b728-167">Project bucket</span></span> | <span data-ttu-id="6b728-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="6b728-168">N/A</span></span> | <span data-ttu-id="6b728-169">Puudub</span><span class="sxs-lookup"><span data-stu-id="6b728-169">N/A</span></span> | <span data-ttu-id="6b728-170">Puudub</span><span class="sxs-lookup"><span data-stu-id="6b728-170">N/A</span></span> | <span data-ttu-id="6b728-171">Vaikesalv luuakse API-d **CreateProjectV1** kasutades.</span><span class="sxs-lookup"><span data-stu-id="6b728-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="6b728-172">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="6b728-172">Project team member</span></span> | <span data-ttu-id="6b728-173">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-173">Yes</span></span> | <span data-ttu-id="6b728-174">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-174">Yes</span></span> | <span data-ttu-id="6b728-175">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-175">Yes</span></span> | <span data-ttu-id="6b728-176">Kasutage loomistoiminguks API-d **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="6b728-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="6b728-177">Project</span><span class="sxs-lookup"><span data-stu-id="6b728-177">Project</span></span> | <span data-ttu-id="6b728-178">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-178">Yes</span></span> | <span data-ttu-id="6b728-179">Ja</span><span class="sxs-lookup"><span data-stu-id="6b728-179">Yes</span></span> | <span data-ttu-id="6b728-180">Puudub</span><span class="sxs-lookup"><span data-stu-id="6b728-180">N/A</span></span> | <span data-ttu-id="6b728-181">Järgmiste väljadega toiminguid ei toetata: **StateCode** (Olekukood), **BulkGenerationStatus** (Hulgiloomise olek), **GlobalRevisionToken** (Üldine redaktsioonitõend), **CalendarID** (Kalendri ID), **Effort** (Panus), **EffortCompleted** (Lõpule jõudnud panus), **EffortRemaining** (Järelejäänud panus), **Progress** (Edenemine), **Finish** (Lõpp), **TaskEarliestStart** (Ülesande varajaseim algus) ja **Duration** (Kestus).</span><span class="sxs-lookup"><span data-stu-id="6b728-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="6b728-182">Neid API-sid saab kutsuda olemiobjektidega, mis sisaldavad kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="6b728-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="6b728-183">ID atribuut on valikuline.</span><span class="sxs-lookup"><span data-stu-id="6b728-183">The ID property is optional.</span></span> <span data-ttu-id="6b728-184">Kui see on antud, proovib süsteem seda kasutada ja loob erandi, kui seda ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="6b728-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="6b728-185">Kui seda ei ole antud, loob süsteem selle.</span><span class="sxs-lookup"><span data-stu-id="6b728-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="6b728-186">Piiratud väljad</span><span class="sxs-lookup"><span data-stu-id="6b728-186">Restricted fields</span></span>

<span data-ttu-id="6b728-187">Järgmistes tabelites määratletakse väljad, mille **loomine** ja **redigeerimine** on piiratud.</span><span class="sxs-lookup"><span data-stu-id="6b728-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="6b728-188">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="6b728-188">Project task</span></span>

| <span data-ttu-id="6b728-189">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="6b728-189">**Logical name**</span></span>                       | <span data-ttu-id="6b728-190">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="6b728-190">**Can create**</span></span> | <span data-ttu-id="6b728-191">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="6b728-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="6b728-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="6b728-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="6b728-193">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-193">no</span></span>             | <span data-ttu-id="6b728-194">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-194">no</span></span>               |
| <span data-ttu-id="6b728-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="6b728-196">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-196">no</span></span>             | <span data-ttu-id="6b728-197">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-197">no</span></span>               |
| <span data-ttu-id="6b728-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="6b728-198">msdyn_actualend</span></span>                        | <span data-ttu-id="6b728-199">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-199">no</span></span>             | <span data-ttu-id="6b728-200">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-200">no</span></span>               |
| <span data-ttu-id="6b728-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="6b728-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="6b728-202">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-202">no</span></span>             | <span data-ttu-id="6b728-203">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-203">no</span></span>               |
| <span data-ttu-id="6b728-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="6b728-205">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-205">no</span></span>             | <span data-ttu-id="6b728-206">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-206">no</span></span>               |
| <span data-ttu-id="6b728-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="6b728-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="6b728-208">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-208">no</span></span>             | <span data-ttu-id="6b728-209">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-209">no</span></span>               |
| <span data-ttu-id="6b728-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="6b728-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="6b728-211">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-211">no</span></span>             | <span data-ttu-id="6b728-212">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-212">no</span></span>               |
| <span data-ttu-id="6b728-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="6b728-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="6b728-214">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-214">no</span></span>             | <span data-ttu-id="6b728-215">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-215">no</span></span>               |
| <span data-ttu-id="6b728-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="6b728-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="6b728-217">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-217">no</span></span>             | <span data-ttu-id="6b728-218">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-218">no</span></span>               |
| <span data-ttu-id="6b728-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b728-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="6b728-220">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-220">no</span></span>             | <span data-ttu-id="6b728-221">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-221">no</span></span>               |
| <span data-ttu-id="6b728-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6b728-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="6b728-223">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-223">no</span></span>             | <span data-ttu-id="6b728-224">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-224">no</span></span>               |
| <span data-ttu-id="6b728-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="6b728-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="6b728-226">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-226">no</span></span>             | <span data-ttu-id="6b728-227">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-227">no</span></span>               |
| <span data-ttu-id="6b728-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="6b728-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="6b728-229">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-229">no</span></span>             | <span data-ttu-id="6b728-230">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-230">no</span></span>               |
| <span data-ttu-id="6b728-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="6b728-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="6b728-232">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-232">no</span></span>             | <span data-ttu-id="6b728-233">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-233">no</span></span>               |
| <span data-ttu-id="6b728-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="6b728-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="6b728-235">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-235">no</span></span>             | <span data-ttu-id="6b728-236">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-236">no</span></span>               |
| <span data-ttu-id="6b728-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="6b728-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="6b728-238">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-238">no</span></span>             | <span data-ttu-id="6b728-239">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-239">no</span></span>               |
| <span data-ttu-id="6b728-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="6b728-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="6b728-241">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-241">no</span></span>             | <span data-ttu-id="6b728-242">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-242">no</span></span>               |
| <span data-ttu-id="6b728-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="6b728-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="6b728-244">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-244">no</span></span>             | <span data-ttu-id="6b728-245">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-245">no</span></span>               |
| <span data-ttu-id="6b728-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="6b728-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="6b728-247">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-247">no</span></span>             | <span data-ttu-id="6b728-248">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-248">no</span></span>               |
| <span data-ttu-id="6b728-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="6b728-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="6b728-250">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-250">no</span></span>             | <span data-ttu-id="6b728-251">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-251">no</span></span>               |
| <span data-ttu-id="6b728-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="6b728-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="6b728-253">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-253">no</span></span>             | <span data-ttu-id="6b728-254">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-254">no</span></span>               |
| <span data-ttu-id="6b728-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="6b728-256">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-256">no</span></span>             | <span data-ttu-id="6b728-257">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-257">no</span></span>               |
| <span data-ttu-id="6b728-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6b728-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="6b728-259">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-259">no</span></span>             | <span data-ttu-id="6b728-260">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-260">no</span></span>               |
| <span data-ttu-id="6b728-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="6b728-262">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-262">no</span></span>             | <span data-ttu-id="6b728-263">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-263">no</span></span>               |
| <span data-ttu-id="6b728-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="6b728-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="6b728-265">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-265">no</span></span>             | <span data-ttu-id="6b728-266">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-266">no</span></span>               |
| <span data-ttu-id="6b728-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="6b728-267">msdyn_progress</span></span>                         | <span data-ttu-id="6b728-268">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-268">no</span></span>             | <span data-ttu-id="6b728-269">ei (jah P4W jaoks)</span><span class="sxs-lookup"><span data-stu-id="6b728-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="6b728-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="6b728-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="6b728-271">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-271">no</span></span>             | <span data-ttu-id="6b728-272">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-272">no</span></span>               |
| <span data-ttu-id="6b728-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="6b728-274">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-274">no</span></span>             | <span data-ttu-id="6b728-275">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-275">no</span></span>               |
| <span data-ttu-id="6b728-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="6b728-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="6b728-277">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-277">no</span></span>             | <span data-ttu-id="6b728-278">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-278">no</span></span>               |
| <span data-ttu-id="6b728-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="6b728-280">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-280">no</span></span>             | <span data-ttu-id="6b728-281">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-281">no</span></span>               |
| <span data-ttu-id="6b728-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="6b728-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="6b728-283">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-283">no</span></span>             | <span data-ttu-id="6b728-284">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-284">no</span></span>               |
| <span data-ttu-id="6b728-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="6b728-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="6b728-286">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-286">no</span></span>             | <span data-ttu-id="6b728-287">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-287">no</span></span>               |
| <span data-ttu-id="6b728-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="6b728-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="6b728-289">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-289">no</span></span>             | <span data-ttu-id="6b728-290">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-290">no</span></span>               |
| <span data-ttu-id="6b728-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="6b728-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="6b728-292">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-292">no</span></span>             | <span data-ttu-id="6b728-293">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-293">no</span></span>               |
| <span data-ttu-id="6b728-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="6b728-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="6b728-295">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-295">no</span></span>             | <span data-ttu-id="6b728-296">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-296">no</span></span>               |
| <span data-ttu-id="6b728-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="6b728-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="6b728-298">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-298">no</span></span>             | <span data-ttu-id="6b728-299">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-299">no</span></span>               |
| <span data-ttu-id="6b728-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6b728-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="6b728-301">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-301">no</span></span>             | <span data-ttu-id="6b728-302">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-302">no</span></span>               |
| <span data-ttu-id="6b728-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="6b728-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="6b728-304">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-304">no</span></span>             | <span data-ttu-id="6b728-305">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-305">no</span></span>               |
| <span data-ttu-id="6b728-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="6b728-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="6b728-307">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-307">no</span></span>             | <span data-ttu-id="6b728-308">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-308">no</span></span>               |
| <span data-ttu-id="6b728-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="6b728-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="6b728-310">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-310">no</span></span>             | <span data-ttu-id="6b728-311">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-311">no</span></span>               |
| <span data-ttu-id="6b728-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="6b728-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="6b728-313">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-313">no</span></span>             | <span data-ttu-id="6b728-314">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-314">no</span></span>               |
| <span data-ttu-id="6b728-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="6b728-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="6b728-316">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-316">no</span></span>             | <span data-ttu-id="6b728-317">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-317">no</span></span>               |
| <span data-ttu-id="6b728-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="6b728-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="6b728-319">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-319">no</span></span>             | <span data-ttu-id="6b728-320">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-320">no</span></span>               |
| <span data-ttu-id="6b728-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="6b728-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="6b728-322">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-322">no</span></span>             | <span data-ttu-id="6b728-323">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-323">no</span></span>               |
| <span data-ttu-id="6b728-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="6b728-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="6b728-325">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-325">no</span></span>             | <span data-ttu-id="6b728-326">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-326">no</span></span>               |
| <span data-ttu-id="6b728-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="6b728-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="6b728-328">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-328">no</span></span>             | <span data-ttu-id="6b728-329">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-329">no</span></span>               |
| <span data-ttu-id="6b728-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="6b728-330">msdyn_summary</span></span>                          | <span data-ttu-id="6b728-331">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-331">no</span></span>             | <span data-ttu-id="6b728-332">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-332">no</span></span>               |
| <span data-ttu-id="6b728-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="6b728-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="6b728-334">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-334">no</span></span>             | <span data-ttu-id="6b728-335">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-335">no</span></span>               |
| <span data-ttu-id="6b728-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="6b728-337">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-337">no</span></span>             | <span data-ttu-id="6b728-338">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="6b728-339">Projektiülesande sõltuvus</span><span class="sxs-lookup"><span data-stu-id="6b728-339">Project task dependency</span></span>

| <span data-ttu-id="6b728-340">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="6b728-340">**Logical name**</span></span>              | <span data-ttu-id="6b728-341">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="6b728-341">**Can create**</span></span> | <span data-ttu-id="6b728-342">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="6b728-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="6b728-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="6b728-343">msdyn_linktype</span></span>                | <span data-ttu-id="6b728-344">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-344">no</span></span>             | <span data-ttu-id="6b728-345">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-345">no</span></span>           |
| <span data-ttu-id="6b728-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="6b728-346">msdyn_linktypename</span></span>            | <span data-ttu-id="6b728-347">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-347">no</span></span>             | <span data-ttu-id="6b728-348">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-348">no</span></span>           |
| <span data-ttu-id="6b728-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="6b728-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="6b728-350">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-350">yes</span></span>            | <span data-ttu-id="6b728-351">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-351">no</span></span>           |
| <span data-ttu-id="6b728-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="6b728-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="6b728-353">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-353">yes</span></span>            | <span data-ttu-id="6b728-354">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-354">no</span></span>           |
| <span data-ttu-id="6b728-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="6b728-355">msdyn_project</span></span>                 | <span data-ttu-id="6b728-356">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-356">yes</span></span>            | <span data-ttu-id="6b728-357">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-357">no</span></span>           |
| <span data-ttu-id="6b728-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="6b728-358">msdyn_projectname</span></span>             | <span data-ttu-id="6b728-359">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-359">yes</span></span>            | <span data-ttu-id="6b728-360">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-360">no</span></span>           |
| <span data-ttu-id="6b728-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="6b728-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="6b728-362">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-362">yes</span></span>            | <span data-ttu-id="6b728-363">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-363">no</span></span>           |
| <span data-ttu-id="6b728-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="6b728-364">msdyn_successortask</span></span>           | <span data-ttu-id="6b728-365">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-365">yes</span></span>            | <span data-ttu-id="6b728-366">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-366">no</span></span>           |
| <span data-ttu-id="6b728-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="6b728-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="6b728-368">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-368">yes</span></span>            | <span data-ttu-id="6b728-369">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="6b728-370">Ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="6b728-370">Resource assignment</span></span>

| <span data-ttu-id="6b728-371">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="6b728-371">**Logical name**</span></span>             | <span data-ttu-id="6b728-372">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="6b728-372">**Can create**</span></span> | <span data-ttu-id="6b728-373">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="6b728-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="6b728-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="6b728-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="6b728-375">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-375">yes</span></span>            | <span data-ttu-id="6b728-376">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-376">no</span></span>           |
| <span data-ttu-id="6b728-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="6b728-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="6b728-378">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-378">yes</span></span>            | <span data-ttu-id="6b728-379">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-379">no</span></span>           |
| <span data-ttu-id="6b728-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="6b728-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="6b728-381">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-381">no</span></span>             | <span data-ttu-id="6b728-382">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-382">no</span></span>           |
| <span data-ttu-id="6b728-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="6b728-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="6b728-384">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-384">no</span></span>             | <span data-ttu-id="6b728-385">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-385">no</span></span>           |
| <span data-ttu-id="6b728-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="6b728-386">msdyn_committype</span></span>             | <span data-ttu-id="6b728-387">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-387">no</span></span>             | <span data-ttu-id="6b728-388">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-388">no</span></span>           |
| <span data-ttu-id="6b728-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="6b728-389">msdyn_committypename</span></span>         | <span data-ttu-id="6b728-390">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-390">no</span></span>             | <span data-ttu-id="6b728-391">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-391">no</span></span>           |
| <span data-ttu-id="6b728-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6b728-392">msdyn_effort</span></span>                 | <span data-ttu-id="6b728-393">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-393">no</span></span>             | <span data-ttu-id="6b728-394">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-394">no</span></span>           |
| <span data-ttu-id="6b728-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b728-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="6b728-396">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-396">no</span></span>             | <span data-ttu-id="6b728-397">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-397">no</span></span>           |
| <span data-ttu-id="6b728-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6b728-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="6b728-399">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-399">no</span></span>             | <span data-ttu-id="6b728-400">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-400">no</span></span>           |
| <span data-ttu-id="6b728-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6b728-401">msdyn_finish</span></span>                 | <span data-ttu-id="6b728-402">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-402">no</span></span>             | <span data-ttu-id="6b728-403">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-403">no</span></span>           |
| <span data-ttu-id="6b728-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="6b728-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="6b728-405">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-405">no</span></span>             | <span data-ttu-id="6b728-406">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-406">no</span></span>           |
| <span data-ttu-id="6b728-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="6b728-408">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-408">no</span></span>             | <span data-ttu-id="6b728-409">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-409">no</span></span>           |
| <span data-ttu-id="6b728-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="6b728-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="6b728-411">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-411">no</span></span>             | <span data-ttu-id="6b728-412">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-412">no</span></span>           |
| <span data-ttu-id="6b728-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6b728-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="6b728-414">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-414">no</span></span>             | <span data-ttu-id="6b728-415">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-415">no</span></span>           |
| <span data-ttu-id="6b728-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="6b728-417">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-417">no</span></span>             | <span data-ttu-id="6b728-418">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-418">no</span></span>           |
| <span data-ttu-id="6b728-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="6b728-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="6b728-420">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-420">no</span></span>             | <span data-ttu-id="6b728-421">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-421">no</span></span>           |
| <span data-ttu-id="6b728-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="6b728-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="6b728-423">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-423">no</span></span>             | <span data-ttu-id="6b728-424">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-424">no</span></span>           |
| <span data-ttu-id="6b728-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="6b728-425">msdyn_projectid</span></span>              | <span data-ttu-id="6b728-426">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-426">yes</span></span>            | <span data-ttu-id="6b728-427">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-427">no</span></span>           |
| <span data-ttu-id="6b728-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="6b728-428">msdyn_projectidname</span></span>          | <span data-ttu-id="6b728-429">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-429">no</span></span>             | <span data-ttu-id="6b728-430">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-430">no</span></span>           |
| <span data-ttu-id="6b728-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="6b728-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="6b728-432">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-432">no</span></span>             | <span data-ttu-id="6b728-433">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-433">no</span></span>           |
| <span data-ttu-id="6b728-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="6b728-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="6b728-435">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-435">no</span></span>             | <span data-ttu-id="6b728-436">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-436">no</span></span>           |
| <span data-ttu-id="6b728-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="6b728-437">msdyn_start</span></span>                  | <span data-ttu-id="6b728-438">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-438">no</span></span>             | <span data-ttu-id="6b728-439">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-439">no</span></span>           |
| <span data-ttu-id="6b728-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="6b728-440">msdyn_taskid</span></span>                 | <span data-ttu-id="6b728-441">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-441">no</span></span>             | <span data-ttu-id="6b728-442">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-442">no</span></span>           |
| <span data-ttu-id="6b728-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="6b728-443">msdyn_taskidname</span></span>             | <span data-ttu-id="6b728-444">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-444">no</span></span>             | <span data-ttu-id="6b728-445">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-445">no</span></span>           |
| <span data-ttu-id="6b728-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="6b728-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="6b728-447">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-447">no</span></span>             | <span data-ttu-id="6b728-448">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="6b728-449">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="6b728-449">Project team member</span></span>

| <span data-ttu-id="6b728-450">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="6b728-450">**Logical name**</span></span>                                 | <span data-ttu-id="6b728-451">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="6b728-451">**Can create**</span></span> | <span data-ttu-id="6b728-452">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="6b728-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="6b728-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="6b728-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="6b728-454">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-454">no</span></span>             | <span data-ttu-id="6b728-455">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-455">no</span></span>           |
| <span data-ttu-id="6b728-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="6b728-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="6b728-457">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-457">no</span></span>             | <span data-ttu-id="6b728-458">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-458">no</span></span>           |
| <span data-ttu-id="6b728-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="6b728-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="6b728-460">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-460">no</span></span>             | <span data-ttu-id="6b728-461">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-461">no</span></span>           |
| <span data-ttu-id="6b728-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="6b728-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="6b728-463">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-463">no</span></span>             | <span data-ttu-id="6b728-464">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-464">no</span></span>           |
| <span data-ttu-id="6b728-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6b728-465">msdyn_effort</span></span>                                     | <span data-ttu-id="6b728-466">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-466">no</span></span>             | <span data-ttu-id="6b728-467">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-467">no</span></span>           |
| <span data-ttu-id="6b728-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b728-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="6b728-469">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-469">no</span></span>             | <span data-ttu-id="6b728-470">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-470">no</span></span>           |
| <span data-ttu-id="6b728-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6b728-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="6b728-472">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-472">no</span></span>             | <span data-ttu-id="6b728-473">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-473">no</span></span>           |
| <span data-ttu-id="6b728-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6b728-474">msdyn_finish</span></span>                                     | <span data-ttu-id="6b728-475">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-475">no</span></span>             | <span data-ttu-id="6b728-476">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-476">no</span></span>           |
| <span data-ttu-id="6b728-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="6b728-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="6b728-478">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-478">no</span></span>             | <span data-ttu-id="6b728-479">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-479">no</span></span>           |
| <span data-ttu-id="6b728-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="6b728-480">msdyn_hours</span></span>                                      | <span data-ttu-id="6b728-481">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-481">no</span></span>             | <span data-ttu-id="6b728-482">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-482">no</span></span>           |
| <span data-ttu-id="6b728-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="6b728-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="6b728-484">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-484">no</span></span>             | <span data-ttu-id="6b728-485">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-485">no</span></span>           |
| <span data-ttu-id="6b728-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="6b728-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="6b728-487">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-487">no</span></span>             | <span data-ttu-id="6b728-488">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-488">no</span></span>           |
| <span data-ttu-id="6b728-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="6b728-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="6b728-490">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-490">no</span></span>             | <span data-ttu-id="6b728-491">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-491">no</span></span>           |
| <span data-ttu-id="6b728-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="6b728-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="6b728-493">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-493">no</span></span>             | <span data-ttu-id="6b728-494">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-494">no</span></span>           |
| <span data-ttu-id="6b728-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="6b728-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="6b728-496">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-496">no</span></span>             | <span data-ttu-id="6b728-497">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-497">no</span></span>           |
| <span data-ttu-id="6b728-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="6b728-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="6b728-499">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-499">no</span></span>             | <span data-ttu-id="6b728-500">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-500">no</span></span>           |
| <span data-ttu-id="6b728-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="6b728-501">msdyn_start</span></span>                                      | <span data-ttu-id="6b728-502">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-502">no</span></span>             | <span data-ttu-id="6b728-503">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="6b728-504">Project</span><span class="sxs-lookup"><span data-stu-id="6b728-504">Project</span></span>

| <span data-ttu-id="6b728-505">**Loogiline nimi**</span><span class="sxs-lookup"><span data-stu-id="6b728-505">**Logical name**</span></span>                       | <span data-ttu-id="6b728-506">**Saab luua**</span><span class="sxs-lookup"><span data-stu-id="6b728-506">**Can create**</span></span> | <span data-ttu-id="6b728-507">**Saab redigeerida**</span><span class="sxs-lookup"><span data-stu-id="6b728-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="6b728-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="6b728-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="6b728-509">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-509">no</span></span>             | <span data-ttu-id="6b728-510">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-510">no</span></span>           |
| <span data-ttu-id="6b728-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="6b728-512">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-512">no</span></span>             | <span data-ttu-id="6b728-513">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-513">no</span></span>           |
| <span data-ttu-id="6b728-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="6b728-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="6b728-515">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-515">no</span></span>             | <span data-ttu-id="6b728-516">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-516">no</span></span>           |
| <span data-ttu-id="6b728-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="6b728-518">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-518">no</span></span>             | <span data-ttu-id="6b728-519">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-519">no</span></span>           |
| <span data-ttu-id="6b728-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="6b728-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="6b728-521">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-521">no</span></span>             | <span data-ttu-id="6b728-522">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-522">no</span></span>           |
| <span data-ttu-id="6b728-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="6b728-524">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-524">no</span></span>             | <span data-ttu-id="6b728-525">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-525">no</span></span>           |
| <span data-ttu-id="6b728-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="6b728-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="6b728-527">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-527">yes</span></span>            | <span data-ttu-id="6b728-528">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-528">no</span></span>           |
| <span data-ttu-id="6b728-529">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="6b728-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="6b728-530">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-530">yes</span></span>            | <span data-ttu-id="6b728-531">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-531">no</span></span>           |
| <span data-ttu-id="6b728-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="6b728-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="6b728-533">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-533">yes</span></span>            | <span data-ttu-id="6b728-534">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-534">no</span></span>           |
| <span data-ttu-id="6b728-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="6b728-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="6b728-536">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-536">no</span></span>             | <span data-ttu-id="6b728-537">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-537">no</span></span>           |
| <span data-ttu-id="6b728-538">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="6b728-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="6b728-539">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-539">no</span></span>             | <span data-ttu-id="6b728-540">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-540">no</span></span>           |
| <span data-ttu-id="6b728-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="6b728-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="6b728-542">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-542">no</span></span>             | <span data-ttu-id="6b728-543">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-543">no</span></span>           |
| <span data-ttu-id="6b728-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="6b728-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="6b728-545">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-545">no</span></span>             | <span data-ttu-id="6b728-546">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-546">no</span></span>           |
| <span data-ttu-id="6b728-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="6b728-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="6b728-548">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-548">no</span></span>             | <span data-ttu-id="6b728-549">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-549">no</span></span>           |
| <span data-ttu-id="6b728-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="6b728-550">msdyn_duration</span></span>                         | <span data-ttu-id="6b728-551">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-551">no</span></span>             | <span data-ttu-id="6b728-552">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-552">no</span></span>           |
| <span data-ttu-id="6b728-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6b728-553">msdyn_effort</span></span>                           | <span data-ttu-id="6b728-554">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-554">no</span></span>             | <span data-ttu-id="6b728-555">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-555">no</span></span>           |
| <span data-ttu-id="6b728-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6b728-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="6b728-557">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-557">no</span></span>             | <span data-ttu-id="6b728-558">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-558">no</span></span>           |
| <span data-ttu-id="6b728-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="6b728-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="6b728-560">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-560">no</span></span>             | <span data-ttu-id="6b728-561">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-561">no</span></span>           |
| <span data-ttu-id="6b728-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6b728-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="6b728-563">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-563">no</span></span>             | <span data-ttu-id="6b728-564">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-564">no</span></span>           |
| <span data-ttu-id="6b728-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6b728-565">msdyn_finish</span></span>                           | <span data-ttu-id="6b728-566">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-566">yes</span></span>            | <span data-ttu-id="6b728-567">jah</span><span class="sxs-lookup"><span data-stu-id="6b728-567">yes</span></span>          |
| <span data-ttu-id="6b728-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="6b728-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="6b728-569">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-569">no</span></span>             | <span data-ttu-id="6b728-570">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-570">no</span></span>           |
| <span data-ttu-id="6b728-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="6b728-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="6b728-572">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-572">no</span></span>             | <span data-ttu-id="6b728-573">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-573">no</span></span>           |
| <span data-ttu-id="6b728-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="6b728-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="6b728-575">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-575">no</span></span>             | <span data-ttu-id="6b728-576">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-576">no</span></span>           |
| <span data-ttu-id="6b728-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="6b728-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="6b728-578">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-578">no</span></span>             | <span data-ttu-id="6b728-579">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-579">no</span></span>           |
| <span data-ttu-id="6b728-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="6b728-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="6b728-581">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-581">no</span></span>             | <span data-ttu-id="6b728-582">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-582">no</span></span>           |
| <span data-ttu-id="6b728-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="6b728-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="6b728-584">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-584">no</span></span>             | <span data-ttu-id="6b728-585">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-585">no</span></span>           |
| <span data-ttu-id="6b728-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="6b728-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="6b728-587">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-587">no</span></span>             | <span data-ttu-id="6b728-588">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-588">no</span></span>           |
| <span data-ttu-id="6b728-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="6b728-590">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-590">no</span></span>             | <span data-ttu-id="6b728-591">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-591">no</span></span>           |
| <span data-ttu-id="6b728-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="6b728-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="6b728-593">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-593">no</span></span>             | <span data-ttu-id="6b728-594">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-594">no</span></span>           |
| <span data-ttu-id="6b728-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="6b728-596">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-596">no</span></span>             | <span data-ttu-id="6b728-597">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-597">no</span></span>           |
| <span data-ttu-id="6b728-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6b728-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="6b728-599">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-599">no</span></span>             | <span data-ttu-id="6b728-600">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-600">no</span></span>           |
| <span data-ttu-id="6b728-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="6b728-602">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-602">no</span></span>             | <span data-ttu-id="6b728-603">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-603">no</span></span>           |
| <span data-ttu-id="6b728-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="6b728-604">msdyn_progress</span></span>                         | <span data-ttu-id="6b728-605">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-605">no</span></span>             | <span data-ttu-id="6b728-606">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-606">no</span></span>           |
| <span data-ttu-id="6b728-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="6b728-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="6b728-608">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-608">no</span></span>             | <span data-ttu-id="6b728-609">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-609">no</span></span>           |
| <span data-ttu-id="6b728-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="6b728-611">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-611">no</span></span>             | <span data-ttu-id="6b728-612">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-612">no</span></span>           |
| <span data-ttu-id="6b728-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="6b728-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="6b728-614">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-614">no</span></span>             | <span data-ttu-id="6b728-615">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-615">no</span></span>           |
| <span data-ttu-id="6b728-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="6b728-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="6b728-617">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-617">no</span></span>             | <span data-ttu-id="6b728-618">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-618">no</span></span>           |
| <span data-ttu-id="6b728-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="6b728-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="6b728-620">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-620">no</span></span>             | <span data-ttu-id="6b728-621">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-621">no</span></span>           |
| <span data-ttu-id="6b728-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="6b728-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="6b728-623">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-623">no</span></span>             | <span data-ttu-id="6b728-624">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-624">no</span></span>           |
| <span data-ttu-id="6b728-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="6b728-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="6b728-626">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-626">no</span></span>             | <span data-ttu-id="6b728-627">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-627">no</span></span>           |
| <span data-ttu-id="6b728-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="6b728-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="6b728-629">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-629">no</span></span>             | <span data-ttu-id="6b728-630">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-630">no</span></span>           |
| <span data-ttu-id="6b728-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="6b728-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="6b728-632">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-632">no</span></span>             | <span data-ttu-id="6b728-633">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-633">no</span></span>           |
| <span data-ttu-id="6b728-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="6b728-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="6b728-635">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-635">no</span></span>             | <span data-ttu-id="6b728-636">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-636">no</span></span>           |
| <span data-ttu-id="6b728-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="6b728-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="6b728-638">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-638">no</span></span>             | <span data-ttu-id="6b728-639">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-639">no</span></span>           |
| <span data-ttu-id="6b728-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="6b728-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="6b728-641">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-641">no</span></span>             | <span data-ttu-id="6b728-642">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-642">no</span></span>           |
| <span data-ttu-id="6b728-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="6b728-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="6b728-644">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-644">no</span></span>             | <span data-ttu-id="6b728-645">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-645">no</span></span>           |
| <span data-ttu-id="6b728-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="6b728-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="6b728-647">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-647">no</span></span>             | <span data-ttu-id="6b728-648">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-648">no</span></span>           |
| <span data-ttu-id="6b728-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="6b728-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="6b728-650">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-650">no</span></span>             | <span data-ttu-id="6b728-651">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-651">no</span></span>           |
| <span data-ttu-id="6b728-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="6b728-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="6b728-653">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-653">no</span></span>             | <span data-ttu-id="6b728-654">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-654">no</span></span>           |
| <span data-ttu-id="6b728-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="6b728-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="6b728-656">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-656">no</span></span>             | <span data-ttu-id="6b728-657">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-657">no</span></span>           |
| <span data-ttu-id="6b728-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="6b728-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="6b728-659">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-659">no</span></span>             | <span data-ttu-id="6b728-660">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-660">no</span></span>           |
| <span data-ttu-id="6b728-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="6b728-662">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-662">no</span></span>             | <span data-ttu-id="6b728-663">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-663">no</span></span>           |
| <span data-ttu-id="6b728-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="6b728-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="6b728-665">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-665">no</span></span>             | <span data-ttu-id="6b728-666">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-666">no</span></span>           |
| <span data-ttu-id="6b728-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6b728-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="6b728-668">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-668">no</span></span>             | <span data-ttu-id="6b728-669">ei</span><span class="sxs-lookup"><span data-stu-id="6b728-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="6b728-670">Piirangud ja teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="6b728-670">Limitations and known issues</span></span>
<span data-ttu-id="6b728-671">Järgnevalt on toodud piirangute ja teadaolevate probleemide loend.</span><span class="sxs-lookup"><span data-stu-id="6b728-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="6b728-672">Ajakava API-sid saavad kasutada ainult **Microsoft Projecti litsentsiga kasutajad.**</span><span class="sxs-lookup"><span data-stu-id="6b728-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="6b728-673">Neid ei saa kasutada järgnevad.</span><span class="sxs-lookup"><span data-stu-id="6b728-673">They can't be used by:</span></span>
    - <span data-ttu-id="6b728-674">Rakenduse kasutajad</span><span class="sxs-lookup"><span data-stu-id="6b728-674">Application users</span></span>
    - <span data-ttu-id="6b728-675">Süsteemi kasutajad</span><span class="sxs-lookup"><span data-stu-id="6b728-675">System users</span></span>
    - <span data-ttu-id="6b728-676">Integratsiooni kasutajad</span><span class="sxs-lookup"><span data-stu-id="6b728-676">Integration users</span></span>
    - <span data-ttu-id="6b728-677">Teised kasutajad, kes ei oma nõutavat litsentsi</span><span class="sxs-lookup"><span data-stu-id="6b728-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="6b728-678">Igal suvandil **OperationSet** saab olla maksimaalselt 100 toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b728-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="6b728-679">Igal kasutajal saab maksimaalselt olla 10 avatud suvandit **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6b728-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="6b728-680">Project Operations toetab praegu projektil kokku maksimaalselt 500 ülesannet.</span><span class="sxs-lookup"><span data-stu-id="6b728-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="6b728-681">Suvandi **OperationSet** tõrkeolek ja tõrkelogid pole hetkel saadaval.</span><span class="sxs-lookup"><span data-stu-id="6b728-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="6b728-682">Projektide ja tööülesannete piirangud ja piirid</span><span class="sxs-lookup"><span data-stu-id="6b728-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="6b728-683">Tõrketöötlus</span><span class="sxs-lookup"><span data-stu-id="6b728-683">Error handling</span></span>

   - <span data-ttu-id="6b728-684">Toimingukomplektide põhjal loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **Toimingutekomplekt**.</span><span class="sxs-lookup"><span data-stu-id="6b728-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="6b728-685">Projekti kavandamise teenuse kaudu loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **PSS-i vealogi**.</span><span class="sxs-lookup"><span data-stu-id="6b728-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="6b728-686">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="6b728-686">Sample scenario</span></span>

<span data-ttu-id="6b728-687">Selles stsenaariumis loote projekti, meeskonnaliikme, neli ülesannet ja kaks ressursi määramist.</span><span class="sxs-lookup"><span data-stu-id="6b728-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="6b728-688">Järgmisena värskendate ühte ülesannet, värskendate projekti, kustutate ühe ülesande, kustutate ühe ressursi määramise ja loote ülesande sõltuvuse.</span><span class="sxs-lookup"><span data-stu-id="6b728-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="6b728-689">Täiendavad näited</span><span class="sxs-lookup"><span data-stu-id="6b728-689">Additional samples</span></span>

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
