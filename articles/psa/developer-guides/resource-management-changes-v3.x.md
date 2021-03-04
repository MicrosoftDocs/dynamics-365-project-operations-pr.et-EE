---
title: Ressursihalduse muudatused (Project Service Automation 3.x)
description: Selles teemas antakse teavet ressursihalduse alas tehtud muudatuste kohta.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148638"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="4e000-103">Ressursihalduse muudatused (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="4e000-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="4e000-104">Selle teema jaotised annavad teavet rakenduse Dynamics 365 Project Service Automation versioon 3.x ressursihalduse alas tehtud muudatuste kohta.</span><span class="sxs-lookup"><span data-stu-id="4e000-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="4e000-105">Projekti prognoosid</span><span class="sxs-lookup"><span data-stu-id="4e000-105">Project estimates</span></span>

<span data-ttu-id="4e000-106">Selle asemel, et võtta aluseks olem **msdyn\_projecttask** (**Projekti ülesanne**), põhinevad projekti prognoosid olemil **msdyn\_resourceassignment** (**Ressursi määramine**).</span><span class="sxs-lookup"><span data-stu-id="4e000-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="4e000-107">Ressursi määramised on muutunud ülesannete kavandamise ja hinnakujunduse juures nö tõe allikaks.</span><span class="sxs-lookup"><span data-stu-id="4e000-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="4e000-108">Reaülesanded</span><span class="sxs-lookup"><span data-stu-id="4e000-108">Line tasks</span></span>

<span data-ttu-id="4e000-109">Rakenduses PSA 3.x on reaülesanded aegunud (iganenud).</span><span class="sxs-lookup"><span data-stu-id="4e000-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="4e000-110">Määramised viitavad nüüd kogu ülesandele, mitte reaülesannetele.</span><span class="sxs-lookup"><span data-stu-id="4e000-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="4e000-111">Järgmises näites kirjeldatakse, kuidas ülesanne, mille nimi on „Testülesanne”, määratakse meeskonnaliikmetele A ja B PSA varasemates versioonides ja PSA versioonis 3.x.</span><span class="sxs-lookup"><span data-stu-id="4e000-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="4e000-112">**Enne PSA versiooni 3.x.**</span><span class="sxs-lookup"><span data-stu-id="4e000-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="4e000-113">Testülesanne</span><span class="sxs-lookup"><span data-stu-id="4e000-113">Test task</span></span>

        - <span data-ttu-id="4e000-114">Testülesanne – reaülesanne 1</span><span class="sxs-lookup"><span data-stu-id="4e000-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="4e000-115">Määramine liikmele A</span><span class="sxs-lookup"><span data-stu-id="4e000-115">Assignment to A</span></span>

        - <span data-ttu-id="4e000-116">Testülesanne – reaülesanne 2</span><span class="sxs-lookup"><span data-stu-id="4e000-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="4e000-117">Määramine liikmele B</span><span class="sxs-lookup"><span data-stu-id="4e000-117">Assignment to B</span></span>

- <span data-ttu-id="4e000-118">**Versioonis PSA 3.x.**</span><span class="sxs-lookup"><span data-stu-id="4e000-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="4e000-119">Testülesanne</span><span class="sxs-lookup"><span data-stu-id="4e000-119">Test task</span></span>

        - <span data-ttu-id="4e000-120">Määramine liikmele A</span><span class="sxs-lookup"><span data-stu-id="4e000-120">Assignment to A</span></span>
        - <span data-ttu-id="4e000-121">Määramine liikmele B</span><span class="sxs-lookup"><span data-stu-id="4e000-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="4e000-122">Määramata määramine</span><span class="sxs-lookup"><span data-stu-id="4e000-122">Unassigned assignment</span></span>

<span data-ttu-id="4e000-123">PSA versioonis 3.x on määramata määramine selline määramine, mis on määratud meeskonnaliikmele **NULL** ja ressursile **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4e000-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="4e000-124">Määramata määramised võivad ilmneda paari stsenaariumi korral.</span><span class="sxs-lookup"><span data-stu-id="4e000-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="4e000-125">Kui ülesanne on loodud, kuid see pole veel ühelegi meeskonnaliikmele määratud, luuakse alati määramata määramine.</span><span class="sxs-lookup"><span data-stu-id="4e000-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="4e000-126">Kui kõik ülesandele määratud isikud eemaldatakse, luuakse selle ülesande jaoks määramata määramine uuesti.</span><span class="sxs-lookup"><span data-stu-id="4e000-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="4e000-127">Väljade ajastamine olemis Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="4e000-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="4e000-128">Olemi **msdyn\_projecttask** väljad on aegunud või teisaldatud olemisse **msdyn\_resourceassignment** või viidatakse neile nüüd olemist **msdyn\_projectteam** (**Projektimeeskonna liige**).</span><span class="sxs-lookup"><span data-stu-id="4e000-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="4e000-129">Aegunud väli olemis msdyn\_projecttask (Projekti ülesanne)</span><span class="sxs-lookup"><span data-stu-id="4e000-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="4e000-130">Uus väli olemis msdyn\_resourceassignment (Ressursi määramine)</span><span class="sxs-lookup"><span data-stu-id="4e000-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="4e000-131">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="4e000-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="4e000-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="4e000-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="4e000-133">Pole</span><span class="sxs-lookup"><span data-stu-id="4e000-133">None</span></span> | |
| <span data-ttu-id="4e000-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="4e000-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="4e000-135">Pole</span><span class="sxs-lookup"><span data-stu-id="4e000-135">None</span></span> | |
| <span data-ttu-id="4e000-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="4e000-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="4e000-137">Pole</span><span class="sxs-lookup"><span data-stu-id="4e000-137">None</span></span> | |
| <span data-ttu-id="4e000-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="4e000-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="4e000-139">Pole</span><span class="sxs-lookup"><span data-stu-id="4e000-139">None</span></span> | |
| <span data-ttu-id="4e000-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="4e000-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="4e000-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="4e000-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="4e000-142">Väljal talletatud JavaScript objektiesituse (JSON) andmestruktuuri vormingut on muudetud.</span><span class="sxs-lookup"><span data-stu-id="4e000-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="4e000-143">Ajakava kontuur</span><span class="sxs-lookup"><span data-stu-id="4e000-143">Schedule contour</span></span>

<span data-ttu-id="4e000-144">Ajakava kontuuri talletatakse iga olemi **Ressursi määramine** (**msdyn\_resourceassignment**) puhul väljal **Plaanitud töö** (**msdyn\_plannedwork**).</span><span class="sxs-lookup"><span data-stu-id="4e000-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="4e000-145">Struktuur</span><span class="sxs-lookup"><span data-stu-id="4e000-145">Structure</span></span>

<span data-ttu-id="4e000-146">Ajakava kontuuri uus struktuur koosneb paindlikest ajasektoritest, mis on määratletud ajakava iga päeva jaoks.</span><span class="sxs-lookup"><span data-stu-id="4e000-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="4e000-147">Igal ajasektoril on järgmised atribuudid.</span><span class="sxs-lookup"><span data-stu-id="4e000-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="4e000-148">**Algus** – päeva töötundide algus projektikalendri järgi.</span><span class="sxs-lookup"><span data-stu-id="4e000-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="4e000-149">**Lõpp** – päeva töötundide lõpp projektikalendri järgi.</span><span class="sxs-lookup"><span data-stu-id="4e000-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="4e000-150">**Tunnid** – päevale määratud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="4e000-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="4e000-151">**Näide**</span><span class="sxs-lookup"><span data-stu-id="4e000-151">**Example**</span></span>

<span data-ttu-id="4e000-152">Selles näites kasutatakse projektikalendrit, kus tööpäev kestab 9–17ni ajavööndis UTC-8.</span><span class="sxs-lookup"><span data-stu-id="4e000-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="4e000-153">Automaatne plaanimine ja käsitsi plaanimine</span><span class="sxs-lookup"><span data-stu-id="4e000-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="4e000-154">Kui ülesanne ajastatakse automaatselt, on tunnid langevalt ja ülesande kestust võidakse vähendada.</span><span class="sxs-lookup"><span data-stu-id="4e000-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="4e000-155">**Näide**</span><span class="sxs-lookup"><span data-stu-id="4e000-155">**Example**</span></span>

<span data-ttu-id="4e000-156">Järgmine ülesanne plaaniti automaatselt 18 tunniks kolme päeva jooksul (3. detsembrist 2018 kuni 5. detsembrini 2018).</span><span class="sxs-lookup"><span data-stu-id="4e000-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="4e000-157">Kui ülesanne plaanitakse käsitsi, jaotatakse tunnid ühtlaselt kõigile kuupäevadele.</span><span class="sxs-lookup"><span data-stu-id="4e000-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="4e000-158">**Näide**</span><span class="sxs-lookup"><span data-stu-id="4e000-158">**Example**</span></span>

<span data-ttu-id="4e000-159">Järgmine ülesanne plaaniti käsitsi 18 tunniks kolme päeva jooksul (3. detsembrist 2018 kuni 5. detsembrini 2018).</span><span class="sxs-lookup"><span data-stu-id="4e000-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="4e000-160">Määramise ühik</span><span class="sxs-lookup"><span data-stu-id="4e000-160">Assignment unit</span></span>

<span data-ttu-id="4e000-161">Määramise ühik on PSA versioonis 3.x kasutuselt kõrvaldatud.</span><span class="sxs-lookup"><span data-stu-id="4e000-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="4e000-162">Ülesande panusetunnid on nüüd võrdselt päeva kaupa jaotatud kõigi määratud ressursside vahel.</span><span class="sxs-lookup"><span data-stu-id="4e000-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="4e000-163">**Näide**</span><span class="sxs-lookup"><span data-stu-id="4e000-163">**Example**</span></span>

<span data-ttu-id="4e000-164">Selles näites on ülesanne määratud kahele ressursile ja see on automaatselt ajastatud 36 tunniks kolme päeva jooksul (3. detsembrist 2018 kuni 5. detsembrini 2018).</span><span class="sxs-lookup"><span data-stu-id="4e000-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="4e000-165">Määramine 1</span><span class="sxs-lookup"><span data-stu-id="4e000-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="4e000-166">Määramine 2</span><span class="sxs-lookup"><span data-stu-id="4e000-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="4e000-167">Hinnadimensioonid</span><span class="sxs-lookup"><span data-stu-id="4e000-167">Pricing dimensions</span></span>

<span data-ttu-id="4e000-168">PSA versioonis 3.x on ressursikohased hinnadimensiooni väljad (nt **Roll** ja **Organisatsiooniüksus**) olemist **msdyn\_projecttask** eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="4e000-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="4e000-169">Neid välju saab nüüd projekti prognooside loomisel tuua vastavast ressursi määramise (**msdyn\_resourceassignment**) projektimeeskonna liikmest (**msdyn\_projectteam**).</span><span class="sxs-lookup"><span data-stu-id="4e000-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="4e000-170">Olemisse **msdyn\_projectteam** on lisatud uus väli **msdyn\_organizationalunit**.</span><span class="sxs-lookup"><span data-stu-id="4e000-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="4e000-171">Aegunud väli olemis msdyn\_projecttask (Projekti ülesanne)</span><span class="sxs-lookup"><span data-stu-id="4e000-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="4e000-172">Väi olemist msdyn\_projectteam (Projektimeeskonna liige), mida selle asemel kasutatakse</span><span class="sxs-lookup"><span data-stu-id="4e000-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="4e000-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4e000-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="4e000-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4e000-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="4e000-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="4e000-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="4e000-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="4e000-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="4e000-177">Kontuurid</span><span class="sxs-lookup"><span data-stu-id="4e000-177">Contours</span></span>

<span data-ttu-id="4e000-178">Hinnakujunduse ja hindamise kontuuriväljad on olemis **msdyn\_projecttask** kasutuselt kõrvaldatud.</span><span class="sxs-lookup"><span data-stu-id="4e000-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="4e000-179">Need on teisaldatud olemisse **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="4e000-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="4e000-180">Aegunud väli olemis msdyn\_projecttask (Projekti ülesanne)</span><span class="sxs-lookup"><span data-stu-id="4e000-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="4e000-181">Uus väli olemis msdyn\_resourceassignment (Ressursi määramine)</span><span class="sxs-lookup"><span data-stu-id="4e000-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="4e000-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="4e000-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="4e000-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="4e000-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="4e000-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="4e000-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="4e000-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="4e000-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="4e000-186">Järgmised väljad on lisatud olemisse **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="4e000-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="4e000-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4e000-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="4e000-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4e000-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="4e000-189">Järgmised plaanitud, tegelike ja ülejäänud kulude ja müügi väljad on olemis **msdyn\_projecttask** muutmata.</span><span class="sxs-lookup"><span data-stu-id="4e000-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="4e000-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4e000-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="4e000-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4e000-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="4e000-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="4e000-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="4e000-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="4e000-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="4e000-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4e000-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="4e000-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4e000-195">msdyn\_remainingsales</span></span>
