---
title: Ülesandele ressurssi määramine
description: Selles teemas kirjeldatakse, kuidas määrata ülesannetele ressursse.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149988"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="9116c-103">Ülesandele ressurssi määramine</span><span class="sxs-lookup"><span data-stu-id="9116c-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9116c-104">Rakenduses Microsoft Dynamics 365 Project Service Automation on kolm võimalust ülesandele ressursi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="9116c-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="9116c-105">Ressursi broneerimine meeskonnaliikmena ja seejärel ressursi määramine ülesandele</span><span class="sxs-lookup"><span data-stu-id="9116c-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="9116c-106">Saate lisada ressursi projekti meeskonnale ja seejärel määrata projekti ajakavas ressurss ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="9116c-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="9116c-107">Lisage vahekaardil **Meeskonnaliige** uus meeskonnaliige, klõpsates nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9116c-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="9116c-108">See avab paneeli **Meeskonnaliikme kiirloomine**, kus saate valida broneeritava ressursi nime ja määrata rolli.</span><span class="sxs-lookup"><span data-stu-id="9116c-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="9116c-109">Valige ressursi broneerimiseks üks järgmistest eraldamismeetoditest.</span><span class="sxs-lookup"><span data-stu-id="9116c-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="9116c-110">**Täisvõimsus** reserveerib määratud ajavahemikuks ressursi täieliku võimsuse.</span><span class="sxs-lookup"><span data-stu-id="9116c-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9116c-111">**Protsendimaht** reserveerib määratud ajavahemikuks teatud protsendi ressursi võimsusest.</span><span class="sxs-lookup"><span data-stu-id="9116c-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9116c-112">**Jaga ühtlaselt tundide järgi** broneerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus ühtlaselt igale päevale.</span><span class="sxs-lookup"><span data-stu-id="9116c-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="9116c-113">**Jaga eesmine koormus tundide järgi** reserveerib ressursi määratud arvu tundideks, jagades aega määratud ajavahemikus nii, et suurem koormus jääks algusesse.</span><span class="sxs-lookup"><span data-stu-id="9116c-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="9116c-114">Suvand **Pole** lisab ressursi meeskonnale, kuid ei loo reserveeringuid, mis hõivaks tema võimsuse.</span><span class="sxs-lookup"><span data-stu-id="9116c-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="9116c-115">Valige ülesande ruudustikus **Ajakava** ressursilahtrist ikoon **Ressurss** ja seejärel jaotisest **Meeskonnaliige** see meeskonnaliige, kelle just lisasite.</span><span class="sxs-lookup"><span data-stu-id="9116c-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="9116c-116">Vahekaartidel **Meeskonnaliikmed** kui ka **Sobitamine** näidatakse ressursi broneeritud ja määratud tunde.</span><span class="sxs-lookup"><span data-stu-id="9116c-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="9116c-117">Tunnid peaksid olema samad, kuid see pole nõutav, sest broneeringud ja määrangud ei ole tihedalt ühendatud.</span><span class="sxs-lookup"><span data-stu-id="9116c-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="9116c-118">Kui need on erinevad, siis esitab vahekaart **Sobitamine** teile üksikasju, näiteks kui määrate ressurssi rohkematele tundidele, kui olete broneerinud.</span><span class="sxs-lookup"><span data-stu-id="9116c-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="9116c-119">Vajaduse korral saate nende andmete põhjal teha parandusi, näiteks pikendada ressursi broneeringuid või muuta määrangut.</span><span class="sxs-lookup"><span data-stu-id="9116c-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="9116c-120">Üldise meeskonnaliikme loomine ülesannete määramistega</span><span class="sxs-lookup"><span data-stu-id="9116c-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="9116c-121">Kui loote üldise meeskonnaliikme ülesande määramise kaudu, loote te kohatäite või üldise ressursi, mis kirjeldab nimega ressursi tunnuseid, keda soovite ülesannetele tööle määrata.</span><span class="sxs-lookup"><span data-stu-id="9116c-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="9116c-122">Seejärel loote nõude (või esitate nõude taotlusega), mida kasutatakse nimega ressursi otsimiseks ja broneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="9116c-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="9116c-123">Valige ülesande ruudustikus **Ajakava** ressursilahtrist ikoon **Ressurss**.</span><span class="sxs-lookup"><span data-stu-id="9116c-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="9116c-124">Sisestage nimi kohatäite ressursi nime jaoks.</span><span class="sxs-lookup"><span data-stu-id="9116c-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="9116c-125">Nt programmihaldur.</span><span class="sxs-lookup"><span data-stu-id="9116c-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="9116c-126">Valige **Loo** ja määrake väljal **Projekti meeskonnaliikme kiirloomine** üldise ressursi roll.</span><span class="sxs-lookup"><span data-stu-id="9116c-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="9116c-127">Saate jätkata sellele kohatäite ressursile ülesannete määramist, kui valite ressursi ülesandele jaotisest **Ressursivalija**.</span><span class="sxs-lookup"><span data-stu-id="9116c-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="9116c-128">Need on loetletud jaotises **Meeskonnaliikmed**.</span><span class="sxs-lookup"><span data-stu-id="9116c-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="9116c-129">Kui olete üldise ressursi määramisega lõpetanud, valige üldine ressurss vahekaardilt **Meeskond** ja valige käsk **Loo nõue**, et luua üldise ressursi jaoks ressursinõue.</span><span class="sxs-lookup"><span data-stu-id="9116c-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="9116c-130">Valige üldise ressursi jaoks käsk **Reserveeri**.</span><span class="sxs-lookup"><span data-stu-id="9116c-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="9116c-131">Seejärel saate kasutada ajakavapaneeli, et otsida ja broneerida päris ressurssi.</span><span class="sxs-lookup"><span data-stu-id="9116c-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="9116c-132">Samuti saate esitada nõude ressursihaldurile täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="9116c-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="9116c-133">Kui üldine ressurss on täidetud nimelise ressursiga, siis eemaldatakse üldine ressurss meeskonnast ja üldisele ressursile määratud ülesanded määratakse nimelisele ressursile, mis täitis üldise ressursi ressursinõude.</span><span class="sxs-lookup"><span data-stu-id="9116c-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="9116c-134">Nimega ressursi määramine kõikide broneeritavate ressursside loendist</span><span class="sxs-lookup"><span data-stu-id="9116c-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="9116c-135">Saate kasutada **Ressursivalija** otsinguvälja, et otsida kõiki broneeritavaid ressursse ja neid ülesandele määrata.</span><span class="sxs-lookup"><span data-stu-id="9116c-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="9116c-136">Sel viisil määratud ressursid lisatakse meeskonda ilma broneeringuta.</span><span class="sxs-lookup"><span data-stu-id="9116c-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="9116c-137">See on sarnane meeskonnaliikmete lisamise ja mitte eraldamise meetodi valimisega.</span><span class="sxs-lookup"><span data-stu-id="9116c-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="9116c-138">Neid kuvatakse vahekaartidel **Meeskond** ja **Sobitamine** ressurssidena, millel on vaid määrangud ja broneeringute puudujääk.</span><span class="sxs-lookup"><span data-stu-id="9116c-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="9116c-139">Reserveerige neid, kui soovite nende saadavaolekut kasutada.</span><span class="sxs-lookup"><span data-stu-id="9116c-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="9116c-140">Valige ülesande ruudustikus **Ajakava** ressursilahtrist ikoon **Ressurss**.</span><span class="sxs-lookup"><span data-stu-id="9116c-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="9116c-141">Alustage nime tippimist.</span><span class="sxs-lookup"><span data-stu-id="9116c-141">Start typing a name.</span></span> <span data-ttu-id="9116c-142">Nime otsingutulemused kuvatakse jaotise **Muud ressursid** all olevas **Ressursivalijas**.</span><span class="sxs-lookup"><span data-stu-id="9116c-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="9116c-143">Valige loendist ressurss, mille soovite ülesandele määrata.</span><span class="sxs-lookup"><span data-stu-id="9116c-143">Select the resource that you want to assign to the task.</span></span>

