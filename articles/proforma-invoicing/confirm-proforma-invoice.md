---
title: Näidisarve kinnitamine
description: Selles teemas antakse teavet fiktiivse arve kinnitamise kohta.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287863"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="bf2c3-103">Näidisarve kinnitamine</span><span class="sxs-lookup"><span data-stu-id="bf2c3-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="bf2c3-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="bf2c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bf2c3-105">Pärast näidisarve kinnitamist värskendatakse projekti arve olekuks **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="bf2c3-106">Kui arve on kinnitatud, muutub see kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="bf2c3-107">Edaspidi saab arvet parandada ainult juhul, kui on kliendi algatatud parandused või krediidid, või kui see on märgitud tasutuks.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="bf2c3-108">Järgmises tabelis on loetletud süsteemi loodud tegelikud näitajad.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="bf2c3-109">Need tegelikud näitajad luuakse teatud toimingute tegemisel projekti arve mustandisse enne selle kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="bf2c3-110">
                    <strong>Stsenaarium</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bf2c3-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="bf2c3-111">
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bf2c3-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bf2c3-112">Ajatehingu arveldamine ilma mustandi arvel tehtud muudatusteta.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-113">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-114">Arveldatud müügi tegelikud näitaja algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bf2c3-115">Ajatehingu arveldamine, mida redigeeriti koguse vähendamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-116">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-117">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-118">Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud tundide ja summa eest pärast parandatud arvude mahaarvamist, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bf2c3-119">Ajatehingu arveldamine, mida redigeeriti koguse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-120">Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-121">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bf2c3-122">Kulu tehingu arveldamine ilma mustandi arvel tehtud muudatusteta.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-123">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-124">Arveldatud müügi tegelik väärtus algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bf2c3-125">Kulu tehingu arveldamine, mida redigeeriti koguse vähendamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-126">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-127">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-128">Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud koguse ja summa eest pärast parandatud arvude mahaarvamist, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bf2c3-129">Kulu tehingu arveldamine, mida redigeeriti koguse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-130">Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-131">Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bf2c3-132">Arve esitamine.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-133">Arveldamata müügi tühistamine algse töölehe rea tasude puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-134">Arveldatud müügi tegelik väärtus algse töölehe rea tasude koguse ja summa puhul.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="bf2c3-135">Vahe-eesmärgi esitamine.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bf2c3-136">Projekti lepingurea algse vahe-eesmärgi vahe-eesmärgi arveldatud müügi tegelik väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf2c3-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]