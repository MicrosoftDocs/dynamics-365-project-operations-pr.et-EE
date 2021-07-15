---
title: Tegelike näitajate ülevaade
description: Selles teemas antakse teavet projektiga seotud tegelike andmete kohta.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368156"
---
# <a name="actuals-overview"></a><span data-ttu-id="ba5e8-103">Tegelike näitajate ülevaade</span><span class="sxs-lookup"><span data-stu-id="ba5e8-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ba5e8-104">Tegelikud andmed on projektiga lõpule viidud tööd.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="ba5e8-105">Projekti tegelikke andmeid saab tuvastada nende alusdokumendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="ba5e8-106">Alusdokumendid sisaldavad aja-, kulu- ja töölehe kandeid, aga ka arveid.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kuidas projekti tegelikud andmed alusdokumentidega ühendatakse?](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="ba5e8-108">Ajakirje esitamisel</span><span class="sxs-lookup"><span data-stu-id="ba5e8-108">Submitting a time entry</span></span>

<span data-ttu-id="ba5e8-109">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjalide töölehe reaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ba5e8-110">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ba5e8-111">Kui ajakirje esitatakse projekti jaoks, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="ba5e8-112">Vaikehindade sisestamise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="ba5e8-113">Kõik ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="ba5e8-114">Need väljad hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="ba5e8-115">Vaikehindu mõjutavate väljade (nt **roll** ja **organisatsiooniüksus**) töölehe reale sisestatakse sobivad hinnad vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="ba5e8-116">Kui lisate ajakirjele kohandatud välja ning soovite, et väljale oleks kantud tegelikud väärtused, looge tegelikes olemites väli ja kasutage välja vastendusi, et kopeerida väli ajakirjest tegelikule.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="ba5e8-117">Kulukirje esitamine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-117">Submitting an expense entry</span></span>

<span data-ttu-id="ba5e8-118">Kui kulukirje esitatakse projekti jaoks, mis on vastendatud aja- ja materjali lepingureaga, luuakse rakenduses PSA kaks töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ba5e8-119">Üks rida on kulu ja teine rida müükide jaoks, mille kohta pole veel arvet.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ba5e8-120">Kui fikseeritud hinnaga sisestus esitatakse projektile, mis on vastendatud fikseeritud hinnaga lepingureaga, luuakse töölehe rida ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="ba5e8-121">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial, mis on lehe jaotises **Kulukirje**.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="ba5e8-122">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ba5e8-123">Hinna enda jaoks on kasutaja sisestatud suurus kulude ja müügi jaoks vaikimisi määratud otse seotud kulukirje töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="ba5e8-124">PSA praeguses versioonis ei ole kategoorial põhinev ühiku vaikehinna kanne saadaval.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="ba5e8-125">Kulude kirjendamiseks kirjete töölehtede kasutamine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="ba5e8-126">PSA-s võimaldavad kirje töölehed teil kirjendada kulu või tulu materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ba5e8-127">Töölehel on päis, read ja toiming **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="ba5e8-128">Toome mõned näited, kus võiksite töölehte kasutada.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="ba5e8-129">Peate kirjendma projektiga seotud tegelikku materjalikulu ja müüki.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="ba5e8-130">Peate tehingu tegelikud andmed teistest süsteemist PSA-sse üle viima.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="ba5e8-131">Peate kirjendama mõnes muus süsteemis aset leidnud kulusid (nt hanke- või alltöövõtu kulud).</span><span class="sxs-lookup"><span data-stu-id="ba5e8-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba5e8-132">Tegelike näitajate loomiseks kirje töölehtede kasutamine peaks olema tehtav ainult kasutajate poolt, kes on täielikult teadlikud projektis tegelike näitajate mõjust raamatupidamisele.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="ba5e8-133">Selle põhjuseks on, et rakendus ei kontrolli töölehe rea tüüpi ega seotud hinda, mis on töölehe reale sisestatud.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ba5e8-134">Selle töölehe tüübi mõju tõttu olge hästi ettevaatlik, et kellele kirje töölehtede loomisele juurdepääs antakse.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="ba5e8-135">Projektisündmustel põhinevate tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-135">Recording actuals based on project events</span></span>

<span data-ttu-id="ba5e8-136">PSA salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ba5e8-137">Need kanded kirjendatakse **tegelike andmetena**.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="ba5e8-138">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="ba5e8-139">**Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse**</span><span class="sxs-lookup"><span data-stu-id="ba5e8-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ba5e8-140">Sündmus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ba5e8-141">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="ba5e8-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ba5e8-142">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="ba5e8-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ba5e8-143">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="ba5e8-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ba5e8-144">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="ba5e8-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ba5e8-145">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="ba5e8-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ba5e8-146">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="ba5e8-146">Actuals</span></span></th>
<th><span data-ttu-id="ba5e8-147">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-147">Transaction currency</span></span></th>
<th><span data-ttu-id="ba5e8-148">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="ba5e8-148">Fixed price</span></span></th>
<th><span data-ttu-id="ba5e8-149">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba5e8-150">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ba5e8-151">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-152">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ba5e8-153">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba5e8-154">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ba5e8-155">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-155">Cost actual</span></span></td>
<td><span data-ttu-id="ba5e8-156">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-157">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-158">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ba5e8-159">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-160">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-161">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ba5e8-162">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba5e8-163">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ba5e8-164">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-164">Cost actual</span></span></td>
<td><span data-ttu-id="ba5e8-165">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-166">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-167">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-168">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-169">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-170">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ba5e8-171">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-172">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ba5e8-173">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba5e8-174">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ba5e8-175">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ba5e8-176">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-177">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="ba5e8-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-178">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-179">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-180">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-181">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="ba5e8-181">Billed sales</span></span></td>
<td><span data-ttu-id="ba5e8-182">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba5e8-183">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ba5e8-184">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ba5e8-185">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-186">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-187">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-188">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-189">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-190">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ba5e8-191">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-192">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ba5e8-193">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba5e8-194">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ba5e8-195">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ba5e8-196">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ba5e8-197">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="ba5e8-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ba5e8-198">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="ba5e8-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ba5e8-199">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-200">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-201">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-202">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="ba5e8-202">Billed sales</span></span></td>
<td><span data-ttu-id="ba5e8-203">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba5e8-204">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ba5e8-205">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ba5e8-206">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-207">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="ba5e8-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ba5e8-208">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-209">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ba5e8-210">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba5e8-211">**Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus**</span><span class="sxs-lookup"><span data-stu-id="ba5e8-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ba5e8-212">Sündmus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ba5e8-213">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="ba5e8-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ba5e8-214">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="ba5e8-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ba5e8-215">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="ba5e8-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ba5e8-216">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="ba5e8-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ba5e8-217">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="ba5e8-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ba5e8-218">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="ba5e8-218">Actuals</span></span></th>
<th><span data-ttu-id="ba5e8-219">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-219">Transaction currency</span></span></th>
<th><span data-ttu-id="ba5e8-220">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="ba5e8-220">Fixed price</span></span></th>
<th><span data-ttu-id="ba5e8-221">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba5e8-222">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ba5e8-223">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-224">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ba5e8-225">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ba5e8-226">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ba5e8-227">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-227">Cost actual</span></span></td>
<td><span data-ttu-id="ba5e8-228">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ba5e8-229">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ba5e8-230">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ba5e8-231">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ba5e8-232">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-233">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ba5e8-234">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-235">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ba5e8-236">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-237">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="ba5e8-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ba5e8-238">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ba5e8-239">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ba5e8-240">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-240">Cost actual</span></span></td>
<td><span data-ttu-id="ba5e8-241">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-242">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-243">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-244">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-245">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="ba5e8-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-246">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ba5e8-247">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-248">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="ba5e8-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ba5e8-249">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-250">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ba5e8-251">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-252">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ba5e8-253">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba5e8-254">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ba5e8-255">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ba5e8-256">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-257">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="ba5e8-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-258">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-259">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ba5e8-260">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-261">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="ba5e8-261">Billed sales</span></span></td>
<td><span data-ttu-id="ba5e8-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba5e8-263">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ba5e8-264">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ba5e8-265">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-266">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-267">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-268">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ba5e8-269">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-270">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ba5e8-271">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-272">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ba5e8-273">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ba5e8-274">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ba5e8-275">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ba5e8-276">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ba5e8-277">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="ba5e8-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ba5e8-278">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="ba5e8-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ba5e8-279">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-280">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ba5e8-281">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="ba5e8-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-282">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="ba5e8-282">Billed sales</span></span></td>
<td><span data-ttu-id="ba5e8-283">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ba5e8-284">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="ba5e8-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ba5e8-285">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="ba5e8-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ba5e8-286">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-287">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="ba5e8-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ba5e8-288">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba5e8-289">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="ba5e8-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ba5e8-290">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="ba5e8-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]