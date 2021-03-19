---
title: Parandatud arved – liht
description: Selles teemas antakse teavet Project Operationsis parandatud arvete kohta.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274228"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="2f823-103">Parandatud arved – liht</span><span class="sxs-lookup"><span data-stu-id="2f823-103">Corrected invoices - lite</span></span>

<span data-ttu-id="2f823-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="2f823-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f823-105">Kinnitatud projekti arvet saab parandada muudatuste või krediidi töötlemiseks, pidades läbirääkimisi kliendi ja projektijuhiga.</span><span class="sxs-lookup"><span data-stu-id="2f823-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="2f823-106">Kinnitatud arve redigeerimiseks avage kinnitatud arve ja valige suvand **Paranda seda arvet**.</span><span class="sxs-lookup"><span data-stu-id="2f823-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2f823-107">See valik pole saadaval, kui projekti arve pole kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="2f823-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="2f823-108">Uus arve mustand luuakse kinnitatud arvelt.</span><span class="sxs-lookup"><span data-stu-id="2f823-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="2f823-109">Kõik varem kinnitatud arve arverea üksikasjad kopeeritakse uude mustandisse.</span><span class="sxs-lookup"><span data-stu-id="2f823-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="2f823-110">Järgnevalt on toodud mõned olulised punktid, et saaksite aru uue parandatud arve rea üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="2f823-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="2f823-111">Kõigi koguste väärtused muudetakse nulliks.</span><span class="sxs-lookup"><span data-stu-id="2f823-111">All quantities are updated to zero.</span></span> <span data-ttu-id="2f823-112">Rakendus eeldab, et kõik arveldatud üksused krediteeritakse täielikult.</span><span class="sxs-lookup"><span data-stu-id="2f823-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="2f823-113">Vajaduse korral saate neid koguseid käsitsi värskendada, et kajastada arveldatud kogust, mitte krediteeritud kogust.</span><span class="sxs-lookup"><span data-stu-id="2f823-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="2f823-114">Teie sisestatud koguse põhjal arvutab rakendus krediteeritud koguse.</span><span class="sxs-lookup"><span data-stu-id="2f823-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="2f823-115">See summa kajastub tegelikes näitajates, mis luuakse parandatud arve kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="2f823-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="2f823-116">Kui muudate maksusummat, peate sisestama õige maksusumma, mitte maksusumma, mis krediteeritakse.</span><span class="sxs-lookup"><span data-stu-id="2f823-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="2f823-117">Varem kinnitatud tootepõhiseid lepinguridu ei kopeerita üle.</span><span class="sxs-lookup"><span data-stu-id="2f823-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="2f823-118">Tootepõhisel projekti arvel ei toetata paranduste töötlemist.</span><span class="sxs-lookup"><span data-stu-id="2f823-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="2f823-119">Vahe-eesmärgi parandused töödeldakse alati täieliku krediidina.</span><span class="sxs-lookup"><span data-stu-id="2f823-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="2f823-120">Honorari või ettemakse summasid saab parandada juhul, kui kliendile esitati arve vale summaga.</span><span class="sxs-lookup"><span data-stu-id="2f823-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="2f823-121">Kui varem kinnitatud arvega vastavusse viimiseks on kasutatud valet summat, siis saate parandada honoraride ja ettemaksete vastavusseviimist.</span><span class="sxs-lookup"><span data-stu-id="2f823-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f823-122">Arve rea üksikasjadel, mis on parandustes muude juba arveldatud tasude jaoks, on välja **Parandus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="2f823-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="2f823-123">Arvetel, millel on parandatud arve rea üksikasju, on välja **Parandustega** väärtuseks samuti **Jah**.</span><span class="sxs-lookup"><span data-stu-id="2f823-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="2f823-124">Parandatud arve kinnitamisel loodud tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="2f823-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="2f823-125">Allpool on tegelikud näitajad, mis on loodud rakendusega, mis on seotud parandatud arve mustandis tehtud toimingutega, enne kinnituse kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="2f823-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="2f823-126">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2f823-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="2f823-127">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2f823-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2f823-128">Kinnitage arveldatud ettemakse või honorari parandamine.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2f823-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-129">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f823-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2f823-130">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="2f823-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-131">Arveldatud müügi tühistamise tegelik näitaja luuakse honorari või ettemakse summa jaoks, et algne arveldatud müük tühistada.</span><span class="sxs-lookup"><span data-stu-id="2f823-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-132">Honorari või ettemakse parandatud arve real luuakse parandatud summa jaoks uus arveldatud müügi tegelik näitaja.</span><span class="sxs-lookup"><span data-stu-id="2f823-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-133">Honorari või ettemakse parandatud arve rea negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="2f823-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2f823-134">Kinnitus varem vastavusse viidud honorari või ettemakse parandamise kohta.</span><span class="sxs-lookup"><span data-stu-id="2f823-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-135">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f823-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2f823-136">See summa on positiivne ja selle eesmärk on tühistada negatiivne summa, mis loodi eelmise vastavusseviimise ajal.</span><span class="sxs-lookup"><span data-stu-id="2f823-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-137">Arveldatud müügi tegelik näitaja tühistatakse eelmise arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f823-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-138">Uus arveldatud müügi tegelik näitaja parandatud honorari summa jaoks, mis rakendatakse parandatud arvele.</span><span class="sxs-lookup"><span data-stu-id="2f823-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-139">Parandatud järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="2f823-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2f823-140">Varem arveldatud ajatehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-141">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-142">Uue arveldamata müügi tegeliku näitaja tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2f823-143">Osalise krediidi arveldamine ajatehinguga.</span><span class="sxs-lookup"><span data-stu-id="2f823-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-144">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-145">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="2f823-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-146">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud tundide ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="2f823-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2f823-147">Varem arveldatud kulutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-148">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-149">Uus arveldamata müügi tegelik näitaja algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2f823-150">Varem arveldatud kulutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-151">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-152">Uus arveldamata müügi tegelik väärtus, mis on arveldatav parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="2f823-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-153">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="2f823-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2f823-154">Varem arveldatud tasutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-155">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-156">Uus arveldamata müügi tegelik näitaja algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2f823-157">Varem arveldatud tasutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-158">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-159">Uus arveldamata müügi tegelik väärtus, mis on arveldatav redigeeritud parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="2f823-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2f823-160">Varem arveldatud vahe-eesmärgi täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-161">Arveldatud müügi tühistamine algse vahe-eesmärgi jaoks mõeldud arverea üksikasjad summa puhul.</span><span class="sxs-lookup"><span data-stu-id="2f823-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="2f823-162">Projekti lepingurea vahe-eesmärgi arve või arveldamise olek on muudetud olekuks **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="2f823-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2f823-163">Varem arveldatud vahe-eesmärgi osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="2f823-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-164">Mittetoetatud</span><span class="sxs-lookup"><span data-stu-id="2f823-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2f823-165">Varem arveldatud tootepõhise lepingurea krediit ja parandused.</span><span class="sxs-lookup"><span data-stu-id="2f823-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2f823-166">Mittetoetatud</span><span class="sxs-lookup"><span data-stu-id="2f823-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]