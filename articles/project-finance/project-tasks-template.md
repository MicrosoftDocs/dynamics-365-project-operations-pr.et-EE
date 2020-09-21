---
title: Projekti ülesannete sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevat tööülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
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
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751029"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c70ba-103">Projekti ülesannete sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c70ba-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c70ba-104">Selles teemas kirjeldatakse malli ja aluseks olevat tööülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c70ba-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c70ba-105">Projekti ülesannete integreerimine, kulukande kategooriad, kuluprognoosid ja funktsioonide lukustamine on saadaval versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="c70ba-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="c70ba-106">Kui kasutate rakendust Enterprise Edition 7.3.0 pärast KB 4132657 ja KB 4132660 installimist, on teil võimalik kasutada malle, et integreerida projekti tööülesanded, kuluarvestuse kategooriad, tunnihinnangud, kuluhinnangud ja tegelikud näitajad ning konfigureerida funktsioonide lukustamist.</span><span class="sxs-lookup"><span data-stu-id="c70ba-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c70ba-107">Kui te peate arvestuse jaotuse lähtestama, soovitasime ka installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="c70ba-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="c70ba-108">Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.</span><span class="sxs-lookup"><span data-stu-id="c70ba-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c70ba-109">Andmevoog rakendusest Project Service Automation rakendusse Finance</span><span class="sxs-lookup"><span data-stu-id="c70ba-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c70ba-110">Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt.</span><span class="sxs-lookup"><span data-stu-id="c70ba-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c70ba-111">Andmete integreerimise funktsiooniga saadaolev integreerimismall võimaldab projekti ülesannete andmete voogu Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c70ba-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c70ba-112">Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="c70ba-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c70ba-113">[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c70ba-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="c70ba-114">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="c70ba-114">Template and task</span></span>

<span data-ttu-id="c70ba-115">Mallile Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="c70ba-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c70ba-116">Projekti ülesannete sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="c70ba-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c70ba-117">**Andmete migreerimise malli nimi:** projekti ülesanded (PSA-st Fini ja Opsi)</span><span class="sxs-lookup"><span data-stu-id="c70ba-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c70ba-118">**Ülesande nimi projektis:** projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="c70ba-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="c70ba-119">Enne kui projekti ülesannete sünkroonimine saab aset leida, peate sünkroonima projekti kontaktid ja projektid.</span><span class="sxs-lookup"><span data-stu-id="c70ba-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c70ba-120">Olemikogum</span><span class="sxs-lookup"><span data-stu-id="c70ba-120">Entity set</span></span>

| <span data-ttu-id="c70ba-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c70ba-121">Project Service Automation</span></span> | <span data-ttu-id="c70ba-122">Finance</span><span class="sxs-lookup"><span data-stu-id="c70ba-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="c70ba-123">Projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="c70ba-123">Project Tasks</span></span>              | <span data-ttu-id="c70ba-124">Integratsiooniolem projekti ülesande jaoks</span><span class="sxs-lookup"><span data-stu-id="c70ba-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c70ba-125">Olemi voog</span><span class="sxs-lookup"><span data-stu-id="c70ba-125">Entity flow</span></span>

<span data-ttu-id="c70ba-126">Projekti ülesandeid hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti tegevused.</span><span class="sxs-lookup"><span data-stu-id="c70ba-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c70ba-127">Eeltingimused ja vastenduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="c70ba-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="c70ba-128">Enne kui projekti ülesannete sünkroonimine saab aset leida, peate sünkroonima projekti kontaktid ja projektid.</span><span class="sxs-lookup"><span data-stu-id="c70ba-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="c70ba-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="c70ba-129">Power Query</span></span>

<span data-ttu-id="c70ba-130">Kui see tingimus on täidetud, siis peate kasutama andmete filtreerimiseks valikut Microsoft Power Query for Excel.</span><span class="sxs-lookup"><span data-stu-id="c70ba-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="c70ba-131">Teil on projekti tööülesannete hulgas ressursiga seotud kirjed.</span><span class="sxs-lookup"><span data-stu-id="c70ba-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="c70ba-132">Kui peate kasutama Power Queryd, järgige seda suunist.</span><span class="sxs-lookup"><span data-stu-id="c70ba-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="c70ba-133">Projekti tööülesannete (PSA-st kuni Fini ja Opsi) mallil on vaikefilter, mis välistab ressursile omased kirjed projekti ülesandest, seades filtri  **IsLineTask** olekule **väär**.</span><span class="sxs-lookup"><span data-stu-id="c70ba-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="c70ba-134">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="c70ba-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c70ba-135">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="c70ba-135">Template mapping in Data integration</span></span>

<span data-ttu-id="c70ba-136">Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näide.</span><span class="sxs-lookup"><span data-stu-id="c70ba-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="c70ba-137">Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="c70ba-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c70ba-138">[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="c70ba-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
