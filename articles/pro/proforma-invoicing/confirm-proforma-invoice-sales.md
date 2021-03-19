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
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274273"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="7b0cb-103">Näidisarve kinnitamine – liht</span><span class="sxs-lookup"><span data-stu-id="7b0cb-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="7b0cb-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="7b0cb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7b0cb-105">Pärast näidisarve kinnitamist värskendatakse projekti arve olekuks **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="7b0cb-106">Kui arve on kinnitatud, muutub see kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="7b0cb-107">Edaspidi saab arvet parandada ainult juhul, kui on kliendi algatatud parandused või krediidid, või kui arve on märgitud tasutuks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="7b0cb-108">Järgmises tabelis on loetletud süsteemi loodud tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="7b0cb-109">Need tegelikud näitajad luuakse teatud toimingute tegemisel projekti arve mustandisse enne selle kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="7b0cb-110">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7b0cb-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="7b0cb-111">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7b0cb-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-112">Ettemaksu või honorari arveldamine</span><span class="sxs-lookup"><span data-stu-id="7b0cb-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-113">Arvestatud müügi tegeliku näitaja tüüp, <strong>Honorar</strong> luuakse ettemakse või honorari summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-114">Honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-115">Pärast honorari või ettemaksu täielikku vastavusseviimist arvega.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-116">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7b0cb-117">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-118">Arveldatud müügi tegelik näitaja selle arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7b0cb-119">Pärast honorari või ettemaksu osalist vastavusseviimist arvega.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-120">Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7b0cb-121">See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-122">Arveldatud müügi tegelik näitaja selle arve summa jaoks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-123">Järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-124">Ajatehingu arveldamine ilma mustandi arvel tehtud muudatusteta.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-125">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-126">Arveldatud müügi tegelikud näitaja algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7b0cb-127">Ajatehingu arveldamine, mida redigeeriti koguse vähendamiseks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-128">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-129">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-130">Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud tundide ja summa eest pärast parandatud arvude mahaarvamist, tegeliku müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-131">Ajatehingu arveldamine, mida redigeeriti koguse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-132">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-133">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-134">Kulu tehingu arveldamine ilma mustandi arvel tehtud muudatusteta.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-135">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-136">Arveldatud müügi tegelik väärtus algse kulukinnituse koguse ja summa puhul</span><span class="sxs-lookup"><span data-stu-id="7b0cb-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7b0cb-137">Kulu tehingu arveldamine, mida redigeeriti koguse vähendamiseks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-138">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-139">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-140">Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud koguse ja summa eest pärast parandatud arvude mahaarvamist, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-141">Kulu tehingu arveldamine, mida redigeeriti koguse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-142">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-143">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b0cb-144">Arve esitamine.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-145">Arveldamata müügi tühistamine algse töölehe rea tasude puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-146">Arveldatud müügi tegelik väärtus algse töölehe rea tasude koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7b0cb-147">Vahe-eesmärgi esitamine.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-148">Projekti lepingurea algse vahe-eesmärgi vahe-eesmärgi arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7b0cb-149">Tootepõhiste lepinguridade arveldamine.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b0cb-150">Selle toote rea arveldatud tegelik müük, mille kogus ja summa pärineb tootepõhiselt lepingurealt.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]