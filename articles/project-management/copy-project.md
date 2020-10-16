---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908055"
---
# <a name="copy-a-project"></a><span data-ttu-id="2bf8e-103">Projekti kopeerimine</span><span class="sxs-lookup"><span data-stu-id="2bf8e-103">Copy a project</span></span>

<span data-ttu-id="2bf8e-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="2bf8e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2bf8e-105">Dynamics 365 Project Operations võimaldab teil kiiresti luua uusi projekte, kasutades vormil **Projekt** toimingut **Kopeeri projekt**.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="2bf8e-106">Projekti kopeerimiseks valige projekt ja seejärel valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="2bf8e-107">Toiming kopeerib järgneva.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-107">The action will copy:</span></span>

- <span data-ttu-id="2bf8e-108">Projekti atribuudid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-108">Project properties</span></span>
- <span data-ttu-id="2bf8e-109">Tööjaotuse struktuur</span><span class="sxs-lookup"><span data-stu-id="2bf8e-109">The Work breakdown structure</span></span>
- <span data-ttu-id="2bf8e-110">Projektimeeskonna liikmed</span><span class="sxs-lookup"><span data-stu-id="2bf8e-110">Project team members</span></span>
- <span data-ttu-id="2bf8e-111">Projekti prognoosid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-111">Project estimates</span></span>
- <span data-ttu-id="2bf8e-112">Projekti kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="2bf8e-113">Projekti atribuudid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-113">Project properties</span></span>

<span data-ttu-id="2bf8e-114">Kui projekt on kopeeritud, kopeeritakse väärtused järgmistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="2bf8e-115">Nimetus</span><span class="sxs-lookup"><span data-stu-id="2bf8e-115">Name</span></span>
- <span data-ttu-id="2bf8e-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bf8e-116">Description</span></span>
- <span data-ttu-id="2bf8e-117">Klient</span><span class="sxs-lookup"><span data-stu-id="2bf8e-117">Customer</span></span>
- <span data-ttu-id="2bf8e-118">Kalendri mall</span><span class="sxs-lookup"><span data-stu-id="2bf8e-118">Calendar Template</span></span>
- <span data-ttu-id="2bf8e-119">Valuuta</span><span class="sxs-lookup"><span data-stu-id="2bf8e-119">Currency</span></span>
- <span data-ttu-id="2bf8e-120">Lepingut sõlmiv üksus</span><span class="sxs-lookup"><span data-stu-id="2bf8e-120">Contracting Unit</span></span>
- <span data-ttu-id="2bf8e-121">Projektijuht</span><span class="sxs-lookup"><span data-stu-id="2bf8e-121">Project Manager</span></span>
- <span data-ttu-id="2bf8e-122">Olek</span><span class="sxs-lookup"><span data-stu-id="2bf8e-122">Status</span></span>
- <span data-ttu-id="2bf8e-123">Üldine projekti olek</span><span class="sxs-lookup"><span data-stu-id="2bf8e-123">Overall Project Status</span></span>
- <span data-ttu-id="2bf8e-124">Kommentaarid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-124">Comments</span></span>
- <span data-ttu-id="2bf8e-125">Prognoosid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-125">Estimates</span></span>
- <span data-ttu-id="2bf8e-126">Eeldatav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bf8e-126">Estimated Start Date</span></span>
- <span data-ttu-id="2bf8e-127">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="2bf8e-127">Finish Date</span></span>
- <span data-ttu-id="2bf8e-128">Tööpanus (tunnid)</span><span class="sxs-lookup"><span data-stu-id="2bf8e-128">Effort (Hours)</span></span>
- <span data-ttu-id="2bf8e-129">Eeldatav tööjõukulu</span><span class="sxs-lookup"><span data-stu-id="2bf8e-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="2bf8e-130">Eeldatav kulude maksumus</span><span class="sxs-lookup"><span data-stu-id="2bf8e-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="2bf8e-131">Tööjaotuse struktuur</span><span class="sxs-lookup"><span data-stu-id="2bf8e-131">Work breakdown structure</span></span>

<span data-ttu-id="2bf8e-132">Kui projekt on kopeeritud, siis kopeeritakse kogu ressursi laaditud tööjaotuse struktuur.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="2bf8e-133">Nimetatud ressursid asendatakse üldiste ressurssidega.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="2bf8e-134">Kui nimetatud ressurssidel ei ole üldise ressursiga sama tööaega, arvutatakse ajakava uuesti ja ülesande kestused võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="2bf8e-135">Projektimeeskonna liikmed</span><span class="sxs-lookup"><span data-stu-id="2bf8e-135">Project team members</span></span>

<span data-ttu-id="2bf8e-136">Kui projektimeeskond kopeeritakse lähteprojektist, kopeeritakse üldised ressursid.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="2bf8e-137">Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid lähteprojektis.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="2bf8e-138">Nimetatud ressursid teisendatakse üldisteks meeskonnaliikmeteks.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="2bf8e-139">Prognoosid</span><span class="sxs-lookup"><span data-stu-id="2bf8e-139">Estimates</span></span>

<span data-ttu-id="2bf8e-140">Kui projekt on kopeeritud, kopeeritakse lähteprojektist nii ressursi kui ka kulu prognoosiread.</span><span class="sxs-lookup"><span data-stu-id="2bf8e-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>