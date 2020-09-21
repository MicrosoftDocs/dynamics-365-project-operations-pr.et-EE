---
title: Kontsernisisese projekti arveldamise konfigureerimine
description: Selles teemas kirjeldatakse, kuidas seadistada projekti arveldamist kahe ettevõtte vahel.
author: KimANelson
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
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750923"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="2d363-103">Kontsernisisese projekti arveldamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2d363-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d363-104">Selles teemas kirjeldatakse, kuidas seadistada projekti arveldamist kahe ettevõtte vahel.</span><span class="sxs-lookup"><span data-stu-id="2d363-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="2d363-105">Selle toiming kasutab USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="2d363-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2d363-106">Minge navigeerimispaani jaotisse **Moodulid > Ostureskontro > Tarnijad > Kõik tarnijad**.</span><span class="sxs-lookup"><span data-stu-id="2d363-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="2d363-107">Loendis **Kõik tarnijad** leidke ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2d363-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="2d363-108">Valige paanil Toiming **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="2d363-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="2d363-109">Valige **Kontsernisisesed**.</span><span class="sxs-lookup"><span data-stu-id="2d363-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="2d363-110">Määrake valiku **Aktiivne** väärtuseks **Jah**, et lubada kontsernisisene kauplemine.</span><span class="sxs-lookup"><span data-stu-id="2d363-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="2d363-111">Väljal **Kliendi ettevõte** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2d363-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="2d363-112">Väljal **Minu konto** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2d363-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="2d363-113">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2d363-113">Select **Save**.</span></span>
9. <span data-ttu-id="2d363-114">Avalehe tagasipöördumiseks sulgege leheküljed.</span><span class="sxs-lookup"><span data-stu-id="2d363-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="2d363-115">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Projektijuhtimise ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2d363-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="2d363-116">Valige vahekaart **Kontsernisisesed** tab.</span><span class="sxs-lookup"><span data-stu-id="2d363-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="2d363-117">Kontsernisisese ressursiplaneerimise ja ajatabelite lubamiseks liigutage liugur asendisse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="2d363-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="2d363-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2d363-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2d363-119">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2d363-119">Select **New**.</span></span>
15. <span data-ttu-id="2d363-120">Väljal **Juriidilise isiku laenamine** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2d363-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="2d363-121">Märkige ruut **Viittulu**.</span><span class="sxs-lookup"><span data-stu-id="2d363-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="2d363-122">Väljal **Vaikeajatabeli kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2d363-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="2d363-123">Väljal **Vaike kulukategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2d363-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="2d363-124">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2d363-124">Select **Save**.</span></span>
20. <span data-ttu-id="2d363-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2d363-125">Close the page.</span></span>
21. <span data-ttu-id="2d363-126">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Postitamine > Pearaamatu postitamise seadistus**.</span><span class="sxs-lookup"><span data-stu-id="2d363-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="2d363-127">Väljal **Pearaamatu kontotüübid** tehke valik.</span><span class="sxs-lookup"><span data-stu-id="2d363-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="2d363-128">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2d363-128">Select **New**.</span></span>
24. <span data-ttu-id="2d363-129">Uue rea väljal **Põhikonto** määrake soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="2d363-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="2d363-130">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2d363-130">Select **Save**.</span></span>
26. <span data-ttu-id="2d363-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2d363-131">Close the page.</span></span>
27. <span data-ttu-id="2d363-132">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Seadistus > Hinnad > Sisehind**.</span><span class="sxs-lookup"><span data-stu-id="2d363-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="2d363-133">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2d363-133">Select **New**.</span></span>
29. <span data-ttu-id="2d363-134">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2d363-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="2d363-135">Väljal **Juriidilise isiku laenamine** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2d363-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="2d363-136">Väljal **Sisehinna mudel** tehke valik.</span><span class="sxs-lookup"><span data-stu-id="2d363-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="2d363-137">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="2d363-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="2d363-138">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2d363-138">Select **Save**.</span></span>

