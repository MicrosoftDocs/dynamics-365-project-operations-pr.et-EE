---
title: Projekti kulukategooriate sünkroonimine rakenduste Finance and Operations ja Project Service Automation vahel
description: Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075095"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="24a36-103">Projekti kulukategooriate sünkroonimine rakenduste Finance and Operations ja Project Service Automation vahel</span><span class="sxs-lookup"><span data-stu-id="24a36-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="24a36-104">Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.</span><span class="sxs-lookup"><span data-stu-id="24a36-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="24a36-105">Projekti ülesannete integreerimine, kulukande kategooriad, kuluprognoosid ja funktsioonide lukustamine on saadaval versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="24a36-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="24a36-106">Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.</span><span class="sxs-lookup"><span data-stu-id="24a36-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="24a36-107">Kui kasutate rakendust Enterprise Edition 7.3.0 pärast KB 4132657 ja KB 4132660 installimist, on teil võimalik kasutada malle, et integreerida projekti tööülesanded, kuluarvestuse kategooriad, tunnihinnangud, kuluhinnangud ja tegelikud näitajad ning konfigureerida funktsioonide lukustamist.</span><span class="sxs-lookup"><span data-stu-id="24a36-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="24a36-108">Kui te peate arvestuse jaotuse lähtestama, soovitame installida ka KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="24a36-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="24a36-109">Andmevoog rakendustele Project Service Automation ja Finance.</span><span class="sxs-lookup"><span data-stu-id="24a36-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="24a36-110">Project Service Automationi ja Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt.</span><span class="sxs-lookup"><span data-stu-id="24a36-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="24a36-111">Andmete integreerimise funktsiooniga saadaolevad integreerimise mallid võimaldavad projekti kandekategooria andmete voogu Finance'i ja Project Service Automationi vahel.</span><span class="sxs-lookup"><span data-stu-id="24a36-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="24a36-112">Kui projekti kulukategooriad on Finance'is määratud, toimub kõigepealt integratsioonivoog Finance'ist Project Service Automatitioni.</span><span class="sxs-lookup"><span data-stu-id="24a36-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="24a36-113">Projekti kulukategooriate integreerimise ID-d värskendatakse sünkroonimise kaudu rakendusest Project Service Automation Finance'i.</span><span class="sxs-lookup"><span data-stu-id="24a36-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="24a36-114">Kui projekti kulukategooriad on Project Service Automationis määratud, toimub kõigepealt integratsioonivoog Project Service Automatitionist Finance'i..</span><span class="sxs-lookup"><span data-stu-id="24a36-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="24a36-115">Projekti kategooriad peavad Finance'is konfigureeritud juba enne Project Service Automationist sünkroonimist.</span><span class="sxs-lookup"><span data-stu-id="24a36-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="24a36-116">Seejärel sünkroonige rakendusest Finance tagasi Project Service Automationisse ja seejärel rakendusest Project Service Automation tagasi Finance'i.</span><span class="sxs-lookup"><span data-stu-id="24a36-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="24a36-117">Sel viisil saate tagada, et kategooriad on lingitud ja duplikaate ei looda.</span><span class="sxs-lookup"><span data-stu-id="24a36-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="24a36-118">Tavaliselt projekti kulukategooriad määratakse Finance'is.</span><span class="sxs-lookup"><span data-stu-id="24a36-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="24a36-119">Kuid kui nad ei ole või kui kulukategooriad on juba loodud rakendusega Project Service Automation, peate esmalt sünkroonima kasutades projekti kulukannete kategooriate (PSA FIN-i ja Opsi) malli abil.</span><span class="sxs-lookup"><span data-stu-id="24a36-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="24a36-120">Seejärel sünkroonitakse, kasutades projekti kulukannete kategooriate (Fin ja Ops PSA-sse) malli.</span><span class="sxs-lookup"><span data-stu-id="24a36-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="24a36-121">Seejärel peaksite käivitama sünkroonimise rakendusest Project Service Automation rakendusse Finance veel üks kord.</span><span class="sxs-lookup"><span data-stu-id="24a36-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="24a36-122">Kui sünkroonite esmalt rakendusest Project Service Automation, peavad enne sünkroonimise käivitamist olema Finance'is täidetud järgmised nõuded.</span><span class="sxs-lookup"><span data-stu-id="24a36-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="24a36-123">Ühiskasutusega kategooria, mis vastab Project Service Automationis seadistatud projektikategooriale peab olemas olema, ja see peab olema lubatud nii **projekti** kui ka **kulu** jaoks.</span><span class="sxs-lookup"><span data-stu-id="24a36-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="24a36-124">Iga Finance'i juriidilise isiku jaoks, mis peab olema integreeritud, peavad olemas olema järgmised projektikategooriad.</span><span class="sxs-lookup"><span data-stu-id="24a36-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="24a36-125">**Projekti kategooria** on olemas.</span><span class="sxs-lookup"><span data-stu-id="24a36-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="24a36-126">**Kasutamine kulus** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="24a36-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="24a36-127">**Aktiivne töölehel** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="24a36-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="24a36-128">**Kandetüübiks** on seatud **kulu**.</span><span class="sxs-lookup"><span data-stu-id="24a36-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="24a36-129">Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="24a36-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="24a36-130">[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="24a36-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="24a36-131">Projekti kulukategooria sünkroonimine rakendustest Finance rakendusse Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="24a36-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="24a36-132">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="24a36-132">Template and task</span></span>

<span data-ttu-id="24a36-133">Mallile Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt** , et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="24a36-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="24a36-134">Projekti kulukategooriate sünkroonimiseks Finance'ist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="24a36-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="24a36-135">**Andmete integreerimise malli nimi:** projekti kulukannete kategooriad (Finist ja Opsist PSA-sse)</span><span class="sxs-lookup"><span data-stu-id="24a36-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="24a36-136">**Tööülesande nimi projektis:** kategooriate sünkroonimine PSA-sse</span><span class="sxs-lookup"><span data-stu-id="24a36-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="24a36-137">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="24a36-137">Entity set</span></span>

| <span data-ttu-id="24a36-138">Finance</span><span class="sxs-lookup"><span data-stu-id="24a36-138">Finance</span></span>                           | <span data-ttu-id="24a36-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="24a36-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="24a36-140">Kategooriate integreerimise olem</span><span class="sxs-lookup"><span data-stu-id="24a36-140">Integration entity for categories</span></span> | <span data-ttu-id="24a36-141">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="24a36-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="24a36-142">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="24a36-142">Entity flow</span></span>

<span data-ttu-id="24a36-143">Projekti kulukategooriaid hallatakse rakenduses Finance ja need sünkroonitakse rakendusega Project Service Automation kandekategooriad.</span><span class="sxs-lookup"><span data-stu-id="24a36-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="24a36-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="24a36-144">Power Query</span></span>

<span data-ttu-id="24a36-145">Kui sünkroonite rakendusega Project Service automation, peate kasutama rakendust Microsoft Power Query Exceli jaoks, et määrata arvetüüp kandekategoorias.</span><span class="sxs-lookup"><span data-stu-id="24a36-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="24a36-146">Projekti kulukannete kategooriate (Fin ja Ops PSA-sse) mallis on vaikeveerg ja vastendus.</span><span class="sxs-lookup"><span data-stu-id="24a36-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="24a36-147">Kui loote oma malli, peate lisama tingimusliku veeru Power Query'is.</span><span class="sxs-lookup"><span data-stu-id="24a36-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="24a36-148">Toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="24a36-148">Follow these steps.</span></span>

1. <span data-ttu-id="24a36-149">Klõpsake noolt, et avada projekti kulu kategooriate ülesande vastendus projekti kulukategooriate (Fin ja Ops PSA-le) malliga.</span><span class="sxs-lookup"><span data-stu-id="24a36-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="24a36-150">Klõpsake linki **Täpsem päring ja filtreerimine** , et avada Power Query.</span><span class="sxs-lookup"><span data-stu-id="24a36-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="24a36-151">Valige **Lisa tingimuslik veerg**.</span><span class="sxs-lookup"><span data-stu-id="24a36-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="24a36-152">Sisestage uue veeru nimi (nt **ArvelduseTüüp)**.</span><span class="sxs-lookup"><span data-stu-id="24a36-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="24a36-153">Sisestage järgmine tingimus: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="24a36-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="24a36-154">Klõpsake veerus **OK**.</span><span class="sxs-lookup"><span data-stu-id="24a36-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="24a36-155">Vastendage see uus veerg kindlasti vastenduse lehel.</span><span class="sxs-lookup"><span data-stu-id="24a36-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="24a36-156">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide.</span><span class="sxs-lookup"><span data-stu-id="24a36-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="24a36-157">Vastendus näitab välja teavet, mis sünkroonitakse Finance'ist Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="24a36-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="24a36-158">[![Projekti kulukategooria malli vastendamine rakendusse Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="24a36-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="24a36-159">Projekti kulukategooria sünkroonimine rakendustest Project Service Automation rakendusse Finance</span><span class="sxs-lookup"><span data-stu-id="24a36-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="24a36-160">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="24a36-160">Template and task</span></span>

<span data-ttu-id="24a36-161">Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance'i kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="24a36-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="24a36-162">**Andmete integreerimise malli nimi:** projekti kulukannete kategooriad (PSA-st Fini ja Opsi)</span><span class="sxs-lookup"><span data-stu-id="24a36-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="24a36-163">**Tööülesande nimi projektis:** sünkroonimiskategooriad Fin-si Ops-i</span><span class="sxs-lookup"><span data-stu-id="24a36-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="24a36-164">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="24a36-164">Entity set</span></span>

| <span data-ttu-id="24a36-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="24a36-165">Project Service Automation</span></span> | <span data-ttu-id="24a36-166">Finance</span><span class="sxs-lookup"><span data-stu-id="24a36-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="24a36-167">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="24a36-167">Transaction categories</span></span>     | <span data-ttu-id="24a36-168">Kategooriate integreerimise olem</span><span class="sxs-lookup"><span data-stu-id="24a36-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="24a36-169">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="24a36-169">Entity flow</span></span>

<span data-ttu-id="24a36-170">Projekti kulukategooriaid hallatakse rakenduses Finance ja need sünkroonitakse rakendusega Project Service Automation kandekategooriad.</span><span class="sxs-lookup"><span data-stu-id="24a36-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="24a36-171">Finance'i sünkroonimine värskendab Finance'i projektikategooria Finance'is Project Service Automationi integratsiooni ID-ga.</span><span class="sxs-lookup"><span data-stu-id="24a36-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="24a36-172">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="24a36-172">Template mapping in Data integration</span></span>

<span data-ttu-id="24a36-173">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide.</span><span class="sxs-lookup"><span data-stu-id="24a36-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="24a36-174">Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="24a36-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="24a36-175">[![Malli vastendamine Project Service Automationist rakendusse Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="24a36-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
