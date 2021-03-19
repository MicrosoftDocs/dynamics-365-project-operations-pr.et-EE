---
title: Kuidas määrata veebirakenduses ülesandele broneeritavat ressurssi
description: Ülevaade võimalustest, kuidas saate broneeritud ressursse määrata.
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
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286288"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="d5692-103">Kuidas määrata veebirakenduses (Project Service v2.x) ülesandele reserveeritavat ressurssi?</span><span class="sxs-lookup"><span data-stu-id="d5692-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d5692-104">Rakenduses Project Service on kaks võimalust ülesandele ressursi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d5692-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="d5692-105">Saate ressursi reserveerida meeskonnaliikmena ja seejärel selle ülesandele määrata.</span><span class="sxs-lookup"><span data-stu-id="d5692-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="d5692-106">Või saate ülesannetele rolli määramisega luua üldise meeskonnaliikme, luua meeskonna ja seejärel täita toetavad nõuded nimelise ressursiga.</span><span class="sxs-lookup"><span data-stu-id="d5692-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="d5692-107">Pange tähele, et kui soovite määrata reserveeritavat ressurssi ülesandele, peab reserveeritava ressursi meeskonnaliikmel olema piisavalt saadaval reserveeringuid.</span><span class="sxs-lookup"><span data-stu-id="d5692-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="d5692-108">Reserveeringu olek peab olema kinnitamise tüübiga Fikseeritult reserveerimine ja olekuga Kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="d5692-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="d5692-109">Kui ressursi jaoks pole piisavalt reserveeringuid, siis eemaldab rakendus Project Service ülesande ja kuvab järgmise tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="d5692-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="d5692-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project* (Ei saanud ressurssi ülesandele määrata – järgmistele ressurssidele pole projekti suhtes piisavalt tunde reserveeritud)</span><span class="sxs-lookup"><span data-stu-id="d5692-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="d5692-111">Ressursi reserveerimine meeskonnaliikmena ja seejärel ressursi määramine ülesandele</span><span class="sxs-lookup"><span data-stu-id="d5692-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="d5692-112">Selle meetodiga saate lisada ressursi projekti meeskonnale ja seejärel määrata projekti ajakavas ülesanded ressursile.</span><span class="sxs-lookup"><span data-stu-id="d5692-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="d5692-113">Seda saate teha järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d5692-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="d5692-114">Lisage meeskonnaliikmete ruudustikus uus meeskonnaliige, klõpsates nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d5692-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="d5692-115">Valige meeskonnaliikme kiirloomise ekraanil reserveeritava ressursi nimi ja määrake roll.</span><span class="sxs-lookup"><span data-stu-id="d5692-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="d5692-116">Valige kuupäevade väärtused **Alates** ja **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="d5692-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d5692-117">![Kuvatõmmis meeskonnaliikme lisamisest](media/FAQ-Resources-to-Tasks2-1.png "Kuvatõmmis meeskonnaliikme lisamisest")</span><span class="sxs-lookup"><span data-stu-id="d5692-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="d5692-118">Valige ressursi reserveerimiseks üks järgmistest eraldamismeetoditest.</span><span class="sxs-lookup"><span data-stu-id="d5692-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="d5692-119">**Täisvõimsus** reserveerib määratud ajavahemikuks ressursi täieliku võimsuse.</span><span class="sxs-lookup"><span data-stu-id="d5692-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d5692-120">**Protsendimaht** reserveerib määratud ajavahemikuks teatud protsendi ressursi võimsusest.</span><span class="sxs-lookup"><span data-stu-id="d5692-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d5692-121">**Jaga ühtlaselt tundide järgi** reserveerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus ühtlaselt igale päevale.</span><span class="sxs-lookup"><span data-stu-id="d5692-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="d5692-122">**Jaga eesmine koormus tundide järgi** reserveerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus nii, et suurem koormus jääks algusesse.</span><span class="sxs-lookup"><span data-stu-id="d5692-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="d5692-123">Ärge valige suvandit **Pole**, kuna see lisab ressursi meeskonnale, kuid ei loo reserveeringuid, mis hõivaks ressursi võimsuse.</span><span class="sxs-lookup"><span data-stu-id="d5692-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="d5692-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d5692-124">Select **Save**.</span></span>

    <span data-ttu-id="d5692-125">Pange tähele, et reserveeringu tunde peab olema piisavalt, et hõlmata ressursile määratavate ülesannete panusetunde ja ajavahemikke.</span><span class="sxs-lookup"><span data-stu-id="d5692-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="d5692-126">Kui need pole kooskõlas, ei saa te ressurssi ülesandele määrata.</span><span class="sxs-lookup"><span data-stu-id="d5692-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="d5692-127">Klõpsake ülesande tööjaotuse struktuuris (WBS) ressursilahtri ripploendit.</span><span class="sxs-lookup"><span data-stu-id="d5692-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="d5692-128">Seejärel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d5692-128">Then:</span></span> 

    1. <span data-ttu-id="d5692-129">Valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d5692-129">Select **Add**.</span></span>
    2. <span data-ttu-id="d5692-130">Valige jaotise **Ressursid** alt ripploend ja valige meeskonnaliige, kelle enne lisasite.</span><span class="sxs-lookup"><span data-stu-id="d5692-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="d5692-131">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5692-131">Select **OK**.</span></span> <span data-ttu-id="d5692-132">Meeskonnaliige on nüüd ülesandele määratud.</span><span class="sxs-lookup"><span data-stu-id="d5692-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d5692-133">![Kuvatõmmis WBS-iga ressursside lisamisest](media/FAQ-Resources-to-Tasks2-2.png "Kuvatõmmis WBS-iga ressursside lisamisest")</span><span class="sxs-lookup"><span data-stu-id="d5692-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="d5692-134">Näete meeskonnaliikmete ruudustikus jaotise Määratud tunnid all ressursi määratud tundide koguaega.</span><span class="sxs-lookup"><span data-stu-id="d5692-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="d5692-135">See on väiksem kui ressursile reserveeritud tunnid või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="d5692-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5692-136">![Kuvatõmmis ressursile määratud tundidest](media/FAQ-Resources-to-Tasks2-3.png "Kuvatõmmis ressursile määratud tundidest")</span><span class="sxs-lookup"><span data-stu-id="d5692-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="d5692-137">Kui ülesanne, mida püüate ressursile reserveerida, algab pärast ressursi reserveeringute lõppkuupäeva, siis ei kuvata ressurssi ripploendis.</span><span class="sxs-lookup"><span data-stu-id="d5692-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="d5692-138">Pange tähele, et saate määrata ressurssi enamatele tundidele kui tema reserveeritud tunnid, kui sellel ressursil on üle jäänud määramata võimsust.</span><span class="sxs-lookup"><span data-stu-id="d5692-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="d5692-139">Sellisel juhul määratakse ressurssi kuni tema reserveeringuteni vaid osaliselt.</span><span class="sxs-lookup"><span data-stu-id="d5692-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="d5692-140">Näete neid üle jäänud määramata ülesannete tunde, kui lisate tööjaotuse struktuurile veeru Mehitamata tunnid.</span><span class="sxs-lookup"><span data-stu-id="d5692-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="d5692-141">Kui ressursid määratakse oma reserveeritud tundidele (nende reserveeritud tunnid võrduvad nende määratud tundidega), siis näete järgmist tõrketeadet, kui üritate neile rohkem ülesandeid määrata.</span><span class="sxs-lookup"><span data-stu-id="d5692-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="d5692-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.* (Ei saanud ressurssi ülesandele määrata – järgmistele ressurssidele pole projekti suhtes piisavalt tunde reserveeritud.)</span><span class="sxs-lookup"><span data-stu-id="d5692-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="d5692-143">Peale selle lisatakse projektijuhi vaikerolliga meeskonnaliige, kes lisatakse meeskonnale projekti loomisel, ilma ühegi reserveeringuta ja talle ei saa määrata ühtegi ülesannet.</span><span class="sxs-lookup"><span data-stu-id="d5692-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="d5692-144">Teda ei kuvata ülesannete ressursside ripploendites.</span><span class="sxs-lookup"><span data-stu-id="d5692-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="d5692-145">Kui soovite seda ressurssi määrata, siis peate ta meeskonnast eemaldama ja seejärel uuesti lisama ükskõik millise eraldamismeetodiga peale Pole.</span><span class="sxs-lookup"><span data-stu-id="d5692-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="d5692-146">Projektijuht lisatakse projekti loomisel meeskonda, et tagada, et projektil oleks vaikimisi vähemalt üks projekti kinnitaja.</span><span class="sxs-lookup"><span data-stu-id="d5692-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="d5692-147">Üldise meeskonnaliikme loomine ülesannete rolli määramistega</span><span class="sxs-lookup"><span data-stu-id="d5692-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="d5692-148">See meetod tagab, et ressurssidel oleks ülesannete jaoks piisavalt reserveeringuid.</span><span class="sxs-lookup"><span data-stu-id="d5692-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="d5692-149">Esmalt loote kohatäite või üldise ressursi, mis kirjeldab nimelise ressursi tunnuseid, keda soovite ülesannetele tööle määrata. Selleks loote pärast ülesannetele rollide määramist meeskonna.</span><span class="sxs-lookup"><span data-stu-id="d5692-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="d5692-150">Seda saate teha järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d5692-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="d5692-151">Valige tööjaotuse struktuuris ülesanne.</span><span class="sxs-lookup"><span data-stu-id="d5692-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="d5692-152">Valige ressursilahtris ripploendi ikoon **Määratud roll**.</span><span class="sxs-lookup"><span data-stu-id="d5692-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="d5692-153">Valige ripploend **Roll** ja seejärel roll üldisele ressursile.</span><span class="sxs-lookup"><span data-stu-id="d5692-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="d5692-154">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5692-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d5692-155">![Kuvatõmmis WBSi abil ressursi lisamisest](media/FAQ-Resources-to-Tasks2-4.png "Kuvatõmmis WBSi abil ressursi lisamisest")</span><span class="sxs-lookup"><span data-stu-id="d5692-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="d5692-156">Kui olete lõpetanud WBS-is ülesannetele rollide määramise, valige käsk **Projektimeeskonna loomine**.</span><span class="sxs-lookup"><span data-stu-id="d5692-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="d5692-157">Rakendus Project Service loob rollide, organisatsiooniüksuste ressursside ja projekti kalendri põhjal vähima arvu üldiseid meeskonnaliikmeid, koondades selleks ülesande määranguid.</span><span class="sxs-lookup"><span data-stu-id="d5692-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5692-158">![Kuvatõmmis projekti meeskonna loomisest](media/FAQ-Resources-to-Tasks2-5.png "Kuvatõmmis projekti meeskonna loomisest")</span><span class="sxs-lookup"><span data-stu-id="d5692-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="d5692-159">Meeskonnaliikmete ruudustikus näete üldise ressursitüübiga ressursse koos rolli ja ametikoha nimega.</span><span class="sxs-lookup"><span data-stu-id="d5692-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="d5692-160">Kui töö lõpetamiseks on rolli jaoks vaja kahte ressurssi, siis loob meeskonna loomise funktsioon kaks meeskonnaliiget ja kasutab nende eristamiseks ametikoha nime.</span><span class="sxs-lookup"><span data-stu-id="d5692-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5692-161">![Kuvatõmmis kahe üldise ressursi lisamisest](media/FAQ-Resources-to-Tasks2-6.png "Kuvatõmmis kahe üldise ressursi lisamisest")</span><span class="sxs-lookup"><span data-stu-id="d5692-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="d5692-162">Saate avada üldise meeskonnaliikme varuressursi nõude, kui valite suvandi Ressursinõue all oleva lingi.</span><span class="sxs-lookup"><span data-stu-id="d5692-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5692-163">![Kuvatõmmis varuressursi nõude avamisest](media/FAQ-Resources-to-Tasks2-7.png "Kuvatõmmis varuressursi nõude avamisest")</span><span class="sxs-lookup"><span data-stu-id="d5692-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="d5692-164">Valige üldise ressursi jaoks suvand **Reserveeri** ja seejärel saate kasutada ajakavapaneeli, et leida ning reserveerida päris ressurss.</span><span class="sxs-lookup"><span data-stu-id="d5692-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="d5692-165">Samuti saate esitada nõude ressursihaldurile täitmiseks, kui valite käsu **Esita taotlus**.</span><span class="sxs-lookup"><span data-stu-id="d5692-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="d5692-166">Kui üldine ressurss on täidetud nimelise ressursiga, siis eemaldatakse üldine ressurss meeskonnast ja üldisele ressursile määratud ülesanded määratakse nimelisele ressursile, mis täitis üldise ressursi ressursinõude.</span><span class="sxs-lookup"><span data-stu-id="d5692-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]