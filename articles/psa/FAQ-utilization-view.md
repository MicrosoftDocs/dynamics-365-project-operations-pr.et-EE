---
title: Arveldatava ressursikasutuse vaatamine
description: Selles teemas antakse teavet ressursi kasutamise vaate kohta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074978"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="a1b21-103">Arveldatava ressursikasutuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="a1b21-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="a1b21-104">Vaates **Kasutamise vaade** lehel **Project Service ressursi kasutamine** kuvatakse tasustatav kasutamine iga broneeritava ressursi kohta.</span><span class="sxs-lookup"><span data-stu-id="a1b21-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="a1b21-105">Vaade põhineb ajakavapaneelil, nii et leiate sellelt mitmeid sarnaseid funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a1b21-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Kasutusvaate kuvatõmmis](media/FAQ-utilization-1.png)
 

<span data-ttu-id="a1b21-107">Arveldatava kasutuse arvutamine toimib järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a1b21-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="a1b21-108">Arveldatav kasutus = (arveldatavad tegelikud tunnid) / (ressursi koormus)</span><span class="sxs-lookup"><span data-stu-id="a1b21-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="a1b21-109">Lahtrites on toodud vaate valitud perioodi (päevade, nädalate või kuude) arvutatud arveldatav kasutus.</span><span class="sxs-lookup"><span data-stu-id="a1b21-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="a1b21-110">Iga lahtri värvid näitavad ressursi arveldatavat kasutust võrreldes nende arveldatava kasutuse eesmärgiga.</span><span class="sxs-lookup"><span data-stu-id="a1b21-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="a1b21-111">Kasutuse eesmärgi saab seada kas ressursi vaikerollis või üksikressursis.</span><span class="sxs-lookup"><span data-stu-id="a1b21-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="a1b21-112">Arvutamisel vaadatakse kõigepealt üksikressurssi ja seejärel alles ressursi vaikerolli.</span><span class="sxs-lookup"><span data-stu-id="a1b21-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="a1b21-113">Ressursi sihi seadmine</span><span class="sxs-lookup"><span data-stu-id="a1b21-113">Set target on a resource</span></span>

1. <span data-ttu-id="a1b21-114">Avage **Ressursid** \> **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="a1b21-115">Seejärel valige kirje avamiseks ressurss.</span><span class="sxs-lookup"><span data-stu-id="a1b21-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="a1b21-116">Vahekaardil **Project Service** saate seada ressursi kasutamise eesmärgi.</span><span class="sxs-lookup"><span data-stu-id="a1b21-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Kuvatõmmis kasutuse eesmärgi seadmisest vahekaardil Project Service](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="a1b21-118">Kasutamise eesmärgi seadmine rollile</span><span class="sxs-lookup"><span data-stu-id="a1b21-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="a1b21-119">Avage **Ressursid** \> **Ressursirollid**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="a1b21-120">Valige roll ja avage kirje.</span><span class="sxs-lookup"><span data-stu-id="a1b21-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="a1b21-121">Seadke rollile kasutuse eesmärk.</span><span class="sxs-lookup"><span data-stu-id="a1b21-121">Set the target utilization for the role.</span></span>

> ![Kuvatõmmis kasutuse eesmärgi seadmisest ressursirollides](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="a1b21-123">Arveldatava ressursikasutuse arvutamine</span><span class="sxs-lookup"><span data-stu-id="a1b21-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="a1b21-124">Selleks et arvutada ressursi arveldatavat kasutust, peate täitma mõne eeltingimuse.</span><span class="sxs-lookup"><span data-stu-id="a1b21-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="a1b21-125">Üksikute ressursside vaikerolli seadmine</span><span class="sxs-lookup"><span data-stu-id="a1b21-125">Set default role for individual resource</span></span>

<span data-ttu-id="a1b21-126">Esiteks, tuleb üksikressursis või ressursirollides määrata kasutuse eesmärk.</span><span class="sxs-lookup"><span data-stu-id="a1b21-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="a1b21-127">Kui kasutate eesmärkide seadmiseks ressursirolle, peab igal üksikressursil olema vaikeroll.</span><span class="sxs-lookup"><span data-stu-id="a1b21-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="a1b21-128">Selle määramiseks avage **Ressursid** \> **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="a1b21-129">Valige ressurss, avage kirje ja seejärel valige vahekaart **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="a1b21-130">Veenduge, et **ressursi rolli** ruudustikus on ressursi jaoks üks roll ja **Vaikimisi** seatakse suvandi väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="a1b21-131">Ressursirolli arveldustüübi vahetamine</span><span class="sxs-lookup"><span data-stu-id="a1b21-131">Change billing type for resource role</span></span>

<span data-ttu-id="a1b21-132">Ressursirollidele peab olema määratud arveldustüübiks **Arveldatav**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="a1b21-133">Avage **Ressursid** \> **Ressursirollid**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="a1b21-134">Avage kirje, mida soovite värskendada ja määrake seejärel vaikearveldustüübiks **Arveldatav**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="a1b21-135">Ressursirollile töötundide määramine</span><span class="sxs-lookup"><span data-stu-id="a1b21-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="a1b21-136">Koormuse arvutamiseks peavad ressursil olema määratud töötunnid.</span><span class="sxs-lookup"><span data-stu-id="a1b21-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="a1b21-137">Avage **Ressursid** \> **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="a1b21-138">Valige kirje avamiseks ressurss ja seejärel valige **Kuva töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="a1b21-139">Saate ressursside loendit hulgivärskendada, kui rakendate vaatest **Ressursiloend** vaatest **töötundide malli**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="a1b21-140">Tasustatava tegeliku tööaja tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="a1b21-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="a1b21-141">Tegelikud arveldatavad tunnid pärinevad olemist **Tegelikud näitajad**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="a1b21-142">Arvutusse kaasatakse tegelikult näitajad arveldustüübiga **Arveldatav** ja seepärast peavad teie projektide tegelikud näitajad olema arveldatavad.</span><span class="sxs-lookup"><span data-stu-id="a1b21-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="a1b21-143">Kui te ei näe arveldatavat kasutust, kontrollige järgmist.</span><span class="sxs-lookup"><span data-stu-id="a1b21-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="a1b21-144">Ressursi koormuse jaoks on töötunnid määratud.</span><span class="sxs-lookup"><span data-stu-id="a1b21-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="a1b21-145">Ressursil on kas üksikult määratud kasutuse eesmärk või talle on määratud vaikeroll.</span><span class="sxs-lookup"><span data-stu-id="a1b21-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="a1b21-146">Rollile on määratud kasutuse eesmärk.</span><span class="sxs-lookup"><span data-stu-id="a1b21-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="a1b21-147">Tegelike näitajate arveldustüübiks on kasutusarvutuse tegemise ajavahemikul määratud **Arveldatav**.</span><span class="sxs-lookup"><span data-stu-id="a1b21-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="a1b21-148">Kui näete tegelikke näitajaid, millel on mõni muu arveldustüüp kui arveldatav, siis kontrollige järgmist.</span><span class="sxs-lookup"><span data-stu-id="a1b21-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="a1b21-149">Tegelikus näitajas kasutatud rollil on vaikearveldustüübiks seatud muu tüüp kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="a1b21-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="a1b21-150">Projekti varundav projekti lepingurea roll on määratud mittearveldatavaks.</span><span class="sxs-lookup"><span data-stu-id="a1b21-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="a1b21-151">Projektil pole seostatud lepingurida.</span><span class="sxs-lookup"><span data-stu-id="a1b21-151">The project does not have an associated contract line.</span></span>

