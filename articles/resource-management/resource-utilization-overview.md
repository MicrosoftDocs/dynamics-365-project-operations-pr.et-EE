---
title: Ressursikasutuse ülevaade
description: Selles teemas antakse teavet ressursi kasutamise kohta rakenduses Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401371"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="ac365-103">Ressursikasutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac365-103">Resource utilization overview</span></span>

<span data-ttu-id="ac365-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="ac365-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac365-105">Ressurssidel võib olla tasustatav sihtkasutus.</span><span class="sxs-lookup"><span data-stu-id="ac365-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="ac365-106">See sihtkasutus on määratletud ressursi vaikerolli atribuudina või määratud iga broneeritava ressursi kirjele.</span><span class="sxs-lookup"><span data-stu-id="ac365-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="ac365-107">Kasutuse arvutused põhinevad tegelikel tundidel, mida ressursid on kinnitatud ajakandeid kasutades edastanud.</span><span class="sxs-lookup"><span data-stu-id="ac365-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="ac365-108">Kasutuse arvutamiseks kasutatakse järgmiseid valemeid.</span><span class="sxs-lookup"><span data-stu-id="ac365-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="ac365-109">Tasustatav kasutus = arveldatavad tegelikud tunnid ÷ ressursivõimsus</span><span class="sxs-lookup"><span data-stu-id="ac365-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="ac365-110">Mittetasustatav kasutus = tegelik aeg koos arveldustüübi ID-ga = mittetasustatav, täiendav või pole saadaval ÷ ressursivõimsus</span><span class="sxs-lookup"><span data-stu-id="ac365-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="ac365-111">Sisemine = tegelik aeg ilma müügilepinguta ÷ ressursivõimsus</span><span class="sxs-lookup"><span data-stu-id="ac365-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="ac365-112">Ressursivõimsus = ressursi töötunnid – kontorist väljasolek – puhkepäevad</span><span class="sxs-lookup"><span data-stu-id="ac365-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="ac365-113">Vaate **Ressursikasutus** leiate paanilt **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="ac365-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="ac365-114">Iga ruudustiku lahter esindab perioodis (nt päev, nädal või kuu) oleva ressursi tasustatavat kasutusprotsenti.</span><span class="sxs-lookup"><span data-stu-id="ac365-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="ac365-115">Lahtrite värvimiseks kasutatakse järgmisi valemeid.</span><span class="sxs-lookup"><span data-stu-id="ac365-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="ac365-116">**Roheline**: arveldatav kasutus > = ressursi eesmärgiks seatud kasutus</span><span class="sxs-lookup"><span data-stu-id="ac365-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="ac365-117">**Kollane**: eesmärgiks seatud kasutus – 20 < = arveldatav kasutus < eesmärgiks seatud kasutus</span><span class="sxs-lookup"><span data-stu-id="ac365-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="ac365-118">**Punane**: arveldatav kasutus < = eesmärgiks seatud kasutus – 20</span><span class="sxs-lookup"><span data-stu-id="ac365-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="ac365-119">Kuna vaade **Ressursikasutus** põhineb ajakavapaneelil, saate oma tulemuste filtreerimiseks kasutada ajakavapaneeli filtreerimise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="ac365-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="ac365-120">Ruudustik nõuab, et määraksite sihtkasutuse kas rollile või konkreetsele ressursile.</span><span class="sxs-lookup"><span data-stu-id="ac365-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="ac365-121">Selle seadistamiseks tehke valikud **Ressursid** > **Ressursi rollid**.</span><span class="sxs-lookup"><span data-stu-id="ac365-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="ac365-122">Peale selle tuleb igale broneeritavale ressursile määrata vaikeroll.</span><span class="sxs-lookup"><span data-stu-id="ac365-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="ac365-123">Avage **Ressursid** > **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="ac365-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="ac365-124">Kontrollige vahekaardil **Project Service**, et ressursi roll oleks määratletud ja väli **On vaikimisi** oleks määratud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ac365-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="ac365-125">Saate lisada veel rolle, kus väärtus **On vaikimisi** = **Ei**.</span><span class="sxs-lookup"><span data-stu-id="ac365-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="ac365-126">Roll, kus väärtust **On vaikimisi** = **Jah**, kasutatakse ressursi kasutuse hindamiseks selle rolli eesmärgi suhtes.</span><span class="sxs-lookup"><span data-stu-id="ac365-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="ac365-127">Vahekaardil **Project Service** saate ressursi jaoks määrata ka eraldi sihtkasutuse.</span><span class="sxs-lookup"><span data-stu-id="ac365-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="ac365-128">Seejärel kasutab kasutuse arvutus seda sihtkasutust, et hinnata ressursi sihti, mitte ressursi vaikerolli sihti.</span><span class="sxs-lookup"><span data-stu-id="ac365-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="ac365-129">Ressursi jaoks kuvatakse kasutus ainult juhul, kui selle ressursi ruudustikus kuvatakse perioodi jooksul kinnitatud, arveldatav aeg.</span><span class="sxs-lookup"><span data-stu-id="ac365-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>
