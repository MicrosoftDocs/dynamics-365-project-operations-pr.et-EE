---
title: Projekti prognooside sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kestuse prognooside ja projekti kuluprognooside sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750953"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="80ee8-103">Projekti prognooside sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80ee8-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="80ee8-104">Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kestuse prognooside ja projekti kuluprognooside sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="80ee8-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="80ee8-105">Projekti ülesannete integreerimine, kulukande kategooriad, kestuse prognoosi ja funktsioonide lukustamine on saadaval versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="80ee8-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="80ee8-106">Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.</span><span class="sxs-lookup"><span data-stu-id="80ee8-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="80ee8-107">Andmevoog rakendusest Project Service Automation rakendusse Finance</span><span class="sxs-lookup"><span data-stu-id="80ee8-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="80ee8-108">Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt.</span><span class="sxs-lookup"><span data-stu-id="80ee8-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="80ee8-109">Andmete integreerimise funktsiooniga saadaolevad integreerimise mallid võimaldavad projekti kestuse prognooside ja projekti kuluprognooside andmete voogu Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="80ee8-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="80ee8-110">Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="80ee8-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="80ee8-111">[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="80ee8-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="80ee8-112">Projekti kestuse prognoosid</span><span class="sxs-lookup"><span data-stu-id="80ee8-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="80ee8-113">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="80ee8-113">Template and tasks</span></span>

<span data-ttu-id="80ee8-114">Saadaolevatele mallidele Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="80ee8-115">Projekti kestuse prognooside sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="80ee8-116">**Andmete migreerimise malli nimi:** projekti kestuse prognoosid (PSA-st Fini ja Opsi)</span><span class="sxs-lookup"><span data-stu-id="80ee8-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="80ee8-117">**Ülesannete nimi projektis:**</span><span class="sxs-lookup"><span data-stu-id="80ee8-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="80ee8-118">Kande seosed</span><span class="sxs-lookup"><span data-stu-id="80ee8-118">Transaction relationships</span></span>
    - <span data-ttu-id="80ee8-119">Kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="80ee8-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="80ee8-120">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="80ee8-120">Entity set</span></span>

| <span data-ttu-id="80ee8-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="80ee8-121">Project Service Automation</span></span> | <span data-ttu-id="80ee8-122">Finance</span><span class="sxs-lookup"><span data-stu-id="80ee8-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="80ee8-123">Projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="80ee8-123">Project tasks</span></span>              | <span data-ttu-id="80ee8-124">Projekti kestuse prognooside integratsiooni olem</span><span class="sxs-lookup"><span data-stu-id="80ee8-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="80ee8-125">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="80ee8-125">Entity flow</span></span>

<span data-ttu-id="80ee8-126">Projekti kestuse prognoose hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti kestuse prognoosid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="80ee8-127">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="80ee8-127">Prerequisites</span></span>

<span data-ttu-id="80ee8-128">Enne projekti kestuse prognooside sünkroonimise toimumist peate sünkroonima projektid, projekti ülesanded ja projekti kulukande kategooriad.</span><span class="sxs-lookup"><span data-stu-id="80ee8-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="80ee8-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="80ee8-129">Power Query</span></span>

<span data-ttu-id="80ee8-130">Projekti kestuse prognooside mallil peate kasutama lisandmoodulit Microsoft Power Query for Excel, et lõpetada järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="80ee8-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="80ee8-131">Määrake vaikimisi prognoosimudeli ID, mida kasutatakse, kui integratsioon loob uue kestuse prognoosid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="80ee8-132">Filtreerige ülesandest välja kõik ressursile omased kirjed, mis kestuse prognoosi integreerimises nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="80ee8-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="80ee8-133">Filtreerige välja kõik tühjad kandekategooria read.</span><span class="sxs-lookup"><span data-stu-id="80ee8-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="80ee8-134">Selle ülesande mitte lõpetamine võib põhjustada valesid kestuse prognoose.</span><span class="sxs-lookup"><span data-stu-id="80ee8-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="80ee8-135">Vaikimisi prognoosi mudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="80ee8-135">Set the default forecast model ID</span></span>

<span data-ttu-id="80ee8-136">Mallis vaikeprognoosi mudeli ID värskendamiseks klõpsake noolt **Vastenda**, et avada vastendamine.</span><span class="sxs-lookup"><span data-stu-id="80ee8-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="80ee8-137">Seejärel valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="80ee8-138">Kui kasutate vaikimisi Projecti kestuse hinnangu (PSA-st Finile ja Opsile) malli, valige loendis **Rakendatud sammud** suvand **Sisestatud tingimus**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="80ee8-139">Kirjes **Funktsioon** asendage osa**O\_forecast** prognoosi mudeli ID nimega, mida peaks integratsiooniga koos kasutama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="80ee8-140">Vaikemallil pärineb prognoosi mudeli ID demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="80ee8-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="80ee8-141">Uue malli loomisel peate selle veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="80ee8-142">Valige Power Querys suvand **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **MudeliID**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="80ee8-143">Sisestage veeru tingimus, kus juhul, kui Projecti ülesanne ei ole null, siis \<sisestage prognoosi mudeli ID\>; vastasel juhul null.</span><span class="sxs-lookup"><span data-stu-id="80ee8-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="80ee8-144">Ressursikohaste kirjete filtreerimine</span><span class="sxs-lookup"><span data-stu-id="80ee8-144">Filter out resource-specific records</span></span>

<span data-ttu-id="80ee8-145">Projecti kestuse prognooside (PSA-st Fini ja Opsi) mallil on vaikimisi filter, mis eemaldab kõik ressursile omased kirjed.</span><span class="sxs-lookup"><span data-stu-id="80ee8-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="80ee8-146">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="80ee8-147">Valige link **Täpsem pärin ja filtreerimine**, et filtreerida veergu **msdyn\_islinetask**, et ainult kirjed olekuga **Väär** oleksid hõlmatud.</span><span class="sxs-lookup"><span data-stu-id="80ee8-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="80ee8-148">Tühjade kandekategooria ridade välja filtreerimine</span><span class="sxs-lookup"><span data-stu-id="80ee8-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="80ee8-149">Peate lisama filtri, et eemaldada kõik read, kus kandekategooriad on tühjad.</span><span class="sxs-lookup"><span data-stu-id="80ee8-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="80ee8-150">See toiming on nõutav olenemata sellest, kas kasutate vaikemalli või loote oma malli.</span><span class="sxs-lookup"><span data-stu-id="80ee8-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="80ee8-151">See filter eemaldab rakendusest Project Service Automation kõik kokkuvõtteread, mille tõttu rakenduse Finance kestuse prognoos võib olla vale.</span><span class="sxs-lookup"><span data-stu-id="80ee8-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="80ee8-152">Valige link **Täpsem päring ja filtreerimine**, et filtreerida välja null-kirjed veerus **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="80ee8-153">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="80ee8-153">Template mapping in Data integration</span></span>

<span data-ttu-id="80ee8-154">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide.</span><span class="sxs-lookup"><span data-stu-id="80ee8-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="80ee8-155">Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="80ee8-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="80ee8-156">[![Malli vastendamine](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="80ee8-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="80ee8-157">Projekti kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="80ee8-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="80ee8-158">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="80ee8-158">Template and tasks</span></span>

<span data-ttu-id="80ee8-159">Projekti kuluprognooside sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="80ee8-160">**Andmete migreerimise malli nimi:** projekti kuluprognoosid (PSA-st Fini ja Opsi)</span><span class="sxs-lookup"><span data-stu-id="80ee8-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="80ee8-161">**Ülesannete nimi projektis:**</span><span class="sxs-lookup"><span data-stu-id="80ee8-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="80ee8-162">Kande seosed</span><span class="sxs-lookup"><span data-stu-id="80ee8-162">Transaction relationships</span></span> 
    - <span data-ttu-id="80ee8-163">Kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="80ee8-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="80ee8-164">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="80ee8-164">Entity set</span></span>

| <span data-ttu-id="80ee8-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="80ee8-165">Project Service Automation</span></span> | <span data-ttu-id="80ee8-166">Finance</span><span class="sxs-lookup"><span data-stu-id="80ee8-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="80ee8-167">Kande ühendused</span><span class="sxs-lookup"><span data-stu-id="80ee8-167">Transaction Connections</span></span>    | <span data-ttu-id="80ee8-168">Projekti kande seoste integratsiooni olem</span><span class="sxs-lookup"><span data-stu-id="80ee8-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="80ee8-169">Prognoosiread</span><span class="sxs-lookup"><span data-stu-id="80ee8-169">Estimate Lines</span></span>             | <span data-ttu-id="80ee8-170">Projekti kuluprognooside integratsiooni olem</span><span class="sxs-lookup"><span data-stu-id="80ee8-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="80ee8-171">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="80ee8-171">Entity flow</span></span>

<span data-ttu-id="80ee8-172">Projekti kuluprognoose hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti kuluprognoosid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="80ee8-173">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="80ee8-173">Prerequisites</span></span>

<span data-ttu-id="80ee8-174">Enne projekti kuluprognooside sünkroonimise toimumist peate sünkroonima projektid, projekti ülesanded ja projekti kulukande kategooriad.</span><span class="sxs-lookup"><span data-stu-id="80ee8-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="80ee8-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="80ee8-175">Power Query</span></span>

<span data-ttu-id="80ee8-176">Projekti kuluprognooside mallil peate kasutama lisandmoodulit Power Quer, et lõpetada järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="80ee8-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="80ee8-177">Filter, et kaasata ainult kuluprognoosi rea kirjeid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="80ee8-178">Määrake vaikimisi prognoosimudeli ID, mida kasutatakse, kui integratsioon loob uue kestuse prognoosid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="80ee8-179">Teisendage arvelduse tüübid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-179">Transform the billing types.</span></span>
- <span data-ttu-id="80ee8-180">Teisendage kandetüübid.</span><span class="sxs-lookup"><span data-stu-id="80ee8-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="80ee8-181">Filter, et kaasata ainult kuluprognoosi read</span><span class="sxs-lookup"><span data-stu-id="80ee8-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="80ee8-182">Projecti kuluprognooside (PSA-st Fini ja Opsi) mallil on vaikefilter, mis sisaldab integratsioonis ainult kuluridu.</span><span class="sxs-lookup"><span data-stu-id="80ee8-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="80ee8-183">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="80ee8-184">Valige ülesanne **Kande seosed** ja klõpsake seejärel noolt **Vastenda**, et avada vastendamine.</span><span class="sxs-lookup"><span data-stu-id="80ee8-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="80ee8-185">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="80ee8-186">Filtreerige veergu **msdyn\_transactiontype1**, et see sisaldaks ainult atribuuti **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="80ee8-187">Vaikimisi prognoosi mudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="80ee8-187">Set the default forecast model ID</span></span>

<span data-ttu-id="80ee8-188">Mallis vaikeprognoosi mudeli ID värskendamiseks valige ülesanne **Kuluprognoosid** ja klõpsake seejärel noolt **Vastenda**, et avada vastendamine.</span><span class="sxs-lookup"><span data-stu-id="80ee8-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="80ee8-189">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="80ee8-190">Kui kasutate vaikimisi Projecti kuluhinnangu (PSA-st Finile ja Opsile) malli, siis valige Power Querys jaotisest **Rakendatud sammud** esimene suvand **Sisestatud tingimus**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="80ee8-191">Kirjes **Funktsioon** asendage osa**O\_forecast** prognoosi mudeli ID nimega, mida peaks integratsiooniga koos kasutama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="80ee8-192">Vaikemallil pärineb prognoosi mudeli ID demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="80ee8-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="80ee8-193">Uue malli loomisel peate selle veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="80ee8-194">Valige Power Querys suvand **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **MudeliID**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="80ee8-195">Sisestage veeru tingimus, kus juhul, kui prognoosi rea ID ei ole null, siis \<sisestage prognoosi mudeli ID\>; vastasel juhul null.</span><span class="sxs-lookup"><span data-stu-id="80ee8-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="80ee8-196">Arvelduse tüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="80ee8-196">Transform the billing types</span></span>

<span data-ttu-id="80ee8-197">Projecti kuluprognooside (PSA-st Fini ja Opsi) mall sisaldab tingimusliku veergu, mida kasutatakse integreerimise ajal Project Service Automationist saadud arvelduse tüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="80ee8-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="80ee8-198">Kui loote oma malli, peate selle tingimusliku veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="80ee8-199">Valige link **Täpsem päring ja filtreerimine** ja valige seejärel **Lisa tingimuslik veerg**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="80ee8-200">Sisestage uue veeru nimi (nt **ArvelduseTüüp)**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="80ee8-201">Seejärel sisestage järgmine tingimus.</span><span class="sxs-lookup"><span data-stu-id="80ee8-201">Then enter the following condition:</span></span>

<span data-ttu-id="80ee8-202">Kui **msdyn\_billingtype** = 192350000, siis **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="80ee8-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="80ee8-203">vastasel juhul kui **msdyn\_billingtype** = 192350001, siis **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="80ee8-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="80ee8-204">vastasel juhul kui **msdyn\_billingtype** = 192350002, siis **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="80ee8-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="80ee8-205">vastasel juhul **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="80ee8-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="80ee8-206">Kandetüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="80ee8-206">Transform the transaction types</span></span>

<span data-ttu-id="80ee8-207">Projecti kuluprognooside (PSA-st Fini ja Opsi) mall sisaldab tingimusliku veergu, mida kasutatakse integreerimise ajal Project Service Automationist saadud kandetüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="80ee8-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="80ee8-208">Kui loote oma malli, peate selle tingimusliku veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="80ee8-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="80ee8-209">Valige link **Täpsem päring ja filtreerimine** ja valige seejärel **Lisa tingimuslik veerg**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="80ee8-210">Sisestage uue veeru nimi (nt **Kandetüüp)**.</span><span class="sxs-lookup"><span data-stu-id="80ee8-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="80ee8-211">Seejärel sisestage järgmine tingimus.</span><span class="sxs-lookup"><span data-stu-id="80ee8-211">Then enter the following condition:</span></span>

<span data-ttu-id="80ee8-212">Kui **msdyn\_transactiontypecode** = 192350000, siis **Kulu**</span><span class="sxs-lookup"><span data-stu-id="80ee8-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="80ee8-213">vastasel juhul kui **msdyn\_transactiontypecode** = 192350005, siis **Müük**</span><span class="sxs-lookup"><span data-stu-id="80ee8-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="80ee8-214">vastasel juhul **null**</span><span class="sxs-lookup"><span data-stu-id="80ee8-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="80ee8-215">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="80ee8-215">Template mapping in Data integration</span></span>

<span data-ttu-id="80ee8-216">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näited.</span><span class="sxs-lookup"><span data-stu-id="80ee8-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="80ee8-217">Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="80ee8-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="80ee8-218">[![Malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="80ee8-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="80ee8-219">[![Malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="80ee8-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
