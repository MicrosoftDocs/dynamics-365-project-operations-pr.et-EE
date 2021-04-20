---
title: Projekti parandusarved
description: See teema sisaldab teavet selle kohta, kuidas luua ja kinnitada Project Operationsis parandusarveid.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866586"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="ba959-103">Projekti parandusarved</span><span class="sxs-lookup"><span data-stu-id="ba959-103">Corrective project invoices</span></span>

<span data-ttu-id="ba959-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="ba959-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba959-105">Kinnitatud projekti arvet saab parandada muudatuste või krediidi töötlemiseks, pidades läbirääkimisi kliendi ja projektijuhiga.</span><span class="sxs-lookup"><span data-stu-id="ba959-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="ba959-106">Kinnitatud arve redigeerimiseks avage kinnitatud arve ja valige suvand **Paranda seda arvet**.</span><span class="sxs-lookup"><span data-stu-id="ba959-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ba959-107">See valik pole saadaval, kui projekti arve pole kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="ba959-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="ba959-108">Uus arve mustand luuakse kinnitatud arvelt.</span><span class="sxs-lookup"><span data-stu-id="ba959-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="ba959-109">Kõik varem kinnitatud arve arverea üksikasjad kopeeritakse uude mustandisse.</span><span class="sxs-lookup"><span data-stu-id="ba959-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="ba959-110">Järgnevalt on toodud mõned olulised punktid, et saaksite aru uue parandatud arve rea üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="ba959-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="ba959-111">Kõigi koguste väärtused muudetakse nulliks.</span><span class="sxs-lookup"><span data-stu-id="ba959-111">All quantities are updated to zero.</span></span> <span data-ttu-id="ba959-112">Rakendus eeldab, et kõik arveldatud üksused krediteeritakse täielikult.</span><span class="sxs-lookup"><span data-stu-id="ba959-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="ba959-113">Vajaduse korral saate neid koguseid käsitsi värskendada, et kajastada arveldatud kogust, mitte krediteeritud kogust.</span><span class="sxs-lookup"><span data-stu-id="ba959-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="ba959-114">Teie sisestatud koguse põhjal arvutab rakendus krediteeritud koguse.</span><span class="sxs-lookup"><span data-stu-id="ba959-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="ba959-115">See summa kajastub tegelikes näitajates, mis luuakse parandatud arve kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="ba959-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="ba959-116">Kui muudate maksusummat, peate sisestama õige maksusumma, mitte maksusumma, mis krediteeritakse.</span><span class="sxs-lookup"><span data-stu-id="ba959-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="ba959-117">Varem kinnitatud tootepõhiseid lepinguridu ei kopeerita üle.</span><span class="sxs-lookup"><span data-stu-id="ba959-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="ba959-118">Tootepõhisel projekti arvel ei toetata paranduste töötlemist.</span><span class="sxs-lookup"><span data-stu-id="ba959-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="ba959-119">Vahe-eesmärgi parandused töödeldakse alati täieliku krediidina.</span><span class="sxs-lookup"><span data-stu-id="ba959-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="ba959-120">Honorari või ettemakse summasid saab parandada juhul, kui kliendile esitati arve vale summaga.</span><span class="sxs-lookup"><span data-stu-id="ba959-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="ba959-121">Kui varem kinnitatud arvega vastavusse viimiseks on kasutatud valet summat, siis saate parandada honoraride ja ettemaksete vastavusseviimist.</span><span class="sxs-lookup"><span data-stu-id="ba959-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba959-122">Arve rea üksikasjadel, mis on parandustes muude juba arveldatud tasude jaoks, on välja **Parandus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ba959-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="ba959-123">Arvetel, millel on parandatud arve rea üksikasju, on välja **Parandustega** väärtuseks samuti **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ba959-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="ba959-124">Parandusarve kinnitamisel loodavad tegelikud näitajad</span><span class="sxs-lookup"><span data-stu-id="ba959-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="ba959-125">Järgmises tabelis on loetletud tegelikud andmed, mis luuakse, kui parandusarve on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="ba959-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ba959-126">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ba959-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ba959-127">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ba959-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="ba959-128">Kinnitage arveldatud ettemakse või honorari parandamine.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ba959-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-129">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="ba959-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ba959-130">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="ba959-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-131">Arveldatud müügi tühistamise tegelik näitaja luuakse honorari või ettemakse summa jaoks, et algne arveldatud müük tühistada.</span><span class="sxs-lookup"><span data-stu-id="ba959-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-132">Honorari või ettemakse parandatud arve real luuakse parandatud summa jaoks uus arveldatud müügi tegelik näitaja.</span><span class="sxs-lookup"><span data-stu-id="ba959-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-133">Honorari või ettemakse parandatud arve rea negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="ba959-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="ba959-134">Kinnitus varem vastavusse viidud honorari või ettemakse parandamise kohta.</span><span class="sxs-lookup"><span data-stu-id="ba959-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-135">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="ba959-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ba959-136">See summa on positiivne ja selle eesmärk on tühistada negatiivne summa, mis loodi eelmise vastavusseviimise ajal.</span><span class="sxs-lookup"><span data-stu-id="ba959-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-137">Arveldatud müügi tegelik näitaja tühistatakse eelmise arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="ba959-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-138">Uus arveldatud müügi tegelik näitaja parandatud honorari summa jaoks, mis rakendatakse parandatud arvele.</span><span class="sxs-lookup"><span data-stu-id="ba959-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-139">Parandatud järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="ba959-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ba959-140">Varem arveldatud ajatehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-141">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-142">Uue arveldamata müügi tegeliku näitaja tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ba959-143">Osalise krediidi arveldamine ajatehinguga.</span><span class="sxs-lookup"><span data-stu-id="ba959-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-144">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-145">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="ba959-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-146">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud tundide ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="ba959-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ba959-147">Varem arveldatud kulutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-148">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-149">Uus arveldamata müügi tegelik näitaja algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ba959-150">Varem arveldatud kulutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-151">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-152">Uus arveldamata müügi tegelik väärtus, mis on arveldatav parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="ba959-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-153">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="ba959-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ba959-154">Varem arveldatud materjali kande täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-155">Esitatud arvega müügi tagasipööramine materjali algsel arverea üksikasjal sisalduvale kogusele ja summale.</span><span class="sxs-lookup"><span data-stu-id="ba959-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-156">Esitatud uus arveldamata müügi tegelik väärtus materjali algsel arverea üksikasjal sisalduvale kogusele ja summale.</span><span class="sxs-lookup"><span data-stu-id="ba959-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ba959-157">Materjali tehingu osalise krediidi eest arve esitamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-158">Esitatud arvega müügi tagasipööramine materjali algse arverea üksikasjal sisalduvale arveldatud kogusele ja summale.</span><span class="sxs-lookup"><span data-stu-id="ba959-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-159">Uus arveldamata müügi tegelik väärtus, mille eest esitatakse arve muudetud arve rea üksikasjades oleva koguse ja summa eest, selle ümberpööramine ja sellega võrdväärse arveldatud müügi tegelik summa.</span><span class="sxs-lookup"><span data-stu-id="ba959-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-160">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="ba959-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ba959-161">Varem arveldatud tasutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-162">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-163">Uus arveldamata müügi tegelik näitaja algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ba959-164">Varem arveldatud tasutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-165">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-166">Uus arveldamata müügi tegelik väärtus, mis on arveldatav redigeeritud parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="ba959-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ba959-167">Varem arveldatud vahe-eesmärgi täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-168">Arveldatud müügi tühistamine algse vahe-eesmärgi jaoks mõeldud arverea üksikasjad summa puhul.</span><span class="sxs-lookup"><span data-stu-id="ba959-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="ba959-169">Vahe-etapi arve olek värskendatakse valikult <b>Kliendi arve on sisestatud</b> valikule <b>Arveldamiseks valmis</b>.</span><span class="sxs-lookup"><span data-stu-id="ba959-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ba959-170">Varem arveldatud vahe-eesmärgi osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="ba959-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-171">Mittetoetatud</span><span class="sxs-lookup"><span data-stu-id="ba959-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ba959-172">Varem arveldatud tootepõhise lepingurea krediit ja parandused.</span><span class="sxs-lookup"><span data-stu-id="ba959-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ba959-173">Mittetoetatud</span><span class="sxs-lookup"><span data-stu-id="ba959-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
