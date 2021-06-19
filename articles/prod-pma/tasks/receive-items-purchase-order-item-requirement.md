---
title: Ostutellimuses üksuste vastuvõtmine üksuse nõudest
description: Selles teemas selgitatakse, kuidas võtta üksuse nõudest tulenevalt võta vastu ostutellimuse eest saadud üksused.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011681"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="52f1c-103">Ostutellimuses üksuste vastuvõtmine üksuse nõudest</span><span class="sxs-lookup"><span data-stu-id="52f1c-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52f1c-104">Selles teemas selgitatakse, kuidas võtta üksuse nõudest tulenevalt võta vastu ostutellimuse eest saadud üksused.</span><span class="sxs-lookup"><span data-stu-id="52f1c-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="52f1c-105">Üksuse kande asemel nõuet kasutades saate planeerida kohaletoimetamise vahetult enne üksuse tegelikku kasutamist, luua ostutellimuse, kaasata üksus kaubandusleppe raamistikku ning kaasata üksuse nõue tootmisplaneerimises.</span><span class="sxs-lookup"><span data-stu-id="52f1c-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="52f1c-106">Selle toiming kasutab USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="52f1c-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="52f1c-107">Minge navigeerimispaani jaotisse **Moodulid > Projektijuhtimine ja raamatupidamine > Projektid > Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="52f1c-108">Valige loendis soovitud real linki.</span><span class="sxs-lookup"><span data-stu-id="52f1c-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="52f1c-109">Valige paanil Toiming suvand **Plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="52f1c-110">Valige **Üksuse nõuded**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="52f1c-111">Tehke valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-111">Select **New**.</span></span>
6. <span data-ttu-id="52f1c-112">Uues rollis sisestage või valige väärtus väljal **Üksuse number**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="52f1c-113">Väljale **Kogus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="52f1c-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="52f1c-114">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-114">Select **Save**.</span></span>
9. <span data-ttu-id="52f1c-115">Valige paanil Toiming käsk **Halda**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="52f1c-116">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-116">Select **Functions**.</span></span>
11. <span data-ttu-id="52f1c-117">Valige suvand **Ostutellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="52f1c-118">Valige märkeruut **Kaasa kõik**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="52f1c-119">Väljal **Hankija konto** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="52f1c-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="52f1c-120">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-120">Select **OK**.</span></span>
15. <span data-ttu-id="52f1c-121">Minge navigeerimispaani jaotisse **Moodulid > Ostureskontro > Ostutellimused > Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="52f1c-122">Valige loendis soovitud real linki.</span><span class="sxs-lookup"><span data-stu-id="52f1c-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="52f1c-123">Valige paanil Toiming suvand **Osta**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="52f1c-124">Tehke valik **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="52f1c-125">Valige paanil Toiming suvand **Saamine**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="52f1c-126">Valige **Toote kviitung**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="52f1c-127">Tippige väljale **Toote kviitung** väärtus.</span><span class="sxs-lookup"><span data-stu-id="52f1c-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="52f1c-128">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="52f1c-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]