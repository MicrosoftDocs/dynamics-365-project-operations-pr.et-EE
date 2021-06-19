---
title: Toote hinnakirjad
description: Selles teemas jagatakse teavet kataloogi hinnakujunduse hinnakirjade kohta, mida kasutatakse projekti hinnapakkumiste ja lepingute jaoks.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004931"
---
# <a name="product-price-lists"></a><span data-ttu-id="9af7a-103">Toote hinnakirjad</span><span class="sxs-lookup"><span data-stu-id="9af7a-103">Product price lists</span></span>

<span data-ttu-id="9af7a-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="9af7a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="9af7a-105">Rakenduses Project Operations toetavad olemid **Toote hinnakirjad** ja seotud hinnakirjaüksused toodete hinnakujunduse funktsiooni projektipõhise hinnapakkumise ja lepinguridadega.</span><span class="sxs-lookup"><span data-stu-id="9af7a-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="9af7a-106">Projektides kasutatavate toodete puhul kasutatakse projekti hinnakirjade hinnakirjaüksuseid.</span><span class="sxs-lookup"><span data-stu-id="9af7a-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="9af7a-107">Tooted tuleb seadistada nii, et neil oleksid tootekataloogi vaikimisi kulu ja hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="9af7a-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="9af7a-108">Kasutage vaikimisi kulu ja hinnakirja hindade konfigureerimiseks loendi hinda, standardkulu ja praegust kulu.</span><span class="sxs-lookup"><span data-stu-id="9af7a-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="9af7a-109">Vaikimisi kasutatakse hinnakirja hindu hinnapakkumise real või projekti lepingurea korral ainult juhul, kui süsteem ei leia hinnapakkumise või projekti lepingu jaoks hinnakirja rida selle toote jaoks.</span><span class="sxs-lookup"><span data-stu-id="9af7a-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="9af7a-110">Tootekataloogi ridade omahinda saab muuta hinnapakkumiste vahel.</span><span class="sxs-lookup"><span data-stu-id="9af7a-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="9af7a-111">See võimalus on oluline, kuna kui te kulusid täpselt ei jälgi, ei saa te projekti kaasamisel määrata operatiivset kasumit.</span><span class="sxs-lookup"><span data-stu-id="9af7a-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="9af7a-112">Vaikimisi on toote standardhind omahind.</span><span class="sxs-lookup"><span data-stu-id="9af7a-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="9af7a-113">Vaikimisi kasutatava omahinda saab hinnapakkumise real uuendada juhul, kui selle hinnapakkumise jaoks on teistsugune kulumäär.</span><span class="sxs-lookup"><span data-stu-id="9af7a-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="9af7a-114">Hinnakirjaüksused</span><span class="sxs-lookup"><span data-stu-id="9af7a-114">Price list items</span></span>

<span data-ttu-id="9af7a-115">Tooteid saate tootekataloogist lisada erinevatesse hinnakirjadesse.</span><span class="sxs-lookup"><span data-stu-id="9af7a-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="9af7a-116">Toodete hinnakirja read viitavad alati kindlale ühikule.</span><span class="sxs-lookup"><span data-stu-id="9af7a-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="9af7a-117">Hinnakirjaüksuse toote hinda saab konfigureerida valuuta summana.</span><span class="sxs-lookup"><span data-stu-id="9af7a-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="9af7a-118">Alternatiivina saab seda konfigureerida loendi hinna, praeguse kulumäära või standardse kulumäära funktsioonina.</span><span class="sxs-lookup"><span data-stu-id="9af7a-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="9af7a-119">Hinnakujunduse funktsionaalsus toetab mitmesuguseid ümardamise võimalusi, kui toote hinnad on konfigureeritud loendi hinna, standardkulu või praeguse kulu funktsioonina.</span><span class="sxs-lookup"><span data-stu-id="9af7a-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="9af7a-120">Lisaks mitme hinna meetodi ja ümardamise suvandi kasutamisele saate allahindluse loendeid seostada hinnakirja üksustega.</span><span class="sxs-lookup"><span data-stu-id="9af7a-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="9af7a-121">Toote vaikehinnakiri</span><span class="sxs-lookup"><span data-stu-id="9af7a-121">Default product price list</span></span>
<span data-ttu-id="9af7a-122">Igal kliendi kirjel on väli **Vaikehinnakiri**, kus saate määrata hinnakirja, mis vastab kliendi valuutale.</span><span class="sxs-lookup"><span data-stu-id="9af7a-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="9af7a-123">Sellele väljale ei sisestata automaatselt vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="9af7a-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="9af7a-124">Kui konkreetse kliendiga on olemas kohandatud hinnakujunduse leping, saate seda välja kasutada hinnakirja seostamiseks selle kliendiga.</span><span class="sxs-lookup"><span data-stu-id="9af7a-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="9af7a-125">Müügivõimaluse, hinnapakkumise ja projekti lepingu olemid kasutavad vaikimisi toodete hinnakirja sisestamiseks järgmist tellimust.</span><span class="sxs-lookup"><span data-stu-id="9af7a-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="9af7a-126">Sama tellimust kasutatakse projekti hinnakirja jaoks.</span><span class="sxs-lookup"><span data-stu-id="9af7a-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="9af7a-127">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="9af7a-127">Quote</span></span>
2.  <span data-ttu-id="9af7a-128">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="9af7a-128">Opportunity</span></span>
3.  <span data-ttu-id="9af7a-129">Klient</span><span class="sxs-lookup"><span data-stu-id="9af7a-129">Customer</span></span>
4.  <span data-ttu-id="9af7a-130">Globaalsätted</span><span class="sxs-lookup"><span data-stu-id="9af7a-130">Global settings</span></span> 

<span data-ttu-id="9af7a-131">Vaikimisi loetleb hinnapakkumise väli **Toode** kõik hinnapakkumise toodete hinnakirja aktiivsed tooted.</span><span class="sxs-lookup"><span data-stu-id="9af7a-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="9af7a-132">Kui toode on inaktiveeritud või kui see on toote mustand, siis seda loendis pole, isegi kui see on hinnakirjas.</span><span class="sxs-lookup"><span data-stu-id="9af7a-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="9af7a-133">Tootekataloogi read lisatakse arve ridadena esimesel arvel, mis on loodud projekti lepingu jaoks.</span><span class="sxs-lookup"><span data-stu-id="9af7a-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="9af7a-134">Arve mustandi korral saab neid arve ridu kustutada.</span><span class="sxs-lookup"><span data-stu-id="9af7a-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="9af7a-135">Sel juhul kuvatakse read järgneval arvel, kuni need arveldatakse, või kuni kliendile saadetakse arve.</span><span class="sxs-lookup"><span data-stu-id="9af7a-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="9af7a-136">Te ei saa arve rea osalist kogust arveldada.</span><span class="sxs-lookup"><span data-stu-id="9af7a-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="9af7a-137">Kui projekti lepingujärgsed toote seeriad on arveldatud, luuakse tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="9af7a-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="9af7a-138">Need tegelikud näitajad pole seostatud projekti olemiga lingitud.</span><span class="sxs-lookup"><span data-stu-id="9af7a-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="9af7a-139">Teisisõnu ei sõltu tootepõhise projekti lepinguread mis tahes projektil põhinevast kasutusest.</span><span class="sxs-lookup"><span data-stu-id="9af7a-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
