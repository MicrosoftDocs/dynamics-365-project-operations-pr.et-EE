---
title: Hinnapakkumise rea arveldatavate komponentide konfigureerimine
description: Selles teemas antakse teavet arveldatavate ja mittearveldatavate komponentide seadistamise kohta projektipõhise hinnapakkumise real.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003761"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="efcd9-103">Hinnapakkumise rea arveldatavate komponentide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="efcd9-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="efcd9-104">_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="efcd9-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="efcd9-105">Projektipõhine hinnapakkumise rida sisaldab *kaasatud* komponente ja *arveldatavaid* komponente.</span><span class="sxs-lookup"><span data-stu-id="efcd9-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="efcd9-106">Kaasatud komponente võidakse:</span><span class="sxs-lookup"><span data-stu-id="efcd9-106">Included components are subject to:</span></span>

  - <span data-ttu-id="efcd9-107">Arveldusmeetod ja kliendi jaotamine</span><span class="sxs-lookup"><span data-stu-id="efcd9-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="efcd9-108">Mitteületatavad limiidid</span><span class="sxs-lookup"><span data-stu-id="efcd9-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="efcd9-109">Projektipõhise hinnapakkumise rea määratletud arve sageduse sätted</span><span class="sxs-lookup"><span data-stu-id="efcd9-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="efcd9-110">Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="efcd9-111">Väli **Arveldamise tüüp** on seatud, mis võimaldab hinnapakkumise rea kontekstis järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="efcd9-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="efcd9-112">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-112">Chargeable</span></span>
  - <span data-ttu-id="efcd9-113">Mittearveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-113">Non-chargeable</span></span>

<span data-ttu-id="efcd9-114">Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.</span><span class="sxs-lookup"><span data-stu-id="efcd9-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="efcd9-115">Arveldatav tegevus määratletakse hinnapakkumise rea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele.</span><span class="sxs-lookup"><span data-stu-id="efcd9-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="efcd9-116">Kui väli **Kaasa tööülesanded** on seatud väärtusele **Kogu projekt** või see on tühjaks jäetud, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.</span><span class="sxs-lookup"><span data-stu-id="efcd9-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="efcd9-117">Hinnapakkumise rea rollidele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Aeg**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="efcd9-118">Kui projekti hinnapakkumise rea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.</span><span class="sxs-lookup"><span data-stu-id="efcd9-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="efcd9-119">Hinnapakkumise rea tehingu kategooriatele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="efcd9-120">Kui projekti hinnapakkumise rea väli **Kaasa kulud** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.</span><span class="sxs-lookup"><span data-stu-id="efcd9-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="efcd9-121">Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="efcd9-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="efcd9-122">Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla projektipõhise hinnapakkumise rea kohta, mis võimaldab järgmist seadistust.</span><span class="sxs-lookup"><span data-stu-id="efcd9-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="efcd9-123">Kui projektipõhise hinnapakkumise rida sisaldab väärtust **Aeg** ja tööülesannet **T1**, seostatakse tööülesanne hinnapakkumise reaga kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="efcd9-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="efcd9-124">Kui olemas on teine hinnapakkumise rida, mis sisaldab väärtust **Kulud**, saate seostada hinnapakkumise rea tööülesannet **T1** sellega kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="efcd9-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="efcd9-125">Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.</span><span class="sxs-lookup"><span data-stu-id="efcd9-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="efcd9-126">Ülesande arveldamise tüübi saab konfigureerida projektipõhise hinnapakkumise rea vahekaardil **Arveldatavad ülesanded**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Hinnapakkumise rea ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="efcd9-127">Teise võimalusena saate värskendada projekti ülesande arveldamise tüüpi väljal **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud hinnapakkumise ridu.</span><span class="sxs-lookup"><span data-stu-id="efcd9-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="efcd9-128">Rolli värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="efcd9-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="efcd9-129">Roll võib konkreetse projektipõhise hinnapakkumise rea puhul olla arveldatav või mittearveldatav.</span><span class="sxs-lookup"><span data-stu-id="efcd9-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="efcd9-130">Rolli arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad rollid**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad rollid**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="efcd9-131">Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="efcd9-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="efcd9-132">Tehingu kategooria võib olla arveldatav või mittearveldatav kindla hinnapakkumise rea kohta.</span><span class="sxs-lookup"><span data-stu-id="efcd9-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="efcd9-133">Tehingu arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad kategooriad**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="efcd9-134">Arveldatavuse lahendamine</span><span class="sxs-lookup"><span data-stu-id="efcd9-134">Resolve chargeability</span></span>
<span data-ttu-id="efcd9-135">Aja jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="efcd9-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="efcd9-136">**Aeg** lisatakse hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="efcd9-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="efcd9-137">**Roll** on hinnapakkumise real konfigureeritud kui tasustatav.</span><span class="sxs-lookup"><span data-stu-id="efcd9-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="efcd9-138">**Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="efcd9-139">Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** samuti tasustavana.</span><span class="sxs-lookup"><span data-stu-id="efcd9-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="efcd9-140">Kulu jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="efcd9-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="efcd9-141">**Kulu** lisatakse hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="efcd9-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="efcd9-142">**Tehingukategooria** on hinnapakkumise real konfigureeritud kui tasustatav.</span><span class="sxs-lookup"><span data-stu-id="efcd9-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="efcd9-143">**Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="efcd9-144">Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** samuti tasustavana.</span><span class="sxs-lookup"><span data-stu-id="efcd9-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="efcd9-145">Materjali jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="efcd9-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="efcd9-146">**Materjalid** lisatakse hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="efcd9-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="efcd9-147">**Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="efcd9-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="efcd9-148">Kui need kas asja on täidetud, peaks **Ülesanne** olema samuti konfigureeritud tasustavana.</span><span class="sxs-lookup"><span data-stu-id="efcd9-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-149">
                    <strong>Kaasab aja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="efcd9-150">
                    <strong>Kaasab kulu</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="efcd9-151">
                    <strong>Sisaldab materjale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="efcd9-152">
                    <strong>Kaasatud ülesanded</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-153">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-154">
                    <strong>Kategooria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-155">
                    <strong>Toiming</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="efcd9-156">
                    <strong>Tasustatavuse mõju</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-157">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-158">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-159">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-160">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-161">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-162">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-163">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-164">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-165">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-166">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-167">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-168">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-169">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-170">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efcd9-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-171">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-172">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-173">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-174">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-175">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-176">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-177">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-178">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-179">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-180">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efcd9-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-181">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-182">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-183">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-184">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-185">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-186">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-187">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-188">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-189">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-190">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efcd9-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-191">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-192">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-193">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-194">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-195">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-196">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-197">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-198">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-199">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-200">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efcd9-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-201">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-202">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-203">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-204">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-205">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-206">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-207">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-208">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-209">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-210">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efcd9-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-211">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-212">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-213">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-214">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-215">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-216">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-218">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-219">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-220">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-221">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-222">
                    <strong>Arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-223">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-224">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-225">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-226">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-228">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-229">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-230">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-231">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-232">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-233">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-234">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-235">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-236">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-237">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="efcd9-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-239">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-240">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-241">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-242">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-243">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-244">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-245">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-246">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-247">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="efcd9-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efcd9-249">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-250">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-251">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-252">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-253">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-254">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-255">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-256">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-257">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-258">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="efcd9-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-260">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-261">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-262">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-263">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-264">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-265">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efcd9-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efcd9-266">Tegeliku materjali arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efcd9-267">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efcd9-268">Ja</span><span class="sxs-lookup"><span data-stu-id="efcd9-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="efcd9-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efcd9-270">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efcd9-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efcd9-271">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efcd9-272">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efcd9-273">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="efcd9-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efcd9-274">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-275">Tegeliku kulu arveldamise tüüp:<strong> mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="efcd9-276">Tegeliku materjali arveldamise tüüp:<strong> pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efcd9-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
