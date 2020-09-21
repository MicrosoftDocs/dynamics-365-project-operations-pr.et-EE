---
title: Kohandatud väljade ja olemite loomine
description: Selles teemas kirjeldatakse, kuidas luua suvandikomplekte ja olemeid oma platvormi Power Apps lahenduses.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751030"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="9b60e-103">Kohandatud väljade ja olemite loomine</span><span class="sxs-lookup"><span data-stu-id="9b60e-103">Create custom fields and entities</span></span> 

<span data-ttu-id="9b60e-104">Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi platvormil Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9b60e-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="9b60e-105">Selles teemas kirjeldatud protseduurid tuleb lõpule viia, kasutades rakenduse Project Service Automation (PSA) veebiliidest.</span><span class="sxs-lookup"><span data-stu-id="9b60e-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b60e-106">Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses.</span><span class="sxs-lookup"><span data-stu-id="9b60e-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="9b60e-107">See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks.</span><span class="sxs-lookup"><span data-stu-id="9b60e-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="9b60e-108">Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="9b60e-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="9b60e-109">Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks</span><span class="sxs-lookup"><span data-stu-id="9b60e-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="9b60e-110">Klõpsake rakenduses PSA nuppu **Sätted** > **Lahendused**, ja seejärel uue lahenduse loomiseks nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="9b60e-111">Sisestage lahenduse nimi, **\<teie organisatsiooni nimi > hinnakujunduse dimensioonid**, sisestage ülejäänud nõutav teave ja klõpsake siis nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="9b60e-113">Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses</span><span class="sxs-lookup"><span data-stu-id="9b60e-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="9b60e-114">Hinnakujunduse dimensioon võib olla suvandikomplekt või olem.</span><span class="sxs-lookup"><span data-stu-id="9b60e-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="9b60e-115">Mõlemad tuleb luua hinnakujunduse lahenduses.</span><span class="sxs-lookup"><span data-stu-id="9b60e-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="9b60e-116">Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="9b60e-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="9b60e-117">Olemil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="9b60e-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="9b60e-118">Klõpsake PSA-s valikuid **Sätted** > **Lahendused** ja seejärel topeltklõpsake **\<oma organisatsiooni nime > hinnakujunduse dimensioone**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="9b60e-119">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="9b60e-120">Klõpsake nuppu **Uus**, et luua uus olem nimega **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="9b60e-121">Sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standardse pealkirja olemi kirjeldus](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="9b60e-123">Suvandikomplektil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="9b60e-123">Option set-based dimensions</span></span> 
<span data-ttu-id="9b60e-124">Saate luua kaks suvandikomplektil põhinevat dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="9b60e-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="9b60e-125">Kasutage suvandit **Ressursi töö asukoht**, et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada rakendamiseks töö lõpetamisel märgistus.</span><span class="sxs-lookup"><span data-stu-id="9b60e-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="9b60e-126">Klõpsake rakenduses PSA nuppu **Sätted** > **Lahendused**, ja seejärel topeltklõpsake **\<teie organisatsiooni nimi > hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9b60e-127">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Suvandikomplektid**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="9b60e-128">Uue suvandikomplekti loomiseks klõpsake nuppu **Uus**, sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="9b60e-129">Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö asukoht</span><span class="sxs-lookup"><span data-stu-id="9b60e-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="9b60e-130">Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö tunnid</span><span class="sxs-lookup"><span data-stu-id="9b60e-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="9b60e-131">Olemil põhinevate dimensioonide andmete loomine</span><span class="sxs-lookup"><span data-stu-id="9b60e-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="9b60e-132">Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="9b60e-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="9b60e-133">Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="9b60e-134">Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.</span><span class="sxs-lookup"><span data-stu-id="9b60e-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="9b60e-135">Klõpsake rakenduses PSA suvandit **Täpsem otsing**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="9b60e-136">Valige olem **Standardne pealkiri** ja klõpsake suvandit **Tulemused**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="9b60e-137">Kuvatakse kõik olemi **Standardne pealkiri** read.</span><span class="sxs-lookup"><span data-stu-id="9b60e-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="9b60e-138">Klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-138">Click **New**.</span></span> <span data-ttu-id="9b60e-139">Sisestage väljale **Nimi** suvand Süsteemi insener, ja klõpsake seejärel nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="9b60e-140">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="9b60e-140">Close the form.</span></span> 
4. <span data-ttu-id="9b60e-141">Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.</span><span class="sxs-lookup"><span data-stu-id="9b60e-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="9b60e-142">Standardse jaotise olemi andmete Näidisandmete</span><span class="sxs-lookup"><span data-stu-id="9b60e-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="9b60e-143">Lisage kõik nõutavad PSA olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse</span><span class="sxs-lookup"><span data-stu-id="9b60e-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="9b60e-144">Hinnakujunduse lahendusele tuleb lisada järgmised Project Service’i olemid.</span><span class="sxs-lookup"><span data-stu-id="9b60e-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="9b60e-145">Kasutage selle protseduuri etappe, et muuta hinnakujunduse lahenduses teatud olulisi skeeme, et olemid oleksid uutest hinnakujunduse dimensioonidest teadlikud.</span><span class="sxs-lookup"><span data-stu-id="9b60e-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="9b60e-146">Klõpsake PSA-s valikuid **Sätted** > **Lahendused** ja seejärel topeltklõpsake **\<oma organisatsiooni nime > hinnakujunduse dimensioone**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9b60e-147">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="9b60e-148">Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.</span><span class="sxs-lookup"><span data-stu-id="9b60e-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="9b60e-149">Tegelik</span><span class="sxs-lookup"><span data-stu-id="9b60e-149">Actual</span></span>
- <span data-ttu-id="9b60e-150">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="9b60e-150">Bookable Resource</span></span>
- <span data-ttu-id="9b60e-151">Prognoosi rida</span><span class="sxs-lookup"><span data-stu-id="9b60e-151">Estimate Line</span></span>
- <span data-ttu-id="9b60e-152">Arve rea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9b60e-152">Invoice Line Detail</span></span>
- <span data-ttu-id="9b60e-153">Töölehe rida</span><span class="sxs-lookup"><span data-stu-id="9b60e-153">Journal Line</span></span>
- <span data-ttu-id="9b60e-154">Projekti lepingurea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9b60e-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="9b60e-155">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="9b60e-155">Project Team Member</span></span>
- <span data-ttu-id="9b60e-156">Hinnapakkumise rea üksikasi</span><span class="sxs-lookup"><span data-stu-id="9b60e-156">Quote Line Detail</span></span>
- <span data-ttu-id="9b60e-157">Rolli hinna hinnalisand</span><span class="sxs-lookup"><span data-stu-id="9b60e-157">Role Price Markup</span></span>
- <span data-ttu-id="9b60e-158">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="9b60e-158">Role Price</span></span> 
- <span data-ttu-id="9b60e-159">Ajakirje</span><span class="sxs-lookup"><span data-stu-id="9b60e-159">Time Entry</span></span> 

> ![Olemasolevate olemite lisamine hinnakujunduse dimensioonide lahendusse](media/Existing-entities-to-PD-solution.png)

> ![Lahenduse komponentide valimine](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="9b60e-162">Veenduge, et kõigi valitud olemite jaoks kaasatakse kõik vormid ja vaated.</span><span class="sxs-lookup"><span data-stu-id="9b60e-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="9b60e-163">Kui teil palutakse kaasata eespool valitud olemite jaoks kõik sõltuvaid olemeid, klõpsake nuppu **Ei**.</span><span class="sxs-lookup"><span data-stu-id="9b60e-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Ära kaasa kõiki seotud komponente](media/Do-not-include-required.png)


