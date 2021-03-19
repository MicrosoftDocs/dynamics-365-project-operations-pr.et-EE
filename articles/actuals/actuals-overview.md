---
title: Tegelikud näitajad
description: Selles teemas antakse teavet tegelike andmetega töötamise kohta Microsofti Dynamics 365 Project Operationsis.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291794"
---
# <a name="actuals"></a><span data-ttu-id="8216b-103">Tegelikud näitajad</span><span class="sxs-lookup"><span data-stu-id="8216b-103">Actuals</span></span> 

<span data-ttu-id="8216b-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="8216b-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8216b-105">Tegelikud andmed on projektiga lõpule viidud tööd.</span><span class="sxs-lookup"><span data-stu-id="8216b-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="8216b-106">Need luuakse aja- ja kulukirjete ja ning töölehe kannete ja arvete tulemusena.</span><span class="sxs-lookup"><span data-stu-id="8216b-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="8216b-107">Töölehe read ja aja esitamine</span><span class="sxs-lookup"><span data-stu-id="8216b-107">Journal lines and time submission</span></span>

<span data-ttu-id="8216b-108">Lisateavet ajakirje kohta vaadake teemast [Ajakirje ülevaade](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8216b-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="8216b-109">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="8216b-109">Time and materials</span></span>

<span data-ttu-id="8216b-110">Kui esitatud ajakirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.</span><span class="sxs-lookup"><span data-stu-id="8216b-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="8216b-111">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="8216b-111">Fixed price</span></span>

<span data-ttu-id="8216b-112">Kui esitatav ajakirje seotakse projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="8216b-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="8216b-113">Vaikimisi hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="8216b-113">Default pricing</span></span>

<span data-ttu-id="8216b-114">Vaikehindade looise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="8216b-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="8216b-115">Ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="8216b-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="8216b-116">Need väärtused hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="8216b-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="8216b-117">Vaikimisi hinnakujundust mõjutavaid välju (nt **Roll** ja **Organisatsiooniüksus**) kasutatakse töölehe rea vastava hinna määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="8216b-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="8216b-118">Saate lisada ajakirjele kohandatud välja.</span><span class="sxs-lookup"><span data-stu-id="8216b-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="8216b-119">Kui soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.</span><span class="sxs-lookup"><span data-stu-id="8216b-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="8216b-120">Töölehe read ja põhikulu esitamine</span><span class="sxs-lookup"><span data-stu-id="8216b-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="8216b-121">Lisateavet kulukirje kohta vaadake teemast [Kulu ülevaade](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8216b-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="8216b-122">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="8216b-122">Time and materials</span></span>

<span data-ttu-id="8216b-123">Kui esitatud põhikulu kirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.</span><span class="sxs-lookup"><span data-stu-id="8216b-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="8216b-124">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="8216b-124">Fixed price</span></span>

<span data-ttu-id="8216b-125">Kui esitatav põhikulu kirje seotakse projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="8216b-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="8216b-126">Vaikimisi hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="8216b-126">Default pricing</span></span>

<span data-ttu-id="8216b-127">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial.</span><span class="sxs-lookup"><span data-stu-id="8216b-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="8216b-128">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="8216b-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="8216b-129">Samas vaikimisi määratakse hinna enda jaoks sisestatav summa otse kulu ja müügiga seotud kulu töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="8216b-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="8216b-130">Kategoorial põhinev ühiku vaikehinna kanne pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="8216b-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="8216b-131">Kirjete töölehtede kasutamine kulude kirjendamiseks</span><span class="sxs-lookup"><span data-stu-id="8216b-131">Use entry journals to record costs</span></span>

<span data-ttu-id="8216b-132">Saate kasutada töölehti kulu või tulu kirjendamiseks materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="8216b-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="8216b-133">Töölehti saab kasutada järgmistel eesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="8216b-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="8216b-134">Projektiga seotud tegeliku materjalikulu ja müügi kirjendamiseks.</span><span class="sxs-lookup"><span data-stu-id="8216b-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="8216b-135">Viige tehingu tegelikud andmed teisest süsteemist Microsoft Dynamics 365 Project Operationsse üle.</span><span class="sxs-lookup"><span data-stu-id="8216b-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="8216b-136">Muus süsteemis aset leidnud kulude kirjendamiseks.</span><span class="sxs-lookup"><span data-stu-id="8216b-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="8216b-137">Need kulud võivad hõlmata hanke- või alltöövõtu kulusid.</span><span class="sxs-lookup"><span data-stu-id="8216b-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8216b-138">Rakendus ei kinnita töölege rea tüüpi ega töölehe reale sisestatud seotud hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="8216b-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="8216b-139">Seega peaksid tegelike näitajate loomiseks kasutama kirjete töölehti ainult kasutaja, kes on täielikult teadlik raamatupidamuslikust mõjust, mis tegelikel näitajatel projektile on.</span><span class="sxs-lookup"><span data-stu-id="8216b-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="8216b-140">Selle töölehe tüübi mõju tõttu peaksite hoolikalt valima, kellel on kirjete töölehtede loomisele juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="8216b-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="8216b-141">Projektisündmuste põhjal tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="8216b-141">Record actuals based on project events</span></span>

<span data-ttu-id="8216b-142">Project Operations salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="8216b-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="8216b-143">Need kanded kirjendatakse tegelike andmetena.</span><span class="sxs-lookup"><span data-stu-id="8216b-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="8216b-144">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="8216b-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="8216b-145">Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse</span><span class="sxs-lookup"><span data-stu-id="8216b-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8216b-146">Sündmus</span><span class="sxs-lookup"><span data-stu-id="8216b-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8216b-147">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="8216b-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8216b-148">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="8216b-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8216b-149">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="8216b-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8216b-150">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="8216b-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8216b-151">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="8216b-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8216b-152">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="8216b-152">Actuals</span></span></th>
<th><span data-ttu-id="8216b-153">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-153">Transaction currency</span></span></th>
<th><span data-ttu-id="8216b-154">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="8216b-154">Fixed price</span></span></th>
<th><span data-ttu-id="8216b-155">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8216b-156">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="8216b-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8216b-157">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="8216b-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-158">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="8216b-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8216b-159">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="8216b-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8216b-160">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="8216b-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8216b-161">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-161">Cost actual</span></span></td>
<td><span data-ttu-id="8216b-162">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-163">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-164">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="8216b-165">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-166">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-167">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="8216b-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8216b-168">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8216b-169">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="8216b-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8216b-170">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-170">Cost actual</span></span></td>
<td><span data-ttu-id="8216b-171">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-172">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-173">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-174">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-175">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-176">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="8216b-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8216b-177">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-178">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="8216b-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8216b-179">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8216b-180">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="8216b-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8216b-181">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8216b-182">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-183">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="8216b-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-184">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-185">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-186">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-187">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="8216b-187">Billed sales</span></span></td>
<td><span data-ttu-id="8216b-188">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8216b-189">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="8216b-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8216b-190">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8216b-191">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-192">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-193">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-194">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-195">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-196">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="8216b-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8216b-197">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-198">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="8216b-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8216b-199">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8216b-200">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="8216b-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8216b-201">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8216b-202">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8216b-203">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="8216b-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8216b-204">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="8216b-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8216b-205">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-206">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-207">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-208">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="8216b-208">Billed sales</span></span></td>
<td><span data-ttu-id="8216b-209">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8216b-210">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="8216b-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8216b-211">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8216b-212">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-213">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="8216b-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8216b-214">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-215">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="8216b-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8216b-216">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="8216b-217">Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="8216b-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8216b-218">Sündmus</span><span class="sxs-lookup"><span data-stu-id="8216b-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8216b-219">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="8216b-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8216b-220">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="8216b-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8216b-221">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="8216b-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8216b-222">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="8216b-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8216b-223">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="8216b-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8216b-224">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="8216b-224">Actuals</span></span></th>
<th><span data-ttu-id="8216b-225">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-225">Transaction currency</span></span></th>
<th><span data-ttu-id="8216b-226">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="8216b-226">Fixed price</span></span></th>
<th><span data-ttu-id="8216b-227">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8216b-228">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="8216b-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8216b-229">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="8216b-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-230">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="8216b-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8216b-231">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="8216b-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="8216b-232">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="8216b-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8216b-233">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-233">Cost actual</span></span></td>
<td><span data-ttu-id="8216b-234">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8216b-235">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8216b-236">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8216b-237">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8216b-238">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-239">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="8216b-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8216b-240">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-241">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="8216b-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8216b-242">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-243">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="8216b-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8216b-244">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8216b-245">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="8216b-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8216b-246">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-246">Cost actual</span></span></td>
<td><span data-ttu-id="8216b-247">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-248">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-249">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-250">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-251">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="8216b-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-252">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="8216b-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8216b-253">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-254">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="8216b-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8216b-255">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-256">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="8216b-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8216b-257">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-258">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="8216b-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8216b-259">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8216b-260">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="8216b-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8216b-261">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8216b-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-263">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="8216b-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-264">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-265">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8216b-266">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-267">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="8216b-267">Billed sales</span></span></td>
<td><span data-ttu-id="8216b-268">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8216b-269">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="8216b-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8216b-270">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8216b-271">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-272">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-273">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-274">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8216b-275">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-276">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="8216b-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8216b-277">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-278">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="8216b-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8216b-279">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8216b-280">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="8216b-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8216b-281">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8216b-282">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8216b-283">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="8216b-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8216b-284">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="8216b-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8216b-285">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-286">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8216b-287">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="8216b-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-288">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="8216b-288">Billed sales</span></span></td>
<td><span data-ttu-id="8216b-289">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8216b-290">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="8216b-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8216b-291">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="8216b-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8216b-292">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-293">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="8216b-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8216b-294">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8216b-295">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="8216b-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8216b-296">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="8216b-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]