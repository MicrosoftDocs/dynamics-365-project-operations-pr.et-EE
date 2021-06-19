---
title: Projektipõhised parandusarved
description: See teema sisaldab teavet selle kohta, kuidas luua ja kinnitada Project Operationsis projektipõhiseid parandusarveid.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012266"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="9d860-103">Projektipõhised parandusarved</span><span class="sxs-lookup"><span data-stu-id="9d860-103">Corrective project-based invoices</span></span>

<span data-ttu-id="9d860-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="9d860-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9d860-105">Kinnitatud projekti arvet saab parandada muudatuste või krediidi töötlemiseks, pidades läbirääkimisi kliendi ja projektijuhiga.</span><span class="sxs-lookup"><span data-stu-id="9d860-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9d860-106">Kinnitatud arve redigeerimiseks avage kinnitatud arve ja valige suvand **Paranda seda arvet**.</span><span class="sxs-lookup"><span data-stu-id="9d860-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9d860-107">See valik pole saadaval, kui projekti arve ei ole kinnitatud või kui projektipõhisel arvel avansid või honorarid või avansside või honoraride vastavusseviimised.</span><span class="sxs-lookup"><span data-stu-id="9d860-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="9d860-108">Uus arve mustand luuakse kinnitatud arvelt.</span><span class="sxs-lookup"><span data-stu-id="9d860-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9d860-109">Kõik varem kinnitatud arve arverea üksikasjad kopeeritakse uude mustandisse.</span><span class="sxs-lookup"><span data-stu-id="9d860-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9d860-110">Järgnevalt on toodud mõned olulised punktid, et saaksite aru uue parandatud arve rea üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="9d860-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9d860-111">Kõigi koguste väärtused muudetakse nulliks.</span><span class="sxs-lookup"><span data-stu-id="9d860-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9d860-112">Dynamics 365 Project Operations eeldab, et kõik arveldatud üksused on täielikult krediteeritud.</span><span class="sxs-lookup"><span data-stu-id="9d860-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9d860-113">Vajaduse korral saate neid koguseid käsitsi värskendada, et kajastada arveldatud kogust, mitte krediteeritud kogust.</span><span class="sxs-lookup"><span data-stu-id="9d860-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9d860-114">Teie sisestatud koguse põhjal arvutab rakendus krediteeritud koguse.</span><span class="sxs-lookup"><span data-stu-id="9d860-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9d860-115">See summa kajastub tegelikes näitajates, mis luuakse parandatud arve kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="9d860-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9d860-116">Kui muudate maksusummat, peate sisestama õige maksusumma, mitte maksusumma, mis krediteeritakse.</span><span class="sxs-lookup"><span data-stu-id="9d860-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9d860-117">Vahe-eesmärgi parandused töödeldakse alati täieliku krediidina.</span><span class="sxs-lookup"><span data-stu-id="9d860-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="9d860-118">Arverea üksikasjadel, mis on muude juba arveldatud kulude parandused, on välja **Parandus** väärtuseks seatud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9d860-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="9d860-119">Arvetel, millel on parandatud arve rea üksikasjad, on välja **Sisaldab parandusi** väärtuseks seatud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9d860-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="9d860-120">Parandusarve kinnitamisel loodavad tegelikud näitajad</span><span class="sxs-lookup"><span data-stu-id="9d860-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="9d860-121">Järgmises tabelis on loetletud tegelikud andmed, mis luuakse, kui parandusarve on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="9d860-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9d860-122">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9d860-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9d860-123">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9d860-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d860-124">Varem arveldatud ajatehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-125">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-126">Uue arveldamata müügi tegeliku näitaja tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d860-127">Osalise krediidi arveldamine ajatehinguga.</span><span class="sxs-lookup"><span data-stu-id="9d860-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-128">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-129">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="9d860-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-130">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud tundide ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="9d860-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d860-131">Varem arveldatud kulutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-132">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-133">Uus arveldamata müügi tegelik näitaja algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d860-134">Varem arveldatud kulutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-135">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-136">Uus arveldamata müügi tegelik väärtus, mis on arveldatav parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="9d860-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-137">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="9d860-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d860-138">Varem arveldatud materjali kande täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-139">Esitatud arvega müügi tagasipööramine materjali algsel arverea üksikasjal sisalduvale kogusele ja summale.</span><span class="sxs-lookup"><span data-stu-id="9d860-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-140">Esitatud uus arveldamata müügi tegelik väärtus materjali algsel arverea üksikasjal sisalduvale kogusele ja summale.</span><span class="sxs-lookup"><span data-stu-id="9d860-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d860-141">Materjali tehingu osalise krediidi eest arve esitamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-142">Esitatud arvega müügi tagasipööramine materjali algse arverea üksikasjal sisalduvale arveldatud kogusele ja summale.</span><span class="sxs-lookup"><span data-stu-id="9d860-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-143">Uus arveldamata müügi tegelik väärtus, mille eest esitatakse arve muudetud arve rea üksikasjades oleva koguse ja summa eest, selle ümberpööramine ja sellega võrdväärse arveldatud müügi tegelik summa.</span><span class="sxs-lookup"><span data-stu-id="9d860-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-144">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="9d860-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d860-145">Varem arveldatud tasutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-146">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-147">Uus arveldamata müügi tegelik näitaja algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d860-148">Varem arveldatud tasutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-149">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-150">Uus arveldamata müügi tegelik väärtus, mis on arveldatav redigeeritud parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="9d860-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9d860-151">Varem arveldatud vahe-eesmärgi täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-152">Arveldatud müügi tühistamine algse vahe-eesmärgi jaoks mõeldud arverea üksikasjad summa puhul.</span><span class="sxs-lookup"><span data-stu-id="9d860-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9d860-153">Vahe-etapi arve olek värskendatakse valikult <b>Kliendi arve on sisestatud</b> valikule <b>Arveldamiseks valmis</b>.</span><span class="sxs-lookup"><span data-stu-id="9d860-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9d860-154">Varem arveldatud vahe-eesmärgi osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="9d860-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d860-155">Seda stsenaariumi ei toetata.</span><span class="sxs-lookup"><span data-stu-id="9d860-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
