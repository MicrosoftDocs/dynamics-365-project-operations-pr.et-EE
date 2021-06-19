---
title: Projektipõhise lepingurea arveldatavate komponentide konfigureerimine
description: Selles teemas antakse teavet selle kohta, kuidas lisada Project Operationsis lepinguridadele arveldatavaid komponente.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003716"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="b8df3-103">Projektipõhise lepingurea arveldatavate komponentide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b8df3-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="b8df3-104">_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="b8df3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b8df3-105">Projektipõhine lepingurida *sisaldas* komponente ja *arveldatavaid* komponente.</span><span class="sxs-lookup"><span data-stu-id="b8df3-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="b8df3-106">Kaasatud komponendid on komponendid, mis kuuluvad:</span><span class="sxs-lookup"><span data-stu-id="b8df3-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="b8df3-107">Arveldusmeetod ja kliendi jaotamine</span><span class="sxs-lookup"><span data-stu-id="b8df3-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="b8df3-108">Mitteületatavad limiidid</span><span class="sxs-lookup"><span data-stu-id="b8df3-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="b8df3-109">Projektipõhise lepingurea määratletud arve sageduse sätted</span><span class="sxs-lookup"><span data-stu-id="b8df3-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="b8df3-110">Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="b8df3-111">Väli **Arveldamise tüüp** on seatud, mis võimaldab lepingurea kontekstis järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b8df3-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="b8df3-112">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-112">Chargeable</span></span>
  - <span data-ttu-id="b8df3-113">Mittearveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-113">Non-chargeable</span></span>

<span data-ttu-id="b8df3-114">Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.</span><span class="sxs-lookup"><span data-stu-id="b8df3-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="b8df3-115">Arveldatav tegevus määratletakse projekti lepingurea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele.</span><span class="sxs-lookup"><span data-stu-id="b8df3-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="b8df3-116">Kui lepingurea väli **Kaasa tööülesanded** on tühi või seatud väärtusele **Kogu projekt**, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.</span><span class="sxs-lookup"><span data-stu-id="b8df3-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="b8df3-117">Projekti lepingurea rollidele määratud arveldatavuse kehtib ainult tehingu klassile **Aeg**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="b8df3-118">Kui lepingurea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.</span><span class="sxs-lookup"><span data-stu-id="b8df3-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="b8df3-119">Projekti lepingurea tehingu kategooriate määratud arveldatavuse kehtib ainult tehingu klassile **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="b8df3-120">Kui väli **Kaasa kulu** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.</span><span class="sxs-lookup"><span data-stu-id="b8df3-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="b8df3-121">Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="b8df3-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="b8df3-122">Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla lepingurea kohta, mis võimaldab järgmist seadistust.</span><span class="sxs-lookup"><span data-stu-id="b8df3-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="b8df3-123">Kui projektipõhine lepingurida sisaldab väärtust **Aeg** ja teatud ülesannet, siis seostatakse väärtust **T1** sellega kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="b8df3-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="b8df3-124">Kui olemas on teine lepingurida, mis sisaldab väärtust **Kulu**, saate seostada lepingurea väärtuse T1 tööülesannet sellega kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="b8df3-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="b8df3-125">Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.</span><span class="sxs-lookup"><span data-stu-id="b8df3-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="b8df3-126">Ülesande arveldamise tüübi saab konfigureerida lepingurea vahekaardil **Arveldatavad ülesanded**, värskendades lepingurea ülesannete andmeruudustikus välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="b8df3-127">Teise võimalusena saate värskendada välja **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud kontaktiridu.</span><span class="sxs-lookup"><span data-stu-id="b8df3-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="b8df3-128">Rolli värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="b8df3-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="b8df3-129">Roll võib olla arveldatav või mittearveldatav kindla lepingurea kohta.</span><span class="sxs-lookup"><span data-stu-id="b8df3-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="b8df3-130">Rolli arveldamise tüüpi saab konfigureerida lepingurea vahekaardil **Arveldatavad rollid**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="b8df3-131">Selleks värskendage andmeruudustikus **Arveldatavad rollid** välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="b8df3-132">Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="b8df3-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="b8df3-133">Tehingu kategooria võib olla arveldatav või mittearveldatav kindla lepingurea kohta.</span><span class="sxs-lookup"><span data-stu-id="b8df3-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="b8df3-134">Tehingu arveldamise tüüpi saab konfigureerida projektipõhise lepingurea vahekaardil **Arveldatavad kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="b8df3-135">Selleks värskendage andmeruudustikus **Arveldatavad kategooriad** välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="b8df3-136">Arveldatavuse lahendamine</span><span class="sxs-lookup"><span data-stu-id="b8df3-136">Resolve chargeability</span></span>

<span data-ttu-id="b8df3-137">Aja jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="b8df3-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="b8df3-138">**Aeg** lisatakse lepingureale.</span><span class="sxs-lookup"><span data-stu-id="b8df3-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="b8df3-139">**Roll** on lepingureal konfigureeritud kui tasustatav.</span><span class="sxs-lookup"><span data-stu-id="b8df3-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="b8df3-140">**Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="b8df3-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="b8df3-141">Kui need kolm asja on täidetud, konfigureeritakse ülesanne tasustavana.</span><span class="sxs-lookup"><span data-stu-id="b8df3-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="b8df3-142">Kulu jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="b8df3-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="b8df3-143">**Kulu** lisatakse lepingureale</span><span class="sxs-lookup"><span data-stu-id="b8df3-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="b8df3-144">**Tehingukategooria** on lepingureal konfigureeritud kui tasustatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="b8df3-145">**Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanne**</span><span class="sxs-lookup"><span data-stu-id="b8df3-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="b8df3-146">Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** tasustavana.</span><span class="sxs-lookup"><span data-stu-id="b8df3-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="b8df3-147">Materjali jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="b8df3-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="b8df3-148">**Materjalid** lisatakse lepingureale</span><span class="sxs-lookup"><span data-stu-id="b8df3-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="b8df3-149">**Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanded**</span><span class="sxs-lookup"><span data-stu-id="b8df3-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="b8df3-150">Kui need kaks asja on täidetud, konfigureeritakse **Ülesanne** tasustavana.</span><span class="sxs-lookup"><span data-stu-id="b8df3-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-151">
                    <strong>Kaasab aja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b8df3-152">
                    <strong>Kaasab kulu</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b8df3-153">
                    <strong>Sisaldab materjale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="b8df3-154">
                    <strong>Kaasatud ülesanded</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-155">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-156">
                    <strong>Kategooria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-157">
                    <strong>Toiming</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="b8df3-158">
                    <strong>Tasustatavuse mõju</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-159">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-160">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-161">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-162">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-163">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-164">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-165">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-166">Tegeliku aja arveldamine: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-167">Tegeliku kulu arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-168">Tegeliku materjali arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-169">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-170">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-171">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-172">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="b8df3-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-173">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-174">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-175">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-176">Tegeliku aja arveldamine: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-177">Tegeliku kulu arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-178">Tegeliku materjali arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-179">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-180">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-181">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-182">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="b8df3-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-183">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-184">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-185">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-186">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-187">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b8df3-188">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-189">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-190">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-191">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-192">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="b8df3-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-193">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-194">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-195">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-196">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-197">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-198">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-199">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-200">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-201">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-202">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="b8df3-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-203">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-204">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-205">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-206">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-207">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-208">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-209">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-210">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-211">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-212">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="b8df3-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-213">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-214">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-215">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-216">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-217">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-218">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-220">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-221">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-222">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-223">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-224">
                    <strong>Arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-225">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-226">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-227">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b8df3-228">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-230">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-231">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-232">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-233">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-234">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-235">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-236">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-237">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-238">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-239">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b8df3-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-241">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-242">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-243">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-244">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-245">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-246">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b8df3-247">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-248">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-249">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b8df3-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b8df3-251">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-252">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-253">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-254">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-255">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-256">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-257">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-258">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-259">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-260">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b8df3-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-262">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-263">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-264">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-265">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-266">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b8df3-267">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="b8df3-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b8df3-268">Tegeliku materjali arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b8df3-269">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b8df3-270">Ja</span><span class="sxs-lookup"><span data-stu-id="b8df3-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b8df3-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b8df3-272">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="b8df3-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b8df3-273">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b8df3-274">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b8df3-275">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="b8df3-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b8df3-276">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-277">Tegeliku kulu arveldamise tüüp:<strong> mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b8df3-278">Tegeliku materjali arveldamise tüüp:<strong> pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b8df3-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
