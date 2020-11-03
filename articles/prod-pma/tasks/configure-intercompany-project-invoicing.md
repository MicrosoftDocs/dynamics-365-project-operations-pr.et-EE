---
title: Kontsernisisese projekti arveldamise konfigureerimine
description: Selles teemas kirjeldatakse, kuidas seadistada projekti arveldamist kahe ettevõtte vahel.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075015"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="1e984-103">Kontsernisisese projekti arveldamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1e984-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e984-104">Selles teemas kirjeldatakse, kuidas seadistada projekti arveldamist kahe ettevõtte vahel.</span><span class="sxs-lookup"><span data-stu-id="1e984-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="1e984-105">Selle toiming kasutab USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="1e984-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1e984-106">Minge navigeerimispaani jaotisse **Moodulid > Ostureskontro > Tarnijad > Kõik tarnijad**.</span><span class="sxs-lookup"><span data-stu-id="1e984-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="1e984-107">Loendis **Kõik tarnijad** leidke ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1e984-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="1e984-108">Valige paanil Toiming **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="1e984-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="1e984-109">Valige **Kontsernisisesed**.</span><span class="sxs-lookup"><span data-stu-id="1e984-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="1e984-110">Määrake valiku **Aktiivne** väärtuseks **Jah** , et lubada kontsernisisene kauplemine.</span><span class="sxs-lookup"><span data-stu-id="1e984-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="1e984-111">Väljal **Kliendi ettevõte** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e984-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="1e984-112">Väljal **Minu konto** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e984-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="1e984-113">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1e984-113">Select **Save**.</span></span>
9. <span data-ttu-id="1e984-114">Avalehe tagasipöördumiseks sulgege leheküljed.</span><span class="sxs-lookup"><span data-stu-id="1e984-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="1e984-115">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Projektijuhtimise ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1e984-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="1e984-116">Valige vahekaart **Kontsernisisesed** tab.</span><span class="sxs-lookup"><span data-stu-id="1e984-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="1e984-117">Kontsernisisese ressursiplaneerimise ja ajatabelite lubamiseks liigutage liugur asendisse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1e984-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="1e984-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1e984-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="1e984-119">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1e984-119">Select **New**.</span></span>
15. <span data-ttu-id="1e984-120">Väljal **Juriidilise isiku laenamine** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e984-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="1e984-121">Märkige ruut **Viittulu**.</span><span class="sxs-lookup"><span data-stu-id="1e984-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="1e984-122">Väljal **Vaikeajatabeli kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e984-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="1e984-123">Väljal **Vaike kulukategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e984-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="1e984-124">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1e984-124">Select **Save**.</span></span>
20. <span data-ttu-id="1e984-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1e984-125">Close the page.</span></span>
21. <span data-ttu-id="1e984-126">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Postitamine > Pearaamatu postitamise seadistus**.</span><span class="sxs-lookup"><span data-stu-id="1e984-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="1e984-127">Väljal **Pearaamatu kontotüübid** tehke valik.</span><span class="sxs-lookup"><span data-stu-id="1e984-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="1e984-128">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1e984-128">Select **New**.</span></span>
24. <span data-ttu-id="1e984-129">Uue rea väljal **Põhikonto** määrake soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="1e984-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="1e984-130">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1e984-130">Select **Save**.</span></span>
26. <span data-ttu-id="1e984-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1e984-131">Close the page.</span></span>
27. <span data-ttu-id="1e984-132">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Hinnad > Sisehind**.</span><span class="sxs-lookup"><span data-stu-id="1e984-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="1e984-133">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1e984-133">Select **New**.</span></span>
29. <span data-ttu-id="1e984-134">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="1e984-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="1e984-135">Väljal **Juriidilise isiku laenamine** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e984-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="1e984-136">Väljal **Sisehinna mudel** tehke valik.</span><span class="sxs-lookup"><span data-stu-id="1e984-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="1e984-137">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="1e984-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="1e984-138">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1e984-138">Select **Save**.</span></span>

