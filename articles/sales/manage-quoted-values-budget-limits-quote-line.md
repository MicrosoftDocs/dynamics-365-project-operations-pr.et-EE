---
title: Projektipõhiste hinnapakkumiste ridade ülevaade
description: Selles teemas antakse teavet projektitööks projektipõhiste hinnapakkumise ridade kasutamise kohta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181852"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="54246-103">Projektipõhiste hinnapakkumiste ridade ülevaade</span><span class="sxs-lookup"><span data-stu-id="54246-103">Project-based quote lines overview</span></span>

<span data-ttu-id="54246-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="54246-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54246-105">Projektipõhised hinnapakkumise read on loodud selleks, et aidata hinnata kohustuse projektitööd.</span><span class="sxs-lookup"><span data-stu-id="54246-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="54246-106">Projektipõhise hinnapakkumise rea struktuuri pikendatakse projekti prognooside alusel järgmiste kontseptsioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="54246-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="54246-107">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="54246-107">Billing Method</span></span>
- <span data-ttu-id="54246-108">Projekti vastendamine</span><span class="sxs-lookup"><span data-stu-id="54246-108">Project Mapping</span></span>
- <span data-ttu-id="54246-109">Kaasatud tehingute klassid</span><span class="sxs-lookup"><span data-stu-id="54246-109">Included Transaction classes</span></span>
- <span data-ttu-id="54246-110">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="54246-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="54246-111">Arveldatavuse seadistus</span><span class="sxs-lookup"><span data-stu-id="54246-111">Chargeability setup</span></span>
- <span data-ttu-id="54246-112">Prognoos hinnapakkumise rea üksikasjade abil</span><span class="sxs-lookup"><span data-stu-id="54246-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="54246-113">Hinnapakkumisrea kliendid</span><span class="sxs-lookup"><span data-stu-id="54246-113">Quote line Customers</span></span>

<span data-ttu-id="54246-114">Järgmine tabel annab teavet projektipõhise hinnapakkumise rea vahekaardi **Üldine** väljade kohta.</span><span class="sxs-lookup"><span data-stu-id="54246-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="54246-115">Need väljad aitavad seadistada projektitöö üksikasjaliku, ligikaudse prognoosi aluse.</span><span class="sxs-lookup"><span data-stu-id="54246-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="54246-116">**Väli**</span><span class="sxs-lookup"><span data-stu-id="54246-116">**Field**</span></span> | <span data-ttu-id="54246-117">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="54246-117">**Description**</span></span> | <span data-ttu-id="54246-118">**Allavoolu mõjud**</span><span class="sxs-lookup"><span data-stu-id="54246-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="54246-119">Nimetus</span><span class="sxs-lookup"><span data-stu-id="54246-119">Name</span></span> | <span data-ttu-id="54246-120">Hinnapakkumise rea nimi, mis peaks aitama teil tuvastada prognoositava hinnapakkumise diskreetse komponendi.</span><span class="sxs-lookup"><span data-stu-id="54246-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="54246-121">Kopeeritud projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-122">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="54246-122">Billing Method</span></span> | <span data-ttu-id="54246-123">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus vastavalt müügivõimaluse rea väljalt.</span><span class="sxs-lookup"><span data-stu-id="54246-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="54246-124">See väli sisaldab kahte põhilist lepingumudelit, mida Dynamics 365 Project Operations toetab.</span><span class="sxs-lookup"><span data-stu-id="54246-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="54246-125">- Fikseeritud hind</span><span class="sxs-lookup"><span data-stu-id="54246-125">- Fixed price</span></span></br><span data-ttu-id="54246-126">- Aeg ja materjal.</span><span class="sxs-lookup"><span data-stu-id="54246-126">- Time and material.</span></span>| <span data-ttu-id="54246-127">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-128">Project</span><span class="sxs-lookup"><span data-stu-id="54246-128">Project</span></span> | <span data-ttu-id="54246-129">Kasutage seda valikulist välja, et tuvastada projekt, mida kasutatakse selle kohustusega seotud töö teostamiseks.</span><span class="sxs-lookup"><span data-stu-id="54246-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="54246-130">Kui projekt on vastendatud hinnapakkumise reaga, aitab see teil seadistada tasustatavad tööülesanded ja esitada hinnapakkumise reale hinnapakkumise rea üksikasjadena projektipõhise prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="54246-131">Kui projekti ei vastendata projektipõhise hinnapakkumise reaga, tuleks prognoos luua käsitsi, luues kõigi hinnapakkumise ridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="54246-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="54246-132">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-133">Kaasa aeg</span><span class="sxs-lookup"><span data-stu-id="54246-133">Include Time</span></span> | <span data-ttu-id="54246-134">Lipp **Jah**/**Ei** näitab, kas valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54246-135">Lipp **Ei** näitab, et valitud projekti ajakandeid või tööjõukulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54246-136">Lipp **Jah** näitab, et valitud projekti ajakanded või tööjõukulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54246-137">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-138">Kaasa kulu</span><span class="sxs-lookup"><span data-stu-id="54246-138">Include Expense</span></span> | <span data-ttu-id="54246-139">Lipp **Jah**/**Ei** näitab, kas valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54246-140">Lipp **Ei** näitab, et valitud projekti kulusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54246-141">Lipp **Jah** näitab, et valitud projekti kulud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54246-142">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-143">Kaasa tasu</span><span class="sxs-lookup"><span data-stu-id="54246-143">Include Fee</span></span> | <span data-ttu-id="54246-144">Lipp **Jah**/**Ei** näitab, kas valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54246-145">Lipp **Ei** näitab, et valitud projekti tasusid ei kaasata selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54246-146">Lipp **Jah** näitab, et valitud projekti tasud kaasatakse selle hinnapakkumise rea prognoosi.</span><span class="sxs-lookup"><span data-stu-id="54246-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54246-147">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-148">Hinnapakkumise summa</span><span class="sxs-lookup"><span data-stu-id="54246-148">Quoted Amount</span></span> | <span data-ttu-id="54246-149">See on hinnapakkumise summa, mis esitatakse kliendile kõigi selle projektipõhise hinnapakkumise rea prognoositavate tööde kohta.</span><span class="sxs-lookup"><span data-stu-id="54246-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="54246-150">Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väärtus müügivõimaluse rea väljalt **Kliendi eelarve**.</span><span class="sxs-lookup"><span data-stu-id="54246-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="54246-151">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea üksikasjade summast.</span><span class="sxs-lookup"><span data-stu-id="54246-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="54246-152">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-153">Hinnanguline maks</span><span class="sxs-lookup"><span data-stu-id="54246-153">Estimated Tax</span></span> | <span data-ttu-id="54246-154">See on redigeeritav väli, et kasutaja saaks lisada hinnapakkumise reale eeldatava maksude summa.</span><span class="sxs-lookup"><span data-stu-id="54246-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="54246-155">Kui projektil põhineva hinnapakkumise real on rea üksikasjad, lukustatakse see väli redigeerimiseks ja summeeritakse hinnapakkumise rea maksu summast.</span><span class="sxs-lookup"><span data-stu-id="54246-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="54246-156">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-157">Hinnapakkumise summa pärast maksude mahaarvamist</span><span class="sxs-lookup"><span data-stu-id="54246-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="54246-158">See väli on hinnapakkumise rea summa pärast maksude mahaarvamist ja on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="54246-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="54246-159">Sellel väljal olev summa arvutatakse kui *Hinnapakkumisega summa + käibemaks*.</span><span class="sxs-lookup"><span data-stu-id="54246-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="54246-160">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-161">Mitteületatav limiit</span><span class="sxs-lookup"><span data-stu-id="54246-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="54246-162">Seda välja saab redigeerida ja see on saadaval ainult projektipõhiste hinnapakkumiste ridadel, millel on arveldamise meetodiks **Aeg ja materjal**.</span><span class="sxs-lookup"><span data-stu-id="54246-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="54246-163">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54246-164">Kliendi eelarve</span><span class="sxs-lookup"><span data-stu-id="54246-164">Customer Budget</span></span> | <span data-ttu-id="54246-165">See väli on redigeeritav ja see kopeeritakse vastavalt müügivõimaluse rea väljalt, kui hinnapakkumine on loodud müügivõimaluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="54246-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="54246-166">Välja väärtus kopeeritakse sellele projekti lepingureale, mis on selle hinnapakkumise rea põhjal hinnapakkumise võitmisel loodud.</span><span class="sxs-lookup"><span data-stu-id="54246-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="54246-167">Projektipõhiste hinnapakkumiste ridade vahekaardi Üldine väljade valideerimise reeglid</span><span class="sxs-lookup"><span data-stu-id="54246-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="54246-168">**1. reegel**: valitud projekti teatud kandeklassi saab lisada ainult hinnapakkumise ühele projektipõhise hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="54246-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="54246-169">**2. reegel**: kui müügivõimalusel on mitu hinnapakkumist, võivad erinevate hinnapakkumiste hinnapakkumise read viidata samale projektile ja sisaldada sama kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="54246-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="54246-170">**3. reegel**: kui hinnapakkumised ei kuulu sama müügivõimaluse juurde, ei saa nad sisaldada sama projekti ja kandeklassi.</span><span class="sxs-lookup"><span data-stu-id="54246-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="54246-171">
                    <strong>Müügivõimalus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="54246-172">
                    <strong>Hinnapakkumine</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="54246-173">
                    <strong>Hinnapakkumise rida</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="54246-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="54246-175">
                    <strong>Kaasa aeg</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="54246-176">
                    <strong>Kaasa kulu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="54246-177">
                    <strong>Kaasa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="54246-178">
                    <strong>tasu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="54246-179">
                    <strong>Kehtiv/kehtetu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="54246-180">
                    <strong>Põhjus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54246-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-181">O1</span><span class="sxs-lookup"><span data-stu-id="54246-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-182">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-183">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-184">P1</span><span class="sxs-lookup"><span data-stu-id="54246-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-185">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-186">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-187">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-188">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="54246-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-189">Reegli nr 1 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="54246-189">Violation of Rule #1.</span></span> <span data-ttu-id="54246-190">P1-projekti aeg, kulud ja tasud on kaasatud mõlemale hinnapakkumise reale, QL1 ja QL2.</span><span class="sxs-lookup"><span data-stu-id="54246-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-191">O1</span><span class="sxs-lookup"><span data-stu-id="54246-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-192">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-193">QL2</span><span class="sxs-lookup"><span data-stu-id="54246-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-194">P1</span><span class="sxs-lookup"><span data-stu-id="54246-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-195">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-196">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-197">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-197">Yes</span></span> </p>
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
<span data-ttu-id="54246-198">O1</span><span class="sxs-lookup"><span data-stu-id="54246-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-199">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-200">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-201">P1</span><span class="sxs-lookup"><span data-stu-id="54246-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-202">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-203">No</span><span class="sxs-lookup"><span data-stu-id="54246-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-204">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-205">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="54246-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-206">Reegli nr 1 rikkumine.</span><span class="sxs-lookup"><span data-stu-id="54246-206">Violation of Rule #1.</span></span> <span data-ttu-id="54246-207">P1-projekti aeg ja tasud on kaasatud mõlemale hinnapakkumise reale, QL1 ja QL2.</span><span class="sxs-lookup"><span data-stu-id="54246-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-208">O1</span><span class="sxs-lookup"><span data-stu-id="54246-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-209">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-210">QL2</span><span class="sxs-lookup"><span data-stu-id="54246-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-211">P1</span><span class="sxs-lookup"><span data-stu-id="54246-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-212">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-213">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-214">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-214">Yes</span></span> </p>
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
<span data-ttu-id="54246-215">O1</span><span class="sxs-lookup"><span data-stu-id="54246-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-216">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-217">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-218">P1</span><span class="sxs-lookup"><span data-stu-id="54246-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-219">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-220">No</span><span class="sxs-lookup"><span data-stu-id="54246-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-221">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-222">Kehtib</span><span class="sxs-lookup"><span data-stu-id="54246-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="54246-223">P1-projekti aeg ja tasud on kaasatud reale QL1.</span><span class="sxs-lookup"><span data-stu-id="54246-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="54246-224">P1-projekti kulu on kaasatud reale QL2.</span><span class="sxs-lookup"><span data-stu-id="54246-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="54246-225">See, mis on igale hinnapakkumise reale kaasatud, ei kattu, seega on see kehtiv.</span><span class="sxs-lookup"><span data-stu-id="54246-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-226">O1</span><span class="sxs-lookup"><span data-stu-id="54246-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-227">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-228">QL2</span><span class="sxs-lookup"><span data-stu-id="54246-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-229">P1</span><span class="sxs-lookup"><span data-stu-id="54246-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-230">No</span><span class="sxs-lookup"><span data-stu-id="54246-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-231">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-232">No</span><span class="sxs-lookup"><span data-stu-id="54246-232">No</span></span> </p>
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
<span data-ttu-id="54246-233">O1</span><span class="sxs-lookup"><span data-stu-id="54246-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-234">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-235">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-236">P1</span><span class="sxs-lookup"><span data-stu-id="54246-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-237">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-238">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-239">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-240">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="54246-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-241">Eeltoodud reegli nr 1 rikkumine</span><span class="sxs-lookup"><span data-stu-id="54246-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="54246-242">Q1 sisaldab kogu projekti P1 aega, kulu ja tasu.</span><span class="sxs-lookup"><span data-stu-id="54246-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="54246-243">QL2 sisaldab kogu projekti P1 aega, kulu ja tasu ning kattub sellega, mis on kaasatud reale Q1.</span><span class="sxs-lookup"><span data-stu-id="54246-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-244">O1</span><span class="sxs-lookup"><span data-stu-id="54246-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-245">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-246">QL2</span><span class="sxs-lookup"><span data-stu-id="54246-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-247">P1</span><span class="sxs-lookup"><span data-stu-id="54246-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-248">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-249">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-250">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-250">Yes</span></span> </p>
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
<span data-ttu-id="54246-251">O1</span><span class="sxs-lookup"><span data-stu-id="54246-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-252">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-253">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-254">P1</span><span class="sxs-lookup"><span data-stu-id="54246-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-255">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-256">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-257">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="54246-258">Kehtib</span><span class="sxs-lookup"><span data-stu-id="54246-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-259">Vastavalt reeglile nr 2 on Q1 ja Q2 kaks sama müügivõimalusega hinnapakkumist, nii et nad saavad mõlemad prognoosida projekti samu komponente.</span><span class="sxs-lookup"><span data-stu-id="54246-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-260">O1</span><span class="sxs-lookup"><span data-stu-id="54246-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-261">Kv2</span><span class="sxs-lookup"><span data-stu-id="54246-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-262">Q2 rida QL1</span><span class="sxs-lookup"><span data-stu-id="54246-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-263">P1</span><span class="sxs-lookup"><span data-stu-id="54246-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-264">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-265">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-266">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-266">Yes</span></span> </p>
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
<span data-ttu-id="54246-267">O1</span><span class="sxs-lookup"><span data-stu-id="54246-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-268">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-269">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-270">P1</span><span class="sxs-lookup"><span data-stu-id="54246-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-271">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-272">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-273">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="54246-274">Kehtib</span><span class="sxs-lookup"><span data-stu-id="54246-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54246-275">Vastavalt reeglile nr 3 on Q1 ja Q2 kaks erineva müügivõimaluse hinnapakkumist, nii et nad ei saa mõlemad prognoosida sama projekti komponente.</span><span class="sxs-lookup"><span data-stu-id="54246-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="54246-276">O2</span><span class="sxs-lookup"><span data-stu-id="54246-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54246-277">Kv1</span><span class="sxs-lookup"><span data-stu-id="54246-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-278">QL1</span><span class="sxs-lookup"><span data-stu-id="54246-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-279">P1</span><span class="sxs-lookup"><span data-stu-id="54246-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-280">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="54246-281">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="54246-282">Ja</span><span class="sxs-lookup"><span data-stu-id="54246-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="54246-283">Kehtetu</span><span class="sxs-lookup"><span data-stu-id="54246-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

