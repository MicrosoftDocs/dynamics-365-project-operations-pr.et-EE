---
title: Projektipõhise lepingurea arveldatavate komponentide konfigureerimine
description: Selles teemas antakse teavet selle kohta, kuidas lisada Project Operationsis lepinguridadele arveldatavaid komponente.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858468"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="efffc-103">Projektipõhise lepingurea arveldatavate komponentide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="efffc-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="efffc-104">_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="efffc-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="efffc-105">Projektipõhine lepingurida *sisaldas* komponente ja *arveldatavaid* komponente.</span><span class="sxs-lookup"><span data-stu-id="efffc-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="efffc-106">Kaasatud komponendid on komponendid, mis kuuluvad:</span><span class="sxs-lookup"><span data-stu-id="efffc-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="efffc-107">Arveldusmeetod ja kliendi jaotamine</span><span class="sxs-lookup"><span data-stu-id="efffc-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="efffc-108">Mitteületatavad limiidid</span><span class="sxs-lookup"><span data-stu-id="efffc-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="efffc-109">Projektipõhise lepingurea määratletud arve sageduse sätted</span><span class="sxs-lookup"><span data-stu-id="efffc-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="efffc-110">Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="efffc-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="efffc-111">Väli **Arveldamise tüüp** on seatud, mis võimaldab lepingurea kontekstis järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="efffc-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="efffc-112">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-112">Chargeable</span></span>
  - <span data-ttu-id="efffc-113">Mittearveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-113">Non-chargeable</span></span>

<span data-ttu-id="efffc-114">Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.</span><span class="sxs-lookup"><span data-stu-id="efffc-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="efffc-115">Arveldatav tegevus määratletakse projekti lepingurea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele.</span><span class="sxs-lookup"><span data-stu-id="efffc-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="efffc-116">Kui lepingurea väli **Kaasa tööülesanded** on tühi või seatud väärtusele **Kogu projekt**, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.</span><span class="sxs-lookup"><span data-stu-id="efffc-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="efffc-117">Projekti lepingurea rollidele määratud arveldatavuse kehtib ainult tehingu klassile **Aeg**.</span><span class="sxs-lookup"><span data-stu-id="efffc-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="efffc-118">Kui lepingurea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.</span><span class="sxs-lookup"><span data-stu-id="efffc-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="efffc-119">Projekti lepingurea tehingu kategooriate määratud arveldatavuse kehtib ainult tehingu klassile **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="efffc-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="efffc-120">Kui väli **Kaasa kulu** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.</span><span class="sxs-lookup"><span data-stu-id="efffc-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="efffc-121">Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="efffc-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="efffc-122">Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla lepingurea kohta, mis võimaldab järgmist seadistust.</span><span class="sxs-lookup"><span data-stu-id="efffc-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="efffc-123">Kui projektipõhine lepingurida sisaldab väärtust **Aeg** ja teatud ülesannet, siis seostatakse väärtust **T1** sellega kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="efffc-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="efffc-124">Kui olemas on teine lepingurida, mis sisaldab väärtust **Kulu**, saate seostada lepingurea väärtuse T1 tööülesannet sellega kui arveldatav.</span><span class="sxs-lookup"><span data-stu-id="efffc-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="efffc-125">Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.</span><span class="sxs-lookup"><span data-stu-id="efffc-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="efffc-126">Ülesande arveldamise tüübi saab konfigureerida lepingurea vahekaardil **Arveldatavad ülesanded**, värskendades lepingurea ülesannete andmeruudustikus välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="efffc-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="efffc-127">Teise võimalusena saate värskendada välja **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud kontaktiridu.</span><span class="sxs-lookup"><span data-stu-id="efffc-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="efffc-128">Rolli värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="efffc-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="efffc-129">Roll võib olla arveldatav või mittearveldatav kindla lepingurea kohta.</span><span class="sxs-lookup"><span data-stu-id="efffc-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="efffc-130">Rolli arveldamise tüüpi saab konfigureerida lepingurea vahekaardil **Arveldatavad rollid**.</span><span class="sxs-lookup"><span data-stu-id="efffc-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="efffc-131">Selleks värskendage andmeruudustikus **Arveldatavad rollid** välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="efffc-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="efffc-132">Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks</span><span class="sxs-lookup"><span data-stu-id="efffc-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="efffc-133">Tehingu kategooria võib olla arveldatav või mittearveldatav kindla lepingurea kohta.</span><span class="sxs-lookup"><span data-stu-id="efffc-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="efffc-134">Tehingu arveldamise tüüpi saab konfigureerida projektipõhise lepingurea vahekaardil **Arveldatavad kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="efffc-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="efffc-135">Selleks värskendage andmeruudustikus **Arveldatavad kategooriad** välja **Arveldamise tüüp**.</span><span class="sxs-lookup"><span data-stu-id="efffc-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="efffc-136">Arveldatavuse lahendamine</span><span class="sxs-lookup"><span data-stu-id="efffc-136">Resolve chargeability</span></span>

<span data-ttu-id="efffc-137">Aja jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="efffc-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="efffc-138">**Aeg** lisatakse lepingureale.</span><span class="sxs-lookup"><span data-stu-id="efffc-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="efffc-139">**Roll** on lepingureal konfigureeritud kui tasustatav.</span><span class="sxs-lookup"><span data-stu-id="efffc-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="efffc-140">**Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="efffc-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="efffc-141">Kui need kolm asja on täidetud, konfigureeritakse ülesanne tasustavana.</span><span class="sxs-lookup"><span data-stu-id="efffc-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="efffc-142">Kulu jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="efffc-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="efffc-143">**Kulu** lisatakse lepingureale</span><span class="sxs-lookup"><span data-stu-id="efffc-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="efffc-144">**Tehingukategooria** on lepingureal konfigureeritud kui tasustatav</span><span class="sxs-lookup"><span data-stu-id="efffc-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="efffc-145">**Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanne**</span><span class="sxs-lookup"><span data-stu-id="efffc-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="efffc-146">Kui need kolm asja on täidetud, konfigureeritakse **Ülesanne** tasustavana.</span><span class="sxs-lookup"><span data-stu-id="efffc-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="efffc-147">Materjali jaoks loodud prognoos või tegelik näitaja loetakse arveldatavaks järgmisel juhul.</span><span class="sxs-lookup"><span data-stu-id="efffc-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="efffc-148">**Materjalid** lisatakse lepingureale</span><span class="sxs-lookup"><span data-stu-id="efffc-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="efffc-149">**Kaasatud ülesanded** on lepingureal seatud valikule **Valitud ülesanded**</span><span class="sxs-lookup"><span data-stu-id="efffc-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="efffc-150">Kui need kaks asja on täidetud, konfigureeritakse **Ülesanne** tasustavana.</span><span class="sxs-lookup"><span data-stu-id="efffc-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-151">
                    <strong>Kaasab aja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="efffc-152">
                    <strong>Kaasab kulu</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="efffc-153">
                    <strong>Sisaldab materjale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="efffc-154">
                    <strong>Kaasatud ülesanded</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-155">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-156">
                    <strong>Kategooria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-157">
                    <strong>Toiming</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="efffc-158">
                    <strong>Tasustatavuse mõju</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-159">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-160">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-161">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-162">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-163">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-164">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-165">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-166">Tegeliku aja arveldamine: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-167">Tegeliku kulu arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-168">Tegeliku materjali arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-169">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-170">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-171">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-172">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efffc-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-173">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-174">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-175">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-176">Tegeliku aja arveldamine: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-177">Tegeliku kulu arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-178">Tegeliku materjali arveldamise tüüp: <strong>arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-179">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-180">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-181">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-182">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efffc-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-183">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-184">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-185">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-186">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-187">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efffc-188">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-189">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-190">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-191">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-192">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efffc-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-193">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-194">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-195">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-196">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-197">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-198">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-199">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-200">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-201">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-202">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efffc-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-203">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-204">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-205">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-206">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-207">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-208">Tegeliku materjali arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-209">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-210">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-211">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-212">Ainult valitud ülesanded</span><span class="sxs-lookup"><span data-stu-id="efffc-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-213">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-214">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-215">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-216">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-217">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-218">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-220">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-221">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-222">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-223">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-224">
                    <strong>Arveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-225">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-226">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-227">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efffc-228">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-230">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-231">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-232">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-233">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-234">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-235">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-236">Tegeliku aja arveldamine: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-237">Tegeliku kulu arveldamise tüüp: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-238">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-239">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="efffc-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-241">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-242">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-243">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-244">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-245">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-246">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efffc-247">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-248">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-249">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="efffc-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="efffc-251">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-252">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-253">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-254">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-255">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-256">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-257">Tegeliku kulu arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-258">Tegeliku materjali arveldamise tüüp: arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-259">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-260">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="efffc-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-262">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-263">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-264">Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-265">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-266">Tegeliku aja arveldamine: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efffc-267">Tegeliku kulu arveldamise tüüp: Arveldatav</span><span class="sxs-lookup"><span data-stu-id="efffc-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="efffc-268">Tegeliku materjali arveldamise tüüp: <strong>pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="efffc-269">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="efffc-270">Ja</span><span class="sxs-lookup"><span data-stu-id="efffc-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="efffc-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="efffc-272">Kogu projekt</span><span class="sxs-lookup"><span data-stu-id="efffc-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="efffc-273">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="efffc-274">
                    <strong>Mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="efffc-275">Ei saa seadistada</span><span class="sxs-lookup"><span data-stu-id="efffc-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="efffc-276">Tegeliku aja arveldamine: <strong>mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-277">Tegeliku kulu arveldamise tüüp:<strong> mittearveldatav</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="efffc-278">Tegeliku materjali arveldamise tüüp:<strong> pole saadaval</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efffc-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
