---
title: Tegelikud
description: Selles teemas antakse teavet projektiga seotud tegelike andmete kohta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751027"
---
# <a name="actuals"></a><span data-ttu-id="1ae55-103">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="1ae55-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1ae55-104">Tegelikud andmed on projektiga lõpule viidud tööd.</span><span class="sxs-lookup"><span data-stu-id="1ae55-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="1ae55-105">Projekti tegelikke andmeid saab tuvastada nende alusdokumendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="1ae55-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="1ae55-106">Alusdokumendid sisaldavad aja-, kulu- ja töölehe kandeid, aga ka arveid.</span><span class="sxs-lookup"><span data-stu-id="1ae55-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kuidas projekti tegelikud andmed alusdokumentidega ühendatakse?](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="1ae55-108">Ajakirje esitamisel</span><span class="sxs-lookup"><span data-stu-id="1ae55-108">Submitting a time entry</span></span>

<span data-ttu-id="1ae55-109">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjalide töölehe reaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="1ae55-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="1ae55-110">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="1ae55-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="1ae55-111">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ae55-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="1ae55-112">Vaikehindade sisestamise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="1ae55-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="1ae55-113">Kõik ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="1ae55-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="1ae55-114">Need väljad hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="1ae55-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="1ae55-115">Vaikehindu mõjutavate väljade (nt **roll** ja **organisatsiooniüksus**) töölehe reale sisestatakse sobivad hinnad vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="1ae55-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="1ae55-116">Kui lisate ajakirjele kohandatud välja ning soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.</span><span class="sxs-lookup"><span data-stu-id="1ae55-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="1ae55-117">Kulukirje esitamine</span><span class="sxs-lookup"><span data-stu-id="1ae55-117">Submitting an expense entry</span></span>

<span data-ttu-id="1ae55-118">Kui kulukirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjali lepingureaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="1ae55-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="1ae55-119">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="1ae55-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="1ae55-120">Kui fikseeritud hinnaga sisestus esitatakse projektile, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ae55-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="1ae55-121">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial, mis on lehe jaotises **Kulukirje**.</span><span class="sxs-lookup"><span data-stu-id="1ae55-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="1ae55-122">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="1ae55-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1ae55-123">Hinna enda jaoks on kasutaja sisestatud suurus kulude ja müügi jaoks vaikimisi määratud otse seotud kulukirje töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="1ae55-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="1ae55-124">PSA praeguses versioonis ei ole kategoorial põhinev ühiku vaikehinna kanne saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ae55-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="1ae55-125">Töölehtede kasutamine kulude kirjendamiseks</span><span class="sxs-lookup"><span data-stu-id="1ae55-125">Using journals to record costs</span></span>

<span data-ttu-id="1ae55-126">PSA-s võimaldavad töölehed teil kirjendada kulu või tulu materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="1ae55-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="1ae55-127">Töölehel on päis, read ja toiming **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="1ae55-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="1ae55-128">Toome mõned näited, kus võiksite töölehte kasutada.</span><span class="sxs-lookup"><span data-stu-id="1ae55-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="1ae55-129">Peate kirjendma projektiga seotud tegelikku materjalikulu ja müüki.</span><span class="sxs-lookup"><span data-stu-id="1ae55-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="1ae55-130">Peate tehingu tegelikud andmed teistest süsteemist PSA-sse üle viima.</span><span class="sxs-lookup"><span data-stu-id="1ae55-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="1ae55-131">Peate kirjendama mõnes muus süsteemis aset leidnud kulusid (nt hanke- või alltöövõtu kulud).</span><span class="sxs-lookup"><span data-stu-id="1ae55-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="1ae55-132">Projektisündmustel põhinevate tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="1ae55-132">Recording actuals based on project events</span></span>

<span data-ttu-id="1ae55-133">PSA salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="1ae55-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="1ae55-134">Need kanded kirjendatakse **tegelike andmetena**.</span><span class="sxs-lookup"><span data-stu-id="1ae55-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="1ae55-135">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="1ae55-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="1ae55-136">**Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse**</span><span class="sxs-lookup"><span data-stu-id="1ae55-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1ae55-137">Sündmus</span><span class="sxs-lookup"><span data-stu-id="1ae55-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1ae55-138">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="1ae55-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1ae55-139">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="1ae55-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1ae55-140">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="1ae55-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1ae55-141">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="1ae55-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1ae55-142">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="1ae55-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1ae55-143">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="1ae55-143">Actuals</span></span></th>
<th><span data-ttu-id="1ae55-144">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-144">Transaction currency</span></span></th>
<th><span data-ttu-id="1ae55-145">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="1ae55-145">Fixed price</span></span></th>
<th><span data-ttu-id="1ae55-146">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ae55-147">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="1ae55-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1ae55-148">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-149">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="1ae55-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1ae55-150">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ae55-151">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="1ae55-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ae55-152">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-152">Cost actual</span></span></td>
<td><span data-ttu-id="1ae55-153">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-154">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-155">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="1ae55-156">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-157">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-158">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1ae55-159">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ae55-160">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="1ae55-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ae55-161">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-161">Cost actual</span></span></td>
<td><span data-ttu-id="1ae55-162">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-163">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-164">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-165">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-166">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-167">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="1ae55-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ae55-168">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-169">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ae55-170">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ae55-171">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="1ae55-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ae55-172">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ae55-173">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-174">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="1ae55-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-175">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-176">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-177">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-178">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="1ae55-178">Billed sales</span></span></td>
<td><span data-ttu-id="1ae55-179">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ae55-180">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="1ae55-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ae55-181">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ae55-182">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-183">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-184">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-185">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-186">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-187">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="1ae55-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ae55-188">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-189">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ae55-190">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ae55-191">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="1ae55-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ae55-192">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ae55-193">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1ae55-194">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="1ae55-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1ae55-195">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="1ae55-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1ae55-196">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-197">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-198">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-199">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="1ae55-199">Billed sales</span></span></td>
<td><span data-ttu-id="1ae55-200">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ae55-201">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="1ae55-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ae55-202">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ae55-203">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-204">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="1ae55-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1ae55-205">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-206">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ae55-207">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ae55-208">**Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus**</span><span class="sxs-lookup"><span data-stu-id="1ae55-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1ae55-209">Sündmus</span><span class="sxs-lookup"><span data-stu-id="1ae55-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1ae55-210">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="1ae55-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1ae55-211">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="1ae55-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1ae55-212">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="1ae55-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1ae55-213">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="1ae55-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1ae55-214">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="1ae55-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1ae55-215">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="1ae55-215">Actuals</span></span></th>
<th><span data-ttu-id="1ae55-216">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-216">Transaction currency</span></span></th>
<th><span data-ttu-id="1ae55-217">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="1ae55-217">Fixed price</span></span></th>
<th><span data-ttu-id="1ae55-218">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ae55-219">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="1ae55-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1ae55-220">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-221">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="1ae55-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1ae55-222">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1ae55-223">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="1ae55-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ae55-224">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-224">Cost actual</span></span></td>
<td><span data-ttu-id="1ae55-225">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1ae55-226">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1ae55-227">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1ae55-228">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1ae55-229">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-230">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1ae55-231">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-232">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="1ae55-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1ae55-233">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-234">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="1ae55-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1ae55-235">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1ae55-236">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="1ae55-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ae55-237">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-237">Cost actual</span></span></td>
<td><span data-ttu-id="1ae55-238">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-239">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-240">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-241">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-242">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="1ae55-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-243">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="1ae55-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1ae55-244">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-245">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="1ae55-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1ae55-246">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-247">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="1ae55-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ae55-248">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-249">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ae55-250">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ae55-251">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="1ae55-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ae55-252">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ae55-253">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-254">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="1ae55-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-255">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-256">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1ae55-257">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-258">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="1ae55-258">Billed sales</span></span></td>
<td><span data-ttu-id="1ae55-259">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ae55-260">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="1ae55-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ae55-261">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ae55-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-263">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-264">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-265">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ae55-266">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-267">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="1ae55-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ae55-268">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-269">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ae55-270">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ae55-271">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="1ae55-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ae55-272">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ae55-273">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1ae55-274">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="1ae55-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1ae55-275">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="1ae55-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1ae55-276">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-277">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1ae55-278">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="1ae55-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-279">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="1ae55-279">Billed sales</span></span></td>
<td><span data-ttu-id="1ae55-280">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ae55-281">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="1ae55-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ae55-282">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="1ae55-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ae55-283">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-284">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="1ae55-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1ae55-285">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ae55-286">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="1ae55-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ae55-287">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="1ae55-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
