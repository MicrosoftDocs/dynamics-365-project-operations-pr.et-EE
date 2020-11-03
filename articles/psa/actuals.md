---
title: Tegelike näitajate ülevaade
description: Selles teemas antakse teavet projektiga seotud tegelike andmete kohta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075154"
---
# <a name="actuals-overview"></a><span data-ttu-id="5524b-103">Tegelike näitajate ülevaade</span><span class="sxs-lookup"><span data-stu-id="5524b-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5524b-104">Tegelikud andmed on projektiga lõpule viidud tööd.</span><span class="sxs-lookup"><span data-stu-id="5524b-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="5524b-105">Projekti tegelikke andmeid saab tuvastada nende alusdokumendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="5524b-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="5524b-106">Alusdokumendid sisaldavad aja-, kulu- ja töölehe kandeid, aga ka arveid.</span><span class="sxs-lookup"><span data-stu-id="5524b-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kuidas projekti tegelikud andmed alusdokumentidega ühendatakse?](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="5524b-108">Ajakirje esitamisel</span><span class="sxs-lookup"><span data-stu-id="5524b-108">Submitting a time entry</span></span>

<span data-ttu-id="5524b-109">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjalide töölehe reaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="5524b-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5524b-110">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="5524b-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5524b-111">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="5524b-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="5524b-112">Vaikehindade sisestamise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="5524b-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="5524b-113">Kõik ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="5524b-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="5524b-114">Need väljad hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="5524b-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="5524b-115">Vaikehindu mõjutavate väljade (nt **roll** ja **organisatsiooniüksus** ) töölehe reale sisestatakse sobivad hinnad vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="5524b-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="5524b-116">Kui lisate ajakirjele kohandatud välja ning soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.</span><span class="sxs-lookup"><span data-stu-id="5524b-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="5524b-117">Kulukirje esitamine</span><span class="sxs-lookup"><span data-stu-id="5524b-117">Submitting an expense entry</span></span>

<span data-ttu-id="5524b-118">Kui kulukirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjali lepingureaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="5524b-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5524b-119">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="5524b-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5524b-120">Kui fikseeritud hinnaga sisestus esitatakse projektile, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="5524b-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="5524b-121">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial, mis on lehe jaotises **Kulukirje**.</span><span class="sxs-lookup"><span data-stu-id="5524b-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="5524b-122">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="5524b-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5524b-123">Hinna enda jaoks on kasutaja sisestatud suurus kulude ja müügi jaoks vaikimisi määratud otse seotud kulukirje töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="5524b-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="5524b-124">PSA praeguses versioonis ei ole kategoorial põhinev ühiku vaikehinna kanne saadaval.</span><span class="sxs-lookup"><span data-stu-id="5524b-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="5524b-125">Kulude kirjendamiseks kirjete töölehtede kasutamine</span><span class="sxs-lookup"><span data-stu-id="5524b-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="5524b-126">PSA-s võimaldavad kirje töölehed teil kirjendada kulu või tulu materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="5524b-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5524b-127">Töölehel on päis, read ja toiming **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="5524b-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="5524b-128">Toome mõned näited, kus võiksite töölehte kasutada.</span><span class="sxs-lookup"><span data-stu-id="5524b-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="5524b-129">Peate kirjendma projektiga seotud tegelikku materjalikulu ja müüki.</span><span class="sxs-lookup"><span data-stu-id="5524b-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="5524b-130">Peate tehingu tegelikud andmed teistest süsteemist PSA-sse üle viima.</span><span class="sxs-lookup"><span data-stu-id="5524b-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="5524b-131">Peate kirjendama mõnes muus süsteemis aset leidnud kulusid (nt hanke- või alltöövõtu kulud).</span><span class="sxs-lookup"><span data-stu-id="5524b-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5524b-132">Tegelike näitajate loomiseks kirje töölehtede kasutamine peaks olema tehtav ainult kasutajate poolt, kes on täielikult teadlikud projektis tegelike näitajate mõjust raamatupidamisele.</span><span class="sxs-lookup"><span data-stu-id="5524b-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="5524b-133">Selle põhjuseks on, et rakendus ei kontrolli töölehe rea tüüpi ega seotud hinda, mis on töölehe reale sisestatud.</span><span class="sxs-lookup"><span data-stu-id="5524b-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5524b-134">Selle töölehe tüübi mõju tõttu olge hästi ettevaatlik, et kellele kirje töölehtede loomisele juurdepääs antakse.</span><span class="sxs-lookup"><span data-stu-id="5524b-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="5524b-135">Projektisündmustel põhinevate tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="5524b-135">Recording actuals based on project events</span></span>

<span data-ttu-id="5524b-136">PSA salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="5524b-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5524b-137">Need kanded kirjendatakse **tegelike andmetena**.</span><span class="sxs-lookup"><span data-stu-id="5524b-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="5524b-138">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="5524b-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="5524b-139">**Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse**</span><span class="sxs-lookup"><span data-stu-id="5524b-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5524b-140">Sündmus</span><span class="sxs-lookup"><span data-stu-id="5524b-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5524b-141">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="5524b-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5524b-142">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="5524b-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5524b-143">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="5524b-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5524b-144">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="5524b-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5524b-145">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="5524b-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5524b-146">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="5524b-146">Actuals</span></span></th>
<th><span data-ttu-id="5524b-147">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-147">Transaction currency</span></span></th>
<th><span data-ttu-id="5524b-148">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="5524b-148">Fixed price</span></span></th>
<th><span data-ttu-id="5524b-149">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5524b-150">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="5524b-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5524b-151">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="5524b-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-152">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="5524b-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5524b-153">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="5524b-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5524b-154">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="5524b-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5524b-155">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-155">Cost actual</span></span></td>
<td><span data-ttu-id="5524b-156">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-157">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-158">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5524b-159">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-160">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-161">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="5524b-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5524b-162">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5524b-163">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="5524b-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5524b-164">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-164">Cost actual</span></span></td>
<td><span data-ttu-id="5524b-165">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-166">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-167">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-168">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-169">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-170">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="5524b-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5524b-171">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-172">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="5524b-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5524b-173">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5524b-174">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="5524b-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5524b-175">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5524b-176">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-177">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="5524b-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-178">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-179">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-180">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-181">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="5524b-181">Billed sales</span></span></td>
<td><span data-ttu-id="5524b-182">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5524b-183">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="5524b-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5524b-184">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5524b-185">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-186">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-187">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-188">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-189">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-190">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="5524b-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5524b-191">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-192">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="5524b-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5524b-193">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5524b-194">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="5524b-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5524b-195">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5524b-196">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5524b-197">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="5524b-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5524b-198">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="5524b-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5524b-199">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-200">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-201">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-202">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="5524b-202">Billed sales</span></span></td>
<td><span data-ttu-id="5524b-203">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5524b-204">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="5524b-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5524b-205">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5524b-206">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-207">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="5524b-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5524b-208">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-209">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="5524b-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5524b-210">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5524b-211">**Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus**</span><span class="sxs-lookup"><span data-stu-id="5524b-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5524b-212">Sündmus</span><span class="sxs-lookup"><span data-stu-id="5524b-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5524b-213">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="5524b-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5524b-214">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="5524b-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5524b-215">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="5524b-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5524b-216">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="5524b-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5524b-217">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="5524b-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5524b-218">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="5524b-218">Actuals</span></span></th>
<th><span data-ttu-id="5524b-219">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-219">Transaction currency</span></span></th>
<th><span data-ttu-id="5524b-220">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="5524b-220">Fixed price</span></span></th>
<th><span data-ttu-id="5524b-221">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5524b-222">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="5524b-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5524b-223">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="5524b-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-224">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="5524b-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5524b-225">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="5524b-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5524b-226">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="5524b-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5524b-227">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-227">Cost actual</span></span></td>
<td><span data-ttu-id="5524b-228">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5524b-229">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5524b-230">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5524b-231">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5524b-232">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-233">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="5524b-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5524b-234">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-235">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="5524b-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5524b-236">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-237">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="5524b-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5524b-238">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5524b-239">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="5524b-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5524b-240">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-240">Cost actual</span></span></td>
<td><span data-ttu-id="5524b-241">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-242">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-243">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-244">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-245">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="5524b-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-246">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="5524b-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5524b-247">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-248">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="5524b-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5524b-249">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-250">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="5524b-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5524b-251">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-252">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="5524b-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5524b-253">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5524b-254">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="5524b-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5524b-255">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5524b-256">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-257">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="5524b-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-258">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-259">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5524b-260">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-261">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="5524b-261">Billed sales</span></span></td>
<td><span data-ttu-id="5524b-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5524b-263">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="5524b-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5524b-264">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5524b-265">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-266">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-267">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-268">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5524b-269">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-270">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="5524b-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5524b-271">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-272">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="5524b-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5524b-273">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5524b-274">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="5524b-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5524b-275">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5524b-276">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5524b-277">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="5524b-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5524b-278">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="5524b-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5524b-279">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-280">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5524b-281">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="5524b-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-282">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="5524b-282">Billed sales</span></span></td>
<td><span data-ttu-id="5524b-283">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5524b-284">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="5524b-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5524b-285">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="5524b-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5524b-286">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-287">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="5524b-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5524b-288">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5524b-289">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="5524b-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5524b-290">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="5524b-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
