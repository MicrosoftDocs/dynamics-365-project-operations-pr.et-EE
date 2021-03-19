---
title: Tootepõhiste hinnapakkumiste ridade ülevaade – liht
description: See teema sisaldab teavet tootepõhiste hinnapakkumise ridadega töötamise kohta.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272563"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="72cb5-103">Tootepõhiste hinnapakkumiste ridade ülevaade – liht</span><span class="sxs-lookup"><span data-stu-id="72cb5-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="72cb5-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="72cb5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72cb5-105">Saate luua tootel põhinevaid hinnapakkumise ridu rakenduses Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="72cb5-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="72cb5-106">Tootepõhiste hinnapakkumiste ridu saab lisada käsitsi või need võivad olla tootekataloogi objektid.</span><span class="sxs-lookup"><span data-stu-id="72cb5-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="72cb5-107">Tootekataloog</span><span class="sxs-lookup"><span data-stu-id="72cb5-107">Product catalog</span></span>

<span data-ttu-id="72cb5-108">Igal tootekataloogi toodetel on vaikimisi ühik ja ühikurühm.</span><span class="sxs-lookup"><span data-stu-id="72cb5-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="72cb5-109">Kui mitmes tootes on sama atribuutide kogum, saate luua tootepere, mis kasutavad neid atribuute ühiselt.</span><span class="sxs-lookup"><span data-stu-id="72cb5-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="72cb5-110">Näiteks ettevõte müüb kordustellimuse litsentse erinevat tüüpi tarkvara jaoks.</span><span class="sxs-lookup"><span data-stu-id="72cb5-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="72cb5-111">Kõikidel kordustellimuse tarkvaradel on järgmised kaks atribuuti.</span><span class="sxs-lookup"><span data-stu-id="72cb5-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="72cb5-112">Kasutajate arv</span><span class="sxs-lookup"><span data-stu-id="72cb5-112">Number of users</span></span>
- <span data-ttu-id="72cb5-113">Kuudes mõõdetud tellimuse kestus</span><span class="sxs-lookup"><span data-stu-id="72cb5-113">A subscription duration measured in months</span></span>

<span data-ttu-id="72cb5-114">Seda tüüpi kataloogi säilitamiseks looge tootepere, mille nimi on **Kordustellimuse tarkvara** ja lisage kasutajate arv ja tellimuse keskus atribuutidena.</span><span class="sxs-lookup"><span data-stu-id="72cb5-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="72cb5-115">Järgmisena saate lisada lisada tooteperesse **Kordustellimuse tarkvara** individuaalseid tooteid.</span><span class="sxs-lookup"><span data-stu-id="72cb5-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="72cb5-116">Tootekataloogi üksuste lisamine projekti hinnapakkumisse</span><span class="sxs-lookup"><span data-stu-id="72cb5-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="72cb5-117">Lehtedel **Projekti hinnapakkumine** ja **Projekti leping** on jaotised projektipõhiste ridade ja tootepõhiste ridade jaoks.</span><span class="sxs-lookup"><span data-stu-id="72cb5-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="72cb5-118">Projektipõhiste ridade puhul sisaldab hinnapakumise rea või projekti lepingurea ripploend kõiki toote hinnakirja tooteid ja ühikuid.</span><span class="sxs-lookup"><span data-stu-id="72cb5-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="72cb5-119">Saate lisada ka tooteid, mis ei kuulu toodete hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="72cb5-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="72cb5-120">Lisaks saate valida tooted teistest hinnakirjadest või otse tootekataloogi kaudu.</span><span class="sxs-lookup"><span data-stu-id="72cb5-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="72cb5-121">Kui valite tooted otse tootekataloogi kaudu, kasutatakse toote müügihinna saamiseks selle toote vaikimisi kasutatavat hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="72cb5-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="72cb5-122">Kui vaike-hinnakirja ei määrata, määratakse hinnaks null (0).</span><span class="sxs-lookup"><span data-stu-id="72cb5-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="72cb5-123">Kui hinnapakkumise rida põhineb tootekataloogil, saate müügihinna alistada otse hinnapakkumise real.</span><span class="sxs-lookup"><span data-stu-id="72cb5-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="72cb5-124">Hinnapakkumise rida väljal **Hinnakujundus**, millel on kaks saadaolevat väärtust.</span><span class="sxs-lookup"><span data-stu-id="72cb5-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="72cb5-125">**Hinnakirja tühistamine**</span><span class="sxs-lookup"><span data-stu-id="72cb5-125">**Override Pricing**</span></span>
- <span data-ttu-id="72cb5-126">**Kasuta vaikeväärtust**</span><span class="sxs-lookup"><span data-stu-id="72cb5-126">**Use Default**</span></span>

<span data-ttu-id="72cb5-127">Kui valite suvandi **Hinnakirja tühistamine**, siis vaikimisi hinda ei määrata.</span><span class="sxs-lookup"><span data-stu-id="72cb5-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="72cb5-128">Selle asemel peate sisestama toote hinna hinnapakkumise real.</span><span class="sxs-lookup"><span data-stu-id="72cb5-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="72cb5-129">Kui valite suvandi **Kasuta vaikeväärtust**, kasutatakse vaikimisi müügihinda ja see väli on redigeerimiseks lukus.</span><span class="sxs-lookup"><span data-stu-id="72cb5-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="72cb5-130">Vaikimisi müügihinnad sisestatakse hinnapakkumise tootepõhistele ridadele.</span><span class="sxs-lookup"><span data-stu-id="72cb5-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="72cb5-131">Välja **Hinnakiri** väärtuseks seatakse **Hinnakirja tühistamine**, et saaksite hinnapakkumise ridadel redigeerida vaikimisi kasutatavat hinda.</span><span class="sxs-lookup"><span data-stu-id="72cb5-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="72cb5-132">See on rakendusele Project Operations omane rakenduse Dynamics 365 Sales tootepõhiste ridade käitumise alistamiseks.</span><span class="sxs-lookup"><span data-stu-id="72cb5-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]