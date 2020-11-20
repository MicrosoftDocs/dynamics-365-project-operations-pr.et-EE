---
title: Kompleksühikute haldamine tootepõhiste lepinguridade jaoks – liht
description: Selles teemas antakse teavet kordustellimusel põhinevate toodete müügi toetamise kohta.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177371"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="8621e-103">Kompleksühikute haldamine tootepõhiste lepinguridade jaoks – liht</span><span class="sxs-lookup"><span data-stu-id="8621e-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="8621e-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="8621e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8621e-105">Dynamics 365 Project Operations kasutab kordustellimuse põhiste toodete müügi toetamiseks koguse tegureid.</span><span class="sxs-lookup"><span data-stu-id="8621e-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="8621e-106">Kordustellimusel põhinevate toodete puhul väljendatakse lepingu või projekti lepingurea kogust kasutaja kuude arvuna.</span><span class="sxs-lookup"><span data-stu-id="8621e-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="8621e-107">Kordustellimuse tarkvara hind talletatakse kataloogis ühe kasutaja kuu hinnana.</span><span class="sxs-lookup"><span data-stu-id="8621e-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="8621e-108">Müügiprotsessi jooksul on hind lepingureal tavaliselt ühe kasutaja hind kuus, mille müügiagent oli kokku leppinud ja diskonteerinud.</span><span class="sxs-lookup"><span data-stu-id="8621e-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="8621e-109">Igal lepingul on erinev arv kasutajaid ja kordustellimuse kuude arv on erinev.</span><span class="sxs-lookup"><span data-stu-id="8621e-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="8621e-110">Kogus, mida kasutatakse lepingurea summa arvutamiseks, on kasutajate arvu ja kordustellimuse kuude arvu toode.</span><span class="sxs-lookup"><span data-stu-id="8621e-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="8621e-111">Seda tüüpi müügi toetamiseks toetab rakendus Project Operations *koguseliste tegurite* kontseptsiooni.</span><span class="sxs-lookup"><span data-stu-id="8621e-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="8621e-112">Koguselised tegurid sõltuvad toote atribuutidest.</span><span class="sxs-lookup"><span data-stu-id="8621e-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="8621e-113">Toote teatud atribuutide konfigureerimisel saate tähistada nende atribuutide alamhulka või kõiki atribuute, näiteks koguselised tegurid.</span><span class="sxs-lookup"><span data-stu-id="8621e-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="8621e-114">Project Operations valideerib, et ainult arvandmed või toote atribuudid, millel on arvuline andmetüüp, märgistatakse koguse tegurina.</span><span class="sxs-lookup"><span data-stu-id="8621e-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="8621e-115">Kui mõne konfigureeritud koguse teguriga toode lisatakse lepingureale, muutub väli **Kogus** kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="8621e-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="8621e-116">Pärast koguseid sisaldavatele toote atribuutidele väärtuste sisestamist arvutab Project Operations lepingurea koguse.</span><span class="sxs-lookup"><span data-stu-id="8621e-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="8621e-117">Näiteks Dynamics 365 Sales võib omada järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="8621e-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="8621e-118">**Kasutajate arv**: kasutajate arv.</span><span class="sxs-lookup"><span data-stu-id="8621e-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="8621e-119">**Kuude arv**: kordustellimuse kuude arv.</span><span class="sxs-lookup"><span data-stu-id="8621e-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="8621e-120">**Toote SKU**: toote varude arvestusühikute (SKU).</span><span class="sxs-lookup"><span data-stu-id="8621e-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="8621e-121">Atribuute **Kasutajate arv** ja **Kuude arv** saab märgistada koguse tegurina, redigeerides tootesarja atribuute.</span><span class="sxs-lookup"><span data-stu-id="8621e-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="8621e-122">Tooteatribuutidest koguseliste tegurite loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="8621e-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="8621e-123">Valige rakenduses **Project Operations** suvand **Müük – toode**.</span><span class="sxs-lookup"><span data-stu-id="8621e-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="8621e-124">Avage toode, mille jaoks peate koguselised tegurid seadistama.</span><span class="sxs-lookup"><span data-stu-id="8621e-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="8621e-125">Veenduge, et toote atribuudid oleks juba häälestatud.</span><span class="sxs-lookup"><span data-stu-id="8621e-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="8621e-126">Valige lehel **Projekti teave** vahekaart **Koguselised tegurid**.</span><span class="sxs-lookup"><span data-stu-id="8621e-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="8621e-127">Valige alamruudustikus suvand **+ uue välja arvutus**.</span><span class="sxs-lookup"><span data-stu-id="8621e-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="8621e-128">Sisestage **koguse teguri** nimi ja valige atribuudi väärtus, mis vastendatakse välja arvutusega.</span><span class="sxs-lookup"><span data-stu-id="8621e-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="8621e-129">Salvestage ja sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="8621e-129">Save and close the form.</span></span>
7. <span data-ttu-id="8621e-130">Korrake samme 2–6 kõigi atribuutide jaoks, mis koos moodustavad tootepõhise lepingurea koguse.</span><span class="sxs-lookup"><span data-stu-id="8621e-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="8621e-131">Kui koguselised tegurid on häälestatud ja kasutaja loob selle toote jaoks lepingurea, siis lepingurea kogus on lukus.</span><span class="sxs-lookup"><span data-stu-id="8621e-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="8621e-132">Kogus arvutatakse seejärel selle lepingurea atribuudi väärtuste tootena.</span><span class="sxs-lookup"><span data-stu-id="8621e-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
