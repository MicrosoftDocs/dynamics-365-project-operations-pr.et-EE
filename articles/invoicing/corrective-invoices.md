---
title: Projektipõhise parandusarvete loomine
description: See teema sisaldab teavet Project Operationsi parandusarvete kohta.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001605"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="e5648-103">Projektipõhise parandusarvete loomine</span><span class="sxs-lookup"><span data-stu-id="e5648-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="e5648-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="e5648-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e5648-105">Kinnitatud projekti arvet saab parandada muudatuste või krediidi töötlemiseks, pidades läbirääkimisi kliendi ja projektijuhiga.</span><span class="sxs-lookup"><span data-stu-id="e5648-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="e5648-106">Kinnitatud arve redigeerimiseks avage kinnitatud arve ja valige suvand **Paranda seda arvet**.</span><span class="sxs-lookup"><span data-stu-id="e5648-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="e5648-107">See valik pole saadaval, kui projekti arve pole kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="e5648-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="e5648-108">Uus arve mustand luuakse kinnitatud arvelt.</span><span class="sxs-lookup"><span data-stu-id="e5648-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="e5648-109">Kõik varem kinnitatud arve arverea üksikasjad kopeeritakse uude mustandisse.</span><span class="sxs-lookup"><span data-stu-id="e5648-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="e5648-110">Järgmised on mõned põhipunktid, mis aitavad teil uue parandatud arve rea üksikasju paremini mõista.</span><span class="sxs-lookup"><span data-stu-id="e5648-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="e5648-111">Kõigi koguste väärtused muudetakse nulliks.</span><span class="sxs-lookup"><span data-stu-id="e5648-111">All quantities are updated to zero.</span></span> <span data-ttu-id="e5648-112">See eeldab, et kõik arveldatud üksused on täielikult krediteeritud.</span><span class="sxs-lookup"><span data-stu-id="e5648-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="e5648-113">Vajaduse korral saate neid koguseid käsitsi värskendada, et kajastada arveldatud kogust, mitte krediteeritud kogust.</span><span class="sxs-lookup"><span data-stu-id="e5648-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="e5648-114">Teie sisestatud koguse põhjal arvutab rakendus krediteeritud koguse.</span><span class="sxs-lookup"><span data-stu-id="e5648-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="e5648-115">See summa kajastub tegelikes näitajates, mis luuakse parandatud arve kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="e5648-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="e5648-116">Kui muudate maksusummat, peate sisestama õige maksusumma, mitte maksusumma, mis krediteeritakse.</span><span class="sxs-lookup"><span data-stu-id="e5648-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="e5648-117">Vahe-eesmärgi parandused töödeldakse alati täieliku krediidina.</span><span class="sxs-lookup"><span data-stu-id="e5648-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="e5648-118">Honorari või ettemakse summasid saab parandada juhul, kui kliendile esitati arve vale summaga.</span><span class="sxs-lookup"><span data-stu-id="e5648-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="e5648-119">Kui varem kinnitatud arvega vastavusse viimiseks on kasutatud valet summat, siis saate parandada honoraride ja ettemaksete vastavusseviimist.</span><span class="sxs-lookup"><span data-stu-id="e5648-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5648-120">Arverea üksikasjadel, mis on muude juba arveldatud kulude parandused, on välja **Parandus** väärtuseks seatud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e5648-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="e5648-121">Arvetel, millel on parandatud arve rea üksikasju, on välja **Parandustega** väärtuseks samuti **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e5648-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="e5648-122">Parandatud arve kinnitamisel loodud tegelikud näitajad</span><span class="sxs-lookup"><span data-stu-id="e5648-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="e5648-123">Järgmises tabelis on loetletud tegelikud andmed, mis luuakse, kui parandusarve on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="e5648-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="e5648-124">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5648-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="e5648-125">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5648-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="e5648-126">Kinnitage arveldatud ettemakse või honorari parandamine.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5648-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-127">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="e5648-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e5648-128">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="e5648-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-129">Arveldatud müügi tühistamise tegelik näitaja luuakse honorari või ettemakse summa jaoks, et algne arveldatud müük tühistada.</span><span class="sxs-lookup"><span data-stu-id="e5648-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-130">Honorari või ettemakse parandatud arve real luuakse parandatud summa jaoks uus arveldatud müügi tegelik näitaja.</span><span class="sxs-lookup"><span data-stu-id="e5648-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-131">Honorari või ettemakse parandatud arve rea negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="e5648-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="e5648-132">Kinnitus varem vastavusse viidud honorari või ettemakse parandamise kohta.</span><span class="sxs-lookup"><span data-stu-id="e5648-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-133">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="e5648-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e5648-134">See summa on positiivne ja selle eesmärk on tühistada negatiivne summa, mis loodi eelmise vastavusseviimise ajal.</span><span class="sxs-lookup"><span data-stu-id="e5648-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-135">Arveldatud müügi tegelik näitaja tühistatakse eelmise arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="e5648-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-136">Uus arveldatud müügi tegelik näitaja parandatud honorari summa jaoks, mis rakendatakse parandatud arvele.</span><span class="sxs-lookup"><span data-stu-id="e5648-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-137">Parandatud järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="e5648-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5648-138">Varem arveldatud ajatehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-139">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-140">Uue arveldamata müügi tegeliku näitaja tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e5648-141">Osalise krediidi arveldamine ajatehinguga.</span><span class="sxs-lookup"><span data-stu-id="e5648-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-142">Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-143">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="e5648-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-144">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud tundide ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="e5648-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5648-145">Varem arveldatud kulutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-146">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-147">Uus arveldamata müügi tegelik näitaja algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e5648-148">Varem arveldatud kulutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-149">Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-150">Uus arveldamata müügi tegelik väärtus, mis on arveldatav parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="e5648-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-151">Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.</span><span class="sxs-lookup"><span data-stu-id="e5648-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5648-152">Varem arveldatud tasutehingu täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-153">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-154">Uus arveldamata müügi tegelik näitaja algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5648-155">Varem arveldatud tasutehingu osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-156">Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-157">Uus arveldamata müügi tegelik väärtus, mis on arveldatav redigeeritud parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="e5648-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e5648-158">Varem arveldatud vahe-eesmärgi täieliku krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-159">Arveldatud müügi tühistamine algse vahe-eesmärgi jaoks mõeldud arverea üksikasjad summa puhul.</span><span class="sxs-lookup"><span data-stu-id="e5648-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="e5648-160">Vahe-etapi arve olek värskendatakse valikult <b>Kliendi arve on sisestatud</b> valikule <b>Arveldamiseks valmis</b>.</span><span class="sxs-lookup"><span data-stu-id="e5648-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e5648-161">Varem arveldatud vahe-eesmärgi osalise krediidi arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e5648-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5648-162">Mittetoetatud</span><span class="sxs-lookup"><span data-stu-id="e5648-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
