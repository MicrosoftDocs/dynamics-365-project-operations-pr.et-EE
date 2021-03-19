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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285613"
---
# <a name="actuals-overview"></a><span data-ttu-id="076a9-103">Tegelike näitajate ülevaade</span><span class="sxs-lookup"><span data-stu-id="076a9-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="076a9-104">Tegelikud andmed on projektiga lõpule viidud tööd.</span><span class="sxs-lookup"><span data-stu-id="076a9-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="076a9-105">Projekti tegelikke andmeid saab tuvastada nende alusdokumendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="076a9-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="076a9-106">Alusdokumendid sisaldavad aja-, kulu- ja töölehe kandeid, aga ka arveid.</span><span class="sxs-lookup"><span data-stu-id="076a9-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kuidas projekti tegelikud andmed alusdokumentidega ühendatakse?](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="076a9-108">Ajakirje esitamisel</span><span class="sxs-lookup"><span data-stu-id="076a9-108">Submitting a time entry</span></span>

<span data-ttu-id="076a9-109">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjalide töölehe reaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="076a9-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="076a9-110">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="076a9-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="076a9-111">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="076a9-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="076a9-112">Vaikehindade sisestamise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="076a9-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="076a9-113">Kõik ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="076a9-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="076a9-114">Need väljad hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="076a9-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="076a9-115">Vaikehindu mõjutavate väljade (nt **roll** ja **organisatsiooniüksus**) töölehe reale sisestatakse sobivad hinnad vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="076a9-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="076a9-116">Kui lisate ajakirjele kohandatud välja ning soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.</span><span class="sxs-lookup"><span data-stu-id="076a9-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="076a9-117">Kulukirje esitamine</span><span class="sxs-lookup"><span data-stu-id="076a9-117">Submitting an expense entry</span></span>

<span data-ttu-id="076a9-118">Kui kulukirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjali lepingureaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="076a9-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="076a9-119">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="076a9-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="076a9-120">Kui fikseeritud hinnaga sisestus esitatakse projektile, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="076a9-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="076a9-121">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial, mis on lehe jaotises **Kulukirje**.</span><span class="sxs-lookup"><span data-stu-id="076a9-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="076a9-122">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="076a9-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="076a9-123">Hinna enda jaoks on kasutaja sisestatud suurus kulude ja müügi jaoks vaikimisi määratud otse seotud kulukirje töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="076a9-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="076a9-124">PSA praeguses versioonis ei ole kategoorial põhinev ühiku vaikehinna kanne saadaval.</span><span class="sxs-lookup"><span data-stu-id="076a9-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="076a9-125">Kulude kirjendamiseks kirjete töölehtede kasutamine</span><span class="sxs-lookup"><span data-stu-id="076a9-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="076a9-126">PSA-s võimaldavad kirje töölehed teil kirjendada kulu või tulu materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="076a9-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="076a9-127">Töölehel on päis, read ja toiming **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="076a9-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="076a9-128">Toome mõned näited, kus võiksite töölehte kasutada.</span><span class="sxs-lookup"><span data-stu-id="076a9-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="076a9-129">Peate kirjendma projektiga seotud tegelikku materjalikulu ja müüki.</span><span class="sxs-lookup"><span data-stu-id="076a9-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="076a9-130">Peate tehingu tegelikud andmed teistest süsteemist PSA-sse üle viima.</span><span class="sxs-lookup"><span data-stu-id="076a9-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="076a9-131">Peate kirjendama mõnes muus süsteemis aset leidnud kulusid (nt hanke- või alltöövõtu kulud).</span><span class="sxs-lookup"><span data-stu-id="076a9-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="076a9-132">Tegelike näitajate loomiseks kirje töölehtede kasutamine peaks olema tehtav ainult kasutajate poolt, kes on täielikult teadlikud projektis tegelike näitajate mõjust raamatupidamisele.</span><span class="sxs-lookup"><span data-stu-id="076a9-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="076a9-133">Selle põhjuseks on, et rakendus ei kontrolli töölehe rea tüüpi ega seotud hinda, mis on töölehe reale sisestatud.</span><span class="sxs-lookup"><span data-stu-id="076a9-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="076a9-134">Selle töölehe tüübi mõju tõttu olge hästi ettevaatlik, et kellele kirje töölehtede loomisele juurdepääs antakse.</span><span class="sxs-lookup"><span data-stu-id="076a9-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="076a9-135">Projektisündmustel põhinevate tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="076a9-135">Recording actuals based on project events</span></span>

<span data-ttu-id="076a9-136">PSA salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="076a9-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="076a9-137">Need kanded kirjendatakse **tegelike andmetena**.</span><span class="sxs-lookup"><span data-stu-id="076a9-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="076a9-138">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="076a9-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="076a9-139">**Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse**</span><span class="sxs-lookup"><span data-stu-id="076a9-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="076a9-140">Sündmus</span><span class="sxs-lookup"><span data-stu-id="076a9-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="076a9-141">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="076a9-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="076a9-142">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="076a9-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="076a9-143">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="076a9-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="076a9-144">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="076a9-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="076a9-145">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="076a9-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="076a9-146">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="076a9-146">Actuals</span></span></th>
<th><span data-ttu-id="076a9-147">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-147">Transaction currency</span></span></th>
<th><span data-ttu-id="076a9-148">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="076a9-148">Fixed price</span></span></th>
<th><span data-ttu-id="076a9-149">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="076a9-150">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="076a9-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="076a9-151">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="076a9-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-152">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="076a9-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="076a9-153">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="076a9-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="076a9-154">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="076a9-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="076a9-155">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-155">Cost actual</span></span></td>
<td><span data-ttu-id="076a9-156">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-157">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-158">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="076a9-159">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-160">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-161">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="076a9-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="076a9-162">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="076a9-163">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="076a9-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="076a9-164">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-164">Cost actual</span></span></td>
<td><span data-ttu-id="076a9-165">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-166">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-167">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-168">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-169">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-170">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="076a9-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="076a9-171">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-172">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="076a9-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="076a9-173">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="076a9-174">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="076a9-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="076a9-175">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="076a9-176">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-177">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="076a9-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-178">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-179">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-180">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-181">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="076a9-181">Billed sales</span></span></td>
<td><span data-ttu-id="076a9-182">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="076a9-183">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="076a9-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="076a9-184">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="076a9-185">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-186">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-187">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-188">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-189">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-190">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="076a9-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="076a9-191">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-192">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="076a9-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="076a9-193">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="076a9-194">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="076a9-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="076a9-195">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="076a9-196">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="076a9-197">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="076a9-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="076a9-198">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="076a9-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="076a9-199">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-200">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-201">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-202">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="076a9-202">Billed sales</span></span></td>
<td><span data-ttu-id="076a9-203">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="076a9-204">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="076a9-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="076a9-205">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="076a9-206">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-207">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="076a9-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="076a9-208">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-209">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="076a9-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="076a9-210">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="076a9-211">**Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus**</span><span class="sxs-lookup"><span data-stu-id="076a9-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="076a9-212">Sündmus</span><span class="sxs-lookup"><span data-stu-id="076a9-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="076a9-213">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="076a9-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="076a9-214">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="076a9-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="076a9-215">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="076a9-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="076a9-216">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="076a9-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="076a9-217">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="076a9-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="076a9-218">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="076a9-218">Actuals</span></span></th>
<th><span data-ttu-id="076a9-219">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-219">Transaction currency</span></span></th>
<th><span data-ttu-id="076a9-220">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="076a9-220">Fixed price</span></span></th>
<th><span data-ttu-id="076a9-221">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="076a9-222">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="076a9-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="076a9-223">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="076a9-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-224">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="076a9-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="076a9-225">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="076a9-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="076a9-226">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="076a9-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="076a9-227">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-227">Cost actual</span></span></td>
<td><span data-ttu-id="076a9-228">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="076a9-229">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="076a9-230">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="076a9-231">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="076a9-232">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-233">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="076a9-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="076a9-234">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-235">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="076a9-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="076a9-236">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-237">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="076a9-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="076a9-238">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="076a9-239">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="076a9-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="076a9-240">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-240">Cost actual</span></span></td>
<td><span data-ttu-id="076a9-241">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-242">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-243">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-244">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-245">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="076a9-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-246">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="076a9-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="076a9-247">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-248">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="076a9-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="076a9-249">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-250">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="076a9-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="076a9-251">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-252">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="076a9-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="076a9-253">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="076a9-254">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="076a9-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="076a9-255">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="076a9-256">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-257">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="076a9-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-258">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-259">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="076a9-260">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-261">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="076a9-261">Billed sales</span></span></td>
<td><span data-ttu-id="076a9-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="076a9-263">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="076a9-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="076a9-264">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="076a9-265">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-266">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-267">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-268">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="076a9-269">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-270">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="076a9-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="076a9-271">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-272">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="076a9-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="076a9-273">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="076a9-274">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="076a9-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="076a9-275">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="076a9-276">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="076a9-277">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="076a9-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="076a9-278">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="076a9-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="076a9-279">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-280">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="076a9-281">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="076a9-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-282">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="076a9-282">Billed sales</span></span></td>
<td><span data-ttu-id="076a9-283">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="076a9-284">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="076a9-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="076a9-285">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="076a9-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="076a9-286">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-287">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="076a9-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="076a9-288">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="076a9-289">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="076a9-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="076a9-290">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="076a9-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]