---
title: Tootepõhiste lepinguridade ülevaade – liht
description: Selles teemas antakse teavet tootepõhiste lepinguridade kohta.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369731"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="90f61-103">Tootepõhiste lepinguridade ülevaade – liht</span><span class="sxs-lookup"><span data-stu-id="90f61-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="90f61-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="90f61-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90f61-105">Saate luua tootel põhinevaid lepinguridu rakenduses Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="90f61-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="90f61-106">Tootepõhiseid lepinguread võivad olla käsitsi loodud read või need võivad olla tootekataloogi objektid.</span><span class="sxs-lookup"><span data-stu-id="90f61-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="90f61-107">Tootekataloog</span><span class="sxs-lookup"><span data-stu-id="90f61-107">Product catalog</span></span>

<span data-ttu-id="90f61-108">Tootekataloogi toodetel on vaikimisi ühik ja ühikurühm.</span><span class="sxs-lookup"><span data-stu-id="90f61-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="90f61-109">Kui mitmes tootes on sama atribuutide kogum, saate luua ka tootepere, millel on ka need atribuudid.</span><span class="sxs-lookup"><span data-stu-id="90f61-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="90f61-110">Kõik ühe tootepere tooted pärivad sama hulga atribuute.</span><span class="sxs-lookup"><span data-stu-id="90f61-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="90f61-111">Näiteks ettevõte müüb kordustellimuse litsentse erinevat tüüpi tarkvara jaoks.</span><span class="sxs-lookup"><span data-stu-id="90f61-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="90f61-112">Kõikidel kordustellimuse tarkvaradel on järgmised kaks atribuuti.</span><span class="sxs-lookup"><span data-stu-id="90f61-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="90f61-113">Kasutajate arv</span><span class="sxs-lookup"><span data-stu-id="90f61-113">Number of users</span></span>
- <span data-ttu-id="90f61-114">Kordustellimuse kestus (kuudes)</span><span class="sxs-lookup"><span data-stu-id="90f61-114">Subscription duration (in months)</span></span>

<span data-ttu-id="90f61-115">Seda tüüpi kataloogi säilitamiseks looge tooteperekond nimega **Kordustellimuse tarkvara**.</span><span class="sxs-lookup"><span data-stu-id="90f61-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="90f61-116">Lisage tooteperekonnale atribuudid **Kasutajate arv** ja **Kordustellimuse kestus**.</span><span class="sxs-lookup"><span data-stu-id="90f61-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="90f61-117">Seejärel lisage tooteperekonda **Kordustellimuse tarkvara** üksikud tooted.</span><span class="sxs-lookup"><span data-stu-id="90f61-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="90f61-118">Tootekataloogi üksuste lisamine projekti lepingusse</span><span class="sxs-lookup"><span data-stu-id="90f61-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="90f61-119">Projekti lepingutel on jaotised kahte tüüpi ridade jaoks - projektipõhised ja tootepõhised.</span><span class="sxs-lookup"><span data-stu-id="90f61-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="90f61-120">Tootepõhised read hõlmavad kõiki lepingu toote hinnakirja tooteid ja ühikuid.</span><span class="sxs-lookup"><span data-stu-id="90f61-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="90f61-121">Lisada saab tooteid, mis ei ole lepingu toodete hinnakirja osaks.</span><span class="sxs-lookup"><span data-stu-id="90f61-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="90f61-122">Saate valida tooteid teistest hinnakirjadest või otse tootekataloogist.</span><span class="sxs-lookup"><span data-stu-id="90f61-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="90f61-123">Kui valite tooted otse tootekataloogi kaudu, kasutatakse toote müügihinna saamiseks selle toote vaikimisi kasutatavat hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="90f61-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="90f61-124">Kui vaike-hinnakirja ei määrata, määratakse hinnaks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="90f61-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="90f61-125">Kui lepingurida põhineb tootekataloogil, saate müügihinna alistada otse real.</span><span class="sxs-lookup"><span data-stu-id="90f61-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="90f61-126">Lepingureal on kahe väärtusega väli **Hinnakujundus**.</span><span class="sxs-lookup"><span data-stu-id="90f61-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="90f61-127">**Hinnakirja tühistamine**</span><span class="sxs-lookup"><span data-stu-id="90f61-127">**Override pricing**</span></span>
- <span data-ttu-id="90f61-128">**Kasuta vaikeväärtust**</span><span class="sxs-lookup"><span data-stu-id="90f61-128">**Use default**</span></span>

<span data-ttu-id="90f61-129">Kui määrate välja **Hinnakujundus** väärtuseks **Hinnakirja tühistamine**, ei määrata vaikehinda.</span><span class="sxs-lookup"><span data-stu-id="90f61-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="90f61-130">Sisestage lepingureal tootele hind.</span><span class="sxs-lookup"><span data-stu-id="90f61-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="90f61-131">Kui määrate välja olekuks **Kasuta vaikeväärtust**, kasutatakse vaikimisi müügihinda ja välja ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="90f61-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="90f61-132">Pärast seda, kui olete Project Operationsi installinud, sisestatakse vaikimisi müügihinnad lepingu tootepõhistele ridadele.</span><span class="sxs-lookup"><span data-stu-id="90f61-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="90f61-133">Välja **Hinnakiri** väärtuseks seatakse **Hinnakirja tühistamine**, et saaksite lepinguridadel vaikimisi kasutatavat hinda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="90f61-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="90f61-134">See on Project Operationsile spetsiifiline tootepõhiste ridade tühistamine käitumine rakenduses Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="90f61-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]