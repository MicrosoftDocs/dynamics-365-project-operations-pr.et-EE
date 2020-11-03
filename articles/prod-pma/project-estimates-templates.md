---
title: Projekti prognooside sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kestuse prognooside ja projekti kuluprognooside sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075084"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="1fbfb-103">Projekti prognooside sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1fbfb-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1fbfb-104">Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kestuse prognooside ja projekti kuluprognooside sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1fbfb-105">Projekti ülesannete integreerimine, kulukande kategooriad, kestuse prognoosi ja funktsioonide lukustamine on saadaval versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="1fbfb-106">Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="1fbfb-107">Andmevoog rakendusest Project Service Automation rakendusse Finance</span><span class="sxs-lookup"><span data-stu-id="1fbfb-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="1fbfb-108">Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1fbfb-109">Andmete integreerimise funktsiooniga saadaolevad integreerimise mallid võimaldavad projekti kestuse prognooside ja projekti kuluprognooside andmete voogu Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1fbfb-110">Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1fbfb-111">[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1fbfb-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="1fbfb-112">Projekti kestuse prognoosid</span><span class="sxs-lookup"><span data-stu-id="1fbfb-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="1fbfb-113">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="1fbfb-113">Template and tasks</span></span>

<span data-ttu-id="1fbfb-114">Saadaolevatele mallidele Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt** , et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1fbfb-115">Projekti kestuse prognooside sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1fbfb-116">**Andmete migreerimise malli nimi:** projekti kestuse prognoosid (PSA-st Fini ja Opsi)</span><span class="sxs-lookup"><span data-stu-id="1fbfb-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1fbfb-117">**Ülesannete nimi projektis:**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="1fbfb-118">Kande seosed</span><span class="sxs-lookup"><span data-stu-id="1fbfb-118">Transaction relationships</span></span>
    - <span data-ttu-id="1fbfb-119">Kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="1fbfb-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="1fbfb-120">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="1fbfb-120">Entity set</span></span>

| <span data-ttu-id="1fbfb-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1fbfb-121">Project Service Automation</span></span> | <span data-ttu-id="1fbfb-122">Finance</span><span class="sxs-lookup"><span data-stu-id="1fbfb-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="1fbfb-123">Projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="1fbfb-123">Project tasks</span></span>              | <span data-ttu-id="1fbfb-124">Projekti kestuse prognooside integratsiooni olem</span><span class="sxs-lookup"><span data-stu-id="1fbfb-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="1fbfb-125">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="1fbfb-125">Entity flow</span></span>

<span data-ttu-id="1fbfb-126">Projekti kestuse prognoose hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti kestuse prognoosid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1fbfb-127">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1fbfb-127">Prerequisites</span></span>

<span data-ttu-id="1fbfb-128">Enne projekti kestuse prognooside sünkroonimise toimumist peate sünkroonima projektid, projekti ülesanded ja projekti kulukande kategooriad.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1fbfb-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="1fbfb-129">Power Query</span></span>

<span data-ttu-id="1fbfb-130">Projekti kestuse prognooside mallil peate kasutama lisandmoodulit Microsoft Power Query for Excel, et lõpetada järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="1fbfb-131">Määrake vaikimisi prognoosimudeli ID, mida kasutatakse, kui integratsioon loob uue kestuse prognoosid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="1fbfb-132">Filtreerige ülesandest välja kõik ressursile omased kirjed, mis kestuse prognoosi integreerimises nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="1fbfb-133">Filtreerige välja kõik tühjad kandekategooria read.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="1fbfb-134">Selle ülesande mitte lõpetamine võib põhjustada valesid kestuse prognoose.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="1fbfb-135">Vaikimisi prognoosi mudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="1fbfb-135">Set the default forecast model ID</span></span>

<span data-ttu-id="1fbfb-136">Mallis vaikeprognoosi mudeli ID värskendamiseks klõpsake noolt **Vastenda** , et avada vastendamine.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1fbfb-137">Seejärel valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="1fbfb-138">Kui kasutate vaikimisi Projecti kestuse hinnangu (PSA-st Finile ja Opsile) malli, valige loendis **Rakendatud sammud** suvand **Sisestatud tingimus**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="1fbfb-139">Kirjes **Funktsioon** asendage osa **O\_forecast** prognoosi mudeli ID nimega, mida peaks integratsiooniga koos kasutama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="1fbfb-140">Vaikemallil pärineb prognoosi mudeli ID demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="1fbfb-141">Uue malli loomisel peate selle veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="1fbfb-142">Valige Power Querys suvand **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **MudeliID**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="1fbfb-143">Sisestage veeru jaoks tingimus, et kui projektiülesanne ei ole tühi, siis \<enter the forecast model ID\>; muul juhul tühi.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="1fbfb-144">Ressursikohaste kirjete filtreerimine</span><span class="sxs-lookup"><span data-stu-id="1fbfb-144">Filter out resource-specific records</span></span>

<span data-ttu-id="1fbfb-145">Projecti kestuse prognooside (PSA-st Fini ja Opsi) mallil on vaikimisi filter, mis eemaldab kõik ressursile omased kirjed.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="1fbfb-146">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="1fbfb-147">Valige link **Täpsem pärin ja filtreerimine** , et filtreerida veergu **msdyn\_islinetask** , et ainult kirjed olekuga **Väär** oleksid hõlmatud.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="1fbfb-148">Tühjade kandekategooria ridade välja filtreerimine</span><span class="sxs-lookup"><span data-stu-id="1fbfb-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="1fbfb-149">Peate lisama filtri, et eemaldada kõik read, kus kandekategooriad on tühjad.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="1fbfb-150">See toiming on nõutav olenemata sellest, kas kasutate vaikemalli või loote oma malli.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="1fbfb-151">See filter eemaldab rakendusest Project Service Automation kõik kokkuvõtteread, mille tõttu rakenduse Finance kestuse prognoos võib olla vale.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="1fbfb-152">Valige link **Täpsem päring ja filtreerimine** , et filtreerida välja null-kirjed veerus **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1fbfb-153">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="1fbfb-153">Template mapping in Data integration</span></span>

<span data-ttu-id="1fbfb-154">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="1fbfb-155">Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1fbfb-156">[![Malli ülesande vastendamine andmete integratsioonis](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1fbfb-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="1fbfb-157">Projekti kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="1fbfb-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="1fbfb-158">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="1fbfb-158">Template and tasks</span></span>

<span data-ttu-id="1fbfb-159">Projekti kuluprognooside sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1fbfb-160">**Andmete migreerimise malli nimi:** projekti kuluprognoosid (PSA-st Fini ja Opsi)</span><span class="sxs-lookup"><span data-stu-id="1fbfb-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1fbfb-161">**Ülesannete nimi projektis:**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="1fbfb-162">Kande seosed</span><span class="sxs-lookup"><span data-stu-id="1fbfb-162">Transaction relationships</span></span> 
    - <span data-ttu-id="1fbfb-163">Kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="1fbfb-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="1fbfb-164">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="1fbfb-164">Entity set</span></span>

| <span data-ttu-id="1fbfb-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1fbfb-165">Project Service Automation</span></span> | <span data-ttu-id="1fbfb-166">Finance</span><span class="sxs-lookup"><span data-stu-id="1fbfb-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="1fbfb-167">Kande ühendused</span><span class="sxs-lookup"><span data-stu-id="1fbfb-167">Transaction Connections</span></span>    | <span data-ttu-id="1fbfb-168">Projekti kande seoste integratsiooni olem</span><span class="sxs-lookup"><span data-stu-id="1fbfb-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="1fbfb-169">Prognoosiread</span><span class="sxs-lookup"><span data-stu-id="1fbfb-169">Estimate Lines</span></span>             | <span data-ttu-id="1fbfb-170">Projekti kuluprognooside integratsiooni olem</span><span class="sxs-lookup"><span data-stu-id="1fbfb-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="1fbfb-171">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="1fbfb-171">Entity flow</span></span>

<span data-ttu-id="1fbfb-172">Projekti kuluprognoose hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti kuluprognoosid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1fbfb-173">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1fbfb-173">Prerequisites</span></span>

<span data-ttu-id="1fbfb-174">Enne projekti kuluprognooside sünkroonimise toimumist peate sünkroonima projektid, projekti ülesanded ja projekti kulukande kategooriad.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1fbfb-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="1fbfb-175">Power Query</span></span>

<span data-ttu-id="1fbfb-176">Projekti kuluprognooside mallil peate kasutama lisandmoodulit Power Quer, et lõpetada järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="1fbfb-177">Filter, et kaasata ainult kuluprognoosi rea kirjeid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="1fbfb-178">Määrake vaikimisi prognoosimudeli ID, mida kasutatakse, kui integratsioon loob uue kestuse prognoosid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="1fbfb-179">Teisendage arvelduse tüübid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-179">Transform the billing types.</span></span>
- <span data-ttu-id="1fbfb-180">Teisendage kandetüübid.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="1fbfb-181">Filter, et kaasata ainult kuluprognoosi read</span><span class="sxs-lookup"><span data-stu-id="1fbfb-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="1fbfb-182">Projecti kuluprognooside (PSA-st Fini ja Opsi) mallil on vaikefilter, mis sisaldab integratsioonis ainult kuluridu.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="1fbfb-183">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="1fbfb-184">Valige ülesanne **Kande seosed** ja klõpsake seejärel noolt **Vastenda** , et avada vastendamine.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1fbfb-185">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="1fbfb-186">Filtreerige veergu **msdyn\_transactiontype1** , et see sisaldaks ainult atribuuti **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="1fbfb-187">Vaikimisi prognoosi mudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="1fbfb-187">Set the default forecast model ID</span></span>

<span data-ttu-id="1fbfb-188">Mallis vaikeprognoosi mudeli ID värskendamiseks valige ülesanne **Kuluprognoosid** ja klõpsake seejärel noolt **Vastenda** , et avada vastendamine.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1fbfb-189">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="1fbfb-190">Kui kasutate vaikimisi Projecti kuluhinnangu (PSA-st Finile ja Opsile) malli, siis valige Power Querys jaotisest **Rakendatud sammud** esimene suvand **Sisestatud tingimus**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="1fbfb-191">Kirjes **Funktsioon** asendage osa **O\_forecast** prognoosi mudeli ID nimega, mida peaks integratsiooniga koos kasutama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="1fbfb-192">Vaikemallil pärineb prognoosi mudeli ID demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="1fbfb-193">Uue malli loomisel peate selle veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="1fbfb-194">Valige Power Querys suvand **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **MudeliID**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="1fbfb-195">Sisestage veeru jaoks tingimus, et kui prognoosi rea ID ei ole tühi, siis \<enter the forecast model ID\>; muul juhul tühi.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="1fbfb-196">Arvelduse tüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="1fbfb-196">Transform the billing types</span></span>

<span data-ttu-id="1fbfb-197">Projecti kuluprognooside (PSA-st Fini ja Opsi) mall sisaldab tingimusliku veergu, mida kasutatakse integreerimise ajal Project Service Automationist saadud arvelduse tüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="1fbfb-198">Kui loote oma malli, peate selle tingimusliku veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="1fbfb-199">Valige link **Täpsem päring ja filtreerimine** ja valige seejärel **Lisa tingimuslik veerg**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="1fbfb-200">Sisestage uue veeru nimi (nt **ArvelduseTüüp)**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="1fbfb-201">Seejärel sisestage järgmine tingimus.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-201">Then enter the following condition:</span></span>

<span data-ttu-id="1fbfb-202">Kui **msdyn\_billingtype** = 192350000, siis **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="1fbfb-203">vastasel juhul kui **msdyn\_billingtype** = 192350001, siis **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="1fbfb-204">vastasel juhul kui **msdyn\_billingtype** = 192350002, siis **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="1fbfb-205">vastasel juhul **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="1fbfb-206">Kandetüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="1fbfb-206">Transform the transaction types</span></span>

<span data-ttu-id="1fbfb-207">Projecti kuluprognooside (PSA-st Fini ja Opsi) mall sisaldab tingimusliku veergu, mida kasutatakse integreerimise ajal Project Service Automationist saadud kandetüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="1fbfb-208">Kui loote oma malli, peate selle tingimusliku veeru lisama.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="1fbfb-209">Valige link **Täpsem päring ja filtreerimine** ja valige seejärel **Lisa tingimuslik veerg**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="1fbfb-210">Sisestage uue veeru nimi (nt **Kandetüüp)**.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="1fbfb-211">Seejärel sisestage järgmine tingimus.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-211">Then enter the following condition:</span></span>

<span data-ttu-id="1fbfb-212">Kui **msdyn\_transactiontypecode** = 192350000, siis **Kulu**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="1fbfb-213">vastasel juhul kui **msdyn\_transactiontypecode** = 192350005, siis **Müük**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="1fbfb-214">vastasel juhul **null**</span><span class="sxs-lookup"><span data-stu-id="1fbfb-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1fbfb-215">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="1fbfb-215">Template mapping in Data integration</span></span>

<span data-ttu-id="1fbfb-216">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näited.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="1fbfb-217">Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="1fbfb-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1fbfb-218">[![Kuluprognoosi kannete malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1fbfb-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="1fbfb-219">[![Kuluprognoosi malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1fbfb-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
