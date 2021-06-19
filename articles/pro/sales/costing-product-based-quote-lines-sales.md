---
title: Tootepõhiste hinnapakkumiste ridade kuluarvutus
description: Selles teemas antakse teavet tootepõhisele hinnapakkumise reale omahinna rakendamise kohta.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003446"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="bd58c-103">Tootepõhiste hinnapakkumiste ridade kuluarvutus</span><span class="sxs-lookup"><span data-stu-id="bd58c-103">Costing product-based quote lines</span></span>

<span data-ttu-id="bd58c-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="bd58c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bd58c-105">Tootepõhistel hinnapakkumise ridadel on rakenduses Dynamics 365 Project Operations ka väli **Omahind**.</span><span class="sxs-lookup"><span data-stu-id="bd58c-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="bd58c-106">Seda välja kasutatakse hinnapakkumise real ja allavooli tasuvuse arvutustes toote omahinna jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="bd58c-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="bd58c-107">Kui kataloogitoote jaoks on loodud projektipõhine hinnapakkumise rida, võetakse projektipõhise hinnapakkumise rea kulu vaikimisi tootekataloogi väljalt **Standardne kulu**.</span><span class="sxs-lookup"><span data-stu-id="bd58c-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="bd58c-108">Tootekataloogi standardkulu väli seadistatakse organisatsiooni põhivaluutas.</span><span class="sxs-lookup"><span data-stu-id="bd58c-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="bd58c-109">Tootepõhise hinnapakkumise rea vaikimisi ühiku kulu teisendatakse hinnapakkumise müügi valuutasse.</span><span class="sxs-lookup"><span data-stu-id="bd58c-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="bd58c-110">Tootepõhise hinnapakkumise rea ühiku kulu</span><span class="sxs-lookup"><span data-stu-id="bd58c-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="bd58c-111">Tootepõhise hinnapakkumise rea üksuse kulu omamise eesmärk oon võimaldada iga toote müügi jaoks erinevad kulud.</span><span class="sxs-lookup"><span data-stu-id="bd58c-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="bd58c-112">See pole tavaline stsenaarium, kuid mõnikord võib tarnija sõltuvalt lõpliku müügi kliendist alandada toote maksumust.</span><span class="sxs-lookup"><span data-stu-id="bd58c-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="bd58c-113">Näiteks:</span><span class="sxs-lookup"><span data-stu-id="bd58c-113">For example:</span></span>

<span data-ttu-id="bd58c-114">Fabrikami robootika installib ettevõtte A Datum Corporation koosteliinidele robotõlgasid.</span><span class="sxs-lookup"><span data-stu-id="bd58c-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="bd58c-115">Fabrikami pakub paigaldusteenused, kuid robotõlgade tootja on Trey robootika.</span><span class="sxs-lookup"><span data-stu-id="bd58c-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="bd58c-116">Kui ettevõtte A Datum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey robotõlgade jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.</span><span class="sxs-lookup"><span data-stu-id="bd58c-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="bd58c-117">Sel juhul loob Fabrikam robotõlgade jaoks tootepõhise hinnapakkumise rea ja sisestab selle hinnapakumise jaoks ühiku maksumuse jaoks erihinna.</span><span class="sxs-lookup"><span data-stu-id="bd58c-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="bd58c-118">See maksumus erineb ettevõtte Trey robotõlgade tavamaksumusest.</span><span class="sxs-lookup"><span data-stu-id="bd58c-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]