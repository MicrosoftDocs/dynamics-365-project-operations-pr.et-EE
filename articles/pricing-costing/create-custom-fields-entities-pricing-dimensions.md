---
title: Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena
description: Selles teemas antakse teavet, kuidas luua kohandatud suvandikomplekte või olemeid.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074994"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="57c5f-103">Kohandatud väljade ja olemite loomine hinnakujunduse dimensioonidena</span><span class="sxs-lookup"><span data-stu-id="57c5f-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="57c5f-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="57c5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="57c5f-105">Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi.</span><span class="sxs-lookup"><span data-stu-id="57c5f-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57c5f-106">Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses.</span><span class="sxs-lookup"><span data-stu-id="57c5f-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="57c5f-107">See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks.</span><span class="sxs-lookup"><span data-stu-id="57c5f-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="57c5f-108">Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="57c5f-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="57c5f-109">Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks</span><span class="sxs-lookup"><span data-stu-id="57c5f-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="57c5f-110">Avage **Sätted** > **Lahendused** ja seejärel uue lahenduse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="57c5f-111">Pange lahendusele nimi **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid** , sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="57c5f-112">Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses</span><span class="sxs-lookup"><span data-stu-id="57c5f-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="57c5f-113">Hinnakujunduse dimensioon võib olla suvandikomplekt või olem.</span><span class="sxs-lookup"><span data-stu-id="57c5f-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="57c5f-114">Mõlemad tuleb luua hinnakujunduse lahenduses.</span><span class="sxs-lookup"><span data-stu-id="57c5f-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="57c5f-115">Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="57c5f-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="57c5f-116">Olemil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="57c5f-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="57c5f-117">Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="57c5f-118">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="57c5f-119">Valige **Uus** , et luua uus olem nimega **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="57c5f-120">Sisestage ülejäänud nõutav teave ja calige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="57c5f-121">Suvandikomplektil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="57c5f-121">Option set-based dimensions</span></span> 
<span data-ttu-id="57c5f-122">Saate luua kaks suvandikomplektil põhinevat dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="57c5f-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="57c5f-123">Kasutage suvandit **Ressursi töö asukoht** , et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö** , et rakendada rakendamiseks töö lõpetamisel märgistus.</span><span class="sxs-lookup"><span data-stu-id="57c5f-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="57c5f-124">Avage **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="57c5f-125">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Suvandikomplektid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="57c5f-126">Uue suvandikomplekti loomiseks valige **Uus** , sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="57c5f-127">Olemil põhinevate dimensioonide andmete loomine</span><span class="sxs-lookup"><span data-stu-id="57c5f-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="57c5f-128">Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="57c5f-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="57c5f-129">Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="57c5f-130">Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.</span><span class="sxs-lookup"><span data-stu-id="57c5f-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="57c5f-131">Valige **Täpsem otsing** , valige olem **Standardpealkiri** ja valige seejärel **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="57c5f-132">Kuvatakse kõik olemi **Standardne pealkiri** read.</span><span class="sxs-lookup"><span data-stu-id="57c5f-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="57c5f-133">Valige **Uus** ja väljale **Nmi** sisestafe Süsteemi insener ja valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="57c5f-134">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="57c5f-134">Close the form.</span></span> 
4. <span data-ttu-id="57c5f-135">Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.</span><span class="sxs-lookup"><span data-stu-id="57c5f-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="57c5f-136">Lisage kõik nõutavad olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse</span><span class="sxs-lookup"><span data-stu-id="57c5f-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="57c5f-137">Hinnakujunduse lahendusele tuleb lisada järgmised olemid.</span><span class="sxs-lookup"><span data-stu-id="57c5f-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="57c5f-138">Kasutage selle protseduuri etappe, et muuta hinnakujunduse lahenduses teatud olulisi skeeme, et olemid oleksid uutest hinnakujunduse dimensioonidest teadlikud.</span><span class="sxs-lookup"><span data-stu-id="57c5f-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="57c5f-139">Valige **Sätted** > **Lahendused** ja topeltklõpsake suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="57c5f-140">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="57c5f-141">Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.</span><span class="sxs-lookup"><span data-stu-id="57c5f-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="57c5f-142">Tegelik</span><span class="sxs-lookup"><span data-stu-id="57c5f-142">Actual</span></span>
  - <span data-ttu-id="57c5f-143">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="57c5f-143">Bookable Resource</span></span>
  - <span data-ttu-id="57c5f-144">Prognoosi rida</span><span class="sxs-lookup"><span data-stu-id="57c5f-144">Estimate Line</span></span>
  - <span data-ttu-id="57c5f-145">Arve rea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="57c5f-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="57c5f-146">Töölehe rida</span><span class="sxs-lookup"><span data-stu-id="57c5f-146">Journal Line</span></span>
  - <span data-ttu-id="57c5f-147">Projekti lepingurea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="57c5f-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="57c5f-148">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="57c5f-148">Project Team Member</span></span>
  - <span data-ttu-id="57c5f-149">Hinnapakkumisrea üksikasi</span><span class="sxs-lookup"><span data-stu-id="57c5f-149">Quote Line Detail</span></span>
  - <span data-ttu-id="57c5f-150">Rolli hinna hinnalisand</span><span class="sxs-lookup"><span data-stu-id="57c5f-150">Role Price Markup</span></span>
  - <span data-ttu-id="57c5f-151">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="57c5f-151">Role Price</span></span> 
  - <span data-ttu-id="57c5f-152">Ajakirje</span><span class="sxs-lookup"><span data-stu-id="57c5f-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="57c5f-153">Veenduge, et kõigi valitud olemite jaoks kaasatakse kõik vormid ja vaated.</span><span class="sxs-lookup"><span data-stu-id="57c5f-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="57c5f-154">Kui teil palutakse kaasata eespool valitud olemite jaoks kõik sõltuvaid olemeid, valige **Ei**.</span><span class="sxs-lookup"><span data-stu-id="57c5f-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

