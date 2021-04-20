---
title: Hinnapakkumise rea arveldatavate komponentide konfigureerimine
description: Selles teemas antakse teavet arveldatavate ja mittearveldatavate komponentide seadistamise kohta projektipõhise hinnapakkumise real.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858288"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="07aca-103">Hinnapakkumise rea arveldatavate komponentide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="07aca-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="07aca-104">_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="07aca-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="07aca-105">Projektipõhine hinnapakkumise rida sisaldab *kaasatud* komponente ja *arveldatavaid* komponente.</span><span class="sxs-lookup"><span data-stu-id="07aca-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="07aca-106">Kaasatud komponente võidakse:</span><span class="sxs-lookup"><span data-stu-id="07aca-106">Included components are subject to:</span></span>

  - <span data-ttu-id="07aca-107">Arveldusmeetod ja kliendi jaotamine</span><span class="sxs-lookup"><span data-stu-id="07aca-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="07aca-108">Mitteületatavad limiidid</span><span class="sxs-lookup"><span data-stu-id="07aca-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="07aca-109">Projektipõhise hinnapakkumise rea määratletud arve sageduse sätted</span><span class="sxs-lookup"><span data-stu-id="07aca-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="07aca-110">Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="07aca-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="07aca-111">Väli **Arveldamise tüüp** on seatud, mis võimaldab hinnapakkumise rea kontekstis järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="07aca-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="07aca-112">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-112">Chargeable</span></span>
  - <span data-ttu-id="07aca-113">Mittearveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-113">Non-chargeable</span></span>

<span data-ttu-id="07aca-114">Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.</span><span class="sxs-lookup"><span data-stu-id="07aca-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="07aca-115">Arveldatav tegevus määratletakse hinnapakkumise rea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele.</span><span class="sxs-lookup"><span data-stu-id="07aca-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="07aca-116">Kui väli **Kaasa tööülesanded** on seatud väärtusele **Kogu projekt** või see on tühjaks jäetud, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.</span><span class="sxs-lookup"><span data-stu-id="07aca-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="07aca-117">Hinnapakkumise rea rollidele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Aeg**.</span><span class="sxs-lookup"><span data-stu-id="07aca-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="07aca-118">Kui projekti hinnapakkumise rea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.</span><span class="sxs-lookup"><span data-stu-id="07aca-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="07aca-119">Hinnapakkumise rea tehingu kategooriatele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="07aca-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="07aca-120">Kui projekti hinnapakkumise rea väli **Kaasa kulud** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.</span><span class="sxs-lookup"><span data-stu-id="07aca-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="07aca-121">Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="07aca-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="07aca-122">Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla projektipõhise hinnapakkumise rea kohta, mis võimaldab järgmist seadistust.</span><span class="sxs-lookup"><span data-stu-id="07aca-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="07aca-123">Kui projektipõhise hinnapakkumise rida sisaldab väärtust **Aeg** ja tööülesannet **T1**, seostatakse tööülesanne hinnapakkumise reaga kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="07aca-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="07aca-124">Kui olemas on teine hinnapakkumise rida, mis sisaldab väärtust **Kulud**, saate seostada hinnapakkumise rea tööülesannet **T1** sellega kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="07aca-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="07aca-125">Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.</span><span class="sxs-lookup"><span data-stu-id="07aca-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="07aca-126">Ülesande arveldamise tüübi saab konfigureerida projektipõhise hinnapakkumise rea vahekaardil **Arveldatavad ülesanded**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Hinnapakkumise rea ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="07aca-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="07aca-127">Teise võimalusena saate värskendada projekti ülesande arveldamise tüüpi väljal **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud hinnapakkumise ridu.</span><span class="sxs-lookup"><span data-stu-id="07aca-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="07aca-128">Rolli värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="07aca-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="07aca-129">Roll võib konkreetse projektipõhise hinnapakkumise rea puhul olla arveldatav või mittearveldatav.</span><span class="sxs-lookup"><span data-stu-id="07aca-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="07aca-130">Rolli arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad rollid**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad rollid**.</span><span class="sxs-lookup"><span data-stu-id="07aca-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="07aca-131">Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="07aca-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="07aca-132">Tehingu kategooria võib olla arveldatav või mittearveldatav kindla hinnapakkumise rea kohta.</span><span class="sxs-lookup"><span data-stu-id="07aca-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="07aca-133">Tehingu arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad kategooriad**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="07aca-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="07aca-134">Arveldatavuse lahendamine</span><span class="sxs-lookup"><span data-stu-id="07aca-134">Resolve chargeability</span></span>
<span data-ttu-id="07aca-135">Aja jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="07aca-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="07aca-136">**Aeg** lisatakse hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="07aca-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="07aca-137">**Roll** on hinnapakkumise real konfigureeritud kui tasustatav.</span><span class="sxs-lookup"><span data-stu-id="07aca-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="07aca-138">**Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="07aca-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="07aca-139">Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** samuti tasustavana.</span><span class="sxs-lookup"><span data-stu-id="07aca-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="07aca-140">Kulu jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="07aca-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="07aca-141">**Kulu** lisatakse hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="07aca-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="07aca-142">**Tehingukategooria** on hinnapakkumise real konfigureeritud kui tasustatav.</span><span class="sxs-lookup"><span data-stu-id="07aca-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="07aca-143">**Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="07aca-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="07aca-144">Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** samuti tasustavana.</span><span class="sxs-lookup"><span data-stu-id="07aca-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="07aca-145">Materjali jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="07aca-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="07aca-146">**Materjalid** lisatakse hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="07aca-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="07aca-147">**Kaasatud ülesanded** on hinnapakkumise real seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="07aca-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="07aca-148">Kui need kas asja on täidetud, peaks **Ülesanne** olema samuti konfigureeritud tasustavana.</span><span class="sxs-lookup"><span data-stu-id="07aca-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-149">
                    <strong>Kaasab aja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="07aca-150">
                    <strong>Kaasab kulu</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="07aca-151">
                    <strong>Sisaldab materjale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="07aca-152">
                    <strong>Kaasatud ülesanded</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-153">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-154">
                    <strong>Kategooria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-155">
                    <strong>Toiming</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="07aca-156">
                    <strong>Tasustatavuse mõju</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-157">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-158">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-159">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-160">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-161">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-162">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-163">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-164">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-165">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-166">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-167">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-168">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-169">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-170">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="07aca-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-171">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-172">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-173">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-174">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-175">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-176">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-177">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-178">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-179">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-180">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="07aca-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-181">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-182">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-183">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-184">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-185">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-186">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-187">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-188">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-189">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-190">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="07aca-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-191">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-192">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-193">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-194">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-195">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-196">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-197">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-198">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-199">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-200">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="07aca-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-201">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-202">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-203">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-204">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-205">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-206">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-207">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-208">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-209">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-210">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="07aca-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-211">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-212">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-213">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-214">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-215">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-216">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-218">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-219">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-220">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-221">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-222">
                    <strong>Arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-223">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-224">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-225">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-226">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-228">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-229">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-230">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-231">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-232">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-233">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-234">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-235">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-236">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-237">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="07aca-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-239">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-240">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-241">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-242">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-243">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-244">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-245">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-246">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-247">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="07aca-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="07aca-249">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-250">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-251">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-252">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-253">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-254">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-255">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-256">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-257">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-258">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="07aca-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-260">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-261">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-262">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-263">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-264">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-265">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="07aca-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="07aca-266">Tegeliku materjali arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="07aca-267">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="07aca-268">Ja</span><span class="sxs-lookup"><span data-stu-id="07aca-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="07aca-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="07aca-270">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="07aca-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="07aca-271">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="07aca-272">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="07aca-273">Ei saa määrata</span><span class="sxs-lookup"><span data-stu-id="07aca-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="07aca-274">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-275">Tegeliku kulu arveldamise tüüp:<strong> mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="07aca-276">Tegeliku materjali arveldamise tüüp:<strong> pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="07aca-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
