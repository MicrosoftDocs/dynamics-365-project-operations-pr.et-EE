---
title: Tootepõhiste hinnapakkumiste ridade kuluarvutus
description: Selles teemas antakse teavet tootepõhisele hinnapakkumise reale omahinna rakendamise kohta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906134"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="19f5b-103">Tootepõhiste hinnapakkumiste ridade kuluarvutus</span><span class="sxs-lookup"><span data-stu-id="19f5b-103">Costing product-based quote lines</span></span>

<span data-ttu-id="19f5b-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="19f5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="19f5b-105">Rakenduse Dynamics 365 Project Operations projektipõhised hinnapakkumise ridadel on ka väli **Omahind**.</span><span class="sxs-lookup"><span data-stu-id="19f5b-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="19f5b-106">Seda välja kasutatakse hinnapakkumise real ja allavooli tasuvuse arvutustes toote omahinna jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="19f5b-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="19f5b-107">Kui kataloogitoote jaoks on loodud projektipõhine hinnapakkumise rida, võetakse projektipõhise hinnapakkumise rea kulu vaikimisi tootekataloogi väljalt **Standardne kulu**.</span><span class="sxs-lookup"><span data-stu-id="19f5b-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="19f5b-108">Tootekataloogi standardkulu väli seadistatakse organisatsiooni põhivaluutas.</span><span class="sxs-lookup"><span data-stu-id="19f5b-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="19f5b-109">Tootepõhise hinnapakkumise rea vaikimisi ühiku kulu teisendatakse hinnapakkumise müügi valuutasse.</span><span class="sxs-lookup"><span data-stu-id="19f5b-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="19f5b-110">Tootepõhise hinnapakkumise rea ühiku kulu</span><span class="sxs-lookup"><span data-stu-id="19f5b-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="19f5b-111">Tootepõhise hinnapakkumise rea üksuse kulu omamise eesmärk oon võimaldada iga toote müügi jaoks erinevad kulud.</span><span class="sxs-lookup"><span data-stu-id="19f5b-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="19f5b-112">See pole tavaline stsenaarium, kuid mõnikord võib tarnija sõltuvalt lõpliku müügi kliendist alandada toote maksumust.</span><span class="sxs-lookup"><span data-stu-id="19f5b-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="19f5b-113">Näiteks:</span><span class="sxs-lookup"><span data-stu-id="19f5b-113">For example:</span></span>

<span data-ttu-id="19f5b-114">Fabrikami robootika installib ettevõtte A Datum Corporation koosteliinidele robotõlgasid.</span><span class="sxs-lookup"><span data-stu-id="19f5b-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="19f5b-115">Fabrikami pakub paigaldusteenused, kuid robotõlgade tootja on Trey robootika.</span><span class="sxs-lookup"><span data-stu-id="19f5b-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="19f5b-116">Kui ettevõtte A Datum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey robotõlgade jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.</span><span class="sxs-lookup"><span data-stu-id="19f5b-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="19f5b-117">Sel juhul loob Fabrikam robotõlgade jaoks tootepõhise hinnapakkumise rea ja sisestab selle hinnapakumise jaoks ühiku maksumuse jaoks erihinna.</span><span class="sxs-lookup"><span data-stu-id="19f5b-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="19f5b-118">See maksumus erineb ettevõtte Trey robotõlgade tavamaksumusest.</span><span class="sxs-lookup"><span data-stu-id="19f5b-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
