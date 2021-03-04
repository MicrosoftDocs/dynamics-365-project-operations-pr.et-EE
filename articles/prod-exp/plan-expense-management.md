---
title: Kuluhalduse konfigureerimine
description: Selles artiklis kirjeldatakse, milliseid kaalutlusi ja otsuseid tuleb plaanimisprotsessis teha enne, kui rakenduses Microsoft Dynamics 365 Finance kuluhalduse konfigureerite.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960332"
---
# <a name="configure-expense-management"></a><span data-ttu-id="3000c-103">Kuluhalduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3000c-103">Configure expense management</span></span>

<span data-ttu-id="3000c-104">Selles teemas kirjeldatakse, milliseid kaalutlusi ja otsuseid tuleb plaanimisprotsessis teha enne, kui kuluhalduse konfigureerite.</span><span class="sxs-lookup"><span data-stu-id="3000c-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="3000c-105">Kuluhalduses saate talletada teavet makseviiside, reisitellimuste, kuluaruannete, poliitikate jms kohta.</span><span class="sxs-lookup"><span data-stu-id="3000c-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="3000c-106">Kuna kuluhalduse konfiguratsiooni plaanimisel tehtud otsused põhinevad teie organisatsiooni hierarhial ja finantsstruktuuril, peate viitama nende alade jaoks plaanitavatele dokumentidele.</span><span class="sxs-lookup"><span data-stu-id="3000c-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="3000c-107">Kontsernisisesed kulud</span><span class="sxs-lookup"><span data-stu-id="3000c-107">Intercompany expenses</span></span>

<span data-ttu-id="3000c-108">Kui lubate kontsernisisesed kulud, lubate juriidilistel olemitel ja töötajatel muude juriidiliste olemite nimel kulusid kanda ning kogute makse oma ettevõtte juriidiliste olemite töötajatelt.</span><span class="sxs-lookup"><span data-stu-id="3000c-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="3000c-109">Näiteks juriidilise olemi A töötaja lõpetab projekti juriidilise olemi B jaoks ja projekt kannab reisiga seotud kulud.</span><span class="sxs-lookup"><span data-stu-id="3000c-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="3000c-110">Kui kontsernisisesed kulud on lubatud, saab töötaja seejärel esitada kuluaruande, mis sisestab kulu juriidilisele olemile B ning kulu tuleb seejärel tasuda juriidilise olemi A poolt. Kui teie ettevõttel pole mitut juriidilist olemit, ei pea te kontsernisiseseid kulusid lubama.</span><span class="sxs-lookup"><span data-stu-id="3000c-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="3000c-111">**Otsus:** kas soovite lubada kontsernisisesed kulud?</span><span class="sxs-lookup"><span data-stu-id="3000c-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="3000c-112">Finantshaldus</span><span class="sxs-lookup"><span data-stu-id="3000c-112">Financial management</span></span>

<span data-ttu-id="3000c-113">Kuluhaldus on tihedalt seotud teie organisatsiooni finantsjuhtimisega.</span><span class="sxs-lookup"><span data-stu-id="3000c-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="3000c-114">Palju teie kuluhalduse konfiguratsioonist võetakse aluseks teie organisatsiooni finantsasjade kohta tehtud otsustele.</span><span class="sxs-lookup"><span data-stu-id="3000c-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="3000c-115">Järgmistes jaotistes kirjeldatakse, millistes valdkondades on vaja plaanimist ja otsuseid, lähtudes teie organisatsiooni finantsotsustest ja juhtiva meeskonna juhistest.</span><span class="sxs-lookup"><span data-stu-id="3000c-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="3000c-116">Päevarahad</span><span class="sxs-lookup"><span data-stu-id="3000c-116">Per diems</span></span>

<span data-ttu-id="3000c-117">Peate määratlema töötaja päevarahad, mida teie organisatsioon pakub.</span><span class="sxs-lookup"><span data-stu-id="3000c-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="3000c-118">Kuna päevarahad on tavaliselt kasutusel kulude katmiseks, nagu toitlustus, majutus ja muud ettenägematud kulud, saate luua reeglid teie organisatsiooni pakutavate päevarahade kohta.</span><span class="sxs-lookup"><span data-stu-id="3000c-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="3000c-119">päevarahade määrad võivad põhineda aastaajal, reisisihtkohal või mõlemal.</span><span class="sxs-lookup"><span data-stu-id="3000c-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="3000c-120">Päevaraha reegli määratlemisel saate määrata, et teatud protsent päevarahade hinnast jäetakse maksmata, kui töötaja saab tasuta einet või teenust.</span><span class="sxs-lookup"><span data-stu-id="3000c-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="3000c-121">Samuti saate määratleda päevarahade määra tasemed, et määrata minimaalse ja maksimaalse tundide arvu, mille võrra päevaraha töötaja reisile rakendada saab.</span><span class="sxs-lookup"><span data-stu-id="3000c-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="3000c-122">**Otsus:**</span><span class="sxs-lookup"><span data-stu-id="3000c-122">**Decisions:**</span></span>

- <span data-ttu-id="3000c-123">Päevarahade vaikereeglid esimese ja viimase päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="3000c-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="3000c-124">Milline on minimaalne tundide arv, mida töötaja saab päeva eest taotleda, et päevaraha saada?</span><span class="sxs-lookup"><span data-stu-id="3000c-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="3000c-125">Kas summa, mida pakutakse esimese ja viimase päeva toitlustuse eest, on väiksem?</span><span class="sxs-lookup"><span data-stu-id="3000c-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="3000c-126">Kui summa on väiksem, siis milline on vähendamise protsent?</span><span class="sxs-lookup"><span data-stu-id="3000c-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3000c-127">Kas summa, mida pakutakse esimese ja viimase päeva majutuse eest, on väiksem?</span><span class="sxs-lookup"><span data-stu-id="3000c-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="3000c-128">Kui summa on väiksem, siis milline on vähendamise protsent?</span><span class="sxs-lookup"><span data-stu-id="3000c-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3000c-129">Kas summa, mida pakutakse esimese ja viimase päeva muude kulude eest, on väiksem?</span><span class="sxs-lookup"><span data-stu-id="3000c-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="3000c-130">Kui summa on väiksem, siis milline on vähendamise protsent?</span><span class="sxs-lookup"><span data-stu-id="3000c-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="3000c-131">Päevaraha vaikereeglid.</span><span class="sxs-lookup"><span data-stu-id="3000c-131">Default per diem rules:</span></span>

    - <span data-ttu-id="3000c-132">Kas päevaraha summa väheneb iga toidukorra eest, kui eine on näiteks tasuta?</span><span class="sxs-lookup"><span data-stu-id="3000c-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="3000c-133">Kui summa on väiksem, siis milline on vähendamise protsent iga eine eest?</span><span class="sxs-lookup"><span data-stu-id="3000c-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="3000c-134">Kas toidukorra summa vähenemine arvutatakse päeva, reisi või päeva toidukordade kohta?</span><span class="sxs-lookup"><span data-stu-id="3000c-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="3000c-135">Kas päevarahade summa ümardatakse tavalisel viisil või ülespoole?</span><span class="sxs-lookup"><span data-stu-id="3000c-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="3000c-136">Kas päevaraha arvutatakse 24-tunnise ajavahemiku või kalendripäeva kohta?</span><span class="sxs-lookup"><span data-stu-id="3000c-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="3000c-137">Päevaraha reeglid, mis põhinevad asukohal.</span><span class="sxs-lookup"><span data-stu-id="3000c-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="3000c-138">Kas päevarahade määrad erinevad olenevalt asukohast?</span><span class="sxs-lookup"><span data-stu-id="3000c-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="3000c-139">Millised asukohad on kaasatud?</span><span class="sxs-lookup"><span data-stu-id="3000c-139">What locations are included?</span></span>
    - <span data-ttu-id="3000c-140">Kui päevaraha määrad erinevad olenevalt asukohast, siis milline protsent on iga asukoha kohta ette nähtud järgmist tüüpi kulutuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="3000c-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="3000c-141">Toidukorrad</span><span class="sxs-lookup"><span data-stu-id="3000c-141">Meals</span></span>
        - <span data-ttu-id="3000c-142">Hotell</span><span class="sxs-lookup"><span data-stu-id="3000c-142">Hotel</span></span>
        - <span data-ttu-id="3000c-143">Muud kulud</span><span class="sxs-lookup"><span data-stu-id="3000c-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="3000c-144">Kuluhalduse töölehed ja kontod</span><span class="sxs-lookup"><span data-stu-id="3000c-144">Expense management journals and accounts</span></span>

<span data-ttu-id="3000c-145">Kuluhaldus eeldab mitme töölehe ja konto kasutamist.</span><span class="sxs-lookup"><span data-stu-id="3000c-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="3000c-146">Peate otsustama näiteks, kas sama kontot kasutatakse sularaha ettemaksete ja krediitkaardiga seotud vaidluste korral.</span><span class="sxs-lookup"><span data-stu-id="3000c-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="3000c-147">**Otsus:**</span><span class="sxs-lookup"><span data-stu-id="3000c-147">**Decisions:**</span></span>

- <span data-ttu-id="3000c-148">Millisele pearaamatu töölehele on kinnitatud kuluaruanded sisestatakse?</span><span class="sxs-lookup"><span data-stu-id="3000c-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="3000c-149">Millist kontot kasutatakse sularaha ettemakseteks?</span><span class="sxs-lookup"><span data-stu-id="3000c-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="3000c-150">Kas sularaha ettemaksed tuleb kohe sisestada?</span><span class="sxs-lookup"><span data-stu-id="3000c-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="3000c-151">Makseviisid</span><span class="sxs-lookup"><span data-stu-id="3000c-151">Payment methods</span></span>

<span data-ttu-id="3000c-152">Kui lubate töötajatel kanda kulusid teie ettevõtte nimel, peate määratlema makseviisid, mida töötajad võivad kasutada.</span><span class="sxs-lookup"><span data-stu-id="3000c-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="3000c-153">Näiteks võite lubada töötajatel kasutada sularaha või ettevõtte krediitkaarti.</span><span class="sxs-lookup"><span data-stu-id="3000c-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="3000c-154">Samuti võite lubada töötajatel kasutada isiklikke krediitkaarte ja seejärel töötajatele summa tagasi maksma.</span><span class="sxs-lookup"><span data-stu-id="3000c-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="3000c-155">Peate tegema järgmised otsused iga makseviisi kohta, mida lubate.</span><span class="sxs-lookup"><span data-stu-id="3000c-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="3000c-156">**Otsus:**</span><span class="sxs-lookup"><span data-stu-id="3000c-156">**Decisions:**</span></span>

- <span data-ttu-id="3000c-157">Millised makseviisid on lubatud?</span><span class="sxs-lookup"><span data-stu-id="3000c-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="3000c-158">Kes katab makseviisi kulud?</span><span class="sxs-lookup"><span data-stu-id="3000c-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="3000c-159">Kas olemas on tasaarvelduskonto tüüp?</span><span class="sxs-lookup"><span data-stu-id="3000c-159">Is there an offset account type?</span></span> <span data-ttu-id="3000c-160">Kui teil on tasaarvelduskonto tüüp, siis mis see on?</span><span class="sxs-lookup"><span data-stu-id="3000c-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="3000c-161">Kui teil on tasaarvelduskonto, siis mis konto see on?</span><span class="sxs-lookup"><span data-stu-id="3000c-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="3000c-162">Kui makseviis on krediitkaart, kas makseviisi saab kasutada ainult koos imporditud tehingutega?</span><span class="sxs-lookup"><span data-stu-id="3000c-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="3000c-163">Kulukategooriad ja jagatud kategooriad</span><span class="sxs-lookup"><span data-stu-id="3000c-163">Expense categories and shared categories</span></span>

<span data-ttu-id="3000c-164">Kui töötajad loovad kuluaruande, peavad kõik kirjendatud kulud olema seostatud kulukategooriaga.</span><span class="sxs-lookup"><span data-stu-id="3000c-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="3000c-165">Kulukategooriate tuletatakse ühiskasutatavatest kategooriatest, mida saab teie organisatsiooni juriidiliste isikutega ühiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="3000c-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="3000c-166">Neid kategooriaid saab jagada ka projektihalduses ja raamatupidamises, olenevalt sellest, kuidas teie organisatsioon on määratletud.</span><span class="sxs-lookup"><span data-stu-id="3000c-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="3000c-167">Vastavalt teie organisatsiooni määratlusele ja juurutuse meeskonna juhistele peate määratlema, kas kuluhalduses kasutatavaid kategooriaid kasutatakse ainult kuluhalduses või kas need tuleks anda ühiskasutusse projektihalduse ja raamatupidamise ja kuluhaldusega.</span><span class="sxs-lookup"><span data-stu-id="3000c-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="3000c-168">Page tähele, et neid kategooriaid saab kasutada ühiselt projekti ja kulude või projekti ja tootmise vahel, kuid mitte kulude ja tootmise vahel.</span><span class="sxs-lookup"><span data-stu-id="3000c-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="3000c-169">Peate iga kulukategooria kohta järgmised otsused tegema.</span><span class="sxs-lookup"><span data-stu-id="3000c-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="3000c-170">**Otsus:**</span><span class="sxs-lookup"><span data-stu-id="3000c-170">**Decisions:**</span></span>

- <span data-ttu-id="3000c-171">Mis on kulukategooria?</span><span class="sxs-lookup"><span data-stu-id="3000c-171">What is the expense category?</span></span> <span data-ttu-id="3000c-172">Näidete hulka kuuluvad lendude, hotelli või kilometraaži kategooria.</span><span class="sxs-lookup"><span data-stu-id="3000c-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="3000c-173">Kas kulukategooriat võib kasutada ka projektijuhtimises ja raamatupidamises?</span><span class="sxs-lookup"><span data-stu-id="3000c-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="3000c-174">Mis on kulutüüp?</span><span class="sxs-lookup"><span data-stu-id="3000c-174">What is the expense type?</span></span>
- <span data-ttu-id="3000c-175">Milline on kulukategooria jaoks vaikimisi kasutatav makseviis?</span><span class="sxs-lookup"><span data-stu-id="3000c-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="3000c-176">Kas kulukategooria kulud tuleb täpsustada?</span><span class="sxs-lookup"><span data-stu-id="3000c-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="3000c-177">Milline on kulukategooria jaoks peamine vaikekonto?</span><span class="sxs-lookup"><span data-stu-id="3000c-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="3000c-178">Milline on kulukategooria üksuse vaikimisi käibemaksurühm?</span><span class="sxs-lookup"><span data-stu-id="3000c-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="3000c-179">Kas kulukategooria jaoks on lubatud täiendavad makseviisid?</span><span class="sxs-lookup"><span data-stu-id="3000c-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="3000c-180">Kui lubatud on täiendavad makseviisid, siis millised need on?</span><span class="sxs-lookup"><span data-stu-id="3000c-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="3000c-181">Kas selles kulukategoorias pm alamkategooriaid?</span><span class="sxs-lookup"><span data-stu-id="3000c-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="3000c-182">Kui on alamkategooriaid, peate langetama ka järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="3000c-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="3000c-183">Kas mõni alamkategooria on maksutagastusest välja jäetud?</span><span class="sxs-lookup"><span data-stu-id="3000c-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="3000c-184">Mis on alamkategooria üksuse käibemaksugrupp?</span><span class="sxs-lookup"><span data-stu-id="3000c-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="3000c-185">Kui kulukategooria on kasutusel ka projektihalduses ja raamatupidamises, vastake ülejäänud küsimustele.</span><span class="sxs-lookup"><span data-stu-id="3000c-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="3000c-186">Muul juhul liikuge edasi järgmise jaotise juurde.</span><span class="sxs-lookup"><span data-stu-id="3000c-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="3000c-187">Milliseid kulukontosid kasutatakse järgmistel kulude korral?</span><span class="sxs-lookup"><span data-stu-id="3000c-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="3000c-188">Kulu</span><span class="sxs-lookup"><span data-stu-id="3000c-188">Cost</span></span>
    - <span data-ttu-id="3000c-189">Palgaarvestuse jaotus</span><span class="sxs-lookup"><span data-stu-id="3000c-189">Payroll allocation</span></span>
    - <span data-ttu-id="3000c-190">WIP-kulu väärtus</span><span class="sxs-lookup"><span data-stu-id="3000c-190">WIP-cost value</span></span>
    - <span data-ttu-id="3000c-191">Kulu-üksus</span><span class="sxs-lookup"><span data-stu-id="3000c-191">Cost-item</span></span>
    - <span data-ttu-id="3000c-192">WIP-kulu väärtuse-üksus</span><span class="sxs-lookup"><span data-stu-id="3000c-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="3000c-193">Tekkepõhine kahjum</span><span class="sxs-lookup"><span data-stu-id="3000c-193">Accrued loss</span></span>
    - <span data-ttu-id="3000c-194">WIP-tekkepõhine kahjum</span><span class="sxs-lookup"><span data-stu-id="3000c-194">WIP-accrued loss</span></span>

- <span data-ttu-id="3000c-195">Milliseid tulukontosid kasutatakse järgmise korral?</span><span class="sxs-lookup"><span data-stu-id="3000c-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="3000c-196">Arveldatud tulu</span><span class="sxs-lookup"><span data-stu-id="3000c-196">Invoiced revenue</span></span>
    - <span data-ttu-id="3000c-197">Viittulu-müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="3000c-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="3000c-198">WIP-müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="3000c-198">WIP-sales value</span></span>
    - <span data-ttu-id="3000c-199">Viittulu-tootmine</span><span class="sxs-lookup"><span data-stu-id="3000c-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="3000c-200">WIP-tootmine</span><span class="sxs-lookup"><span data-stu-id="3000c-200">WIP-production</span></span>
    - <span data-ttu-id="3000c-201">Viittulu-kasum</span><span class="sxs-lookup"><span data-stu-id="3000c-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="3000c-202">WIP-kasum</span><span class="sxs-lookup"><span data-stu-id="3000c-202">WIP-profit</span></span>
    - <span data-ttu-id="3000c-203">Viittulu-kordustellimus</span><span class="sxs-lookup"><span data-stu-id="3000c-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="3000c-204">WIP-kordustellimus</span><span class="sxs-lookup"><span data-stu-id="3000c-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="3000c-205">Maksud</span><span class="sxs-lookup"><span data-stu-id="3000c-205">Taxes</span></span>

<span data-ttu-id="3000c-206">Kuluga seotud maksude puhul peate määratlema, mis on kuluaruannetes kaasatud või lubatud.</span><span class="sxs-lookup"><span data-stu-id="3000c-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="3000c-207">**Otsus:**</span><span class="sxs-lookup"><span data-stu-id="3000c-207">**Decisions:**</span></span>

- <span data-ttu-id="3000c-208">Kas kulu summa sisaldab käibemaksu?</span><span class="sxs-lookup"><span data-stu-id="3000c-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="3000c-209">Kas maksutagastus peaks olema kulude korral lubatud?</span><span class="sxs-lookup"><span data-stu-id="3000c-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="3000c-210">Kui plaanisite pearaamatut ning otsustasite rakendada USA käibemaksu ja kasutada käibemaksu reegleid, ei saa te kulude osas maksude tagasinõudmist lubada.</span><span class="sxs-lookup"><span data-stu-id="3000c-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="3000c-211">(USA käibemaksu ja maksude reeglite kasutamise rakendamiseks seadke suvandi **Rakenda käibemaksu maksustamise reegleid** väärtuseks **Jah**.)</span><span class="sxs-lookup"><span data-stu-id="3000c-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="3000c-212">Poliitikad</span><span class="sxs-lookup"><span data-stu-id="3000c-212">Policies</span></span>

<span data-ttu-id="3000c-213">Kui loote kuluaruande poliitikad, saate aidata oma organisatsioonil aega ja raha säästa, kui töötajad selle nimel kulusid kannavad.</span><span class="sxs-lookup"><span data-stu-id="3000c-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="3000c-214">Poliitikad aitavad tagada, et töötajad jäävad eelarvesse, esitavad kogu nõutava teabe ja kulutavad raha ainult otstarbeliselt.</span><span class="sxs-lookup"><span data-stu-id="3000c-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="3000c-215">Peate iga teie loodud kuluaruande poliitika ja iga kuluaruande kinnitamise poliitika kohta järgmised otsused tegema.</span><span class="sxs-lookup"><span data-stu-id="3000c-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="3000c-216">**Otsus:**</span><span class="sxs-lookup"><span data-stu-id="3000c-216">**Decisions:**</span></span>

- <span data-ttu-id="3000c-217">Mis on poliitika nimi?</span><span class="sxs-lookup"><span data-stu-id="3000c-217">What is the name of the policy?</span></span>
- <span data-ttu-id="3000c-218">Mille jaoks kulude poliitika on?</span><span class="sxs-lookup"><span data-stu-id="3000c-218">What is the expense policy for?</span></span>
- <span data-ttu-id="3000c-219">Kui olete varem otsustanud lubada kontsernisisesed kulud, siis millistele teie organisatsiooni ettevõtetele see poliitika rakendub?</span><span class="sxs-lookup"><span data-stu-id="3000c-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="3000c-220">Millal poliitika jõustub?</span><span class="sxs-lookup"><span data-stu-id="3000c-220">When does the policy become effective?</span></span>
- <span data-ttu-id="3000c-221">Millal poliitika aegub?</span><span class="sxs-lookup"><span data-stu-id="3000c-221">When does the policy expire?</span></span>
- <span data-ttu-id="3000c-222">Mis on poliitika reegel?</span><span class="sxs-lookup"><span data-stu-id="3000c-222">What is the policy rule?</span></span>
- <span data-ttu-id="3000c-223">Mis on poliitika reegli tulemus?</span><span class="sxs-lookup"><span data-stu-id="3000c-223">What is the outcome of the policy rule?</span></span>
