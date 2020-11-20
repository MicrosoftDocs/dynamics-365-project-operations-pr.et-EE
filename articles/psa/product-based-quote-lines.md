---
title: Tootepõhised hinnapakkumise read
description: Selles teemas antakse teavet tootel põhinevate hinnapakkumiste ridade kohta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123193"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="fa503-103">Tootepõhised hinnapakkumise read</span><span class="sxs-lookup"><span data-stu-id="fa503-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="fa503-104">Saate luua tootel põhinevaid hinnapakkumise ridu rakenduses Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fa503-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="fa503-105">Tootepõhiste hinnapakkumiste ridu saab sisestada ridadel või need võivad olla tootekataloogi objektid.</span><span class="sxs-lookup"><span data-stu-id="fa503-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="fa503-106">Tootekataloog</span><span class="sxs-lookup"><span data-stu-id="fa503-106">Product catalog</span></span>

<span data-ttu-id="fa503-107">Dynamics 365 tootekataloogi toodetel on vaikimisi ühik ja ühikurühm.</span><span class="sxs-lookup"><span data-stu-id="fa503-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="fa503-108">Kui mitmes tootes on sama atribuutide kogum, saate luua ka tootepere, millel on ka need atribuudid.</span><span class="sxs-lookup"><span data-stu-id="fa503-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="fa503-109">Kõik ühe tootepere tooted pärivad sama hulga atribuute.</span><span class="sxs-lookup"><span data-stu-id="fa503-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="fa503-110">Näiteks ettevõte müüb kordustellimuse litsentse mitmesuguste tarkvarade jaoks.</span><span class="sxs-lookup"><span data-stu-id="fa503-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="fa503-111">Kõikidel kordustellimuse tarkvaradel on järgmised kaks atribuuti.</span><span class="sxs-lookup"><span data-stu-id="fa503-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="fa503-112">Aktiivsete kasutajate arv</span><span class="sxs-lookup"><span data-stu-id="fa503-112">Number of users</span></span> 
- <span data-ttu-id="fa503-113">Kordustellimuse kestus (kuudes)</span><span class="sxs-lookup"><span data-stu-id="fa503-113">Subscription duration (in months)</span></span>

<span data-ttu-id="fa503-114">Seda tüüpi kataloogi säilitamiseks on hea viis luua tootepere, mille nimi on **Kordustellimuse tarkvara** ja millel on atribuudid **Kasutajate arv** ja **Kordustellimuse kestus**.</span><span class="sxs-lookup"><span data-stu-id="fa503-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="fa503-115">Seejärel saate lisada üksikuid tooteid, näiteks **Dynamics 365 Sales** või **Dynamics 365 Field Service**, tooteperele **Kordustellimuse tarkvara**.</span><span class="sxs-lookup"><span data-stu-id="fa503-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="fa503-116">Tootekataloogi üksuste lisamine projekti hinnapakkumisesse</span><span class="sxs-lookup"><span data-stu-id="fa503-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="fa503-117">Projekti hinnapakkumise ja projekti lepingu lehtedel on jaotised kahte tüüpi ridade jaoks: projektil põhinevad read ja tootepõhised read.</span><span class="sxs-lookup"><span data-stu-id="fa503-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="fa503-118">Tootepõhiste ridade puhul kasutatakse rakendust Dynamics 365, et lisada tooteid tootekataloogi hinnapakkumisse.</span><span class="sxs-lookup"><span data-stu-id="fa503-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="fa503-119">Müügipakkumise rea või projekti lepingurea ripploendis on kõik tooted ja ühikud, mis on seotud hinnapakkumise või projekti lepinguga.</span><span class="sxs-lookup"><span data-stu-id="fa503-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="fa503-120">Saate lisada ka tooteid, mis ei kuulu hinnapakkumise toodete hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="fa503-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="fa503-121">Lisaks saate valida tooted teistest hinnakirjadest või valida tooteid otse tootekataloogi kaudu.</span><span class="sxs-lookup"><span data-stu-id="fa503-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="fa503-122">Kui valite tooted otse tootekataloogi kaudu, kasutatakse toote müügihinna saamiseks selle toote vaikimisi kasutatavat hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="fa503-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="fa503-123">Kui vaike-hinnakirja ei määrata, määratakse hinnaks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fa503-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="fa503-124">Kui hinnapakkumise rida põhineb tootekataloogil, saate müügihinna alistada otse hinnapakkumise real.</span><span class="sxs-lookup"><span data-stu-id="fa503-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="fa503-125">Võtke arvesse, et Dynamics 365 on hinnapakkumise real on väli **Hinnakiri**.</span><span class="sxs-lookup"><span data-stu-id="fa503-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="fa503-126">Saadaval on kaks väärtust.</span><span class="sxs-lookup"><span data-stu-id="fa503-126">Two values are available:</span></span>

- <span data-ttu-id="fa503-127">Hinnakirja tühistamine</span><span class="sxs-lookup"><span data-stu-id="fa503-127">Override pricing</span></span>  
- <span data-ttu-id="fa503-128">Kasuta vaikeväärtust</span><span class="sxs-lookup"><span data-stu-id="fa503-128">Use default</span></span>

<span data-ttu-id="fa503-129">Kui määrate selle välja väärtuseks **Hinnakirja tühistamine**, ei sea Dynamics 365 vaikimisi hinda.</span><span class="sxs-lookup"><span data-stu-id="fa503-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="fa503-130">Toote hinna peate sisestama hinnapakkumise real.</span><span class="sxs-lookup"><span data-stu-id="fa503-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="fa503-131">Kui määrate selle välja väärtuseks **Kasuta vaikesätet**, kasutab Dynamics 365 vaikimisi müügihinda ja lukustab välja, et seda ei saaks redigeerida.</span><span class="sxs-lookup"><span data-stu-id="fa503-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="fa503-132">Pärast seda, kui olete installinud PSA, sisestatakse vaikimisi müügihinnad hinnapakkumise tootepõhistele ridadele.</span><span class="sxs-lookup"><span data-stu-id="fa503-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="fa503-133">Välja **Hinnakiri** väärtuseks seatakse **Hinnakirja tühistamine**, et saaksite hinnapakkumise ridadel redigeerida vaikimisi kasutatavat hinda.</span><span class="sxs-lookup"><span data-stu-id="fa503-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Hinnakirja tühistamise määramine](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="fa503-135">Toodete koguselised tegurid</span><span class="sxs-lookup"><span data-stu-id="fa503-135">Quantity factors for products</span></span>

<span data-ttu-id="fa503-136">PSA kasutab kordustellimuse põhiste toodete müügi toetamiseks koguselisi tegureid.</span><span class="sxs-lookup"><span data-stu-id="fa503-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="fa503-137">Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.</span><span class="sxs-lookup"><span data-stu-id="fa503-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="fa503-138">Tavaliselt talletatakse kordustellimuse tarkvara hinda kataloogis ühe kasutaja kuu hinnana.</span><span class="sxs-lookup"><span data-stu-id="fa503-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="fa503-139">Kuid selle asemel võite kasutada ka muid aja kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="fa503-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="fa503-140">Müügiprotsessi jooksul on hind hinnapakkumise real tavaliselt ühe kasutaja hind kuus, mille IT müügiagent oli kokku leppinud ja diskonteerinud.</span><span class="sxs-lookup"><span data-stu-id="fa503-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="fa503-141">Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev.</span><span class="sxs-lookup"><span data-stu-id="fa503-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="fa503-142">Kogus, mida kasutatakse hinnapakkumise rea summa arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu toode.</span><span class="sxs-lookup"><span data-stu-id="fa503-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="fa503-143">Seda tüüpi müügi toetamiseks võttis PSA kasutusele koguselised tegurid.</span><span class="sxs-lookup"><span data-stu-id="fa503-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="fa503-144">Koguselised tegurid sõltuvad toote atribuutidest rakenduses Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fa503-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="fa503-145">Toote teatud atribuutide konfigureerimisel võimaldab PSA teil tähistada nende atribuutide alamhulka või kõiki atribuute, näiteks koguselised tegurid.</span><span class="sxs-lookup"><span data-stu-id="fa503-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="fa503-146">PSA kinnitab, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina.</span><span class="sxs-lookup"><span data-stu-id="fa503-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="fa503-147">Kui toode, mille jaoks on konfigureeritud koguselised tegurid, lisatakse hinnapakkumise reale, muutub  hinnapakkumise rea väli **Hinnapakkumine** kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="fa503-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="fa503-148">Pärast koguseid sisaldavatele toote atribuutidele väärtuste sisestamist arvutab PSA hinnapakkumise rea koguse.</span><span class="sxs-lookup"><span data-stu-id="fa503-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="fa503-149">Näiteks Dynamics 365 võib sisaldada järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="fa503-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="fa503-150">**Kasutajate arv** – kasutajate arv</span><span class="sxs-lookup"><span data-stu-id="fa503-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="fa503-151">**Kuude arv** – kordustellimuse kuude arv</span><span class="sxs-lookup"><span data-stu-id="fa503-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="fa503-152">**Toote SKU**</span><span class="sxs-lookup"><span data-stu-id="fa503-152">**Product SKU**</span></span> 

<span data-ttu-id="fa503-153">Atribuute **Kasutajate arv** ja **Kuude arv** saab märgistada koguse tegurina, redigeerides tootesarja atribuute.</span><span class="sxs-lookup"><span data-stu-id="fa503-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Kasutajate arvu ja kuude arvu märgistamine kvaliteeditegurina](media/basic-guide-11.png)
 
