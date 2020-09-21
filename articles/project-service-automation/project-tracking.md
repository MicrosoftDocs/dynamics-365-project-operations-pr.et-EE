---
title: Projekti edenemine ja tarbitud kulud
description: Selles teemas kirjeldatakse, kuidas jälgida projekti edenemist ja tarbitud kulusid.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751023"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="6c0d0-103">Projekti edenemine ja tarbitud kulud</span><span class="sxs-lookup"><span data-stu-id="6c0d0-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6c0d0-104">Vajadus edenemise jälgimiseks ajakava suhtes sõltub majandusharust.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="6c0d0-105">Mõned majandusharud jälgivad minimaalsel tasandil, samas kui teised jälgivad kõrgemal tasemel.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="6c0d0-106">Selles teemas kirjeldatakse, kuidas kasutada ajakava oma organisatsiooni vajadustele vastavalt.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="6c0d0-107">Panuse jälgimise vaade</span><span class="sxs-lookup"><span data-stu-id="6c0d0-107">Effort tracking view</span></span>

<span data-ttu-id="6c0d0-108">Vaade **Panuse jälgimine** jälgib ajakavas ülesannete edenemist.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="6c0d0-109">See võrdleb ülesandele tegelikult kulutatud panusetunde ülesandele plaanitud panusetundidega.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="6c0d0-110">Rakendus PSA kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="6c0d0-111">Edenemisprotsent = tegelik panus senini ÷ ülesandele plaanitud panus</span><span class="sxs-lookup"><span data-stu-id="6c0d0-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="6c0d0-112">Lõpetamise prognoos (ETC) = plaanitud panus – seni tehtud tegelik panus</span><span class="sxs-lookup"><span data-stu-id="6c0d0-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="6c0d0-113">Hinnang lõpetamisel (EAC) = ülejäänud panus + seni tehtud tegelik panus</span><span class="sxs-lookup"><span data-stu-id="6c0d0-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="6c0d0-114">Eeldatav panuse hälve = plaanitud panus – EAC</span><span class="sxs-lookup"><span data-stu-id="6c0d0-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="6c0d0-115">Rakendus PSA näitab ülesande eeldatavat panuse hälvet.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="6c0d0-116">Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="6c0d0-117">Seega on see graafikust maas.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="6c0d0-118">Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="6c0d0-119">Seega on see graafikust ees.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="6c0d0-120">Panuse ümberkavandamine</span><span class="sxs-lookup"><span data-stu-id="6c0d0-120">Re-projecting effort</span></span>

<span data-ttu-id="6c0d0-121">On tavaline, et projektijuht vaatab ülesande esialgsed prognoosid üle.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="6c0d0-122">Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="6c0d0-123">Kuid me ei soovita projektijuhtidel muuta alusnumbreid, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="6c0d0-124">Projektijuht saab ülesannete panust ümber kavandada kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="6c0d0-125">Alistada vaikimisi ETC ülesande tegeliku järelejäänud panuse uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="6c0d0-126">Alistada vaikimisi edenemisprotsent ülesande tegeliku edenemise uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="6c0d0-127">Kõik need lähenemised põhjustavad ülesande ETC, EAC ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="6c0d0-128">Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="6c0d0-129">Kokkuvõtlike ülesannete panuse ümberkavandamine</span><span class="sxs-lookup"><span data-stu-id="6c0d0-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="6c0d0-130">Kokkuvõtvate või konteinerülesannete panust saab ümber kavandada.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="6c0d0-131">Sõltumata sellest, kas kasutaja kavandab ümber järelejäänud panust või kokkuvõtlike ülesannete edenemisprotsenti kasutades, algab järgmine arvutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="6c0d0-132">Arvutatakse ülesande EAC, ETC ja edenemisprotsent.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="6c0d0-133">Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui oli ülesande esialgne EAC.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="6c0d0-134">Iga individuaalse ülesande puhul arvutatakse uus EAC kuni lehesõlme ülesannete tasemeni.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="6c0d0-135">Mõjutatud alamülesannete jaoks (kuni lehesõlme tasemeni) arvutatakse EAC väärtuse põhjal ümber nende ETC ja edenemisprotsent.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="6c0d0-136">Selle tulemuseks on ülesande panuse hälbe uus prognoos.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="6c0d0-137">Kokkuvõtlike ülesannete EAC-d arvutatakse ümber juursõlme tasemeni.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="6c0d0-138">Kulude jälgimise vaade</span><span class="sxs-lookup"><span data-stu-id="6c0d0-138">Cost tracking view</span></span> 

<span data-ttu-id="6c0d0-139">Vaates **Kulude jälgimine** võrreldakse ülesandele kulutatud tegelikku kulu ülesandele plaanitud kuluga.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="6c0d0-140">See vaade kuvab ainult tööjõukulud ja ei sisalda kuluhinnangute kulusid.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="6c0d0-141">Rakendus PSA kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="6c0d0-142">Tarbitud kulu protsent = senini kulutatud tegelik kulu ÷ ülesandele plaanitud kulu</span><span class="sxs-lookup"><span data-stu-id="6c0d0-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="6c0d0-143">Lõpetamise kulu (CTC) = plaanitud kulu – seni kulutatud tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="6c0d0-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="6c0d0-144">EAC = CTC + seni kulutatud tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="6c0d0-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="6c0d0-145">Eeldatav kuluhälve = plaanitud kulu – EAC</span><span class="sxs-lookup"><span data-stu-id="6c0d0-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="6c0d0-146">Ülesandes on kuvatud kuluhälbe projektsioon.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="6c0d0-147">Kui EAC on plaanitud kulust suurem, siis eeldatakse, et ülesanne on algselt plaanitust kulukam.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="6c0d0-148">Seega on suundumuseks eelarve ületamine.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="6c0d0-149">Kui EAC on plaanitud kulust väiksem, siis eeldatakse, et ülesanne on algselt plaanitust odavam.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="6c0d0-150">Seega on suundumuseks eelarve ülejääk.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="6c0d0-151">Projektijuhi tehtud kulude ümberkavandamine</span><span class="sxs-lookup"><span data-stu-id="6c0d0-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="6c0d0-152">Kui panus kavandatakse ümber, arvutatakse CTC, EAC, tarbitud kulu protsent ja eeldatav kuluhälve kõik vaates **Kulude jälgimine** ümber.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="6c0d0-153">Projekti oleku kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="6c0d0-153">Project status summary</span></span>

<span data-ttu-id="6c0d0-154">Andmete jälitamine vaadetes **Panuse jälgimine** ja **Kulude jälgimine** kuvab edenemise ja tarbitud kulud projekti juursõlme, kokkuvõtlike ülesannete ja lehesõlme tasemetel.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="6c0d0-155">Lehe **Projektiolem** jaotises **Olek** kuvatakse projektitaseme oleku kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="6c0d0-156">Oleku kokkuvõtte väljad</span><span class="sxs-lookup"><span data-stu-id="6c0d0-156">Status summary fields</span></span>

<span data-ttu-id="6c0d0-157">Väli **Üldine projekti olek** on redigeeritav väli, mis kuvab projekti üldise oleku.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="6c0d0-158">See kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane).</span><span class="sxs-lookup"><span data-stu-id="6c0d0-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="6c0d0-159">Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="6c0d0-160">Väli **Olekut värskendatud** pole redigeeritav ja väärtus on ajatempel, mis näitab, millal olekut viimati värskendati.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="6c0d0-161">Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="6c0d0-162">Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, saate need väljad määrata väärtusele **Ees**.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="6c0d0-163">Kui juursõlme ajakava ja kuluhälve on negatiivsed, saate need määrata väärtusele **Taga**.</span><span class="sxs-lookup"><span data-stu-id="6c0d0-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
