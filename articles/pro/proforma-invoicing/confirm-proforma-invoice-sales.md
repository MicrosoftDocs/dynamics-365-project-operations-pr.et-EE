---
title: Näidisarve kinnitamine – liht
description: Selles teemas antakse teavet Project Operationsis näidisarvete kinnitamise kohta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176516"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="264b9-103">Näidisarve kinnitamine – liht</span><span class="sxs-lookup"><span data-stu-id="264b9-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="264b9-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="264b9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="264b9-105">Pärast näidisarve kinnitamist värskendatakse projekti arve olekuks **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="264b9-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="264b9-106">Kui arve on kinnitatud, muutub see kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="264b9-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="264b9-107">Edaspidi saab arvet parandada ainult juhul, kui on kliendi algatatud parandused või krediidid, või kui arve on märgitud tasutuks.</span><span class="sxs-lookup"><span data-stu-id="264b9-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="264b9-108">Järgmises tabelis on loetletud süsteemi loodud tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="264b9-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="264b9-109">Need tegelikud näitajad luuakse teatud toimingute tegemisel projekti arve mustandisse enne selle kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="264b9-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="264b9-110">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="264b9-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="264b9-111">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="264b9-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-112">Ettemaksu või honorari arveldamine</span><span class="sxs-lookup"><span data-stu-id="264b9-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-113">Arvestatud müügi tegeliku näitaja tüüp, <strong>Honorar</strong> luuakse ettemakse või honorari summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="264b9-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-114">Honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="264b9-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-115">Pärast honorari või ettemaksu täielikku vastavusseviimist arvega.</span><span class="sxs-lookup"><span data-stu-id="264b9-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-116">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="264b9-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="264b9-117">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="264b9-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-118">Arveldatud müügi tegelik näitaja selle arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="264b9-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="264b9-119">Pärast honorari või ettemaksu osalist vastavusseviimist arvega.</span><span class="sxs-lookup"><span data-stu-id="264b9-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-120">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="264b9-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="264b9-121">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="264b9-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-122">Arveldatud müügi tegelik näitaja selle arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="264b9-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-123">Järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="264b9-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-124">Ajatehingu arveldamine ilma mustandi arvel tehtud muudatusteta.</span><span class="sxs-lookup"><span data-stu-id="264b9-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-125">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-126">Arveldatud müügi tegelikud näitaja algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="264b9-127">Ajatehingu arveldamine, mida redigeeriti koguse vähendamiseks.</span><span class="sxs-lookup"><span data-stu-id="264b9-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-128">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-129">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-130">Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud tundide ja summa eest pärast parandatud arvude mahaarvamist, tegeliku müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-131">Ajatehingu arveldamine, mida redigeeriti koguse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="264b9-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-132">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-133">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-134">Kulu tehingu arveldamine ilma mustandi arvel tehtud muudatusteta.</span><span class="sxs-lookup"><span data-stu-id="264b9-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-135">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-136">Arveldatud müügi tegelik väärtus algse kulukinnituse koguse ja summa puhul</span><span class="sxs-lookup"><span data-stu-id="264b9-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="264b9-137">Kulu tehingu arveldamine, mida redigeeriti koguse vähendamiseks.</span><span class="sxs-lookup"><span data-stu-id="264b9-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-138">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-139">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-140">Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud koguse ja summa eest pärast parandatud arvude mahaarvamist, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-141">Kulu tehingu arveldamine, mida redigeeriti koguse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="264b9-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-142">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-143">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="264b9-144">Arve esitamine.</span><span class="sxs-lookup"><span data-stu-id="264b9-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-145">Arveldamata müügi tühistamine algse töölehe rea tasude puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-146">Arveldatud müügi tegelik väärtus algse töölehe rea tasude koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="264b9-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="264b9-147">Vahe-eesmärgi esitamine.</span><span class="sxs-lookup"><span data-stu-id="264b9-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-148">Projekti lepingurea algse vahe-eesmärgi vahe-eesmärgi arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="264b9-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="264b9-149">Tootepõhiste lepinguridade arveldamine.</span><span class="sxs-lookup"><span data-stu-id="264b9-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="264b9-150">Selle toote rea arveldatud tegelik müük, mille kogus ja summa pärineb tootepõhiselt lepingurealt.</span><span class="sxs-lookup"><span data-stu-id="264b9-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
