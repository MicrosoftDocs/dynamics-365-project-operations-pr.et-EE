---
title: Tegelikud näitajad
description: Selles teemas antakse teavet tegelike andmetega töötamise kohta Microsofti Dynamics 365 Project Operationsis.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852539"
---
# <a name="actuals"></a><span data-ttu-id="81b8a-103">Tegelikud näitajad</span><span class="sxs-lookup"><span data-stu-id="81b8a-103">Actuals</span></span> 

<span data-ttu-id="81b8a-104">_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_</span><span class="sxs-lookup"><span data-stu-id="81b8a-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81b8a-105">Tegelikud andmed esindavad projekti läbivaadatud ja kinnitatud finantsilist ning ajakava edenemist.</span><span class="sxs-lookup"><span data-stu-id="81b8a-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="81b8a-106">Need luuakse aja, kulu, materjali kasutuskirjete, töölehe kannete ja arvete kinnitamise tulemusena.</span><span class="sxs-lookup"><span data-stu-id="81b8a-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="81b8a-107">Töölehe read ja aja esitamine</span><span class="sxs-lookup"><span data-stu-id="81b8a-107">Journal lines and time submission</span></span>

<span data-ttu-id="81b8a-108">Lisateavet ajakirje kohta vaadake teemast [Ajakirje ülevaade](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="81b8a-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="81b8a-109">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="81b8a-109">Time and materials</span></span>

<span data-ttu-id="81b8a-110">Kui esitatud ajakirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="81b8a-111">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-111">Fixed price</span></span>

<span data-ttu-id="81b8a-112">Kui esitatav ajakirje seotakse projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="81b8a-113">Vaikimisi hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="81b8a-113">Default pricing</span></span>

<span data-ttu-id="81b8a-114">Vaikehindade looise loogika asub töölehe real.</span><span class="sxs-lookup"><span data-stu-id="81b8a-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="81b8a-115">Ajakirje välja väärtused kopeeritakse töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="81b8a-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="81b8a-116">Need väärtused hõlmavad tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja vastava hinnakirja valuutat.</span><span class="sxs-lookup"><span data-stu-id="81b8a-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="81b8a-117">Vaikimisi hinnakujundust mõjutavaod välju (nt **roll** ja **ressursiüksus**) kasutatakse töölehe rea sobiva hinna kindlakstegemiseks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="81b8a-118">Saate lisada ajakirjele kohandatud välja.</span><span class="sxs-lookup"><span data-stu-id="81b8a-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="81b8a-119">Kui soovite kanda välja väärtuse tegelikele väärtustele, looge väli tabelites **Tegelikud** ja **Töölehe kanne**.</span><span class="sxs-lookup"><span data-stu-id="81b8a-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="81b8a-120">Kasutage kohandatud koodi, et edastada valitud välja väärtuse töölehe rea kaudu ajakirjest tegelikele näitajatele, kasutades kande päritolu.</span><span class="sxs-lookup"><span data-stu-id="81b8a-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="81b8a-121">Lisateavet kannete päritolu ja ühenduste kohta vaadake teemast [Tegelike näitajate seostamine algsete kirjetega](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="81b8a-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="81b8a-122">Töölehe read ja põhikulu esitamine</span><span class="sxs-lookup"><span data-stu-id="81b8a-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="81b8a-123">Lisateavet kulukirje kohta vaadake teemast [Kulu ülevaade](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="81b8a-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="81b8a-124">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="81b8a-124">Time and materials</span></span>

<span data-ttu-id="81b8a-125">Kui esitatud põhikulu kirje on seotud projektiga, mis on vastendatud mõne aja ja materjali lepingureaga, loob süsteem kaks töölehe rida – ühe kulu ja ühe arveldamata müügi jaoks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="81b8a-126">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-126">Fixed price</span></span>

<span data-ttu-id="81b8a-127">Kui esitatud põhikulu kirje on ühendatud projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="81b8a-128">Vaikimisi hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="81b8a-128">Default pricing</span></span>

<span data-ttu-id="81b8a-129">Kulude vaikehindade sisestamise loogika põhineb kulukategoorial.</span><span class="sxs-lookup"><span data-stu-id="81b8a-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="81b8a-130">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="81b8a-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="81b8a-131">Vaikimisi hinnakujundust mõjutavaod välju (nt **tehingukategooria** ja **ressursiüksus**) kasutatakse töölehe rea sobiva hinna kindlakstegemiseks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="81b8a-132">Samas toimib see ainult juhul, kui hinnakirjas on hinnakujundusmeetodiks **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="81b8a-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="81b8a-133">Kui hinnakujundusmeetodiks on **Kulu** või **Hinnalisand kulule**, kasutatakse kulukirje loomisel sisestatud hinda kulude jaoks ja müügiesindaja rea hind arvutatakse hinnakujundusmeetodi põhjal.</span><span class="sxs-lookup"><span data-stu-id="81b8a-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="81b8a-134">Saate lisata kulukirjele kohandatud välja.</span><span class="sxs-lookup"><span data-stu-id="81b8a-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="81b8a-135">Kui soovite kanda välja väärtuse tegelikele väärtustele, looge väli tabelites **Tegelikud** ja **Töölehe kanne**.</span><span class="sxs-lookup"><span data-stu-id="81b8a-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="81b8a-136">Kasutage kohandatud koodi, et edastada valitud välja väärtuse töölehe rea kaudu ajakirjest tegelikele näitajatele, kasutades kande päritolu.</span><span class="sxs-lookup"><span data-stu-id="81b8a-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="81b8a-137">Lisateavet kannete päritolu ja ühenduste kohta vaadake teemast [Tegelike näitajate seostamine algsete kirjetega](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="81b8a-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="81b8a-138">Töölehe kanded ja materjali kasutuslogi esitamine</span><span class="sxs-lookup"><span data-stu-id="81b8a-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="81b8a-139">Lisateavet kulukirje kohta vaadake teemast [Materjalide kasutuslogi](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="81b8a-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="81b8a-140">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="81b8a-140">Time and materials</span></span>

<span data-ttu-id="81b8a-141">Kui edastatud materjalide kasutuslogi kirje on seotud aja ja materjalide lepingureaga vastendatud projektiga, loob süsteem kaks tekstirida – ühe kulu ja ühe tasustamata müügi jaoks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="81b8a-142">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-142">Fixed price</span></span>

<span data-ttu-id="81b8a-143">Kui esitatud materjali kasutuslogi kirje on ühendatud projektiga, mis on vastendatud fikseeritud hinnaga lepingureaga, loob süsteem ühe töölehe rea ainult kulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="81b8a-144">Vaikimisi hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="81b8a-144">Default pricing</span></span>

<span data-ttu-id="81b8a-145">Materjali vaikehindade sisestamise loogika põhineb tootel ja ühikukombinatsioonil.</span><span class="sxs-lookup"><span data-stu-id="81b8a-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="81b8a-146">Sobiva hinnakirja määratlemiseks kasutatakse tehingu kuupäeva, lepingurida, millega projekt on vastendatud, ja valuutat.</span><span class="sxs-lookup"><span data-stu-id="81b8a-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="81b8a-147">Vaikimisi hinnakujundust mõjutavaod välju (nt **toote ID** ja **ressursiüksus**) kasutatakse töölehe rea sobiva hinna kindlakstegemiseks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="81b8a-148">Kuid see toimib ainult kataloogitoodete puhul.</span><span class="sxs-lookup"><span data-stu-id="81b8a-148">However, this only works for catalog products.</span></span> <span data-ttu-id="81b8a-149">Sisestatavate toodete puhul kasutatakse materjalide kasutuslogi kirje loomisel sisestatud hinda töölehe ridade kulu- ja müügihinnana.</span><span class="sxs-lookup"><span data-stu-id="81b8a-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="81b8a-150">Saate lisata kirjele **Materjali kasutuslogi** kohandatud välja.</span><span class="sxs-lookup"><span data-stu-id="81b8a-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="81b8a-151">Kui soovite kanda välja väärtuse tegelikele väärtustele, looge väli tabelites **Tegelikud** ja **Töölehe kanne**.</span><span class="sxs-lookup"><span data-stu-id="81b8a-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="81b8a-152">Kasutage kohandatud koodi, et edastada valitud välja väärtuse töölehe rea kaudu ajakirjest tegelikele näitajatele, kasutades kande päritolu.</span><span class="sxs-lookup"><span data-stu-id="81b8a-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="81b8a-153">Lisateavet kannete päritolu ja ühenduste kohta vaadake teemast [Tegelike näitajate seostamine algsete kirjetega](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="81b8a-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="81b8a-154">Kirjete töölehtede kasutamine kulude kirjendamiseks</span><span class="sxs-lookup"><span data-stu-id="81b8a-154">Use entry journals to record costs</span></span>

<span data-ttu-id="81b8a-155">Saate kasutada töölehti kulu või tulu kirjendamiseks materjali-, tasu-, aja-, kulu- või maksukannete järgi.</span><span class="sxs-lookup"><span data-stu-id="81b8a-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="81b8a-156">Töölehti saab kasutada järgmistel eesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="81b8a-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="81b8a-157">Viige tehingu tegelikud andmed teisest süsteemist Microsoft Dynamics 365 Project Operationsse üle.</span><span class="sxs-lookup"><span data-stu-id="81b8a-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="81b8a-158">Muus süsteemis aset leidnud kulude kirjendamiseks.</span><span class="sxs-lookup"><span data-stu-id="81b8a-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="81b8a-159">Need kulud võivad hõlmata hanke- või alltöövõtu kulusid.</span><span class="sxs-lookup"><span data-stu-id="81b8a-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81b8a-160">Rakendus ei kinnita töölege rea tüüpi ega töölehe reale sisestatud seotud hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="81b8a-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="81b8a-161">Seega peaksid tegelike näitajate loomiseks kasutama kirjete töölehti ainult kasutaja, kes on täielikult teadlik raamatupidamuslikust mõjust, mis tegelikel näitajatel projektile on.</span><span class="sxs-lookup"><span data-stu-id="81b8a-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="81b8a-162">Selle töölehe tüübi mõju tõttu peaksite hoolikalt valima, kellel on kirjete töölehtede loomisele juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="81b8a-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="81b8a-163">Projektisündmuste põhjal tegelike andmete kirjendamine</span><span class="sxs-lookup"><span data-stu-id="81b8a-163">Record actuals based on project events</span></span>

<span data-ttu-id="81b8a-164">Project Operations salvestab projekti jooksul toimuvad finantstehingud.</span><span class="sxs-lookup"><span data-stu-id="81b8a-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="81b8a-165">Need kanded kirjendatakse tegelike andmetena.</span><span class="sxs-lookup"><span data-stu-id="81b8a-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="81b8a-166">Järgmistes tabelites on esitatud mitmesugused tegelike andmete tüübid, mis olenevad sellest, kas projekt on aja- ja materjalikulu või fikseeritud hinnaga projekt, mis on eelmüügi etapis, või on see sisemine projekt.</span><span class="sxs-lookup"><span data-stu-id="81b8a-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="81b8a-167">Ressurss kuulub projekti tellijaga samasse organisatsiooniüksusse</span><span class="sxs-lookup"><span data-stu-id="81b8a-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="81b8a-168">Sündmus</span><span class="sxs-lookup"><span data-stu-id="81b8a-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="81b8a-169">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="81b8a-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="81b8a-170">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="81b8a-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="81b8a-171">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="81b8a-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="81b8a-172">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="81b8a-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="81b8a-173">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="81b8a-174">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="81b8a-174">Actuals</span></span></th>
<th><span data-ttu-id="81b8a-175">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-175">Transaction currency</span></span></th>
<th><span data-ttu-id="81b8a-176">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-176">Fixed price</span></span></th>
<th><span data-ttu-id="81b8a-177">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b8a-178">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="81b8a-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="81b8a-179">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-180">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="81b8a-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="81b8a-181">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81b8a-182">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="81b8a-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81b8a-183">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-183">Cost actual</span></span></td>
<td><span data-ttu-id="81b8a-184">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-185">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-186">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="81b8a-187">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-188">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-189">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="81b8a-190">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81b8a-191">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="81b8a-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81b8a-192">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-192">Cost actual</span></span></td>
<td><span data-ttu-id="81b8a-193">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-194">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-195">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-196">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-197">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-198">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="81b8a-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81b8a-199">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-200">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81b8a-201">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81b8a-202">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="81b8a-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81b8a-203">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81b8a-204">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-205">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="81b8a-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-206">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-207">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-208">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-209">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="81b8a-209">Billed sales</span></span></td>
<td><span data-ttu-id="81b8a-210">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81b8a-211">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="81b8a-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81b8a-212">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81b8a-213">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-214">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-215">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-216">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-217">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-218">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="81b8a-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81b8a-219">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-220">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81b8a-221">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81b8a-222">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="81b8a-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81b8a-223">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81b8a-224">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="81b8a-225">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="81b8a-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="81b8a-226">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="81b8a-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="81b8a-227">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-228">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-229">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-230">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="81b8a-230">Billed sales</span></span></td>
<td><span data-ttu-id="81b8a-231">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81b8a-232">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="81b8a-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81b8a-233">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81b8a-234">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-235">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="81b8a-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="81b8a-236">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-237">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="81b8a-238">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="81b8a-239">Ressurss kuulub organisatsiooniüksusse, mis ei ole sama kui projekti tellija organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="81b8a-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="81b8a-240">Sündmus</span><span class="sxs-lookup"><span data-stu-id="81b8a-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="81b8a-241">Arveldatav või müüdud projekt</span><span class="sxs-lookup"><span data-stu-id="81b8a-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="81b8a-242">Eelmüügi etapis projekt</span><span class="sxs-lookup"><span data-stu-id="81b8a-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="81b8a-243">Sisemine projekt</span><span class="sxs-lookup"><span data-stu-id="81b8a-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="81b8a-244">Aeg ja materjalid</span><span class="sxs-lookup"><span data-stu-id="81b8a-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="81b8a-245">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="81b8a-246">Tegelikud</span><span class="sxs-lookup"><span data-stu-id="81b8a-246">Actuals</span></span></th>
<th><span data-ttu-id="81b8a-247">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-247">Transaction currency</span></span></th>
<th><span data-ttu-id="81b8a-248">Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="81b8a-248">Fixed price</span></span></th>
<th><span data-ttu-id="81b8a-249">Tehingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b8a-250">Ajakirje on loodud.</span><span class="sxs-lookup"><span data-stu-id="81b8a-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="81b8a-251">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-252">Ajakirje on esitatud.</span><span class="sxs-lookup"><span data-stu-id="81b8a-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="81b8a-253">Tegelike andmete olemites puudub tegevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="81b8a-254">Kellaaeg kinnitatakse ning sel ajal ei tehta tasustatava tööaja muudatusi ega suurendata seda.</span><span class="sxs-lookup"><span data-stu-id="81b8a-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81b8a-255">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-255">Cost actual</span></span></td>
<td><span data-ttu-id="81b8a-256">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="81b8a-257">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="81b8a-258">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="81b8a-259">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="81b8a-260">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-261">Arveldamata tegelik müük – arveldatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="81b8a-262">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-263">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="81b8a-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="81b8a-264">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-265">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="81b8a-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="81b8a-266">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="81b8a-267">Kellaaeg kinnitatakse ning sel ajal ei vähendata tasustatavat tööaega.</span><span class="sxs-lookup"><span data-stu-id="81b8a-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81b8a-268">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-268">Cost actual</span></span></td>
<td><span data-ttu-id="81b8a-269">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-270">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-271">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-272">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-273">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="81b8a-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-274">Ressursiühiku maksumus</span><span class="sxs-lookup"><span data-stu-id="81b8a-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="81b8a-275">Ressursiühiku valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-276">Organisatsiooniüksuste vaheline müük</span><span class="sxs-lookup"><span data-stu-id="81b8a-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="81b8a-277">Lepingut sõlmiva üksuse valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-278">Arveldamata tegelik müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="81b8a-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81b8a-279">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-280">Arveldamata tegelik müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81b8a-281">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81b8a-282">Arve kinnitatakse, ei toimu tasustatava tööaja muudatusi ega vähendamist.</span><span class="sxs-lookup"><span data-stu-id="81b8a-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81b8a-283">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81b8a-284">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-285">Arveldatud müük vahekokkuvõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="81b8a-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-286">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-287">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="81b8a-288">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-289">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="81b8a-289">Billed sales</span></span></td>
<td><span data-ttu-id="81b8a-290">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81b8a-291">Arve on kinnitatud, tasutatavas tööajas esineb vähenemist.</span><span class="sxs-lookup"><span data-stu-id="81b8a-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81b8a-292">Arveldamata müügi tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81b8a-293">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-294">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-295">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-296">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81b8a-297">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-298">Arveldatud müük – uue koguse arveldus</span><span class="sxs-lookup"><span data-stu-id="81b8a-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81b8a-299">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-300">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81b8a-301">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81b8a-302">Arvet parandatakse, et suurendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="81b8a-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81b8a-303">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81b8a-304">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="81b8a-305">Arveldatud müük vahekokkuvõtete jaoks</span><span class="sxs-lookup"><span data-stu-id="81b8a-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="81b8a-306">Vahekokkuvõtte muutmine olekust <strong>arveldatud</strong> olekuks <strong>arveks valmis</strong></span><span class="sxs-lookup"><span data-stu-id="81b8a-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="81b8a-307">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-308">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="81b8a-309">Pole rakendatav</span><span class="sxs-lookup"><span data-stu-id="81b8a-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-310">Arveldatud müük</span><span class="sxs-lookup"><span data-stu-id="81b8a-310">Billed sales</span></span></td>
<td><span data-ttu-id="81b8a-311">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81b8a-312">Arvet parandatakse, et vähendada tasustatava kogust.</span><span class="sxs-lookup"><span data-stu-id="81b8a-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81b8a-313">Arveldatud müük – tagasipööramine</span><span class="sxs-lookup"><span data-stu-id="81b8a-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81b8a-314">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-315">Arveldatud müük uue koguse jaoks</span><span class="sxs-lookup"><span data-stu-id="81b8a-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="81b8a-316">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b8a-317">Arveldatud müük – mitte-arveldatav erinevus</span><span class="sxs-lookup"><span data-stu-id="81b8a-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="81b8a-318">Projektilepingu valuuta</span><span class="sxs-lookup"><span data-stu-id="81b8a-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
