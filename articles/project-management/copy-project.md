---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091249"
---
# <a name="copy-a-project"></a><span data-ttu-id="a87dd-103">Projekti kopeerimine</span><span class="sxs-lookup"><span data-stu-id="a87dd-103">Copy a project</span></span>

<span data-ttu-id="a87dd-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="a87dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a87dd-105">Dynamics 365 Project Operationsi abil saate kiiresti uusi projekte koostada, valides **Kopeeri projekt** vormil **Projektid**.</span><span class="sxs-lookup"><span data-stu-id="a87dd-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="a87dd-106">Projekti kopeerimiseks avage projekt, mida soovite kopeerida, ja seejärel valige toiming **Kopeeri projekt**.</span><span class="sxs-lookup"><span data-stu-id="a87dd-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="a87dd-107">Toiminguga kopeeritakse järgnev.</span><span class="sxs-lookup"><span data-stu-id="a87dd-107">The action will copy the following:</span></span>

- <span data-ttu-id="a87dd-108">Projekti atribuudid</span><span class="sxs-lookup"><span data-stu-id="a87dd-108">Project properties</span></span> 
- <span data-ttu-id="a87dd-109">Tööjaotuse struktuur</span><span class="sxs-lookup"><span data-stu-id="a87dd-109">Work breakdown structure</span></span>
- <span data-ttu-id="a87dd-110">Projektimeeskonna liikmed</span><span class="sxs-lookup"><span data-stu-id="a87dd-110">Project team members</span></span>
- <span data-ttu-id="a87dd-111">Projekti prognoosid</span><span class="sxs-lookup"><span data-stu-id="a87dd-111">Project estimates</span></span>
- <span data-ttu-id="a87dd-112">Projekti kuluprognoosid</span><span class="sxs-lookup"><span data-stu-id="a87dd-112">Project expense estimates</span></span>
- <span data-ttu-id="a87dd-113">Projektimaterjali prognoosid</span><span class="sxs-lookup"><span data-stu-id="a87dd-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="a87dd-114">Projekti atribuudid</span><span class="sxs-lookup"><span data-stu-id="a87dd-114">Project properties</span></span>

<span data-ttu-id="a87dd-115">Kui projekt on kopeeritud, kopeeritakse väärtused järgmistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="a87dd-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="a87dd-116">Nimetus</span><span class="sxs-lookup"><span data-stu-id="a87dd-116">Name</span></span>
- <span data-ttu-id="a87dd-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a87dd-117">Description</span></span>
- <span data-ttu-id="a87dd-118">Klient</span><span class="sxs-lookup"><span data-stu-id="a87dd-118">Customer</span></span>
- <span data-ttu-id="a87dd-119">Kalendri mall</span><span class="sxs-lookup"><span data-stu-id="a87dd-119">Calendar Template</span></span>
- <span data-ttu-id="a87dd-120">Valuuta</span><span class="sxs-lookup"><span data-stu-id="a87dd-120">Currency</span></span>
- <span data-ttu-id="a87dd-121">Lepingut sõlmiv üksus</span><span class="sxs-lookup"><span data-stu-id="a87dd-121">Contracting Unit</span></span>
- <span data-ttu-id="a87dd-122">Projektijuht</span><span class="sxs-lookup"><span data-stu-id="a87dd-122">Project Manager</span></span>
- <span data-ttu-id="a87dd-123">Olek</span><span class="sxs-lookup"><span data-stu-id="a87dd-123">Status</span></span>
- <span data-ttu-id="a87dd-124">Üldine projekti olek</span><span class="sxs-lookup"><span data-stu-id="a87dd-124">Overall Project Status</span></span>
- <span data-ttu-id="a87dd-125">Kommentaarid</span><span class="sxs-lookup"><span data-stu-id="a87dd-125">Comments</span></span>
- <span data-ttu-id="a87dd-126">Prognoosid</span><span class="sxs-lookup"><span data-stu-id="a87dd-126">Estimates</span></span>
- <span data-ttu-id="a87dd-127">Eeldatav alguskuupäev: see on kuupäev, millal projekt koopiast luuakse.</span><span class="sxs-lookup"><span data-stu-id="a87dd-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="a87dd-128">Eeldatav lõpukuupäev: seda kuupäeva muudetakse koopiast loodud uue projekti alguskuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="a87dd-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="a87dd-129">Tööpanus (tunnid)</span><span class="sxs-lookup"><span data-stu-id="a87dd-129">Effort (Hours)</span></span>
- <span data-ttu-id="a87dd-130">Eeldatav tööjõukulu</span><span class="sxs-lookup"><span data-stu-id="a87dd-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="a87dd-131">Eeldatav kulude maksumus</span><span class="sxs-lookup"><span data-stu-id="a87dd-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="a87dd-132">Eeldatav materjalikulu</span><span class="sxs-lookup"><span data-stu-id="a87dd-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="a87dd-133">Projekti kopeerimine on pikaaegne toiming.</span><span class="sxs-lookup"><span data-stu-id="a87dd-133">Copy project is a long running operation.</span></span> <span data-ttu-id="a87dd-134">Kopeeritakse ka projektikirjed, nende vastavad atribuudid ja paljud seostuvad olemid.</span><span class="sxs-lookup"><span data-stu-id="a87dd-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="a87dd-135">Toimingu pikaajalise loomuse tõttu on pärast koopia käivitamist sihtprojekti leht redigeerimiseks lukus, kuni kopeerimistoiming on lõpule jõudnud.</span><span class="sxs-lookup"><span data-stu-id="a87dd-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="a87dd-136">Tööjaotuse struktuur</span><span class="sxs-lookup"><span data-stu-id="a87dd-136">Work breakdown structure</span></span>

<span data-ttu-id="a87dd-137">Kui projekt on kopeeritud, siis kopeeritakse kogu ressursi laaditud tööjaotuse struktuur.</span><span class="sxs-lookup"><span data-stu-id="a87dd-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="a87dd-138">Nimetatud ressursid asendatakse üldiste ressurssidega.</span><span class="sxs-lookup"><span data-stu-id="a87dd-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="a87dd-139">Kui nimetatud ressurssidel ei ole üldise ressursiga sama tööaega, arvutatakse ajakava uuesti ja ülesande kestused võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="a87dd-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="a87dd-140">Projektimeeskonna liikmed</span><span class="sxs-lookup"><span data-stu-id="a87dd-140">Project team members</span></span>

<span data-ttu-id="a87dd-141">Kui projektimeeskond kopeeritakse lähteprojektist, kopeeritakse üldised ressursid.</span><span class="sxs-lookup"><span data-stu-id="a87dd-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="a87dd-142">Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid lähteprojektis.</span><span class="sxs-lookup"><span data-stu-id="a87dd-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="a87dd-143">Nimetatud ressursid teisendatakse üldisteks meeskonnaliikmeteks.</span><span class="sxs-lookup"><span data-stu-id="a87dd-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="a87dd-144">Prognoosid</span><span class="sxs-lookup"><span data-stu-id="a87dd-144">Estimates</span></span>

<span data-ttu-id="a87dd-145">Kui projekt on kopeeritud, kopeeritakse ressursi, kulu ja materjali prognoosi read lähteprojektist.</span><span class="sxs-lookup"><span data-stu-id="a87dd-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="a87dd-146">Lisateavet programmiliselt valikule Kopeeri projekt juurdepääsemise kohta leiate teemast [Projektimallide väljatöötamine toiminguga Kopeeri projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="a87dd-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
