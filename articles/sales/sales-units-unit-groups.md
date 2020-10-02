---
title: Ühikud ja ühikurühmad
description: Selles teemas antakse teavet ühikute ja ühikurühmade loomise kohta rakenduses Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898751"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="7c293-103">Ühikud ja ühikurühmad</span><span class="sxs-lookup"><span data-stu-id="7c293-103">Units and unit groups</span></span>

<span data-ttu-id="7c293-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="7c293-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7c293-105">Ühikud on kogused või mõõtühikud, milles tooteid või teenuseid müüte.</span><span class="sxs-lookup"><span data-stu-id="7c293-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="7c293-106">Näiteks kui müüte aiatarvikuid, võite müüa seemneid pakkide, karpide ja kaubaalustena.</span><span class="sxs-lookup"><span data-stu-id="7c293-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="7c293-107">Ühikurühm on nende ühikute kogum.</span><span class="sxs-lookup"><span data-stu-id="7c293-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="7c293-108">Selle teema juhiste täitmiseks veenduge, et teile on määratud süsteemiadministraatori või müügiesindaja halduri roll või samaväärsed õigused.</span><span class="sxs-lookup"><span data-stu-id="7c293-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="7c293-109">Ühikurühma loomine</span><span class="sxs-lookup"><span data-stu-id="7c293-109">Create a unit group</span></span>

1. <span data-ttu-id="7c293-110">Valige saidikaardil **Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="7c293-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="7c293-111">Valige **Uus** ja sisestage ühiku nimi dialoogiaknasse **Ühikurühma loomine**.</span><span class="sxs-lookup"><span data-stu-id="7c293-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="7c293-112">Sisestage väljale **Põhiüksus** väikseim peamine mõõtühik, milles toodet müüakse.</span><span class="sxs-lookup"><span data-stu-id="7c293-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="7c293-113">Näiteks võite sisestada "tk" või "unts".</span><span class="sxs-lookup"><span data-stu-id="7c293-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="7c293-114">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c293-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="7c293-115">Ühikute lisamine ühikurühmale</span><span class="sxs-lookup"><span data-stu-id="7c293-115">Add units to a unit group</span></span>

1. <span data-ttu-id="7c293-116">Avage ühikurühm ja valige vahekaardil **Seostuvad** valik **Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="7c293-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="7c293-117">Näete, et põhiühik on juba lisatud.</span><span class="sxs-lookup"><span data-stu-id="7c293-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="7c293-118">Valige käsk **Lisa uus ühik** ja klõpsake lehel **Kiirloomine: ühik** väljal **Nimi** ja sisestage ühikule nimi.</span><span class="sxs-lookup"><span data-stu-id="7c293-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="7c293-119">Sisestage väljale **Kogus** ühikus sisalduv kogus.</span><span class="sxs-lookup"><span data-stu-id="7c293-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="7c293-120">Kui karp sisaldab nt kahte tükki, sisestage „2”.</span><span class="sxs-lookup"><span data-stu-id="7c293-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="7c293-121">Valige väljal **Põhiühik** põhiühik, et luua ühiku jaoks madalaim mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="7c293-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="7c293-122">Näiteks võite valida "Tk".</span><span class="sxs-lookup"><span data-stu-id="7c293-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="7c293-123">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7c293-123">Select **Save**:</span></span>
