---
title: Projektipõhiste hinnapakkumiste ridade ülevaade
description: Selles teemas antakse teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858693"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="28107-103">Projektipõhiste hinnapakkumiste ridade ülevaade</span><span class="sxs-lookup"><span data-stu-id="28107-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="28107-104">_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="28107-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="28107-105">Projektipõhised hinnapakkumise read on loodud selleks, et aidata hinnata kohustuse projektitööd.</span><span class="sxs-lookup"><span data-stu-id="28107-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="28107-106">Projektipõhise hinnapakkumise rea struktuuri pikendatakse projekti prognooside alusel järgmiste kontseptsioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="28107-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="28107-107">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="28107-107">Billing Method</span></span>
- <span data-ttu-id="28107-108">Projekti ja ülesannete vastendamine</span><span class="sxs-lookup"><span data-stu-id="28107-108">Project and Task Mapping</span></span>
- <span data-ttu-id="28107-109">Kaasatud tehingute klassid</span><span class="sxs-lookup"><span data-stu-id="28107-109">Included Transaction classes</span></span>
- <span data-ttu-id="28107-110">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="28107-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="28107-111">Arveldatavuse seadistus</span><span class="sxs-lookup"><span data-stu-id="28107-111">Chargeability setup</span></span>
- <span data-ttu-id="28107-112">Prognoos hinnapakkumise rea üksikasjade abil</span><span class="sxs-lookup"><span data-stu-id="28107-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="28107-113">Hinnapakkumisrea kliendid</span><span class="sxs-lookup"><span data-stu-id="28107-113">Quote line Customers</span></span>

<span data-ttu-id="28107-114">Järgmine tabel annab teavet projektipõhise hinnapakkumise rea vahekaardi **Üldine** väljade kohta.</span><span class="sxs-lookup"><span data-stu-id="28107-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="28107-115">Need väljad aitavad seadistada projektitöö üksikasjaliku, ligikaudse prognoosi aluse.</span><span class="sxs-lookup"><span data-stu-id="28107-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="28107-116">**Väli**</span><span class="sxs-lookup"><span data-stu-id="28107-116">**Field**</span></span> | <span data-ttu-id="28107-117">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="28107-117">**Description**</span></span> | <span data-ttu-id="28107-118">**Allavoolu mõjud**</span><span class="sxs-lookup"><span data-stu-id="28107-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="28107-119">Nimetus</span><span class="sxs-lookup"><span data-stu-id="28107-119">Name</span></span> | <span data-ttu-id="28107-120">Hinnapakkumise rea nimi, mis aitab teil teha kindlaks prognoositava hinnapakkumise diskreetse komponendi.</span><span class="sxs-lookup"><span data-stu-id="28107-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="28107-121">Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="28107-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-122">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="28107-122">Billing Method</span></span> | <span data-ttu-id="28107-123">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt.</span><span class="sxs-lookup"><span data-stu-id="28107-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="28107-124">See väli sisaldab kahte peamist lepingumudelit, mida rakendus Dynamics 365 Project Operations toetab.</span><span class="sxs-lookup"><span data-stu-id="28107-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="28107-125">- Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="28107-125">- Fixed price</span></span></br><span data-ttu-id="28107-126">- Aeg ja materjal.</span><span class="sxs-lookup"><span data-stu-id="28107-126">- Time and material.</span></span>| <span data-ttu-id="28107-127">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-128">Project</span><span class="sxs-lookup"><span data-stu-id="28107-128">Project</span></span> | <span data-ttu-id="28107-129">Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks.</span><span class="sxs-lookup"><span data-stu-id="28107-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="28107-130">Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi.</span><span class="sxs-lookup"><span data-stu-id="28107-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="28107-131">Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="28107-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="28107-132">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="28107-133">Kaasatud ülesanded</span><span class="sxs-lookup"><span data-stu-id="28107-133">Included Tasks</span></span> | <span data-ttu-id="28107-134">Näitab, kas seda hinnapakkumise rida kasutatakse valitud projekti kõigi või mõnede projekti toimingute jaoks.</span><span class="sxs-lookup"><span data-stu-id="28107-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="28107-135">Sellel väljal on järgmised võimalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="28107-135">This field has the following possible values:</span></span></br><span data-ttu-id="28107-136">- Kõik projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="28107-136">- All project tasks</span></span></br><span data-ttu-id="28107-137">- Ainult valitud projekti ülesanded</span><span class="sxs-lookup"><span data-stu-id="28107-137">- Selected project tasks only</span></span></br><span data-ttu-id="28107-138">Tühi väärtus sellel väljal võrdub valikuga **Kõik projekti ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="28107-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="28107-139">Kui projekti lehel on valitud **Ainult valitud projekti ülesanded**, saate vahekaardil **Ülesande arvelduse seadistus** valida konkreetsed tööülesanded, et seostada need selle hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="28107-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="28107-140">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-141">Kaasa aeg</span><span class="sxs-lookup"><span data-stu-id="28107-141">Include Time</span></span> | <span data-ttu-id="28107-142">Väärtus **Jah**/**Ei** näitab, kas valitud projekti tehingu või tööjõu maksumused lisatakse selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-143">Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="28107-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-144">Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="28107-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="28107-145">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-146">Kaasa kulu</span><span class="sxs-lookup"><span data-stu-id="28107-146">Include Expense</span></span> | <span data-ttu-id="28107-147">Väärtus **Jah**/**Ei** näitab, kas valitud projekti kulu maksumused lisatakse selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-148">Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="28107-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-149">Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="28107-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="28107-150">See väärtus kopeeritakse üle projekti lepingurea, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-151">Kaasa materjal</span><span class="sxs-lookup"><span data-stu-id="28107-151">Include Material</span></span> | <span data-ttu-id="28107-152">Väärtus **Jah**/**Ei** näitab, kas valitud projekti materjali maksumused lisatakse selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-153">Väärtus **Ei** näitab, et materjali maksumust ei lisata selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-154">Väärtus **Jah** näitab, et materjali maksumus lisatakse selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="28107-155">See väärtus kopeeritakse üle projekti lepingurea, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-156">Kaasa tasu</span><span class="sxs-lookup"><span data-stu-id="28107-156">Include Fee</span></span> | <span data-ttu-id="28107-157">Väärtus **Jah**/**Ei** näitab, kas valitud projekti tasud lisatakse selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-158">Väärtus **Ei** näitab, et valitud projekti tasusid ei lisata selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="28107-159">Väärtus **Jah** näitab, et valitud projekti tasud lisatakse selle hinnapakkumise rea prognoosile.</span><span class="sxs-lookup"><span data-stu-id="28107-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="28107-160">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-161">Hinnapakkumise summa</span><span class="sxs-lookup"><span data-stu-id="28107-161">Quoted Amount</span></span> | <span data-ttu-id="28107-162">See on summa, mis esitatakse kliendile hinnapakkumisena selle projektipõhise hinnapakkumise rea kogu prognoositud töö kohta.</span><span class="sxs-lookup"><span data-stu-id="28107-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="28107-163">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**.</span><span class="sxs-lookup"><span data-stu-id="28107-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="28107-164">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast.</span><span class="sxs-lookup"><span data-stu-id="28107-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="28107-165">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-166">Hinnanguline maks</span><span class="sxs-lookup"><span data-stu-id="28107-166">Estimated Tax</span></span> | <span data-ttu-id="28107-167">See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa.</span><span class="sxs-lookup"><span data-stu-id="28107-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="28107-168">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast.</span><span class="sxs-lookup"><span data-stu-id="28107-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="28107-169">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-170">Hinnapakkumise summa pärast maksude mahaarvamist</span><span class="sxs-lookup"><span data-stu-id="28107-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="28107-171">See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="28107-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="28107-172">Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*.</span><span class="sxs-lookup"><span data-stu-id="28107-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="28107-173">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-174">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="28107-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="28107-175">Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**.</span><span class="sxs-lookup"><span data-stu-id="28107-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="28107-176">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="28107-177">Kliendi eelarve</span><span class="sxs-lookup"><span data-stu-id="28107-177">Customer Budget</span></span> | <span data-ttu-id="28107-178">See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="28107-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="28107-179">See väärtus kopeeritakse projekti lepingureale, mis luuakse selle hinnapakkumise rea põhjal, kui hinnapakkumine on võidetud.</span><span class="sxs-lookup"><span data-stu-id="28107-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="28107-180">Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid</span><span class="sxs-lookup"><span data-stu-id="28107-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="28107-181">**1. reegel**: kui väli **Kaasatud ülesanded** on tühi või seadistatud väärtusele **Kõik projekti ülesanded**, kaasatakse projekt hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="28107-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="28107-182">**2. reegel**: kui väli **Kaasatud ülesanded** on tühi või kui selle sätte väärtuseks on seatud **kõik projekti tööülesanded**, saab projekti ja teatud kandeklassi kaasata ainult hinnapakkumise ühele projektipõhisele hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="28107-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="28107-183">**3. reegel**: kui väli **Kaasatud ülesanded** on seadistatud väärtusele **Ainult valitud projekti ülesanded**, saab projekti ja teatud kandeklassi kaasata hinnapakkumise mitmele projektipõhisele hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="28107-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="28107-184">**4. reegel**: kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="28107-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="28107-185">**5. reegel**: kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="28107-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="28107-186">
                    <strong>Müügivõimalus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="28107-187">
                    <strong>Hinnapakkumine</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="28107-188">
                    <strong>Hinnapakkumise rida</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="28107-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="28107-190">
                    <strong>Kaasatud ülesanded</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="28107-191">
                    <strong>Kaasa aeg</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="28107-192">
                    <strong>Kaasa kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="28107-193">
                    <strong>Kaasa materjal</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="28107-194">
                    <strong>Kaasamine</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="28107-195">
                    <strong>Tasu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="28107-196">
                    <strong>Kehtiv/kehtetu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="28107-197">
                    <strong>Põhjus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28107-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-198">O1</span><span class="sxs-lookup"><span data-stu-id="28107-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-199">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-200">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-201">P1</span><span class="sxs-lookup"><span data-stu-id="28107-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-202">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-203">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-204">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-205">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-206">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-207">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="28107-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-208">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="28107-208">Violation of Rule #2.</span></span> <span data-ttu-id="28107-209">P1-projekti aeg, kulud ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2</span><span class="sxs-lookup"><span data-stu-id="28107-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-210">O1</span><span class="sxs-lookup"><span data-stu-id="28107-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-211">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-212">QL2</span><span class="sxs-lookup"><span data-stu-id="28107-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-213">P1</span><span class="sxs-lookup"><span data-stu-id="28107-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-214">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-215">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-216">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-217">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-218">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-219">O1</span><span class="sxs-lookup"><span data-stu-id="28107-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-220">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-221">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-222">P1</span><span class="sxs-lookup"><span data-stu-id="28107-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-223">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-224">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-225">No</span><span class="sxs-lookup"><span data-stu-id="28107-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-226">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-227">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-228">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="28107-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-229">Reegli nr 2 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="28107-229">Violation of Rule #2.</span></span> <span data-ttu-id="28107-230">P1-projekti aeg, materjal ja tasud on kaasatud hinnapakkumise ridadele QL1 ja QL2</span><span class="sxs-lookup"><span data-stu-id="28107-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-231">O1</span><span class="sxs-lookup"><span data-stu-id="28107-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-232">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-233">QL2</span><span class="sxs-lookup"><span data-stu-id="28107-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-234">P1</span><span class="sxs-lookup"><span data-stu-id="28107-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-235">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-236">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-237">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-238">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-239">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-240">O1</span><span class="sxs-lookup"><span data-stu-id="28107-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-241">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-242">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-243">P1</span><span class="sxs-lookup"><span data-stu-id="28107-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-244">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-245">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-246">No</span><span class="sxs-lookup"><span data-stu-id="28107-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-247">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-248">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-249">Sobiv</span><span class="sxs-lookup"><span data-stu-id="28107-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-250">P1-projekti aeg, materjal ja tasud on kaasatud reale QL1</span><span class="sxs-lookup"><span data-stu-id="28107-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="28107-251">P1-projekti kulu on kaasatud reale QL2</span><span class="sxs-lookup"><span data-stu-id="28107-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="28107-252">Igal hinnapakkumise real olev ei kattu ja on seetõttu kehtiv.</span><span class="sxs-lookup"><span data-stu-id="28107-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-253">O1</span><span class="sxs-lookup"><span data-stu-id="28107-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-254">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-255">QL2</span><span class="sxs-lookup"><span data-stu-id="28107-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-256">P1</span><span class="sxs-lookup"><span data-stu-id="28107-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-257">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-258">No</span><span class="sxs-lookup"><span data-stu-id="28107-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-259">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-260">No</span><span class="sxs-lookup"><span data-stu-id="28107-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-261">No</span><span class="sxs-lookup"><span data-stu-id="28107-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-262">O1</span><span class="sxs-lookup"><span data-stu-id="28107-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-263">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-264">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-265">P1</span><span class="sxs-lookup"><span data-stu-id="28107-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-266">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="28107-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-267">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-268">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-269">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-270">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-271">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="28107-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-272">Reegli nr 2 rikkumine</span><span class="sxs-lookup"><span data-stu-id="28107-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="28107-273">Q1 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas</span><span class="sxs-lookup"><span data-stu-id="28107-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="28107-274">QL2 hõlmab kogu projektiga P1 seotud aega, kulutusi ja tasusid ning seega kattub see sellega, mis on kaasatud Q1-te.</span><span class="sxs-lookup"><span data-stu-id="28107-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-275">O1</span><span class="sxs-lookup"><span data-stu-id="28107-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-276">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-277">QL2</span><span class="sxs-lookup"><span data-stu-id="28107-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-278">P1</span><span class="sxs-lookup"><span data-stu-id="28107-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-279">Tühi</span><span class="sxs-lookup"><span data-stu-id="28107-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-280">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-281">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-282">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-283">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-284">O1</span><span class="sxs-lookup"><span data-stu-id="28107-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-285">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-286">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-287">P1</span><span class="sxs-lookup"><span data-stu-id="28107-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-288">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="28107-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-289">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-290">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-291">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-292">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-293">Sobiv</span><span class="sxs-lookup"><span data-stu-id="28107-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-294">Reegli nr 3 järgi</span><span class="sxs-lookup"><span data-stu-id="28107-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="28107-295">Q1 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas.</span><span class="sxs-lookup"><span data-stu-id="28107-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="28107-296">QL2 sisaldab aega, materjale, kulusid ja tasusid P1-projekti ülesannete alamhulgas.</span><span class="sxs-lookup"><span data-stu-id="28107-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="28107-297">Ainus täiendav valideerimine on QL1 toimingute alamhulga ümber, mis erineb QL2 tööülesannete alamhulgast, tagamaks, et poleks kattumist.</span><span class="sxs-lookup"><span data-stu-id="28107-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="28107-298">Seda teeb süsteem ülesannete sidumisel.</span><span class="sxs-lookup"><span data-stu-id="28107-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-299">O1</span><span class="sxs-lookup"><span data-stu-id="28107-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-300">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-301">QL2</span><span class="sxs-lookup"><span data-stu-id="28107-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-302">P1</span><span class="sxs-lookup"><span data-stu-id="28107-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-303">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="28107-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-304">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-305">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-306">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-307">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-308">O1</span><span class="sxs-lookup"><span data-stu-id="28107-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-309">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-310">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-311">P1</span><span class="sxs-lookup"><span data-stu-id="28107-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-312">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="28107-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-313">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-314">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-315">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-316">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-317">Sobiv</span><span class="sxs-lookup"><span data-stu-id="28107-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-318">Reegli nr 5 järgi on Q1 ja Q2 kaks sama müügivõimaluse hinnapakkumist, seega saavad mõlemad hinnata projekti samu komponente.</span><span class="sxs-lookup"><span data-stu-id="28107-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-319">O1</span><span class="sxs-lookup"><span data-stu-id="28107-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-320">Kv2</span><span class="sxs-lookup"><span data-stu-id="28107-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-321">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-322">P1</span><span class="sxs-lookup"><span data-stu-id="28107-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-323">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="28107-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-324">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-325">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-326">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-327">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-328">O1</span><span class="sxs-lookup"><span data-stu-id="28107-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-329">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-330">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-331">P1</span><span class="sxs-lookup"><span data-stu-id="28107-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-332">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="28107-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-333">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-334">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-335">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-336">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-337">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="28107-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="28107-338">Reegli nr 4 järgi on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, seega ei saa need mõlemad hinnata sama projekti samu komponente.</span><span class="sxs-lookup"><span data-stu-id="28107-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="28107-339">O2</span><span class="sxs-lookup"><span data-stu-id="28107-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="28107-340">Kv1</span><span class="sxs-lookup"><span data-stu-id="28107-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="28107-341">QL1</span><span class="sxs-lookup"><span data-stu-id="28107-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-342">P1</span><span class="sxs-lookup"><span data-stu-id="28107-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="28107-343">Kõik projekti ülesanded või tühi</span><span class="sxs-lookup"><span data-stu-id="28107-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="28107-344">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="28107-345">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="28107-346">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="28107-347">Ja</span><span class="sxs-lookup"><span data-stu-id="28107-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
