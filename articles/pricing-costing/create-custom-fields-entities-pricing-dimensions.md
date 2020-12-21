---
title: Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena
description: Selles teemas antakse teavet, kuidas luua kohandatud suvandikomplekte või olemeid.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642808"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="b4a40-103">Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena</span><span class="sxs-lookup"><span data-stu-id="b4a40-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="b4a40-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="b4a40-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b4a40-105">Läbige järgmised etapid, kui soovite luua kohandatud suvandikomplekti või olemit, et kasutada seda hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="b4a40-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="b4a40-106">Lisateabe saamiseks vt [Hinnakujunduse dimensioonide ülevaade](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b4a40-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b4a40-107">Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses.</span><span class="sxs-lookup"><span data-stu-id="b4a40-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b4a40-108">See oluline hea tava annab tulevikus paindlikkuse, et vajaduse korral saaks teha uuendusi või eemaldada muudatusi.</span><span class="sxs-lookup"><span data-stu-id="b4a40-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="b4a40-109">See aitab teie tööd ka uuesti kasutada ja muudab pärast kõigi nõutavate muudatuste tegemist lihtsamaks nende muudatuste portimise teise eksemplari, eksportige see lahendus kui **Hallatav lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="b4a40-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b4a40-110">Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses</span><span class="sxs-lookup"><span data-stu-id="b4a40-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b4a40-111">Hinnakujunduse dimensioon võib olla suvandikomplekt või olem.</span><span class="sxs-lookup"><span data-stu-id="b4a40-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b4a40-112">Mõlemad tuleb luua hinnakujunduse lahenduses.</span><span class="sxs-lookup"><span data-stu-id="b4a40-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b4a40-113">Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="b4a40-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b4a40-114">Olemil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="b4a40-114">Entity-based dimensions</span></span>
<span data-ttu-id="b4a40-115">Olemil põhinevate dimensioonide loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b4a40-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="b4a40-116">Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b4a40-117">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b4a40-118">Valige **Uus**, et luua uus olem nimega **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="b4a40-119">Sisestage ülejäänud nõutav teave ja calige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Standardse pealkirja olemi kirjeldus](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="b4a40-121">Suvandikomplektil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="b4a40-121">Option set-based dimensions</span></span> 
<span data-ttu-id="b4a40-122">Saate luua kaks suvandikomplektil põhinevat dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="b4a40-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="b4a40-123">Kasutage **Ressursi töö asukohta**, et jälgida asukohaga **Kodu** töö ja asukohaga **Kohapealne** töö hinda.</span><span class="sxs-lookup"><span data-stu-id="b4a40-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="b4a40-124">Kasutage suvandit **Ressursi tööaeg** koos väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada töö lõpetamisel hinnalisandit.</span><span class="sxs-lookup"><span data-stu-id="b4a40-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="b4a40-125">Järgmine graafiline vaade sisaldab dimensiooni **Ressursi tööasukoht**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö asukoht](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="b4a40-127">Järgmine graafiline vaade sisaldab dimensiooni **Ressursi töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö tunnid](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="b4a40-129">Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b4a40-130">Valige rakenduses Solution Explorer vasakul navigeerimispaanil **Suvandikomplektid**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b4a40-131">Uue suvandikomplekti loomiseks valige **Uus**, sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b4a40-132">Olemil põhinevate dimensioonide andmete loomine</span><span class="sxs-lookup"><span data-stu-id="b4a40-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b4a40-133">Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="b4a40-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b4a40-134">Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b4a40-135">Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.</span><span class="sxs-lookup"><span data-stu-id="b4a40-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b4a40-136">Valige **Täpsem otsing**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="b4a40-137">Valige olem **Standardne pealkiri** ja seejärel **Tulemused**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="b4a40-138">Kuvatakse kõik olemi **Standardne pealkiri** read.</span><span class="sxs-lookup"><span data-stu-id="b4a40-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="b4a40-139">Valige **Uus** ja väljale **Nmi** sisestafe Süsteemi insener ja valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b4a40-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="b4a40-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4a40-140">Close the page.</span></span> 
5. <span data-ttu-id="b4a40-141">Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.</span><span class="sxs-lookup"><span data-stu-id="b4a40-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Näidisandmed olemi Standardne pealkiri jaoks](media/ST-data.png)
