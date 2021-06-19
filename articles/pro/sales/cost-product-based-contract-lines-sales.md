---
title: Tootepõhiste lepinguridade kulu – liht
description: Selles teemas antakse teavet loomise kohta.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003536"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="d6aab-103">Tootepõhiste lepinguridade kulu – liht</span><span class="sxs-lookup"><span data-stu-id="d6aab-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="d6aab-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="d6aab-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d6aab-105">Tootepõhised lepinguread rakenduses Dynamics 365 Project Operations sisaldavad välja **Omahind**, mis talletab toote omahinna allavoolu kasumlikkuse arvestuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="d6aab-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="d6aab-106">Kui kataloogitoote jaoks luuakse tootepõhine lepingurida, siis rea kulu vaikeväärtuseks on tootekataloogi väli **Standardkulu**.</span><span class="sxs-lookup"><span data-stu-id="d6aab-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="d6aab-107">Tootekataloogi väli **Standardkulu** seadistatakse organisatsiooni põhivaluutas.</span><span class="sxs-lookup"><span data-stu-id="d6aab-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="d6aab-108">Kui ühiku omahind on lepingureal vaikimisi määratud, teisendatakse see lepingus toodud müügivaluutaks.</span><span class="sxs-lookup"><span data-stu-id="d6aab-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="d6aab-109">Tootepõhise lepingurea ühiku omahind</span><span class="sxs-lookup"><span data-stu-id="d6aab-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="d6aab-110">Tootepõhise lepingurea ühiku omahind võimaldada iga ühiku müügi jaoks erineva toote omahinna.</span><span class="sxs-lookup"><span data-stu-id="d6aab-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="d6aab-111">Kuigi see ei ole alati vajalik, on olemas teatud stsenaariumid, mille korral tarnija teeb toote omahinna osas kliendile allahindluse.</span><span class="sxs-lookup"><span data-stu-id="d6aab-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="d6aab-112">Siin on ühe võimaliku stsenaariumi näide.</span><span class="sxs-lookup"><span data-stu-id="d6aab-112">Consider the following scenario:</span></span>

<span data-ttu-id="d6aab-113">Fabrikami robootika installib ettevõtte Adatum Corporation koosteliinidele robotõlgasid.</span><span class="sxs-lookup"><span data-stu-id="d6aab-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="d6aab-114">Fabrikam pakub paigaldusteenuseid, kuid robotkäed on pärit ettevõttelt Trey Research.</span><span class="sxs-lookup"><span data-stu-id="d6aab-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="d6aab-115">Kui ettevõtte Adatum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey Research jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.</span><span class="sxs-lookup"><span data-stu-id="d6aab-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="d6aab-116">Sel juhul loob Fabrikam robotkäte jaoks tootepõhise lepingurea.</span><span class="sxs-lookup"><span data-stu-id="d6aab-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="d6aab-117">Selle lepingu jaoks sisestatakse kulu üksuse kohta.</span><span class="sxs-lookup"><span data-stu-id="d6aab-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="d6aab-118">Kulu erineb Trey Research robotkäte kulust.</span><span class="sxs-lookup"><span data-stu-id="d6aab-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]