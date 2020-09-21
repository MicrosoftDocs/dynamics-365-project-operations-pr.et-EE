---
title: Tööjõukulude ja väljaminekute standardsete kulude konfigureerimine
description: Selles teemas kirjeldatakse, kuidas seadistada projekti tööjõu ja väljaminekute jaoks standardseid kulusid.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751056"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="49e9c-103">Tööjõukulude ja väljaminekute standardsete kulude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="49e9c-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49e9c-104">Selles teemas kirjeldatakse, kuidas seadistada projekti tööjõu ja väljaminekute jaoks standardseid kulusid.</span><span class="sxs-lookup"><span data-stu-id="49e9c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="49e9c-105">Selle toiming kasutab USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="49e9c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="49e9c-106">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Hinnad > Omahind (tund)**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="49e9c-107">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-107">Select **New**.</span></span>
3. <span data-ttu-id="49e9c-108">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="49e9c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="49e9c-109">Väljale **Omahind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="49e9c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="49e9c-110">Saate seadistada projekti kategooria standardse omahinna või seadistada omahinna töötaja numbri, projekti numbri, kategooria, kuupäeva või mis tahes kombinatsiooni järgi.</span><span class="sxs-lookup"><span data-stu-id="49e9c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="49e9c-111">Rakendatav omahind on kõrgeima tasemega omahind.</span><span class="sxs-lookup"><span data-stu-id="49e9c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="49e9c-112">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-112">Select **Save**.</span></span>
6. <span data-ttu-id="49e9c-113">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Hinnad > Müügihind (tund)**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="49e9c-114">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-114">Select **New**.</span></span>
8. <span data-ttu-id="49e9c-115">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="49e9c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="49e9c-116">Väljal **Kehtivusaeg** tehke valik.</span><span class="sxs-lookup"><span data-stu-id="49e9c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="49e9c-117">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="49e9c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="49e9c-118">Saate seadistada standardse müügihinna tundide või projekti kategooria jaoks.</span><span class="sxs-lookup"><span data-stu-id="49e9c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="49e9c-119">Samuti saate seadistada müügihinnad töötajate arvu, projekti numbri, kategooria, kande kuupäeva või nende kombinatsiooni järgi.</span><span class="sxs-lookup"><span data-stu-id="49e9c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="49e9c-120">Tegelik müügihind, mida rakendatakse juhul, kui töötaja sisestab tehingu Tunni töölehele, on kõrgeima tasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="49e9c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="49e9c-121">Näiteks kui seadistatakse nii üldine müügihind kui ka töötajale omane müügihind, kasutatakse töötajale määratud müügihinda.</span><span class="sxs-lookup"><span data-stu-id="49e9c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="49e9c-122">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-122">Select **Save**.</span></span>
12. <span data-ttu-id="49e9c-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="49e9c-123">Close the page.</span></span>
13. <span data-ttu-id="49e9c-124">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Hinnad > Omahind (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="49e9c-125">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-125">Select **New**.</span></span>
15. <span data-ttu-id="49e9c-126">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="49e9c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="49e9c-127">Väljale **Omahind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="49e9c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="49e9c-128">Saab täita mitu välja, kuid see on minimaalne, mis kirje salvestamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="49e9c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="49e9c-129">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-129">Select **Save**.</span></span>
18. <span data-ttu-id="49e9c-130">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Hinnad > Müügihind (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="49e9c-131">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-131">Select **New**.</span></span>
20. <span data-ttu-id="49e9c-132">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="49e9c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="49e9c-133">Väljal **Kehtivusaeg** tehke valik.</span><span class="sxs-lookup"><span data-stu-id="49e9c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="49e9c-134">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="49e9c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="49e9c-135">Tegelik müügihind, mida rakendatakse juhul, kui töötaja sisestab tehingu Kulu töölehele, on kõrgeima tasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="49e9c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="49e9c-136">Näiteks kui seadistatakse nii üldine müügihind kui ka töötajale omane müügihind, kasutatakse töötajale määratud müügihinda.</span><span class="sxs-lookup"><span data-stu-id="49e9c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="49e9c-137">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="49e9c-137">Select **Save**.</span></span>

