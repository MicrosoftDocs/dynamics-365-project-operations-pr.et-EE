---
title: Tootepõhiste hinnapakkumise ridade kompleksühikute haldus, näiteks kasutaja kohta või kuu kohta
description: Selles teemas antakse teavet tootepõhiste hinnapakkumise ridade kompleksühikute halduse kohta.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965766"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="28921-103">Tootepõhiste hinnapakkumise ridade kompleksühikute haldus, näiteks kasutaja kohta või kuu kohta</span><span class="sxs-lookup"><span data-stu-id="28921-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="28921-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="28921-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28921-105">Dynamics 365 Project Operations kasutab kordustellimuse põhiste toodete müügi toetamiseks koguse tegureid.</span><span class="sxs-lookup"><span data-stu-id="28921-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="28921-106">Kordustellimusel põhinevate toodete puhul väljendatakse hinnapakkumise või projekti lepingurea kogust kasutaja kuude arvuna.</span><span class="sxs-lookup"><span data-stu-id="28921-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="28921-107">Tavaliselt talletatakse kordustellimuse tarkvara hinda kataloogis ühe kasutaja kuu hinnana.</span><span class="sxs-lookup"><span data-stu-id="28921-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="28921-108">Müügiprotsessi jooksul on hind hinnapakkumise real tavaliselt ühe kasutaja hind kuus, mille IT müügiagent oli kokku leppinud ja diskonteerinud.</span><span class="sxs-lookup"><span data-stu-id="28921-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="28921-109">Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev.</span><span class="sxs-lookup"><span data-stu-id="28921-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="28921-110">Kogus, mida kasutatakse hinnapakkumise rea arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu korrutis.</span><span class="sxs-lookup"><span data-stu-id="28921-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="28921-111">Seda tüüpi müügi toetamiseks võttis Project Operations kasutusele koguse tegurite kontseptsiooni.</span><span class="sxs-lookup"><span data-stu-id="28921-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="28921-112">Koguselised tegurid sõltuvad toote atribuutidest rakenduses Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="28921-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="28921-113">Toote teatud atribuutide konfigureerimisel võimaldab Project Operations teil tähistada nende atribuutide alamhulka või kõiki atribuute koguse teguritena.</span><span class="sxs-lookup"><span data-stu-id="28921-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="28921-114">Project Operations valideerib, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina.</span><span class="sxs-lookup"><span data-stu-id="28921-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="28921-115">Kui lisate hinnapakkumise reale koguse teguritega toote, muutub väli **Kogus** kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="28921-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="28921-116">Pärast koguse teguritest toote atribuutidele väärtuste sisestamist arvutab Project Operations hinnapakkumise rea koguse.</span><span class="sxs-lookup"><span data-stu-id="28921-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="28921-117">Näiteks Dynamics 365 Sales võib omada järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="28921-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="28921-118">**Kasutajate arv**: kasutajate arv</span><span class="sxs-lookup"><span data-stu-id="28921-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="28921-119">**Kuude arv**: kordustellimuse kuude arv</span><span class="sxs-lookup"><span data-stu-id="28921-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="28921-120">**Toote SKU**</span><span class="sxs-lookup"><span data-stu-id="28921-120">**Product SKU**</span></span>

<span data-ttu-id="28921-121">Atribuute **Kasutajate arv** ja **Kuude arv** saate märgistada koguse tegurina, redigeerides tootesarja atribuute.</span><span class="sxs-lookup"><span data-stu-id="28921-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="28921-122">Toote atribuutidest koguse tegurite loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="28921-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="28921-123">Minge Project Operationsi vasakpoolsel navigeerimispaanil jaotisse **Müük** > **Tooted**.</span><span class="sxs-lookup"><span data-stu-id="28921-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="28921-124">Avage toode, mille jaoks peate määrama koguse tegurid.</span><span class="sxs-lookup"><span data-stu-id="28921-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="28921-125">Veenduge, et toote atribuudid on juba konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="28921-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="28921-126">Valige toote lehel **Projekti teave** vahekaart **Koguse tegurid**.</span><span class="sxs-lookup"><span data-stu-id="28921-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="28921-127">Valige alamruudustikus suvand **+ uue välja arvutus**.</span><span class="sxs-lookup"><span data-stu-id="28921-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="28921-128">Sisestage koguse teguri nimi ja valige atribuudi väärtus, mis vastendatakse välja arvutusega.</span><span class="sxs-lookup"><span data-stu-id="28921-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="28921-129">Salvestage ja sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="28921-129">Save and close the form.</span></span> <span data-ttu-id="28921-130">Korrake neid juhiseid kõigi atribuutide jaoks, mida kasutatakse tootepõhise hinnapakkumise rea koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="28921-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="28921-131">Tootepõhise hinnapakkumise rea loomisel on lukustatakse hinnapakkumise rea kogus.</span><span class="sxs-lookup"><span data-stu-id="28921-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="28921-132">Kogus arvutatakse selle hinnapakkumise rea jaoks sisestatud atribuudi väärtuste korrutisena.</span><span class="sxs-lookup"><span data-stu-id="28921-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
