---
title: Projektipõhised hinnapakkumise read (Pro)
description: Selles teemas antakse teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908057"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="6f53c-104">Projektipõhised hinnapakkumise read (Pro)</span><span class="sxs-lookup"><span data-stu-id="6f53c-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="6f53c-105">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="6f53c-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6f53c-106">Projektipõhised hinnapakkumise read on loodud selleks, et aidata hinnata kohustuse projektitööd.</span><span class="sxs-lookup"><span data-stu-id="6f53c-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6f53c-107">Projektipõhise hinnapakkumise rea struktuuri pikendatakse projekti prognooside alusel järgmiste kontseptsioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6f53c-108">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="6f53c-108">Billing Method</span></span>
- <span data-ttu-id="6f53c-109">Projekti ja ülesannete vastendamine</span><span class="sxs-lookup"><span data-stu-id="6f53c-109">Project and Task Mapping</span></span>
- <span data-ttu-id="6f53c-110">Kaasatud tehingute klassid</span><span class="sxs-lookup"><span data-stu-id="6f53c-110">Included Transaction classes</span></span>
- <span data-ttu-id="6f53c-111">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="6f53c-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6f53c-112">Arveldatavuse seadistus</span><span class="sxs-lookup"><span data-stu-id="6f53c-112">Chargeability setup</span></span>
- <span data-ttu-id="6f53c-113">Prognoos hinnapakkumise rea üksikasjade abil</span><span class="sxs-lookup"><span data-stu-id="6f53c-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6f53c-114">Hinnapakkumisrea kliendid</span><span class="sxs-lookup"><span data-stu-id="6f53c-114">Quote line Customers</span></span>

<span data-ttu-id="6f53c-115">Järgmine tabel annab teavet projektipõhise hinnapakkumise rea vahekaardi **Üldine** väljade kohta.</span><span class="sxs-lookup"><span data-stu-id="6f53c-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6f53c-116">Need väljad aitavad seadistada projektitöö üksikasjaliku, ligikaudse prognoosi aluse.</span><span class="sxs-lookup"><span data-stu-id="6f53c-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6f53c-117">**Väli**</span><span class="sxs-lookup"><span data-stu-id="6f53c-117">**Field**</span></span> | <span data-ttu-id="6f53c-118">**Asjakohasus, eesmärk ja juhised**</span><span class="sxs-lookup"><span data-stu-id="6f53c-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="6f53c-119">**Allavoolu mõjud**</span><span class="sxs-lookup"><span data-stu-id="6f53c-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6f53c-120">Nimetus</span><span class="sxs-lookup"><span data-stu-id="6f53c-120">Name</span></span> | <span data-ttu-id="6f53c-121">Hinnapakkumise rea nimi, mis peaks aitama teil tuvastada prognoositava hinnapakkumise diskreetse komponendi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6f53c-122">Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-123">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="6f53c-123">Billing Method</span></span> | <span data-ttu-id="6f53c-124">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt.</span><span class="sxs-lookup"><span data-stu-id="6f53c-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6f53c-125">See väli sisaldab kahte põhilist lepingumudelit, mida Dynamics 365 Project Operations toetab.</span><span class="sxs-lookup"><span data-stu-id="6f53c-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6f53c-126">- Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="6f53c-126">- Fixed price</span></span></br><span data-ttu-id="6f53c-127">- Aeg ja materjal.</span><span class="sxs-lookup"><span data-stu-id="6f53c-127">- Time and material.</span></span>| <span data-ttu-id="6f53c-128">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-129">Project</span><span class="sxs-lookup"><span data-stu-id="6f53c-129">Project</span></span> | <span data-ttu-id="6f53c-130">Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks.</span><span class="sxs-lookup"><span data-stu-id="6f53c-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6f53c-131">Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6f53c-132">Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="6f53c-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6f53c-133">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="6f53c-134">Kaasatud ülesanded</span><span class="sxs-lookup"><span data-stu-id="6f53c-134">Included Tasks</span></span> | <span data-ttu-id="6f53c-135">Näitab, kas seda hinnapakkumise rida kasutatakse valitud projekti kõigi või mõnede projekti toimingute jaoks.</span><span class="sxs-lookup"><span data-stu-id="6f53c-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="6f53c-136">Sellel väljal on järgmised võimalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="6f53c-136">This field has the following possible values:</span></span></br><span data-ttu-id="6f53c-137">- Kõik projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="6f53c-137">- All project tasks</span></span></br><span data-ttu-id="6f53c-138">- Ainult valitud projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="6f53c-138">- Selected project tasks only</span></span></br><span data-ttu-id="6f53c-139">Tühi väärtus sellel väljal võrdub valikuga **Kõik projekti ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="6f53c-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="6f53c-140">Kui projekti lehel on valitud **Ainult valitud projekti ülesanded**, võimaldab vahekaart **Ülesande arvelduse seadistus** teil valida konkreetsed ülesanded selle hinnapakkumise reaga sidumiseks.</span><span class="sxs-lookup"><span data-stu-id="6f53c-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="6f53c-141">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-142">Kaasa aeg</span><span class="sxs-lookup"><span data-stu-id="6f53c-142">Include Time</span></span> | <span data-ttu-id="6f53c-143">Lipp **Jah**/**Ei** näitab, kas valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6f53c-144">Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6f53c-145">Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6f53c-146">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-147">Kaasa kulu</span><span class="sxs-lookup"><span data-stu-id="6f53c-147">Include Expense</span></span> | <span data-ttu-id="6f53c-148">Lipp **Jah**/**Ei** näitab, kas valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6f53c-149">Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6f53c-150">Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6f53c-151">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-152">Kaasa tasu</span><span class="sxs-lookup"><span data-stu-id="6f53c-152">Include Fee</span></span> | <span data-ttu-id="6f53c-153">Lipp **Jah**/**Ei** näitab, kas valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6f53c-154">Lipp **Ei** näitab, et valitud projekti tasusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6f53c-155">Lipp **Jah** näitab, et valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6f53c-156">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-157">Hinnapakkumise summa</span><span class="sxs-lookup"><span data-stu-id="6f53c-157">Quoted Amount</span></span> | <span data-ttu-id="6f53c-158">See on hinnapakkumise summa, mis esitatakse kliendile kõigi selle projektipõhise hinnapakkumise rea prognoositavate tööde kohta.</span><span class="sxs-lookup"><span data-stu-id="6f53c-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6f53c-159">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**.</span><span class="sxs-lookup"><span data-stu-id="6f53c-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6f53c-160">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast.</span><span class="sxs-lookup"><span data-stu-id="6f53c-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6f53c-161">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-162">Hinnanguline maks</span><span class="sxs-lookup"><span data-stu-id="6f53c-162">Estimated Tax</span></span> | <span data-ttu-id="6f53c-163">See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa.</span><span class="sxs-lookup"><span data-stu-id="6f53c-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6f53c-164">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast.</span><span class="sxs-lookup"><span data-stu-id="6f53c-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6f53c-165">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-166">Hinnapakkumise summa pärast maksude mahaarvamist</span><span class="sxs-lookup"><span data-stu-id="6f53c-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="6f53c-167">See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6f53c-168">Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*.</span><span class="sxs-lookup"><span data-stu-id="6f53c-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6f53c-169">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-170">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="6f53c-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="6f53c-171">Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**.</span><span class="sxs-lookup"><span data-stu-id="6f53c-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6f53c-172">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6f53c-173">Kliendi eelarve</span><span class="sxs-lookup"><span data-stu-id="6f53c-173">Customer Budget</span></span> | <span data-ttu-id="6f53c-174">See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="6f53c-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6f53c-175">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="6f53c-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6f53c-176">Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid</span><span class="sxs-lookup"><span data-stu-id="6f53c-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6f53c-177">**1. reegel**: kui väli **Kaasatud ülesanded** on tühi või seadistatud väärtusele **Kõik projekti ülesanded**, kaasatakse projekt hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="6f53c-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="6f53c-178">**2. reegel**: kui väli **Kaasatud ülesanded** on tühi või kui selle sätte väärtuseks on seatud **kõik projekti tööülesanded**, saab projekti ja teatud kandeklassi kaasata ainult hinnapakkumise ühele projektipõhisele hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="6f53c-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6f53c-179">**3. reegel**: kui väli **Kaasatud ülesanded** on seadistatud väärtusele **Ainult valitud projekti ülesanded**, saab projekti ja teatud kandeklassi kaasata hinnapakkumise mitmele projektipõhisele hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="6f53c-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="6f53c-180">**4. reegel**: kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6f53c-181">**5. reegel**: kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="6f53c-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6f53c-182">
                    <strong>Müügivõimalus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6f53c-183">
                    <strong>Hinnapakkumine</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6f53c-184">
                    <strong>Hinnapakkumise rida</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6f53c-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="6f53c-186">
                    <strong>Kaasatud ülesanded</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6f53c-187">
                    <strong>Kaasa aeg</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6f53c-188">
                    <strong>Kaasa kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6f53c-189">
                    <strong>Kaasa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6f53c-190">
                    <strong>Tasu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6f53c-191">
                    <strong>Kehtiv/kehtetu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6f53c-192">
                    <strong>Põhjus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6f53c-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-193">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-194">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-195">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-196">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-197">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-198">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-199">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-200">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-201">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="6f53c-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-202">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="6f53c-202">Violation of Rule #2.</span></span> <span data-ttu-id="6f53c-203">P1-projekti aeg, kulud ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2.</span><span class="sxs-lookup"><span data-stu-id="6f53c-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-204">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-205">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-206">QL2</span><span class="sxs-lookup"><span data-stu-id="6f53c-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-207">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-208">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-209">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-210">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-211">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-212">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-213">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-214">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-215">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-216">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-217">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-218">No</span><span class="sxs-lookup"><span data-stu-id="6f53c-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-219">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-220">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="6f53c-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-221">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="6f53c-221">Violation of Rule #2.</span></span> <span data-ttu-id="6f53c-222">P1-projekti aeg ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2.</span><span class="sxs-lookup"><span data-stu-id="6f53c-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-223">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-224">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-225">QL2</span><span class="sxs-lookup"><span data-stu-id="6f53c-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-226">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-227">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-228">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-229">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-230">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-231">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-232">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-233">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-234">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-235">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-236">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-237">No</span><span class="sxs-lookup"><span data-stu-id="6f53c-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-238">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-239">Kehtib</span><span class="sxs-lookup"><span data-stu-id="6f53c-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="6f53c-240">P1-projekti tasud on kaasatud reale QL1.</span><span class="sxs-lookup"><span data-stu-id="6f53c-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6f53c-241">P1-projekti kulu on kaasatud reale QL2.</span><span class="sxs-lookup"><span data-stu-id="6f53c-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6f53c-242">See, mis on igale hinnapakkumise reale kaasatud, ei kattu ja on see kehtiv.</span><span class="sxs-lookup"><span data-stu-id="6f53c-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-243">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-244">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-245">QL2</span><span class="sxs-lookup"><span data-stu-id="6f53c-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-246">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-247">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-248">No</span><span class="sxs-lookup"><span data-stu-id="6f53c-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-249">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-250">No</span><span class="sxs-lookup"><span data-stu-id="6f53c-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-251">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-252">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-254">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-255">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="6f53c-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-256">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-257">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-258">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-259">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="6f53c-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-260">Eeltoodud reegli nr 2 rikkumine</span><span class="sxs-lookup"><span data-stu-id="6f53c-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="6f53c-261">Q1 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="6f53c-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6f53c-262">QL2 sisaldab kogu projekti P1 aega, kulu ja tasu ning kattub sellega, mis on kaasatud reale Q1.</span><span class="sxs-lookup"><span data-stu-id="6f53c-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-263">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-264">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-265">QL2</span><span class="sxs-lookup"><span data-stu-id="6f53c-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-266">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-267">Tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-268">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-269">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-270">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-271">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-272">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-273">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-274">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-275">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="6f53c-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-276">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-277">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-278">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-279">Kehtib</span><span class="sxs-lookup"><span data-stu-id="6f53c-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-280">Vastavalt eeltoodud reeglile nr 3,</span><span class="sxs-lookup"><span data-stu-id="6f53c-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="6f53c-281">Q1 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="6f53c-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6f53c-282">QL2 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="6f53c-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6f53c-283">Ainus täiendav valideerimine toimub QL1 tööülesannete alamhulga ümber, mis erineb QL2 tööülesannete alamhulgast.</span><span class="sxs-lookup"><span data-stu-id="6f53c-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="6f53c-284">See tagab, et kattumist ei esineks.</span><span class="sxs-lookup"><span data-stu-id="6f53c-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="6f53c-285">Seda teeb süsteem ülesannete sidumisel.</span><span class="sxs-lookup"><span data-stu-id="6f53c-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-286">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-287">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-288">QL2</span><span class="sxs-lookup"><span data-stu-id="6f53c-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-289">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-290">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="6f53c-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-291">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-292">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-293">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-294">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-295">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-296">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-297">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-298">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-299">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-300">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-301">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6f53c-302">Kehtib</span><span class="sxs-lookup"><span data-stu-id="6f53c-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-303">Vastavalt reeglile nr 5 on Q1 ja Q2 kaks sama müügivõimalusega hinnapakkumist, nii et nad saavad mõlemad prognoosida projekti samu komponente.</span><span class="sxs-lookup"><span data-stu-id="6f53c-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-304">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-305">Kv2</span><span class="sxs-lookup"><span data-stu-id="6f53c-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-306">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-307">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-308">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-309">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-310">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-311">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-312">O1</span><span class="sxs-lookup"><span data-stu-id="6f53c-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-313">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-314">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-315">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-316">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-317">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-318">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-319">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6f53c-320">Kehtib</span><span class="sxs-lookup"><span data-stu-id="6f53c-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6f53c-321">Vastavalt reeglile nr 4 on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, nii et nad ei saa mõlemad prognoosida sama projekti komponente.</span><span class="sxs-lookup"><span data-stu-id="6f53c-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6f53c-322">O2</span><span class="sxs-lookup"><span data-stu-id="6f53c-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6f53c-323">Kv1</span><span class="sxs-lookup"><span data-stu-id="6f53c-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-324">QL1</span><span class="sxs-lookup"><span data-stu-id="6f53c-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-325">P1</span><span class="sxs-lookup"><span data-stu-id="6f53c-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6f53c-326">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="6f53c-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-327">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6f53c-328">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6f53c-329">Ja</span><span class="sxs-lookup"><span data-stu-id="6f53c-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6f53c-330">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="6f53c-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

