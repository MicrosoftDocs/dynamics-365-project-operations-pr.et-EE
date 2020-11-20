---
title: Soovitatavate ressursside ülevaade
description: Selles teemas kirjeldatakse projektile ressursside pakkumist.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401168"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a6cfc-103">Soovitatavate ressursside ülevaade</span><span class="sxs-lookup"><span data-stu-id="a6cfc-103">Review proposed resources</span></span>

<span data-ttu-id="a6cfc-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="a6cfc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6cfc-105">Ressursihaldurid saavad projektijuhile ressursi pakkuda ressursitaotluse kaudu.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a6cfc-106">Tehke taotluse ruudustikust või taotlusest endast valik **Ressursside leidmine**</span><span class="sxs-lookup"><span data-stu-id="a6cfc-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a6cfc-107">Valige lehel **Ajakava abimees** ressurss ja seejärel tehke paani **Ressursi broneeringu loomine** väljal **Broneeringu olek** valik **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a6cfc-108">Ilmnevad järgmised olekuvärskendused.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-108">The following status updates occur:</span></span>

- <span data-ttu-id="a6cfc-109">Lehel **Ajakava abimees** värskendatakse olekuindikaatoreid näitamaks, et broneering on soovituslik, mitte fikseeritult broneeritud.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a6cfc-110">Ressursitaotluses muudetakse olekuks **Vajab ülevaatamist**.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a6cfc-111">Projekti vahekaardil **Meeskond** muudetakse üldiste meeskonnaliikmete väärtus **Taotluse olek** väärtusele **Vajab ülevaatamist**.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a6cfc-112">Projektijuht saab ettepaneku vastu võtta või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a6cfc-113">Ressursihaldurid saavad ressursitaotluste töötlemisel kasutada kõiki järgmiseid meetodeid.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a6cfc-114">Pakkuda nõudluse rahuldamiseks mitmeid ressursse, kui nõutavate tundide täitmiseks pole saadaval ühte ainukest ressurssi.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a6cfc-115">Seejärel jaotatakse pakutud tunnid mitme ressursi vahel, mis suudavad nõutavate tundide nõudlust rahuldada.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a6cfc-116">Selle stsenaariumi korral ei saa tunnid kattuda.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a6cfc-117">Pakkuda vähem ressursse, kui on vaja.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a6cfc-118">Selle stsenaariumi korral on pakutud ressursi võimsus väiksem kui nõutavad tunnid, mille taotleja määras.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a6cfc-119">Seega, kui taotleja võtab pakutud ressursid vastu, luuakse ülejäänud nõudluse hõivamiseks täitmata ressursi nõue.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a6cfc-120">Broneerida nõudluse rahuldamiseks mitmeid ressursse, kui töö lõpule viimiseks pole saadaval ühte ainukest ressurssi.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a6cfc-121">Broneerida vähem ressursse, kui on vaja.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a6cfc-122">Sel juhul on broneeritud tunde vähem kui nõutud tunde.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a6cfc-123">Süsteem juhendab teid, et pakuksite broneeringute asemel ressursse, et taotleja saaks järelejäänud nõudlust kontrollida ja jälgida.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a6cfc-124">Ressursi saadavus</span><span class="sxs-lookup"><span data-stu-id="a6cfc-124">Resource availability</span></span>

<span data-ttu-id="a6cfc-125">On ülioluline, et ressursihaldurid saaksid vaadata ressursside saadavust ja värskendada broneeringuid.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a6cfc-126">Mõnel juhul ametlik nõudlus puudub (ressursitaotlus), kuid ressursihaldur peab vastama kavandamata nõudlusele, mis esitatakse selliste kanalite nagu meil, telefonikõne või kiirsõnumid kaudu.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a6cfc-127">Ressursihaldurid kasutavad ajakavapaneeli ressursside ja broneeringute värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a6cfc-128">Ressurssi töötundide alusel arvutatakse ressursi saadavust.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a6cfc-129">Ressursibroneeringud tarbivad ressursside võimsust.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a6cfc-130">Ajakavapaneel kasutab broneeringute, saadavuse ja ülebroneerimiste ning ka broneeringute oleku kuvamiseks värve ja varjustust.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a6cfc-131">Ajakavapaneeli üks säte võimaldab teil kuvada legendi.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a6cfc-132">Kui ajakavapaneelil kuvatakse konkreetse broneeritava ressursi kõrval parempoole suunatud nool, saab ressurssi laiendada, et kuvada selle töö üksikasju, millele ressurss on broneeritud.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a6cfc-133">Kuna rakendus Dynamics 365 Project Operations kasutab mootorit Universal Resource Scheduling, ja kui teil on installitud ka rakendus Dynamics 365 Field Service, saate vaadata üksikasju projektide ressursibroneeringute, töötellimuste ja muude olemite kohta, millele olete kavandamise laiendanud.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a6cfc-134">Konkreetse ressursi kohta lisateabe saamiseks paremklõpsake seda, et avada ressursikaart.</span><span class="sxs-lookup"><span data-stu-id="a6cfc-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

