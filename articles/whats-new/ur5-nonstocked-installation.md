---
title: Project Operationsi värskendamine Finance'i keskkonnas
description: See teema sisaldab teavet selle kohta, kuidas värskendada Project Operationsi Dynamics 365 Finance'i keskkonnas.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816620"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="7e4b6-103">Project Operationsi värskendamine Finance'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="7e4b6-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="7e4b6-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="7e4b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="7e4b6-105">See teema sisaldab teavet selle kohta, kuidas värskendada rakendust Dynamics 365 Project Operations Dynamics 365 Finance'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="7e4b6-106">Project Operationsi uuendamiseks värskendusele 5 (UR5) on vaja kolme toimingut.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="7e4b6-107">Paketi importimine eelvaate projekti</span><span class="sxs-lookup"><span data-stu-id="7e4b6-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="7e4b6-108">Värskenduse rakendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="7e4b6-109">Dataverse'i keskkonna värskendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="7e4b6-110">Importige pakett oma LCS-projekti</span><span class="sxs-lookup"><span data-stu-id="7e4b6-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="7e4b6-111">Logige teenusesse [Lifecycle Services (LCS)](https://lcs.dynamics.com/) sisse projekti omaniku või keskkonna haldurina.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="7e4b6-112">Valige projektide loendist oma LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="7e4b6-113">Avage lehel **Projekt** rühmas **Keskkonnad** see keskkond, mida soovite värskendada.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="7e4b6-114">Kontrollige, et keskkond töötab.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-114">Verify that the environment is running.</span></span> <span data-ttu-id="7e4b6-115">Kui see pole käivitunud, käivitage keskkond.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="7e4b6-116">Valige jaotise **Uus väljaanne** osas **Saadaolevad värskendused** 10.0.15 nägemiseks **Vaata värskendust**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Värskenduse vaatamise nupp](media/view-update.png)

6. <span data-ttu-id="7e4b6-118">Valige lehel **Binaarsed värskendused** suvand **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="7e4b6-119">Valige lehel **Värskenduste vaatamine ja salvestamine** suvand **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="7e4b6-120">Sisestage paketi nimi avanevale paanile **Paketi salvestamine varateeki** ja seejärel valige **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="7e4b6-121">Kui LCS on paketi salvestamise lõpetanud, lubatakse nupp **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="7e4b6-122">Valige nupp **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-122">Select **Done**.</span></span> <span data-ttu-id="7e4b6-123">LCS kontrollib paketti.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-123">LCS will verify the package.</span></span> <span data-ttu-id="7e4b6-124">Kontrollimine võib võtta paar minutit või kuni ühe tunni.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="7e4b6-125">Paketi värskenduse rakendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-125">Apply the package update</span></span>

1. <span data-ttu-id="7e4b6-126">Valige LCS-is lehel **Keskkonna üksikasjad** jaotis **Haldamine** > **Värskenduste rakendamine**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="7e4b6-127">Valige loendist varem salvestatud pakett ja seejärel valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="7e4b6-128">Valige **Jah**, et kinnitada oma paketi juurutamise soov.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Paketi juurutamise dialoogikanda kinnitamine](media/confirm-package-deployment.png)

4. <span data-ttu-id="7e4b6-130">Valige **Jah**, et kinnitada oma soov rakendust värskendada.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Rakenduse värskendamise dialoogiakna kinnitamine](media/confirm-application-update.png)

<span data-ttu-id="7e4b6-132">Juurutamine ja rakenduse värskendamine algab.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="7e4b6-133">Lehe **Keskkonna üksikasjad** parempoolses ülanurgas värskendatakse keskkonna olekuks **Hooldus**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="7e4b6-134">Värskendamine lõppeb umbes kahe tunni pärast.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="7e4b6-135">Rakenduse väljalaske teave värskendatakse olekusse **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** ja keskkonna olek värskendatakse olekule **Juurutatud**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="7e4b6-136">Dataverse'i keskkonna värskendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="7e4b6-137">Logige sisse [Power Platformi halduskeskusesse](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="7e4b6-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="7e4b6-138">Otsige ja avage loendist keskkond, mida kasutasite Project Operationsi installimiseks.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="7e4b6-139">Valige lehel **Keskkonnad** jaotis **Ressurss** > **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="7e4b6-140">Otsige loendist üles **Microsoft Dynamics 365 Project Operations** ja valige veerust **Olek** väärtus **Värskendus saadaval**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="7e4b6-141">Märkige ruut **Nõustun teenusetingimustega** ja seejärel valige **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="7e4b6-142">Installitakse lahenduse uusim versioon.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="7e4b6-143">Pärast installimise lõpule viimist on teil installitud versioon 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="7e4b6-144">Uute funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="7e4b6-145">Topeltkirjutuse vastendamise lubamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-145">Enable dual-write mapping</span></span>

<span data-ttu-id="7e4b6-146">Pärast Finance'i ja Dataverse'i keskkondade värskendamise lõpule viimist saate lubada vajalikud topeltkirjutuse vastendused.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="7e4b6-147">Topletkirjutuse vastenduse lubamiseks viige lõpule järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="7e4b6-148">Turvasätete värskendamine Customer Engagementi keskkonnas</span><span class="sxs-lookup"><span data-stu-id="7e4b6-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="7e4b6-149">Andmeolemite värskendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="7e4b6-150">Topeltkirjutuse vastenduste värskendamine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="7e4b6-151">Dataverse'i keskkonna turvasätete värskendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="7e4b6-152">UR5-le värskendamise osana on nõutavad järgmised olemite turbeõiguste värskendused.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="7e4b6-153">Avage Dataverse'i keskkonnas **Sätted** ja valige rühmas **Süsteem** valik **Turve**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataversei keskkonna sätted](media/Picture21.png)

2. <span data-ttu-id="7e4b6-155">Valige suvand **Turberollid**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="7e4b6-156">Valige rollide loendist **topeltkirjutuse rakenduse kasutaja** ja valige vahekaart **Kohandatud olemid**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="7e4b6-157">Kontrollige, et rollil oleksid õigused **Lugemine** ja **Lisamine** järgmistele üksustele.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="7e4b6-158">**Valuuta vahetuskurssi tüüp**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="7e4b6-159">**Kontoplaan**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="7e4b6-160">**Finantskalender**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="7e4b6-161">**Pearaamat**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-161">**Ledger**</span></span>

5. <span data-ttu-id="7e4b6-162">Pärast turberoll värskendamist minge jaotisesse **Sätted** > **Turvalisus** > **Meeskonnad**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="7e4b6-163">Kontrollige, et meeskonnale oleks rakendatud roll **topeltkirjutuse rakenduse kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="7e4b6-164">Uuendusest andmeolemite värskendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="7e4b6-165">Avage Finance'i keskkonnas tööruum **Andmehaldus** ja seejärel avage leht **Raamistiku parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="7e4b6-166">Valige vahekaardil **Olemi sätted** suvand **Olemi loendi värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="7e4b6-167">Olemi värskendamise kinnitamiseks valige **Sulge**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7e4b6-168">Selle toimingu lõpule viimine võtab aega umbes 20 minutit.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="7e4b6-169">Teid teavitatakse, kui värskendamine on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="7e4b6-170">Topeltkirjutuse vastenduste värskendamine</span><span class="sxs-lookup"><span data-stu-id="7e4b6-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="7e4b6-171">Valige tööruumis **Andmehaldus** valik **Topeltkirjutus**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="7e4b6-172">Valige **Rakenda lahendused**, valige loendist mõlemad lahendused ja seejärel valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="7e4b6-173">Valige lehel **Topeltkirjutus** järgmised tabelivastendused ja seejärel valige **Peata**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="7e4b6-174">**Project Operationsi integratsiooni tegelikud näitajad (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="7e4b6-175">**Project Operationsi integratsiooni projekti kulukategooriad (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="7e4b6-176">**Project Operationsi integratsiooni tegelike näitajate projekti kulude ekspordi olem (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="7e4b6-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="7e4b6-177">Rakendage lehel **Tabelivastenduse versioon** vastenduse uus versioon kõigile kolmele olemile.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="7e4b6-178">Valige vastenduste taaskäivitamiseks lehel **Topeltkijutamine** käsk Käivita.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="7e4b6-179">Valige vastenduste loendist vastendus **Pearaamat (msdyn_ledgers)** koos kõige eeltingimustega ja valige märkeruut **Algne sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="7e4b6-180">Valige väljal **Alge sünkroonimise ülem** **rakendustekomplekt Finance and Operations** ja seejärel valige **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="7e4b6-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Pearaamatu vastenduse sünkroonimine](media/DW6.png)
 
