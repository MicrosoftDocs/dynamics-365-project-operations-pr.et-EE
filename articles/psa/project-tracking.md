---
title: Projekti edenemine ja kulu tarbimine
description: Selles teemas kirjeldatakse projekti edenemise ja tarbitud kulude jälgimist.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283633"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="ae126-103">Projekti edenemine ja kulu tarbimine</span><span class="sxs-lookup"><span data-stu-id="ae126-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ae126-104">Vajadus edenemise jälgimiseks ajakava suhtes sõltub majandusharust.</span><span class="sxs-lookup"><span data-stu-id="ae126-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="ae126-105">Mõned majandusharud jälgivad minimaalsel tasandil, samas kui teised jälgivad kõrgemal tasemel.</span><span class="sxs-lookup"><span data-stu-id="ae126-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="ae126-106">Selles teemas kirjeldatakse, kuidas kasutada ajakava oma organisatsiooni vajadustele vastavalt.</span><span class="sxs-lookup"><span data-stu-id="ae126-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="ae126-107">Panuse jälgimise vaade</span><span class="sxs-lookup"><span data-stu-id="ae126-107">Effort tracking view</span></span>

<span data-ttu-id="ae126-108">Vaade **Panuse jälgimine** jälgib ajakavas ülesannete edenemist.</span><span class="sxs-lookup"><span data-stu-id="ae126-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="ae126-109">See võrdleb tegelikult ülesande peale kulutatud panusetunde ülesandele plaanitud kulutatud tundidega.</span><span class="sxs-lookup"><span data-stu-id="ae126-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="ae126-110">Rakendus Project Service Automation kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.</span><span class="sxs-lookup"><span data-stu-id="ae126-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="ae126-111">Algselt ülesande loomisel: planeeritud kulu määrakse lõpetamisel prognoositud kulule.</span><span class="sxs-lookup"><span data-stu-id="ae126-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="ae126-112">Kui ülesande jaoks salvestatakse tegelikud näitajad, arvutatakse koormuse jälrgimise vaade järgnevalt</span><span class="sxs-lookup"><span data-stu-id="ae126-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="ae126-113">Edenemisprotsent = seni tehtud tegelik panus ÷ hinnang lõpetamisel (EAC)</span><span class="sxs-lookup"><span data-stu-id="ae126-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="ae126-114">Lõpetamise prognoos (ETC) = hinnang lõpetamisel (EAC) – seni tehtud tegelik panus</span><span class="sxs-lookup"><span data-stu-id="ae126-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="ae126-115">EAC = ülejäänud panus + seni tehtud tegelik panus</span><span class="sxs-lookup"><span data-stu-id="ae126-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="ae126-116">Eeldatav panuse hälve = plaanitud panus – EAC</span><span class="sxs-lookup"><span data-stu-id="ae126-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="ae126-117">Rakendus Project Service Automation näitab ülesande eeldatavat panuse hälvet.</span><span class="sxs-lookup"><span data-stu-id="ae126-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="ae126-118">Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega.</span><span class="sxs-lookup"><span data-stu-id="ae126-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="ae126-119">Seega on see graafikust maas.</span><span class="sxs-lookup"><span data-stu-id="ae126-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="ae126-120">Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega.</span><span class="sxs-lookup"><span data-stu-id="ae126-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="ae126-121">Seega on see graafikust ees.</span><span class="sxs-lookup"><span data-stu-id="ae126-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="ae126-122">Panuse ümberkavandamine</span><span class="sxs-lookup"><span data-stu-id="ae126-122">Reprojecting effort</span></span>

<span data-ttu-id="ae126-123">On tavaline, et projektijuht vaatab ülesande esialgsed prognoosid üle.</span><span class="sxs-lookup"><span data-stu-id="ae126-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="ae126-124">Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut.</span><span class="sxs-lookup"><span data-stu-id="ae126-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="ae126-125">Kuid me ei soovita projektijuhtidel muuta alusnumbreid, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.</span><span class="sxs-lookup"><span data-stu-id="ae126-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="ae126-126">Projektijuht saab ülesannete panust ümber kavandada kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="ae126-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="ae126-127">Alistada vaikimisi ETC ülesande tegeliku järelejäänud panuse uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="ae126-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="ae126-128">Alistada vaikimisi edenemisprotsent ülesande tegeliku edenemise uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="ae126-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="ae126-129">Kõik need lähenemised põhjustavad ülesande ETC, EAC ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist.</span><span class="sxs-lookup"><span data-stu-id="ae126-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="ae126-130">Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.</span><span class="sxs-lookup"><span data-stu-id="ae126-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="ae126-131">Kokkuvõtlike ülesannete panuse ümberkavandamine</span><span class="sxs-lookup"><span data-stu-id="ae126-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="ae126-132">Kokkuvõtvate või konteinerülesannete panust saab ümber kavandada.</span><span class="sxs-lookup"><span data-stu-id="ae126-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="ae126-133">Sõltumata sellest, kas kasutaja kavandab ümber järelejäänud panust või kokkuvõtlike ülesannete edenemisprotsenti kasutades, algab järgmine arvutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="ae126-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="ae126-134">Arvutatakse ülesande EAC, ETC ja edenemisprotsent.</span><span class="sxs-lookup"><span data-stu-id="ae126-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="ae126-135">Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui oli ülesande esialgne EAC.</span><span class="sxs-lookup"><span data-stu-id="ae126-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="ae126-136">Iga individuaalse ülesande puhul arvutatakse uus EAC kuni lehesõlme ülesannete tasemeni.</span><span class="sxs-lookup"><span data-stu-id="ae126-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="ae126-137">Mõjutatud alamülesannete jaoks (kuni lehesõlme tasemeni) arvutatakse EAC väärtuse põhjal ümber nende ETC ja edenemisprotsent.</span><span class="sxs-lookup"><span data-stu-id="ae126-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="ae126-138">Selle tulemuseks on ülesande panuse hälbe uus prognoos.</span><span class="sxs-lookup"><span data-stu-id="ae126-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="ae126-139">Kokkuvõtlike ülesannete EAC-d arvutatakse ümber juursõlme tasemeni.</span><span class="sxs-lookup"><span data-stu-id="ae126-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="ae126-140">Kulude jälgimise vaade</span><span class="sxs-lookup"><span data-stu-id="ae126-140">Cost tracking view</span></span> 

<span data-ttu-id="ae126-141">Vaates **Kulude jälgimine** võrreldakse ülesandele kulutatud tegelikku kulu plaanitud kuluga.</span><span class="sxs-lookup"><span data-stu-id="ae126-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="ae126-142">See vaade kuvab ainult tööjõukulud ja ei sisalda kuluhinnangute kulusid.</span><span class="sxs-lookup"><span data-stu-id="ae126-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="ae126-143">Rakendus Project Service Automation kasutab jälgimismõõdikute arvutamiseks järgmisi valemeid.</span><span class="sxs-lookup"><span data-stu-id="ae126-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="ae126-144">Ülesande loomisel on planeeritud kulu võrdne lõpetamisel prognoositud kuluga.</span><span class="sxs-lookup"><span data-stu-id="ae126-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="ae126-145">Kui ülesande jaoks on tegelikud näitajad salvestatud, arvutatakse kulu jaoks vaates **Jälgimine** järgnev:</span><span class="sxs-lookup"><span data-stu-id="ae126-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="ae126-146">Tarbitud kulu protsent = senini kulutatud tegelik kulu ÷ ülesande lõpetamisel prognoositud kulu</span><span class="sxs-lookup"><span data-stu-id="ae126-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="ae126-147">Lõpetamise kulu (CTC) = lõpetamisel prognoositud kulu – seni kulutatud tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ae126-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="ae126-148">Lõpetamisel prognoositud kulu = CTC + seni kulutatud tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ae126-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="ae126-149">Eeldatav kuluhälve = plaanitud kulu – lõpetamisel prognoositud kulu</span><span class="sxs-lookup"><span data-stu-id="ae126-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="ae126-150">Ülesandes on kuvatud kuluhälbe projektsioon.</span><span class="sxs-lookup"><span data-stu-id="ae126-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="ae126-151">Kui lõpetamisel prognoositud kulu on plaanitud kulust suurem, siis eeldatakse, et ülesanne on algselt plaanitust kulukam.</span><span class="sxs-lookup"><span data-stu-id="ae126-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="ae126-152">Seega on suundumuseks eelarve ületamine.</span><span class="sxs-lookup"><span data-stu-id="ae126-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="ae126-153">Kui lõpetamisel prognoositud kulu on plaanitud kulust väiksem, siis eeldatakse, et ülesanne on algselt plaanitust odavam ja suundumuseks on eelarve ülejääk.</span><span class="sxs-lookup"><span data-stu-id="ae126-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="ae126-154">Projektijuhi kulude ümberkavandamine</span><span class="sxs-lookup"><span data-stu-id="ae126-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="ae126-155">Kui panus kavandatakse ümber, arvutatakse CTC, lõpetamisel prognoositud kulu, tarbitud kulu protsent ja eeldatav kuluhälve kõik vaates **Kulude jälgimine** ümber.</span><span class="sxs-lookup"><span data-stu-id="ae126-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="ae126-156">Projekti oleku kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="ae126-156">Project status summary</span></span>

<span data-ttu-id="ae126-157">Andmete jälitamine vaadetes **Panuse jälgimine** ja **Kulude jälgimine** kuvab edenemise ja tarbitud kulud projekti juursõlme, kokkuvõtlike ülesannete ja lehesõlme tasemetel.</span><span class="sxs-lookup"><span data-stu-id="ae126-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="ae126-158">Lehe **Projektiolem** jaotises **Olek** kuvatakse projektitaseme oleku kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="ae126-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="ae126-159">Oleku kokkuvõtte väljad</span><span class="sxs-lookup"><span data-stu-id="ae126-159">Status summary fields</span></span>

<span data-ttu-id="ae126-160">Väli **Üldine projekti olek** on redigeeritav väli, mis kuvab projekti üldise oleku.</span><span class="sxs-lookup"><span data-stu-id="ae126-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="ae126-161">See kasutab kasvavale ohule viitamiseks värvkodeerimist (nt roheline, kollane ja punane).</span><span class="sxs-lookup"><span data-stu-id="ae126-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="ae126-162">Väli **Kommentaarid** võimaldab projektijuhil sisestada oleku kohta konkreetseid märkuseid.</span><span class="sxs-lookup"><span data-stu-id="ae126-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="ae126-163">Väli **Olekut värskendatud** pole redigeeritav ja väärtus on ajatempel, mis näitab, millal olekut viimati värskendati.</span><span class="sxs-lookup"><span data-stu-id="ae126-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="ae126-164">Väljad **Ajakava täitmine** ja **Kulude täitmine** määratakse jälgimise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="ae126-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="ae126-165">Kui vaates **Panuse jälgimine** on juursõlme ajakava ja kuluhälve positiivsed, saate need väljad määrata väärtusele **Ees**.</span><span class="sxs-lookup"><span data-stu-id="ae126-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="ae126-166">Kui juursõlme ajakava ja kuluhälve on negatiivsed, saate need määrata väärtusele **Taga**.</span><span class="sxs-lookup"><span data-stu-id="ae126-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]