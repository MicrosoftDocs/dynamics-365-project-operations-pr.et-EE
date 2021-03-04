---
title: Kuidas ressursse rakenduse versioonis 2.x esialgselt reserveerida?
description: Selles artiklis kirjeldatakse, kuidas Project Service’iga projektimeeskonna liikmeid esialgselt reserveerida.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6bd13c448f4ce16fb93843df54f26cdd9bb884f4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146478"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="383b4-103">Kuidas ressursse veebirakenduses (Project Service'i rakendus v2.x) esialgselt reserveerida?</span><span class="sxs-lookup"><span data-stu-id="383b4-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="383b4-104">Saate ressurssi esialgselt projektimeeskonda reserveerida, andmaks teada, et planeerite ressursi projekti määrata.</span><span class="sxs-lookup"><span data-stu-id="383b4-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="383b4-105">Esialgselt reserveerimised ei lisa ressursile koormust.</span><span class="sxs-lookup"><span data-stu-id="383b4-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="383b4-106">Esialgselt reserveeritud meeskonnaliikmetele pole võimalik projekti ülesandeid määrata.</span><span class="sxs-lookup"><span data-stu-id="383b4-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="383b4-107">Ülesandeid saab määrata ainult sellistele ressurssidele, kellel on olek Fikseeritult reserveeritud ja kinnitamise tüüp Kinnitatud (eeldusel, et neil on ülesande täitmiseks piisavalt fikseeritult reserveeritud tunde).</span><span class="sxs-lookup"><span data-stu-id="383b4-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="383b4-108">Esialgselt reserveeritud meeskonnaliikmed kuvatakse ruudustikus Meeskonnaliige koos nende esialgselt reserveeritud tundidega veerus Esialgselt reserveerimine.</span><span class="sxs-lookup"><span data-stu-id="383b4-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="383b4-109">Nad kuvatakse ka ajakavapaneelil.</span><span class="sxs-lookup"><span data-stu-id="383b4-109">They also show up on the schedule board.</span></span> <span data-ttu-id="383b4-110">Need ei lisa ressursile koormust, kuna esialgselt reserveerimine ei lisa ressursile koormust.</span><span class="sxs-lookup"><span data-stu-id="383b4-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="383b4-111">Rakenduse Project Service versiooniga 2.x on meeskonnaliikme esialgseks projekti reserveerimiseks kolm võimalust.</span><span class="sxs-lookup"><span data-stu-id="383b4-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="383b4-112">Saate esialgselt reserveerida ajakavapaneelil, funktsiooniga Reserveeringute haldamine või üldise ressursi loomisega.</span><span class="sxs-lookup"><span data-stu-id="383b4-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="383b4-113">Neid meetodeid on kirjeldatud allpool.</span><span class="sxs-lookup"><span data-stu-id="383b4-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="383b4-114">Esialgselt reserveerimine ajakavapaneelil</span><span class="sxs-lookup"><span data-stu-id="383b4-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="383b4-115">Tehke ajakavapaneelil ressursi esialgselt reserveerimiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="383b4-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="383b4-116">Avage ajakavapaneel.</span><span class="sxs-lookup"><span data-stu-id="383b4-116">Open the schedule board.</span></span>
2. <span data-ttu-id="383b4-117">Valige ajakavapaneeli alumise paneeli Broneeringu nõuded vahekaart Projekt.</span><span class="sxs-lookup"><span data-stu-id="383b4-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="383b4-118">Leidke projekt, kuhu soovite ressursi esialgselt reserveerida.</span><span class="sxs-lookup"><span data-stu-id="383b4-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="383b4-119">Kui teil on mitu projekti, klõpsake veeru Projekt päist ja kasutage projekti otsimiseks filtreerimistööriista.</span><span class="sxs-lookup"><span data-stu-id="383b4-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="383b4-120">Klõpsake projekti ja lohistage see ressursi ajaruudustikku.</span><span class="sxs-lookup"><span data-stu-id="383b4-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="383b4-121">See avab paremal paneeli Ressursi broneeringu loomine.</span><span class="sxs-lookup"><span data-stu-id="383b4-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="383b4-122">Täpsustage algus- ja lõppkuupäeva, valige broneeringu olekuks Esialgne ja määrake tunnid.</span><span class="sxs-lookup"><span data-stu-id="383b4-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="383b4-123">Klõpsake valikut Broneeri.</span><span class="sxs-lookup"><span data-stu-id="383b4-123">Click Book.</span></span>
7. <span data-ttu-id="383b4-124">Projekti naastes kuvatakse ressurss veerus Esialgselt reserveerimine meeskonnaliikmena koos esialgselt reserveeritud tundidega.</span><span class="sxs-lookup"><span data-stu-id="383b4-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="383b4-125">Pange tähele, et te ei saa neile tööjaotuse struktuuris (WBS) ülesandeid määrata, kuna selleks peaks ressurss olema kindlalt reserveeritud.</span><span class="sxs-lookup"><span data-stu-id="383b4-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="383b4-126">Esialgselt reserveerimine funktsiooniga Reserveeringute haldamine</span><span class="sxs-lookup"><span data-stu-id="383b4-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="383b4-127">Tehke funktsiooniga Reserveeringute haldamine esialgselt reserveerimiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="383b4-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="383b4-128">Klõpsake meeskonnaliikme ruudustikus käsku Uus.</span><span class="sxs-lookup"><span data-stu-id="383b4-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="383b4-129">Valige reserveeritav ressurss, roll, algus-/lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="383b4-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="383b4-130">Valige mis tahes eraldusmeetod peale valiku Puudub.</span><span class="sxs-lookup"><span data-stu-id="383b4-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="383b4-131">Täiskoormus</span><span class="sxs-lookup"><span data-stu-id="383b4-131">Full Capacity</span></span>
- <span data-ttu-id="383b4-132">Osakoormus</span><span class="sxs-lookup"><span data-stu-id="383b4-132">Percentage Capacity</span></span>
- <span data-ttu-id="383b4-133">Jaga ühtlaselt tundide järgi</span><span class="sxs-lookup"><span data-stu-id="383b4-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="383b4-134">Jaga eesmine koormus tundide järgi</span><span class="sxs-lookup"><span data-stu-id="383b4-134">By Hours Front Load</span></span>
4. <span data-ttu-id="383b4-135">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="383b4-135">Click Save.</span></span> <span data-ttu-id="383b4-136">Näete ressurssi meeskonnaruudustikus ja tunde olekuga Fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="383b4-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="383b4-137">Klõpsake ressursi reserveerimiste haldamiseks valikut Reserveeringute haldamine.</span><span class="sxs-lookup"><span data-stu-id="383b4-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="383b4-138">Kui ajakavapaneel avatakse, laiendage ressurssi ressursi reserveerimiste vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="383b4-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="383b4-139">Reserveerimine kuvatakse olekuga Fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="383b4-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="383b4-140">Paremklõpsake reserveerimist ja valige jaotises Oleku muutmine Esialgselt reserveerimine ja seejärel Esialgne.</span><span class="sxs-lookup"><span data-stu-id="383b4-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="383b4-141">Nüüd on broneeringu olek Esialgne.</span><span class="sxs-lookup"><span data-stu-id="383b4-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="383b4-142">Pärast ajakavapaneeli sulgemist näete, et ressursi tunnid meeskonnaliikme ruudustikus on muudetud olekust Fikseeritud olekusse Esialgne.</span><span class="sxs-lookup"><span data-stu-id="383b4-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="383b4-143">Pange tähele, et kui reserveerite ressursi meeskonda ja määrate talle WBS-is ülesandeid, eemaldatakse ressursile määratud ülesanded reserveeringute haldamises tehtud kindlast esialgseks muutmise järel, kuna ülesandeid saab määrata ainult kindalt reserveeritud ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="383b4-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="383b4-144">Esialgselt reserveerimine üldise ressursi loomisega</span><span class="sxs-lookup"><span data-stu-id="383b4-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="383b4-145">Saate luua esialgse reserveerimise, kui loote üldise ressursi meeskonnaliikme, täidate ajakavapaneeli või ressursitaotluse ja muudate reserveerimisel tüüpi.</span><span class="sxs-lookup"><span data-stu-id="383b4-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="383b4-146">Seda saate teha järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="383b4-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="383b4-147">Määrake rollidele, millele soovite üldiseid meeskonnaliikmeid luua, ülesanded projekti WBS-is.</span><span class="sxs-lookup"><span data-stu-id="383b4-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="383b4-148">Klõpsake valikut Projektimeeskonna loomine.</span><span class="sxs-lookup"><span data-stu-id="383b4-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="383b4-149">Valige projekti meeskonnaliikme ruudustikus üldine ressurss ja klõpsake valikut Broneeri.</span><span class="sxs-lookup"><span data-stu-id="383b4-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="383b4-150">Valige ajakavapaneelil ressurss, mille soovite broneerida.</span><span class="sxs-lookup"><span data-stu-id="383b4-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="383b4-151">Muutke ajakavapaneeli paneelil Ressursi broneeringu loomine reserveerimise olekuks Esialgne.</span><span class="sxs-lookup"><span data-stu-id="383b4-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="383b4-152">Klõpsake valikut Broneeri või Broneeri ja välju.</span><span class="sxs-lookup"><span data-stu-id="383b4-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="383b4-153">Pärast ajakavapaneeli sulgemist näete, et valitud ressurss lisati koos esialgselt reserveerimise ja määratud tundidega meeskonda.</span><span class="sxs-lookup"><span data-stu-id="383b4-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="383b4-154">Samuti näete, et üldine ressurss jääb meeskonda, märkimaks, et esialgselt reserveeritud meeskonnaliikmele on ülesanded määratud.</span><span class="sxs-lookup"><span data-stu-id="383b4-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="383b4-155">Kui olete valmis esialgselt reserveeritud meeskonnaliikme ressursi kindlaks meeskonnaliikmeks määrama, et talle ülesandeid määrata, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="383b4-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="383b4-156">Valige ressurss ja klõpsake valikut Reserveeringute haldamine.</span><span class="sxs-lookup"><span data-stu-id="383b4-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="383b4-157">Kui ajakavapaneel avatakse, laiendage ressurssi ressursi reserveerimiste vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="383b4-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="383b4-158">Reserveerimine kuvatakse olekuga Esialgne.</span><span class="sxs-lookup"><span data-stu-id="383b4-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="383b4-159">Paremklõpsake reserveerimist ja valige jaotises Reserveeringute haldamine Fikseeritult reserveerimine ja seejärel Fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="383b4-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="383b4-160">Nüüd on broneeringu olek Fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="383b4-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="383b4-161">Pärast ajakavapaneeli sulgemist näete, et ressursi tunnid meeskonnaliikme ruudustikus on muudetud olekust Esialgne olekusse Fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="383b4-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="383b4-162">Nüüd saate ressursile ülesandeid määrata (eeldusel, et kindlalt reserveeritud tunnid ja ülesande täitmiseks kuluvad tunnid on omavahel kooskõlas).</span><span class="sxs-lookup"><span data-stu-id="383b4-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="383b4-163">Pange tähele, et kui järgisite üldise ressursi täitmiseks ülalpool 3. üksuses toodud toiminguid esialgselt reserveeritud ressursi muutmiseks kindlaks reserveerimiseks, siis eemaldatakse üldine meeskonnaliige meeskonnast.</span><span class="sxs-lookup"><span data-stu-id="383b4-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
