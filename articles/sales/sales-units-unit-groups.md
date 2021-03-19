---
title: Ühikud ja ühikurühmad
description: Selles teemas antakse teavet ühikute ja ühikurühmade loomise kohta rakenduses Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277333"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="4234f-103">Ühikud ja ühikurühmad</span><span class="sxs-lookup"><span data-stu-id="4234f-103">Units and unit groups</span></span>

<span data-ttu-id="4234f-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4234f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4234f-105">Ühikud on kogused või mõõtühikud, milles tooteid või teenuseid müüte.</span><span class="sxs-lookup"><span data-stu-id="4234f-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="4234f-106">Näiteks kui müüte aiatarvikuid, võite müüa seemneid pakkide, karpide ja kaubaalustena.</span><span class="sxs-lookup"><span data-stu-id="4234f-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="4234f-107">Ühikurühm on nende ühikute kogum.</span><span class="sxs-lookup"><span data-stu-id="4234f-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="4234f-108">Selle teema juhiste täitmiseks veenduge, et teile on määratud süsteemiadministraatori või müügiesindaja halduri roll või samaväärsed õigused.</span><span class="sxs-lookup"><span data-stu-id="4234f-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="4234f-109">Ühikurühma loomine</span><span class="sxs-lookup"><span data-stu-id="4234f-109">Create a unit group</span></span>

1. <span data-ttu-id="4234f-110">Valige saidikaardil **Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="4234f-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="4234f-111">Valige **Uus** ja sisestage ühiku nimi dialoogiaknasse **Ühikurühma loomine**.</span><span class="sxs-lookup"><span data-stu-id="4234f-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="4234f-112">Sisestage väljale **Põhiüksus** väikseim peamine mõõtühik, milles toodet müüakse.</span><span class="sxs-lookup"><span data-stu-id="4234f-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="4234f-113">Näiteks võite sisestada "tk" või "unts".</span><span class="sxs-lookup"><span data-stu-id="4234f-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="4234f-114">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4234f-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="4234f-115">Ühikute lisamine ühikurühmale</span><span class="sxs-lookup"><span data-stu-id="4234f-115">Add units to a unit group</span></span>

1. <span data-ttu-id="4234f-116">Avage ühikurühm ja valige vahekaardil **Seostuvad** valik **Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="4234f-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="4234f-117">Näete, et põhiühik on juba lisatud.</span><span class="sxs-lookup"><span data-stu-id="4234f-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="4234f-118">Valige käsk **Lisa uus ühik** ja klõpsake lehel **Kiirloomine: ühik** väljal **Nimi** ja sisestage ühikule nimi.</span><span class="sxs-lookup"><span data-stu-id="4234f-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="4234f-119">Sisestage väljale **Kogus** ühikus sisalduv kogus.</span><span class="sxs-lookup"><span data-stu-id="4234f-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="4234f-120">Kui karp sisaldab nt kahte tükki, sisestage „2”.</span><span class="sxs-lookup"><span data-stu-id="4234f-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="4234f-121">Valige väljal **Põhiühik** põhiühik, et luua ühiku jaoks madalaim mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="4234f-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="4234f-122">Näiteks võite valida "Tk".</span><span class="sxs-lookup"><span data-stu-id="4234f-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="4234f-123">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4234f-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]