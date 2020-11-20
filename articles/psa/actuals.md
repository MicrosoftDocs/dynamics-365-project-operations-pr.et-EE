---
title: Tegelike näitajate ülevaade
description: Selles teemas antakse teavet projektiga seotud tegelike andmete kohta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129763"
---
# <a name="actuals-overview"></a><span data-ttu-id="66fe7-103">Tegelike näitajate ülevaade</span><span class="sxs-lookup"><span data-stu-id="66fe7-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="66fe7-104">Tegelikud andmed on projektiga lõpule viidud tööd.</span><span class="sxs-lookup"><span data-stu-id="66fe7-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="66fe7-105">Projekti tegelikke andmeid saab tuvastada nende alusdokumendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="66fe7-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="66fe7-106">Alusdokumendid sisaldavad aja-, kulu- ja töölehe kandeid, aga ka arveid.</span><span class="sxs-lookup"><span data-stu-id="66fe7-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kuidas projekti tegelikud andmed alusdokumentidega ühendatakse?](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="66fe7-108">Ajakirje esitamisel</span><span class="sxs-lookup"><span data-stu-id="66fe7-108">Submitting a time entry</span></span>

<span data-ttu-id="66fe7-109">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjalide töölehe reaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="66fe7-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="66fe7-110">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="66fe7-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="66fe7-111">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="66fe7-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="66fe7-112">Vaikehindade sisestamise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="66fe7-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="66fe7-113">Kõik ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="66fe7-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="66fe7-114">Need väljad hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="66fe7-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="66fe7-115">Vaikehindu mõjutavate väljade (nt **roll** ja **organisatsiooniüksus**) töölehe reale sisestatakse sobivad hinnad vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="66fe7-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="66fe7-116">Kui lisate ajakirjele kohandatud välja ning soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.</span><span class="sxs-lookup"><span data-stu-id="66fe7-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="66fe7-117">Kulukirje esitamine</span><span class="sxs-lookup"><span data-stu-id="66fe7-117">Submitting an expense entry</span></span>

<span data-ttu-id="66fe7-118">Kui kulukirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjali lepingureaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="66fe7-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="66fe7-119">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="66fe7-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="66fe7-120">Kui fikseeritud hinnaga sisestus esitatakse projektile, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="66fe7-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="66fe7-121">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial, mis on lehe jaotises **Kulukirje**.</span><span class="sxs-lookup"><span data-stu-id="66fe7-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="66fe7-122">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="66fe7-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="66fe7-123">Hinna enda jaoks on kasutaja sisestatud suurus kulude ja müügi jaoks vaikimisi määratud otse seotud kulukirje töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="66fe7-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="66fe7-124">PSA praeguses versioonis ei ole kategoorial põhinev ühiku vaikehinna kanne saadaval.</span><span class="sxs-lookup"><span data-stu-id="66fe7-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="66fe7-125">Kulude kirjendamiseks kirjete töölehtede kasutamine</span><span class="sxs-lookup"><span data-stu-id="66fe7-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="66fe7-126">PSA-s võimaldavad kirje töölehed teil kirjendada kulu või tulu materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="66fe7-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="66fe7-127">Töölehel on päis, read ja toiming **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="66fe7-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="66fe7-128">Toome mõned näited, kus võiksite töölehte kasutada.</span><span class="sxs-lookup"><span data-stu-id="66fe7-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="66fe7-129">Peate kirjendma projektiga seotud tegelikku materjalikulu ja müüki.</span><span class="sxs-lookup"><span data-stu-id="66fe7-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="66fe7-130">Peate tehingu tegelikud andmed teistest süsteemist PSA-sse üle viima.</span><span class="sxs-lookup"><span data-stu-id="66fe7-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="66fe7-131">Peate kirjendama mõnes muus süsteemis aset leidnud kulusid (nt hanke- või alltöövõtu kulud).</span><span class="sxs-lookup"><span data-stu-id="66fe7-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66fe7-132">Tegelike näitajate loomiseks kirje töölehtede kasutamine peaks olema tehtav ainult kasutajate poolt, kes on täielikult teadlikud projektis tegelike näitajate mõjust raamatupidamisele.</span><span class="sxs-lookup"><span data-stu-id="66fe7-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="66fe7-133">Selle põhjuseks on, et rakendus ei kontrolli töölehe rea tüüpi ega seotud hinda, mis on töölehe reale sisestatud.</span><span class="sxs-lookup"><span data-stu-id="66fe7-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="66fe7-134">Selle töölehe tüübi mõju tõttu olge hästi ettevaatlik, et kellele kirje töölehtede loomisele juurdepääs antakse.</span><span class="sxs-lookup"><span data-stu-id="66fe7-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="66fe7-135">Projektisündmustel põhinevate tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="66fe7-135">Recording actuals based on project events</span></span>

<span data-ttu-id="66fe7-136">PSA salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="66fe7-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="66fe7-137">Need kanded kirjendatakse **tegelike andmetena**.</span><span class="sxs-lookup"><span data-stu-id="66fe7-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="66fe7-138">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="66fe7-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="66fe7-139">**Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse**</span><span class="sxs-lookup"><span data-stu-id="66fe7-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="66fe7-140">Sündmus</span><span class="sxs-lookup"><span data-stu-id="66fe7-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="66fe7-141">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="66fe7-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="66fe7-142">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="66fe7-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="66fe7-143">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="66fe7-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="66fe7-144">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="66fe7-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="66fe7-145">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="66fe7-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="66fe7-146">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="66fe7-146">Actuals</span></span></th>
<th><span data-ttu-id="66fe7-147">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-147">Transaction currency</span></span></th>
<th><span data-ttu-id="66fe7-148">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="66fe7-148">Fixed price</span></span></th>
<th><span data-ttu-id="66fe7-149">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="66fe7-150">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="66fe7-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="66fe7-151">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-152">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="66fe7-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="66fe7-153">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66fe7-154">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="66fe7-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="66fe7-155">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-155">Cost actual</span></span></td>
<td><span data-ttu-id="66fe7-156">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-157">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-158">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="66fe7-159">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-160">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-161">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="66fe7-162">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66fe7-163">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="66fe7-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="66fe7-164">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-164">Cost actual</span></span></td>
<td><span data-ttu-id="66fe7-165">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-166">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-167">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-168">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-169">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-170">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="66fe7-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="66fe7-171">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-172">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="66fe7-173">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66fe7-174">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="66fe7-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="66fe7-175">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="66fe7-176">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-177">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="66fe7-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-178">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-179">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-180">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-181">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="66fe7-181">Billed sales</span></span></td>
<td><span data-ttu-id="66fe7-182">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66fe7-183">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="66fe7-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="66fe7-184">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="66fe7-185">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-186">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-187">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-188">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-189">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-190">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="66fe7-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="66fe7-191">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-192">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="66fe7-193">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66fe7-194">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="66fe7-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="66fe7-195">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="66fe7-196">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="66fe7-197">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="66fe7-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="66fe7-198">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="66fe7-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="66fe7-199">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-200">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-201">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-202">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="66fe7-202">Billed sales</span></span></td>
<td><span data-ttu-id="66fe7-203">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66fe7-204">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="66fe7-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="66fe7-205">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="66fe7-206">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-207">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="66fe7-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="66fe7-208">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-209">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="66fe7-210">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="66fe7-211">**Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus**</span><span class="sxs-lookup"><span data-stu-id="66fe7-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="66fe7-212">Sündmus</span><span class="sxs-lookup"><span data-stu-id="66fe7-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="66fe7-213">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="66fe7-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="66fe7-214">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="66fe7-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="66fe7-215">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="66fe7-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="66fe7-216">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="66fe7-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="66fe7-217">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="66fe7-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="66fe7-218">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="66fe7-218">Actuals</span></span></th>
<th><span data-ttu-id="66fe7-219">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-219">Transaction currency</span></span></th>
<th><span data-ttu-id="66fe7-220">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="66fe7-220">Fixed price</span></span></th>
<th><span data-ttu-id="66fe7-221">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="66fe7-222">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="66fe7-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="66fe7-223">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-224">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="66fe7-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="66fe7-225">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="66fe7-226">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="66fe7-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="66fe7-227">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-227">Cost actual</span></span></td>
<td><span data-ttu-id="66fe7-228">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="66fe7-229">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="66fe7-230">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="66fe7-231">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="66fe7-232">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-233">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="66fe7-234">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-235">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="66fe7-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="66fe7-236">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-237">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="66fe7-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="66fe7-238">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="66fe7-239">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="66fe7-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="66fe7-240">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-240">Cost actual</span></span></td>
<td><span data-ttu-id="66fe7-241">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-242">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-243">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-244">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-245">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="66fe7-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-246">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="66fe7-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="66fe7-247">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-248">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="66fe7-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="66fe7-249">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-250">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="66fe7-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="66fe7-251">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-252">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="66fe7-253">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66fe7-254">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="66fe7-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="66fe7-255">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="66fe7-256">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-257">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="66fe7-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-258">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-259">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="66fe7-260">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-261">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="66fe7-261">Billed sales</span></span></td>
<td><span data-ttu-id="66fe7-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66fe7-263">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="66fe7-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="66fe7-264">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="66fe7-265">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-266">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-267">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-268">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66fe7-269">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-270">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="66fe7-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="66fe7-271">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-272">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="66fe7-273">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66fe7-274">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="66fe7-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="66fe7-275">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="66fe7-276">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="66fe7-277">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="66fe7-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="66fe7-278">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="66fe7-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="66fe7-279">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-280">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="66fe7-281">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="66fe7-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-282">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="66fe7-282">Billed sales</span></span></td>
<td><span data-ttu-id="66fe7-283">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66fe7-284">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="66fe7-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="66fe7-285">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="66fe7-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="66fe7-286">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-287">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="66fe7-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="66fe7-288">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66fe7-289">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="66fe7-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="66fe7-290">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="66fe7-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
