---
title: Mis on uut, märts 2021 – Project Operations Lite juurutamine
description: See teema sisaldab teavet Project Operations Lite’i juurutuse 2021. aasta märtsi väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499992"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="0dccc-103">Mis on uut, märts 2021 – Project Operations Lite juurutamine</span><span class="sxs-lookup"><span data-stu-id="0dccc-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="0dccc-104">_Kohaldub: lihtjuurutus - tehing proforma arveldusega_</span><span class="sxs-lookup"><span data-stu-id="0dccc-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0dccc-105">See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="0dccc-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="0dccc-106">Project Operations Dataverse’i keskkonna versioonis 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="0dccc-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="0dccc-107">Kvaliteedi värskendused</span><span class="sxs-lookup"><span data-stu-id="0dccc-107">Quality updates</span></span>

| <span data-ttu-id="0dccc-108">**Funktsiooni ala**</span><span class="sxs-lookup"><span data-stu-id="0dccc-108">**Feature area**</span></span> | <span data-ttu-id="0dccc-109">**Viitenumber**</span><span class="sxs-lookup"><span data-stu-id="0dccc-109">**Reference number**</span></span> | <span data-ttu-id="0dccc-110">**Kvaliteedi värskendus**</span><span class="sxs-lookup"><span data-stu-id="0dccc-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0dccc-111">Arveldamine ja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="0dccc-111">Billing and pricing</span></span> | <span data-ttu-id="0dccc-112">2133873</span><span class="sxs-lookup"><span data-stu-id="0dccc-112">2133873</span></span> | <span data-ttu-id="0dccc-113">Parandatud on **Ühiku müügihinna** valuuta sümbol ruudustikus **Kuluprognoosid**.</span><span class="sxs-lookup"><span data-stu-id="0dccc-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="0dccc-114">Arveldamine ja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="0dccc-114">Billing and pricing</span></span> | <span data-ttu-id="0dccc-115">2174616</span><span class="sxs-lookup"><span data-stu-id="0dccc-115">2174616</span></span> | <span data-ttu-id="0dccc-116">Kui hinnapakkumine võidetakse, viidatakse lepingu kohandatud hinnakirjale lepingurea üksikasjades, mis kopeeritakse hinnapakkumisest.</span><span class="sxs-lookup"><span data-stu-id="0dccc-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="0dccc-117">Müügivõimaluse haldus</span><span class="sxs-lookup"><span data-stu-id="0dccc-117">Opportunity Management</span></span> | <span data-ttu-id="0dccc-118">2167475</span><span class="sxs-lookup"><span data-stu-id="0dccc-118">2167475</span></span> | <span data-ttu-id="0dccc-119">Parandatud on maksusumma parandusarves, mis pärines arveldamata tegelikust kirjest.</span><span class="sxs-lookup"><span data-stu-id="0dccc-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="0dccc-120">Müügivõimaluse haldus</span><span class="sxs-lookup"><span data-stu-id="0dccc-120">Opportunity Management</span></span> | <span data-ttu-id="0dccc-121">2176285</span><span class="sxs-lookup"><span data-stu-id="0dccc-121">2176285</span></span> | <span data-ttu-id="0dccc-122">Maksusummat ei tohi kopeerida müügilepingu/hinnapakkumise rea üksikasjadest kululepingu/hinnapakkumise rea üksikasjadesse.</span><span class="sxs-lookup"><span data-stu-id="0dccc-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="0dccc-123">Müügivõimaluse haldus</span><span class="sxs-lookup"><span data-stu-id="0dccc-123">Opportunity Management</span></span> | <span data-ttu-id="0dccc-124">2188079</span><span class="sxs-lookup"><span data-stu-id="0dccc-124">2188079</span></span> | <span data-ttu-id="0dccc-125">Jagatud arveldamise reeglit ei tohi luua lepingute jaoks, mis ei põhine tööl.</span><span class="sxs-lookup"><span data-stu-id="0dccc-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="0dccc-126">Plaanimine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="0dccc-126">Planning and Tracking</span></span> | <span data-ttu-id="0dccc-127">2138853</span><span class="sxs-lookup"><span data-stu-id="0dccc-127">2138853</span></span> | <span data-ttu-id="0dccc-128">Projekti kopeerimise funktsioon värskendati, et tagada tööülesandele viitavate kuluprognoosi ridade kopeerimine sihtprojekti.</span><span class="sxs-lookup"><span data-stu-id="0dccc-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="0dccc-129">Plaanimine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="0dccc-129">Planning and Tracking</span></span> | <span data-ttu-id="0dccc-130">2173259</span><span class="sxs-lookup"><span data-stu-id="0dccc-130">2173259</span></span> | <span data-ttu-id="0dccc-131">Projekti kopeerimisfunktsioon on värskendatud, et tagada, et see ei kuvaks teatud stsenaariumite korral tõrketeadet **WBS-i kopeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0dccc-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="0dccc-132">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="0dccc-132">Time and Expense</span></span> | <span data-ttu-id="0dccc-133">2148910</span><span class="sxs-lookup"><span data-stu-id="0dccc-133">2148910</span></span> | <span data-ttu-id="0dccc-134">Lahendatud on kuvamisprobleem lehel **Kirje redigeerimine** ruudustikus **Ajakirje**.</span><span class="sxs-lookup"><span data-stu-id="0dccc-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="0dccc-135">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="0dccc-135">Time and Expense</span></span> | <span data-ttu-id="0dccc-136">2159798</span><span class="sxs-lookup"><span data-stu-id="0dccc-136">2159798</span></span> | <span data-ttu-id="0dccc-137">Süvendati kontrolli tagamaks, et kinnitatud kulukirjeid ei saaks redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0dccc-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


