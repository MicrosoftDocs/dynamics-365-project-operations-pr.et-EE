---
title: Tootepõhiste lepinguridade kulu – liht
description: Selles teemas antakse teavet loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764454"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="58ca9-103">Tootepõhiste lepinguridade kulu – liht</span><span class="sxs-lookup"><span data-stu-id="58ca9-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="58ca9-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="58ca9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="58ca9-105">Tootepõhised lepinguread rakenduses Dynamics 365 Project Operations sisaldavad välja **Omahind**, mis talletab toote omahinna allavoolu kasumlikkuse arvestuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="58ca9-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="58ca9-106">Kui kataloogitoote jaoks luuakse tootepõhine lepingurida, siis rea kulu vaikeväärtuseks on tootekataloogi väli **Standardkulu**.</span><span class="sxs-lookup"><span data-stu-id="58ca9-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="58ca9-107">Tootekataloogi väli **Standardkulu** seadistatakse organisatsiooni põhivaluutas.</span><span class="sxs-lookup"><span data-stu-id="58ca9-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="58ca9-108">Kui ühiku omahind on lepingureal vaikimisi määratud, teisendatakse see lepingus toodud müügivaluutaks.</span><span class="sxs-lookup"><span data-stu-id="58ca9-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="58ca9-109">Tootepõhise lepingurea ühiku omahind</span><span class="sxs-lookup"><span data-stu-id="58ca9-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="58ca9-110">Tootepõhise lepingurea ühiku omahind võimaldada iga ühiku müügi jaoks erineva toote omahinna.</span><span class="sxs-lookup"><span data-stu-id="58ca9-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="58ca9-111">Kuigi see ei ole alati vajalik, on olemas teatud stsenaariumid, mille korral tarnija teeb toote omahinna osas kliendile allahindluse.</span><span class="sxs-lookup"><span data-stu-id="58ca9-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="58ca9-112">Siin on ühe võimaliku stsenaariumi näide.</span><span class="sxs-lookup"><span data-stu-id="58ca9-112">Consider the following scenario:</span></span>

<span data-ttu-id="58ca9-113">Fabrikami robootika installib ettevõtte Adatum Corporation koosteliinidele robotõlgasid.</span><span class="sxs-lookup"><span data-stu-id="58ca9-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="58ca9-114">Fabrikam pakub paigaldusteenuseid, kuid robotkäed on pärit ettevõttelt Trey Research.</span><span class="sxs-lookup"><span data-stu-id="58ca9-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="58ca9-115">Kui ettevõtte Adatum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey Research jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.</span><span class="sxs-lookup"><span data-stu-id="58ca9-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="58ca9-116">Sel juhul loob Fabrikam robotkäte jaoks tootepõhise lepingurea.</span><span class="sxs-lookup"><span data-stu-id="58ca9-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="58ca9-117">Selle lepingu jaoks sisestatakse kulu üksuse kohta.</span><span class="sxs-lookup"><span data-stu-id="58ca9-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="58ca9-118">Kulu erineb Trey Research robotkäte kulust.</span><span class="sxs-lookup"><span data-stu-id="58ca9-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
