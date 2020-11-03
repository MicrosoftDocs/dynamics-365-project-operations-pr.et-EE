---
title: Projekti ressursside seadistamine
description: Selles teemas antakse teavet projekti ressursside seadistamise või taotlemise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075128"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="b9a8b-103">Projekti ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="b9a8b-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9a8b-104">Peate seadistama kalendri ja seostama selle töövõtja või töötajaga.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="b9a8b-105">Kalendrit kasutatakse projekti kavandamiseks ja projekti jaoks reserveeritavate ressursside tööaegade jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="b9a8b-106">Kalendri seadistamisel saavad projektijuhid ressursi optimeerimise raames teha ressursi tasandamist.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="b9a8b-107">Kalendri ajakava põhjal saab ressurssidele lisada piiranguid.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="b9a8b-108">Kalendri saate seadistada lehel **Kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="b9a8b-109">Kui te seadistate projekti ressursina töötaja, saate valida töötajate seast, kes töötavad ettevõttes, kelle jaoks ressurssi seadistate.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="b9a8b-110">Teise võimalusena saate valida töötajad teistest ettevõtetest oma organisatsioonis.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="b9a8b-111">Neid töötajaid nimetatakse kontsernisisesteks ressurssideks.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="b9a8b-112">Järgmised protseduurid selgitavad, kuidas seadistada töötajat oma ettevõttes projekti ressursina ja kuidas seadistada kontsernisisene projekti ressurss.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="b9a8b-113">Töötaja seadistamine projekti ressursina</span><span class="sxs-lookup"><span data-stu-id="b9a8b-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="b9a8b-114">Lehel **Töötajad** loendis **Töötajad** valige töötaja, kelle projekti ressursina lisate, ja avage töötaja kirje.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="b9a8b-115">Paanil Toiming valige **Projekt** &gt; **Seadistamine** &gt; **Projekti seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="b9a8b-116">Valige kalender ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="b9a8b-117">Saate määrata ka ressursi jaoks eelmääramise tüübina vaikeprojektid.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="b9a8b-118">Eelmääramisi saab kasutada juhul, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss hakkab tööle.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="b9a8b-119">Eelmääramised võivad põhineda ka projekti sponsori või kliendi taotlusel.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="b9a8b-120">Projekti eelmääramiseks lehel **Projektide määramine** vahekaardil **Projektid** loendis **Ülejäänud projektid** valige vastav projekt.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="b9a8b-121">Kontsernisisese ressursi seadistamine</span><span class="sxs-lookup"><span data-stu-id="b9a8b-121">Set up an intercompany resource</span></span>

<span data-ttu-id="b9a8b-122">Kui seadistate töötaja kontsernisisese ressursina, peate seadistamise lõpetama nii laenu andvale ettevõttele kui ka laenavale ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="b9a8b-123">Laenu andvas ettevõttes</span><span class="sxs-lookup"><span data-stu-id="b9a8b-123">In the lending company</span></span>

1. <span data-ttu-id="b9a8b-124">Rakenduses Finance kontrollige, kas laenu andev ettevõte on valitud, ja täitke seejärel toiming eelmises jaotises „Töötaja projekti ressursina häälestamine”.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="b9a8b-125">Valige lehel **Kontsernisisene raamatupidamine** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="b9a8b-126">Valige väljal **Juriidilise üksuse ID** laenu andev ettevõte.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="b9a8b-127">Täitke ülejäänud väljad vajaduse järgi ja valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="b9a8b-128">Valige lehel **Ülekandehind** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="b9a8b-129">Valige väljal **Laenu võttev juriidiline olem** vastav ettevõte.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="b9a8b-130">Laenavale ettevõttele ainult selle jaotise alguses loodud ressursi laenamiseks valige väljal **Ressurss** loodud ressursi nimi.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="b9a8b-131">Laenavas ettevõttes laenavala ettevõttele kõikide ressursside kättesaadavaks tegemiseks jätke väli **Ressurss** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="b9a8b-132">Lehel **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Kontsernisisesed** määrake suvand **Luba kontsernisisesed ressursiplaneerimine ja ajatabelid** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="b9a8b-133">Laenu võtvas ettevõttes</span><span class="sxs-lookup"><span data-stu-id="b9a8b-133">In the borrowing company</span></span>

- <span data-ttu-id="b9a8b-134">Sisestage lehel **Ressursside loend** otsingufiltrisse ressursi nimi, mille laenava ettevõtte jaoks lõite, et kontrollida, kas nimi sisaldub laenu võtva ettevõtte ressursside loendis.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="b9a8b-135">Projekti ressursside taotlemine</span><span class="sxs-lookup"><span data-stu-id="b9a8b-135">Request project resources</span></span>
<span data-ttu-id="b9a8b-136">Projekti ressursi ajastamise funktsioon võimaldab ressursihalduritel levitada töötajate ressursse kaasamistele või projektidele.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="b9a8b-137">Selle funktsiooni lubamiseks täitke järgmised tööülesanded või veenduge, et need oleks täidetud.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="b9a8b-138">Seadistage numriseeriad.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-138">Set up number sequences.</span></span>
- <span data-ttu-id="b9a8b-139">Seadistage projektihalduse ja raamatupidamise töövood.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="b9a8b-140">Lubage ressursitaotluste töövood.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-140">Enable resource request workflows.</span></span>

<span data-ttu-id="b9a8b-141">Pärast eelnevate toimingute lõpuleviimist saate vastavalt vajadusele täita järgmisi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="b9a8b-142">Looge ressursi taotlus esialgselt broneeritud personali ressursilt.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="b9a8b-143">Jälgige ressursitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-143">Monitor resource requests.</span></span>
- <span data-ttu-id="b9a8b-144">Täitke ressursitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="b9a8b-145">Taotlege personali ressurssi WBS-ilt.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="b9a8b-146">Broneerige ressursid projektile ilma personaliga ressursi taotlust.</span><span class="sxs-lookup"><span data-stu-id="b9a8b-146">Book resources to a project without having a request for a staffed resource.</span></span>
