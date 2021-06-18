---
title: Kohandatud väljade ja olemite loomine
description: Selles teemas kirjeldatakse, kuidas luua suvandikomplekte ja olemeid oma platvormi Power Apps lahenduses.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998946"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c461f-103">Kohandatud väljade ja olemite loomine</span><span class="sxs-lookup"><span data-stu-id="c461f-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c461f-104">Läbige järgmised etapid iga kord, kui soovite luua kohandatud suvandikomplekt või olemi platvormil Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c461f-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c461f-105">Selles teemas kirjeldatud protseduurid tuleb lõpule viia, kasutades rakenduse Project Service Automation (PSA) veebiliidest.</span><span class="sxs-lookup"><span data-stu-id="c461f-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c461f-106">Soovitame teil teha kõik kohandatud hinnakujunduse dimensiooni muudatused eraldi lahenduses.</span><span class="sxs-lookup"><span data-stu-id="c461f-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c461f-107">See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks.</span><span class="sxs-lookup"><span data-stu-id="c461f-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c461f-108">Kui olete kõik vajalikud muudatused teinud, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="c461f-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c461f-109">Kohandatud väljade ja suvandikomplekti loomine hinnakujunduse dimensiooni lahenduses</span><span class="sxs-lookup"><span data-stu-id="c461f-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c461f-110">Hinnakujunduse dimensioon võib olla suvandikomplekt või olem.</span><span class="sxs-lookup"><span data-stu-id="c461f-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c461f-111">Mõlemad tuleb luua hinnakujunduse lahenduses.</span><span class="sxs-lookup"><span data-stu-id="c461f-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c461f-112">Selle protseduuri etapid selgitavad, kuidas luua olemil ja suvandikomplektil põhinevaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="c461f-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c461f-113">Olemil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="c461f-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="c461f-114">Klõpsake PSA-s **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="c461f-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c461f-115">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="c461f-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c461f-116">Klõpsake nuppu **Uus**, et luua uus olem nimega **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="c461f-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c461f-117">Sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c461f-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standardse pealkirja olemi kirjeldus](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c461f-119">Suvandikomplektil põhinevad dimensioonid</span><span class="sxs-lookup"><span data-stu-id="c461f-119">Option set-based dimensions</span></span> 
<span data-ttu-id="c461f-120">Saate luua kaks suvandikomplektil põhinevat dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="c461f-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c461f-121">Kasutage suvandit **Ressursi töö asukoht**, et jälgida asukoha **Kodu** ja **Kohapeal** töö hinda ning kasutada suvandit **Ressursi töö aega** väärtustega **Regulaarne** ja **Ületunnitöö**, et rakendada rakendamiseks töö lõpetamisel märgistus.</span><span class="sxs-lookup"><span data-stu-id="c461f-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c461f-122">Klõpsake PSA-s **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="c461f-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c461f-123">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvand **Suvandikomplektid**.</span><span class="sxs-lookup"><span data-stu-id="c461f-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c461f-124">Uue suvandikomplekti loomiseks klõpsake nuppu **Uus**, sisestage ülejäänud nõutav teave ja seejärel klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c461f-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c461f-125">Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö asukoht</span><span class="sxs-lookup"><span data-stu-id="c461f-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c461f-126">Suvandikomplektil põhinev hinnakujunduse dimensioon nimega ressursi töö tunnid</span><span class="sxs-lookup"><span data-stu-id="c461f-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c461f-127">Olemil põhinevate dimensioonide andmete loomine</span><span class="sxs-lookup"><span data-stu-id="c461f-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c461f-128">Olemil põhinevate dimensioonide andmeid saate luua ka käsitsi, või kasutada rakenduse Microsoft Excel importimise või hoolduskõnede funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c461f-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c461f-129">Selle protseduuri etappide abil saate luua kaks standardset pealkirja, **Süsteemide insener** ja **Süsteemide vaneminsener** olemil põhinevast dimensioonist, **Standardne pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="c461f-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c461f-130">Kui andmed, mida soovite luua, on väikesed, nagu järgmises näites, saate kasutada standardset vormi.</span><span class="sxs-lookup"><span data-stu-id="c461f-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c461f-131">Klõpsake rakenduses PSA suvandit **Täpsem otsing**.</span><span class="sxs-lookup"><span data-stu-id="c461f-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c461f-132">Valige olem **Standardne pealkiri** ja klõpsake suvandit **Tulemused**.</span><span class="sxs-lookup"><span data-stu-id="c461f-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c461f-133">Kuvatakse kõik olemi **Standardne pealkiri** read.</span><span class="sxs-lookup"><span data-stu-id="c461f-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c461f-134">Klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c461f-134">Click **New**.</span></span> <span data-ttu-id="c461f-135">Sisestage väljale **Nimi** suvand Süsteemi insener, ja klõpsake seejärel nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c461f-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c461f-136">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="c461f-136">Close the form.</span></span> 
4. <span data-ttu-id="c461f-137">Korrake etappe 1–3, et luua teine standardne suvandile Süsteemi vaneminsener.</span><span class="sxs-lookup"><span data-stu-id="c461f-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c461f-138">Standardse jaotise olemi andmete Näidisandmete</span><span class="sxs-lookup"><span data-stu-id="c461f-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]