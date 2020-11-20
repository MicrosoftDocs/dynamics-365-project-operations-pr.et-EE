---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131788"
---
# <a name="copy-a-project"></a><span data-ttu-id="8d497-103">Projekti kopeerimine</span><span class="sxs-lookup"><span data-stu-id="8d497-103">Copy a project</span></span>

<span data-ttu-id="8d497-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="8d497-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d497-105">Dynamics 365 Project Operations võimaldab teil kiiresti luua uusi projekte, valides vormil **Projektid** toimingu **Kopeeri projekt**.</span><span class="sxs-lookup"><span data-stu-id="8d497-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="8d497-106">Projekti kopeerimiseks avage projekt, mida soovite kopeerida, ja seejärel valige toiming **Kopeeri projekt**.</span><span class="sxs-lookup"><span data-stu-id="8d497-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="8d497-107">Toiming kopeerib järgneva.</span><span class="sxs-lookup"><span data-stu-id="8d497-107">The action will copy:</span></span>

- <span data-ttu-id="8d497-108">Projekti atribuudid</span><span class="sxs-lookup"><span data-stu-id="8d497-108">Project properties</span></span>
- <span data-ttu-id="8d497-109">Tööjaotuse struktuur</span><span class="sxs-lookup"><span data-stu-id="8d497-109">The Work breakdown structure</span></span>
- <span data-ttu-id="8d497-110">Projektimeeskonna liikmed</span><span class="sxs-lookup"><span data-stu-id="8d497-110">Project team members</span></span>
- <span data-ttu-id="8d497-111">Projekti prognoosid</span><span class="sxs-lookup"><span data-stu-id="8d497-111">Project estimates</span></span>
- <span data-ttu-id="8d497-112">Projekti kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="8d497-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="8d497-113">Projekti atribuudid</span><span class="sxs-lookup"><span data-stu-id="8d497-113">Project properties</span></span>

<span data-ttu-id="8d497-114">Kui projekt on kopeeritud, kopeeritakse väärtused järgmistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="8d497-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="8d497-115">Nimetus</span><span class="sxs-lookup"><span data-stu-id="8d497-115">Name</span></span>
- <span data-ttu-id="8d497-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8d497-116">Description</span></span>
- <span data-ttu-id="8d497-117">Klient</span><span class="sxs-lookup"><span data-stu-id="8d497-117">Customer</span></span>
- <span data-ttu-id="8d497-118">Kalendri mall</span><span class="sxs-lookup"><span data-stu-id="8d497-118">Calendar Template</span></span>
- <span data-ttu-id="8d497-119">Valuuta</span><span class="sxs-lookup"><span data-stu-id="8d497-119">Currency</span></span>
- <span data-ttu-id="8d497-120">Lepingut sõlmiv üksus</span><span class="sxs-lookup"><span data-stu-id="8d497-120">Contracting Unit</span></span>
- <span data-ttu-id="8d497-121">Projektijuht</span><span class="sxs-lookup"><span data-stu-id="8d497-121">Project Manager</span></span>
- <span data-ttu-id="8d497-122">Olek</span><span class="sxs-lookup"><span data-stu-id="8d497-122">Status</span></span>
- <span data-ttu-id="8d497-123">Üldine projekti olek</span><span class="sxs-lookup"><span data-stu-id="8d497-123">Overall Project Status</span></span>
- <span data-ttu-id="8d497-124">Kommentaarid</span><span class="sxs-lookup"><span data-stu-id="8d497-124">Comments</span></span>
- <span data-ttu-id="8d497-125">Prognoosid</span><span class="sxs-lookup"><span data-stu-id="8d497-125">Estimates</span></span>
- <span data-ttu-id="8d497-126">Eeldatav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8d497-126">Estimated Start Date</span></span>
- <span data-ttu-id="8d497-127">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="8d497-127">Finish Date</span></span>
- <span data-ttu-id="8d497-128">Tööpanus (tunnid)</span><span class="sxs-lookup"><span data-stu-id="8d497-128">Effort (Hours)</span></span>
- <span data-ttu-id="8d497-129">Eeldatav tööjõukulu</span><span class="sxs-lookup"><span data-stu-id="8d497-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="8d497-130">Eeldatav kulude maksumus</span><span class="sxs-lookup"><span data-stu-id="8d497-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="8d497-131">Tööjaotuse struktuur</span><span class="sxs-lookup"><span data-stu-id="8d497-131">Work breakdown structure</span></span>

<span data-ttu-id="8d497-132">Kui projekt on kopeeritud, siis kopeeritakse kogu ressursi laaditud tööjaotuse struktuur.</span><span class="sxs-lookup"><span data-stu-id="8d497-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="8d497-133">Nimetatud ressursid asendatakse üldiste ressurssidega.</span><span class="sxs-lookup"><span data-stu-id="8d497-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="8d497-134">Kui nimetatud ressurssidel ei ole üldise ressursiga sama tööaega, arvutatakse ajakava uuesti ja ülesande kestused võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="8d497-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="8d497-135">Projektimeeskonna liikmed</span><span class="sxs-lookup"><span data-stu-id="8d497-135">Project team members</span></span>

<span data-ttu-id="8d497-136">Kui projektimeeskond kopeeritakse lähteprojektist, kopeeritakse üldised ressursid.</span><span class="sxs-lookup"><span data-stu-id="8d497-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="8d497-137">Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid lähteprojektis.</span><span class="sxs-lookup"><span data-stu-id="8d497-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="8d497-138">Nimetatud ressursid teisendatakse üldisteks meeskonnaliikmeteks.</span><span class="sxs-lookup"><span data-stu-id="8d497-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="8d497-139">Prognoosid</span><span class="sxs-lookup"><span data-stu-id="8d497-139">Estimates</span></span>

<span data-ttu-id="8d497-140">Kui projekt on kopeeritud, kopeeritakse lähteprojektist nii ressursi kui ka kulu prognoosiread.</span><span class="sxs-lookup"><span data-stu-id="8d497-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="8d497-141">Lisateavet programmiliselt valikule Kopeeri projekt juurdepääsemise kohta leiate teemast [Projektimallide väljatöötamine toiminguga Kopeeri projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="8d497-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
