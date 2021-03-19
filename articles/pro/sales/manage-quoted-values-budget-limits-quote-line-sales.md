---
title: Projektipõhiste hinnapakkumiste ridade ülevaade – liht
description: Selles teemas antakse teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272968"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="db309-104">Projektipõhiste hinnapakkumiste ridade ülevaade – liht</span><span class="sxs-lookup"><span data-stu-id="db309-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="db309-105">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="db309-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="db309-106">Projektipõhised hinnapakkumise read on loodud selleks, et aidata hinnata kohustuse projektitööd.</span><span class="sxs-lookup"><span data-stu-id="db309-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="db309-107">Projektipõhise hinnapakkumise rea struktuuri pikendatakse projekti prognooside alusel järgmiste kontseptsioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="db309-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="db309-108">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="db309-108">Billing Method</span></span>
- <span data-ttu-id="db309-109">Projekti ja ülesannete vastendamine</span><span class="sxs-lookup"><span data-stu-id="db309-109">Project and Task Mapping</span></span>
- <span data-ttu-id="db309-110">Kaasatud tehingute klassid</span><span class="sxs-lookup"><span data-stu-id="db309-110">Included Transaction classes</span></span>
- <span data-ttu-id="db309-111">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="db309-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="db309-112">Arveldatavuse seadistus</span><span class="sxs-lookup"><span data-stu-id="db309-112">Chargeability setup</span></span>
- <span data-ttu-id="db309-113">Prognoos hinnapakkumise rea üksikasjade abil</span><span class="sxs-lookup"><span data-stu-id="db309-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="db309-114">Hinnapakkumisrea kliendid</span><span class="sxs-lookup"><span data-stu-id="db309-114">Quote line Customers</span></span>

<span data-ttu-id="db309-115">Järgmine tabel annab teavet projektipõhise hinnapakkumise rea vahekaardi **Üldine** väljade kohta.</span><span class="sxs-lookup"><span data-stu-id="db309-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="db309-116">Need väljad aitavad seadistada projektitöö üksikasjaliku, ligikaudse prognoosi aluse.</span><span class="sxs-lookup"><span data-stu-id="db309-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="db309-117">**Väli**</span><span class="sxs-lookup"><span data-stu-id="db309-117">**Field**</span></span> | <span data-ttu-id="db309-118">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="db309-118">**Description**</span></span> | <span data-ttu-id="db309-119">**Allavoolu mõjud**</span><span class="sxs-lookup"><span data-stu-id="db309-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="db309-120">Nimetus</span><span class="sxs-lookup"><span data-stu-id="db309-120">Name</span></span> | <span data-ttu-id="db309-121">Hinnapakkumise rea nimi, mis peaks aitama teil tuvastada prognoositava hinnapakkumise diskreetse komponendi.</span><span class="sxs-lookup"><span data-stu-id="db309-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="db309-122">Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-123">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="db309-123">Billing Method</span></span> | <span data-ttu-id="db309-124">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt.</span><span class="sxs-lookup"><span data-stu-id="db309-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="db309-125">See väli sisaldab kahte peamist lepingumudelit, mida rakendus Dynamics 365 Project Operations toetab.</span><span class="sxs-lookup"><span data-stu-id="db309-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="db309-126">- Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="db309-126">- Fixed price</span></span></br><span data-ttu-id="db309-127">- Aeg ja materjal.</span><span class="sxs-lookup"><span data-stu-id="db309-127">- Time and material.</span></span>| <span data-ttu-id="db309-128">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-129">Project</span><span class="sxs-lookup"><span data-stu-id="db309-129">Project</span></span> | <span data-ttu-id="db309-130">Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks.</span><span class="sxs-lookup"><span data-stu-id="db309-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="db309-131">Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="db309-132">Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="db309-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="db309-133">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="db309-134">Kaasatud ülesanded</span><span class="sxs-lookup"><span data-stu-id="db309-134">Included Tasks</span></span> | <span data-ttu-id="db309-135">Näitab, kas seda hinnapakkumise rida kasutatakse valitud projekti kõigi või mõnede projekti toimingute jaoks.</span><span class="sxs-lookup"><span data-stu-id="db309-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="db309-136">Sellel väljal on järgmised võimalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="db309-136">This field has the following possible values:</span></span></br><span data-ttu-id="db309-137">- Kõik projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="db309-137">- All project tasks</span></span></br><span data-ttu-id="db309-138">- Ainult valitud projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="db309-138">- Selected project tasks only</span></span></br><span data-ttu-id="db309-139">Tühi väärtus sellel väljal võrdub valikuga **Kõik projekti ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="db309-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="db309-140">Kui projekti lehel on valitud **Ainult valitud projekti ülesanded**, võimaldab vahekaart **Ülesande arvelduse seadistus** teil valida konkreetsed ülesanded selle hinnapakkumise reaga sidumiseks.</span><span class="sxs-lookup"><span data-stu-id="db309-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="db309-141">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-142">Kaasa aeg</span><span class="sxs-lookup"><span data-stu-id="db309-142">Include Time</span></span> | <span data-ttu-id="db309-143">Lipp **Jah**/**Ei** näitab, kas valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="db309-144">Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="db309-145">Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="db309-146">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-147">Kaasa kulu</span><span class="sxs-lookup"><span data-stu-id="db309-147">Include Expense</span></span> | <span data-ttu-id="db309-148">Lipp **Jah**/**Ei** näitab, kas valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="db309-149">Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="db309-150">Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="db309-151">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-152">Kaasa tasu</span><span class="sxs-lookup"><span data-stu-id="db309-152">Include Fee</span></span> | <span data-ttu-id="db309-153">Lipp **Jah**/**Ei** näitab, kas valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="db309-154">Lipp **Ei** näitab, et valitud projekti tasusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="db309-155">Lipp **Jah** näitab, et valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="db309-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="db309-156">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-157">Hinnapakkumise summa</span><span class="sxs-lookup"><span data-stu-id="db309-157">Quoted Amount</span></span> | <span data-ttu-id="db309-158">See on hinnapakkumise summa, mis esitatakse kliendile kõigi selle projektipõhise hinnapakkumise rea prognoositavate tööde kohta.</span><span class="sxs-lookup"><span data-stu-id="db309-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="db309-159">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**.</span><span class="sxs-lookup"><span data-stu-id="db309-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="db309-160">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast.</span><span class="sxs-lookup"><span data-stu-id="db309-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="db309-161">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-162">Hinnanguline maks</span><span class="sxs-lookup"><span data-stu-id="db309-162">Estimated Tax</span></span> | <span data-ttu-id="db309-163">See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa.</span><span class="sxs-lookup"><span data-stu-id="db309-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="db309-164">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast.</span><span class="sxs-lookup"><span data-stu-id="db309-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="db309-165">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-166">Hinnapakkumise summa pärast maksude mahaarvamist</span><span class="sxs-lookup"><span data-stu-id="db309-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="db309-167">See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="db309-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="db309-168">Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*.</span><span class="sxs-lookup"><span data-stu-id="db309-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="db309-169">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-170">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="db309-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="db309-171">Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**.</span><span class="sxs-lookup"><span data-stu-id="db309-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="db309-172">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db309-173">Kliendi eelarve</span><span class="sxs-lookup"><span data-stu-id="db309-173">Customer Budget</span></span> | <span data-ttu-id="db309-174">See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="db309-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="db309-175">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="db309-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="db309-176">Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid</span><span class="sxs-lookup"><span data-stu-id="db309-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="db309-177">**1. reegel**: kui väli **Kaasatud ülesanded** on tühi või seadistatud väärtusele **Kõik projekti ülesanded**, kaasatakse projekt hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="db309-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="db309-178">**2. reegel**: kui väli **Kaasatud ülesanded** on tühi või kui selle sätte väärtuseks on seatud **kõik projekti tööülesanded**, saab projekti ja teatud kandeklassi kaasata ainult hinnapakkumise ühele projektipõhisele hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="db309-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="db309-179">**3. reegel**: kui väli **Kaasatud ülesanded** on seadistatud väärtusele **Ainult valitud projekti ülesanded**, saab projekti ja teatud kandeklassi kaasata hinnapakkumise mitmele projektipõhisele hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="db309-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="db309-180">**4. reegel**: kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="db309-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="db309-181">**5. reegel**: kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="db309-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="db309-182">
                    <strong>Müügivõimalus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="db309-183">
                    <strong>Hinnapakkumine</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="db309-184">
                    <strong>Hinnapakkumise rida</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="db309-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="db309-186">
                    <strong>Kaasatud ülesanded</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="db309-187">
                    <strong>Kaasa aeg</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="db309-188">
                    <strong>Kaasa kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="db309-189">
                    <strong>Kaasa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="db309-190">
                    <strong>Tasu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="db309-191">
                    <strong>Kehtiv/kehtetu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="db309-192">
                    <strong>Põhjus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db309-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-193">O1</span><span class="sxs-lookup"><span data-stu-id="db309-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-194">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-195">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-196">P1</span><span class="sxs-lookup"><span data-stu-id="db309-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-197">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-198">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-199">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-200">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-201">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="db309-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-202">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="db309-202">Violation of Rule #2.</span></span> <span data-ttu-id="db309-203">P1-projekti aeg, kulud ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2.</span><span class="sxs-lookup"><span data-stu-id="db309-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-204">O1</span><span class="sxs-lookup"><span data-stu-id="db309-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-205">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-206">QL2</span><span class="sxs-lookup"><span data-stu-id="db309-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-207">P1</span><span class="sxs-lookup"><span data-stu-id="db309-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-208">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-209">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-210">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-211">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-211">Yes</span></span> </p>
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
<span data-ttu-id="db309-212">O1</span><span class="sxs-lookup"><span data-stu-id="db309-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-213">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-214">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-215">P1</span><span class="sxs-lookup"><span data-stu-id="db309-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-216">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-217">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-218">No</span><span class="sxs-lookup"><span data-stu-id="db309-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-219">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-220">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="db309-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-221">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="db309-221">Violation of Rule #2.</span></span> <span data-ttu-id="db309-222">P1-projekti aeg ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2.</span><span class="sxs-lookup"><span data-stu-id="db309-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-223">O1</span><span class="sxs-lookup"><span data-stu-id="db309-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-224">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-225">QL2</span><span class="sxs-lookup"><span data-stu-id="db309-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-226">P1</span><span class="sxs-lookup"><span data-stu-id="db309-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-227">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-228">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-229">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-230">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-230">Yes</span></span> </p>
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
<span data-ttu-id="db309-231">O1</span><span class="sxs-lookup"><span data-stu-id="db309-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-232">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-233">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-234">P1</span><span class="sxs-lookup"><span data-stu-id="db309-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-235">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-236">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-237">No</span><span class="sxs-lookup"><span data-stu-id="db309-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-238">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-239">Kehtib</span><span class="sxs-lookup"><span data-stu-id="db309-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="db309-240">P1-projekti tasud on kaasatud reale QL1.</span><span class="sxs-lookup"><span data-stu-id="db309-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="db309-241">P1-projekti kulu on kaasatud reale QL2.</span><span class="sxs-lookup"><span data-stu-id="db309-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="db309-242">See, mis on igale hinnapakkumise reale kaasatud, ei kattu ja on see kehtiv.</span><span class="sxs-lookup"><span data-stu-id="db309-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-243">O1</span><span class="sxs-lookup"><span data-stu-id="db309-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-244">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-245">QL2</span><span class="sxs-lookup"><span data-stu-id="db309-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-246">P1</span><span class="sxs-lookup"><span data-stu-id="db309-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-247">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-248">No</span><span class="sxs-lookup"><span data-stu-id="db309-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-249">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-250">No</span><span class="sxs-lookup"><span data-stu-id="db309-250">No</span></span> </p>
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
<span data-ttu-id="db309-251">O1</span><span class="sxs-lookup"><span data-stu-id="db309-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-252">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-253">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-254">P1</span><span class="sxs-lookup"><span data-stu-id="db309-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-255">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="db309-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-256">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-257">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-258">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-259">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="db309-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-260">Eeltoodud reegli nr 2 rikkumine</span><span class="sxs-lookup"><span data-stu-id="db309-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="db309-261">Q1 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="db309-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="db309-262">QL2 sisaldab kogu projekti P1 aega, kulu ja tasu ning kattub sellega, mis on kaasatud reale Q1.</span><span class="sxs-lookup"><span data-stu-id="db309-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-263">O1</span><span class="sxs-lookup"><span data-stu-id="db309-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-264">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-265">QL2</span><span class="sxs-lookup"><span data-stu-id="db309-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-266">P1</span><span class="sxs-lookup"><span data-stu-id="db309-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-267">Tühi</span><span class="sxs-lookup"><span data-stu-id="db309-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-268">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-269">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-270">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-270">Yes</span></span> </p>
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
<span data-ttu-id="db309-271">O1</span><span class="sxs-lookup"><span data-stu-id="db309-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-272">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-273">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-274">P1</span><span class="sxs-lookup"><span data-stu-id="db309-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-275">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="db309-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-276">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-277">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-278">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-279">Kehtib</span><span class="sxs-lookup"><span data-stu-id="db309-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-280">Vastavalt eeltoodud reeglile nr 3,</span><span class="sxs-lookup"><span data-stu-id="db309-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="db309-281">Q1 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="db309-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="db309-282">QL2 sisaldab projekti P1 ülesannete alamhulga aega, kulusid ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="db309-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="db309-283">Ainus täiendav valideerimine toimub QL1 tööülesannete alamhulga ümber, mis erineb QL2 tööülesannete alamhulgast.</span><span class="sxs-lookup"><span data-stu-id="db309-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="db309-284">See tagab, et kattumist ei esineks.</span><span class="sxs-lookup"><span data-stu-id="db309-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="db309-285">Seda teeb süsteem ülesannete sidumisel.</span><span class="sxs-lookup"><span data-stu-id="db309-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-286">O1</span><span class="sxs-lookup"><span data-stu-id="db309-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-287">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-288">QL2</span><span class="sxs-lookup"><span data-stu-id="db309-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-289">P1</span><span class="sxs-lookup"><span data-stu-id="db309-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-290">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="db309-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-291">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-292">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-293">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-293">Yes</span></span> </p>
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
<span data-ttu-id="db309-294">O1</span><span class="sxs-lookup"><span data-stu-id="db309-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-295">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-296">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-297">P1</span><span class="sxs-lookup"><span data-stu-id="db309-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-298">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="db309-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-299">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-300">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-301">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="db309-302">Kehtib</span><span class="sxs-lookup"><span data-stu-id="db309-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-303">Vastavalt reeglile nr 5 on Q1 ja Q2 kaks sama müügivõimalusega hinnapakkumist, nii et nad saavad mõlemad prognoosida projekti samu komponente.</span><span class="sxs-lookup"><span data-stu-id="db309-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-304">O1</span><span class="sxs-lookup"><span data-stu-id="db309-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-305">Kv2</span><span class="sxs-lookup"><span data-stu-id="db309-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-306">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-307">P1</span><span class="sxs-lookup"><span data-stu-id="db309-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-308">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="db309-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-309">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-310">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-311">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-311">Yes</span></span> </p>
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
<span data-ttu-id="db309-312">O1</span><span class="sxs-lookup"><span data-stu-id="db309-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-313">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-314">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-315">P1</span><span class="sxs-lookup"><span data-stu-id="db309-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-316">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="db309-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-317">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-318">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-319">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="db309-320">Kehtib</span><span class="sxs-lookup"><span data-stu-id="db309-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db309-321">Vastavalt reeglile nr 4 on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, nii et nad ei saa mõlemad prognoosida sama projekti komponente.</span><span class="sxs-lookup"><span data-stu-id="db309-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db309-322">O2</span><span class="sxs-lookup"><span data-stu-id="db309-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db309-323">Kv1</span><span class="sxs-lookup"><span data-stu-id="db309-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-324">QL1</span><span class="sxs-lookup"><span data-stu-id="db309-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-325">P1</span><span class="sxs-lookup"><span data-stu-id="db309-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="db309-326">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="db309-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-327">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db309-328">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db309-329">Ja</span><span class="sxs-lookup"><span data-stu-id="db309-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="db309-330">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="db309-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]