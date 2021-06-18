---
title: Projekti ostutellimused
description: Selles artiklis kirjeldatakse mitmesuguseid meetodeid, mida saate kasutada projekti jaoks ostutellimuste loomiseks. Kasutatav meetod oleneb ostutellimuse eesmärgist ja millal ostetud üksuseid kasutatakse ning need projekti kuludesse kantakse.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999351"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="f1985-104">Projekti ostutellimused</span><span class="sxs-lookup"><span data-stu-id="f1985-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1985-105">Selles artiklis kirjeldatakse mitmesuguseid meetodeid, mida saate kasutada projekti jaoks ostutellimuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f1985-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="f1985-106">Kasutatav meetod oleneb ostutellimuse eesmärgist ja millal ostetud üksuseid kasutatakse ning need projekti kuludesse kantakse.</span><span class="sxs-lookup"><span data-stu-id="f1985-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="f1985-107">Ostutellimuse loomise meetodid</span><span class="sxs-lookup"><span data-stu-id="f1985-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="f1985-108">Saate kasutada ühte järgmistest meetoditest, et luua suvandis Projektihaldus ja raamatupidamine ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="f1985-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="f1985-109">Ostutellimuse eesmärk määratleb, millal ostutellimust kasutatakse, ja seega, millal kantakse üksused projekti kuludesse.</span><span class="sxs-lookup"><span data-stu-id="f1985-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1985-110">Meetod</span><span class="sxs-lookup"><span data-stu-id="f1985-110">Method</span></span></th>
<th><span data-ttu-id="f1985-111">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="f1985-111">Purpose</span></span></th>
<th><span data-ttu-id="f1985-112">Üksuste kasutamine</span><span class="sxs-lookup"><span data-stu-id="f1985-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f1985-113">Looge ostutellimus otse projektist.</span><span class="sxs-lookup"><span data-stu-id="f1985-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="f1985-114">Kasutage seda meetodit väliselt tarnijalt üksuste ostmiseks projektis kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="f1985-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="f1985-115">Ostutellimuse saate luua kahel viisidel.</span><span class="sxs-lookup"><span data-stu-id="f1985-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="f1985-116">Projektist endast.</span><span class="sxs-lookup"><span data-stu-id="f1985-116">From the project itself.</span></span> <span data-ttu-id="f1985-117">Sellisel juhul on projekt juba ostutellimuse jaoks määratletud.</span><span class="sxs-lookup"><span data-stu-id="f1985-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="f1985-118">Navigeerides projekti ostutellimusele.</span><span class="sxs-lookup"><span data-stu-id="f1985-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="f1985-119">Ostutellimuse loomiseks peate valima nii hankija kui ka projekti.</span><span class="sxs-lookup"><span data-stu-id="f1985-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="f1985-120">Üksused võetakse kasutusele, kui tarnija arvet värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="f1985-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1985-121">Looge ostutellimus müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="f1985-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="f1985-122">Kasutage seda meetodit üksuste ostmiseks, kui loote projektist müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="f1985-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="f1985-123">Üksused võetakse kasutusele, kui müügitellimuse eest on kliendile saadetud arve.</span><span class="sxs-lookup"><span data-stu-id="f1985-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1985-124">Müügitellimuse loomine üksuse nõudest.</span><span class="sxs-lookup"><span data-stu-id="f1985-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="f1985-125">Kasutage seda meetodit üksuste ostmiseks, kui loote projektist üksuse nõude.</span><span class="sxs-lookup"><span data-stu-id="f1985-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="f1985-126">Üksused võetakse kasutusele, kui üksuse nõude saatelehte värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="f1985-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="f1985-127">Hankija arve või saatelehe uuendamisel palutakse teil uuendada saateleht nõutavale üksusele.</span><span class="sxs-lookup"><span data-stu-id="f1985-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="f1985-128">Lisateavet vt teemast [Üksuse nõudest ostutellimuse üksuste vastuvõtmine](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="f1985-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]