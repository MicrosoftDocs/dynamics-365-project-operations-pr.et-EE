---
title: Projektile ressursside pakkumine
description: Selles teemas kirjeldatakse projektile ressursside pakkumist.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120178"
---
# <a name="propose-project-resources"></a><span data-ttu-id="91cda-103">Projektile ressursside pakkumine</span><span class="sxs-lookup"><span data-stu-id="91cda-103">Propose project resources</span></span>

<span data-ttu-id="91cda-104">Ressursihaldurid saavad projektijuhile ressursi pakkuda ressursitaotluse kaudu.</span><span class="sxs-lookup"><span data-stu-id="91cda-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="91cda-105">Tehke taotluse ruudustikust või taotlusest endast valik **Ressursside leidmine**</span><span class="sxs-lookup"><span data-stu-id="91cda-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="91cda-106">Valige lehel **Ajakava abimees** ressurss ja seejärel tehke paani **Ressursi broneeringu loomine** väljal **Broneeringu olek** valik **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="91cda-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Soovitatud ressurss on valitud.](media/Resource-Management-image62.png)

<span data-ttu-id="91cda-108">Ilmnevad järgmised olekuvärskendused.</span><span class="sxs-lookup"><span data-stu-id="91cda-108">The following status updates occur:</span></span>

- <span data-ttu-id="91cda-109">Lehel **Ajakava abimees** värskendatakse olekuindikaatoreid näitamaks, et broneering on soovituslik, mitte fikseeritult broneeritud.</span><span class="sxs-lookup"><span data-stu-id="91cda-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Soovitatud broneeringu olekuindikaatorid lehel Ajakava abimees](media/Resource-Management-image63.png)

- <span data-ttu-id="91cda-111">Ressursitaotluses muudetakse olekuks **Vajab ülevaatamist**.</span><span class="sxs-lookup"><span data-stu-id="91cda-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Ressursitaotluse olek muudeti väärtusele Vajab ülevaatamist.](media/Resource-Management-image64.png)

- <span data-ttu-id="91cda-113">Projekti vahekaardil **Meeskond** muudetakse üldiste meeskonnaliikmete väärtus **Taotluse olek** väärtusele **Vajab ülevaatamist**.</span><span class="sxs-lookup"><span data-stu-id="91cda-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Üldiste meeskonnaliikmete taotluse olek muudeti vahekaardil Meeskond väärtusele Vajab ülevaatamist](media/Resource-Management-image48.png)

<span data-ttu-id="91cda-115">Projektijuht saab ettepaneku vastu võtta või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="91cda-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="91cda-116">Ressursihaldurid saavad ressursitaotluste töötlemisel kasutada kõiki järgmiseid meetodeid.</span><span class="sxs-lookup"><span data-stu-id="91cda-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="91cda-117">Pakkuda nõudluse rahuldamiseks mitmeid ressursse, kui nõutavate tundide täitmiseks pole saadaval ühte ainukest ressurssi.</span><span class="sxs-lookup"><span data-stu-id="91cda-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="91cda-118">Seejärel jaotatakse pakutud tunnid mitme ressursi vahel, mis suudavad nõutavate tundide nõudlust rahuldada.</span><span class="sxs-lookup"><span data-stu-id="91cda-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="91cda-119">Selle stsenaariumi korral ei saa tunnid kattuda.</span><span class="sxs-lookup"><span data-stu-id="91cda-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="91cda-120">Pakkuda vähem ressursse, kui on vaja.</span><span class="sxs-lookup"><span data-stu-id="91cda-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="91cda-121">Selle stsenaariumi korral on pakutud ressursi võimsus väiksem kui nõutavad tunnid, mille taotleja määras.</span><span class="sxs-lookup"><span data-stu-id="91cda-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="91cda-122">Seega, kui taotleja võtab pakutud ressursid vastu, luuakse ülejäänud nõudluse hõivamiseks täitmata ressursi nõue.</span><span class="sxs-lookup"><span data-stu-id="91cda-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="91cda-123">Broneerida nõudluse rahuldamiseks mitmeid ressursse, kui töö lõpule viimiseks pole saadaval ühte ainukest ressurssi.</span><span class="sxs-lookup"><span data-stu-id="91cda-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="91cda-124">Broneerida vähem ressursse, kui on vaja.</span><span class="sxs-lookup"><span data-stu-id="91cda-124">Book fewer resources than are required.</span></span> <span data-ttu-id="91cda-125">Sel juhul on broneeritud tunde vähem kui nõutud tunde.</span><span class="sxs-lookup"><span data-stu-id="91cda-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="91cda-126">Süsteem juhendab teid, et pakuksite broneeringute asemel ressursse, et taotleja saaks järelejäänud nõudlust kontrollida ja jälgida.</span><span class="sxs-lookup"><span data-stu-id="91cda-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="91cda-127">Tasustatav kasutus</span><span class="sxs-lookup"><span data-stu-id="91cda-127">Billable utilization</span></span>

<span data-ttu-id="91cda-128">Ressurssidel võib olla tasustatav sihtkasutus.</span><span class="sxs-lookup"><span data-stu-id="91cda-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="91cda-129">See sihtkasutus on määratletud kas ressursi vaikerolli atribuudina või määratud iga broneeritava ressursi kirjele.</span><span class="sxs-lookup"><span data-stu-id="91cda-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="91cda-130">Kasutuse arvutused põhinevad tegelikel tundidel, mida ressursid on kinnitatud ajakandeid kasutades edastanud.</span><span class="sxs-lookup"><span data-stu-id="91cda-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="91cda-131">Kasutuse arvutamiseks kasutatakse järgmiseid valemeid.</span><span class="sxs-lookup"><span data-stu-id="91cda-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="91cda-132">Tasustatav kasutus = arveldatavad tegelikud tunnid ÷ ressursivõimsus</span><span class="sxs-lookup"><span data-stu-id="91cda-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="91cda-133">Mittetasustatav kasutus = tegelik aeg koos arveldustüübi ID-ga = mittetasustatav, täiendav või pole saadaval ÷ ressursivõimsus</span><span class="sxs-lookup"><span data-stu-id="91cda-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="91cda-134">Sisemine = tegelik aeg ilma müügilepinguta ÷ ressursivõimsus</span><span class="sxs-lookup"><span data-stu-id="91cda-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="91cda-135">Ressursivõimsus = ressursi töötunnid – kontorist väljasolek – puhkepäevad</span><span class="sxs-lookup"><span data-stu-id="91cda-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="91cda-136">Vaate **Ressursikasutus** leiate paanilt **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="91cda-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Ressursikasutuse vaade](media/Resource-Management-image65.png)

<span data-ttu-id="91cda-138">Iga ruudustiku lahter esindab perioodis (nt päev, nädal või kuu) oleva ressursi tasustatavat kasutusprotsenti.</span><span class="sxs-lookup"><span data-stu-id="91cda-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="91cda-139">Lahtrite värvimiseks kasutatakse järgmisi valemeid.</span><span class="sxs-lookup"><span data-stu-id="91cda-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="91cda-140">**Roheline:** tasustatav kasutus \>= ressursi sihtkasutus</span><span class="sxs-lookup"><span data-stu-id="91cda-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="91cda-141">**Kollane:** sihtkasutus – 20 \<= tasustatav kasutus \< sihtkasutus</span><span class="sxs-lookup"><span data-stu-id="91cda-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="91cda-142">**Punane:** tasustatav kasutus \< sihtkasutus – 20</span><span class="sxs-lookup"><span data-stu-id="91cda-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="91cda-143">Kuna vaade **Ressursikasutus** põhineb ajakavapaneelil, saate oma tulemuste filtreerimiseks kasutada ajakavapaneeli filtreerimise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="91cda-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="91cda-144">Ruudustik nõuab, et määraksite sihtkasutuse kas rollile või konkreetsele ressursile.</span><span class="sxs-lookup"><span data-stu-id="91cda-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="91cda-145">Selle seadistamiseks tehke valikud **Ressursid** \> **Ressursi rollid**.</span><span class="sxs-lookup"><span data-stu-id="91cda-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="91cda-146">Peale selle tuleb igale broneeritavale ressursile määrata vaikeroll.</span><span class="sxs-lookup"><span data-stu-id="91cda-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="91cda-147">Avage **Ressursid** \> **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="91cda-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="91cda-148">Kontrollige vahekaardil **Project Service**, et ressursi roll oleks määratletud ja selle väli **On vaikimisi** oleks määratud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="91cda-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="91cda-149">Saate lisada veel rolle, kus väärtus **On vaikimisi = Ei**.</span><span class="sxs-lookup"><span data-stu-id="91cda-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="91cda-150">Roll, kus väärtust **On vaikimisi = Jah**, kasutatakse ressursi kasutuse hindamiseks selle rolli eesmärgi suhtes.</span><span class="sxs-lookup"><span data-stu-id="91cda-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Vaikeroll on määratud](media/Resource-Management-image67.png)

<span data-ttu-id="91cda-152">Vahekaardil **Project Service** saate ressursi jaoks määrata ka eraldi sihtkasutuse.</span><span class="sxs-lookup"><span data-stu-id="91cda-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="91cda-153">Seejärel kasutab kasutuse arvutus seda sihtkasutust, et hinnata ressursi sihti, mitte ressursi vaikerolli sihti.</span><span class="sxs-lookup"><span data-stu-id="91cda-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="91cda-154">Ressursi jaoks kuvatakse kasutus ainult juhul, kui sellel ressursil on ruudustikus kuvatud perioodi jooksul kinnitatud, arveldatavat aega.</span><span class="sxs-lookup"><span data-stu-id="91cda-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="91cda-155">Ressursi saadavus</span><span class="sxs-lookup"><span data-stu-id="91cda-155">Resource availability</span></span>

<span data-ttu-id="91cda-156">On ülioluline, et ressursihaldurid saaksid vaadata ressursside saadavust ja värskendada broneeringuid.</span><span class="sxs-lookup"><span data-stu-id="91cda-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="91cda-157">Mõnel juhul ametlik nõudlus puudub (ressursitaotlus), kuid ressursihaldur peab vastama kavandamata nõudlusele, mis esitatakse selliste kanalite nagu meil, telefonikõne või kiirsõnumid kaudu.</span><span class="sxs-lookup"><span data-stu-id="91cda-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="91cda-158">Ressursihaldurid kasutavad ajakavapaneeli ressursside ja broneeringute värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="91cda-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="91cda-159">Ressurssi töötundide alusel arvutatakse ressursi saadavust.</span><span class="sxs-lookup"><span data-stu-id="91cda-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="91cda-160">Ressursibroneeringud tarbivad ressursside võimsust.</span><span class="sxs-lookup"><span data-stu-id="91cda-160">Resource bookings consume the capacity of the resources.</span></span>

![Ajakavapaneel](media/Resource-Management-image68.png)

<span data-ttu-id="91cda-162">Ajakavapaneel kasutab broneeringute, saadavuse ja ülebroneerimiste ning ka broneeringute oleku kuvamiseks värve ja varjustust.</span><span class="sxs-lookup"><span data-stu-id="91cda-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="91cda-163">Ajakavapaneeli üks säte võimaldab teil kuvada legendi.</span><span class="sxs-lookup"><span data-stu-id="91cda-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="91cda-164">Kui ajakavapaneelil kuvatakse konkreetse broneeritava ressursi kõrval parempoole suunatud nool, saab ressurssi laiendada, et kuvada selle töö üksikasju, millele ressurss on broneeritud.</span><span class="sxs-lookup"><span data-stu-id="91cda-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Broneeritav ressurss on ajakavapaneelil laiendatud](media/Resource-Management-image69.png)

<span data-ttu-id="91cda-166">Kuna rakendus Dynamics 365 Project Service Automation kasutab mootorit Universal Resource Scheduling, ja kui teil on installitud ka rakendus Dynamics 365 Field Service, saate vaadata üksikasju projektide ressursibroneeringute, töötellimuste ja muude olemite kohta, millele olete kavandamise laiendanud.</span><span class="sxs-lookup"><span data-stu-id="91cda-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Projektide ressursibroneeringute ja töötellimuste üksikasjad](media/Resource-Management-image70.png)

<span data-ttu-id="91cda-168">Konkreetse ressursi kohta lisateabe saamiseks paremklõpsake seda, et avada ressursikaart.</span><span class="sxs-lookup"><span data-stu-id="91cda-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Ressursikaart](media/Resource-Management-image71.png)
