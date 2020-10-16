---
title: Uue keskkonna ettevalmistamine
description: Selles teemas antakse teavet uue Project Operationsi keskkonna ettevalmistamise kohta.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949357"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="dc2f9-103">Uue keskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="dc2f9-103">Provision a new environment</span></span>

<span data-ttu-id="dc2f9-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="dc2f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dc2f9-105">Selles teemas antakse teavet uue Dynamics 365 Project Operationsi keskkonna ettevalmistamise kohta ressursi-/mitteaktsiapõhiste stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="dc2f9-106">Project Operationsi automaatse ettevalmistamise lubamine LCS projektis</span><span class="sxs-lookup"><span data-stu-id="dc2f9-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="dc2f9-107">Kasutage järgmisi samme, et lubada Project Operationsi automaatse ettevalmistamise voog oma LCS projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="dc2f9-108">Minge jaotisse [LCS](https://lcs.dynamics.com/v2) ja valige paan **Funktsioonide halduse eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="dc2f9-109">Valige loendis **Eelvaate funktsioon** jaotis **Project Operations** ja valige Project Operationsi lubamiseks suvand **Eelvaate funktsioon lubatud**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="dc2f9-110">Seda sammu teostatakse iga LCS projekti kohta vaid ühe korra.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="dc2f9-111">Project Operationsi keskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="dc2f9-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="dc2f9-112">Avage uue Dynamics 365 Finance [eelvaatekeskkonna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) või [liivakasti-/töökeskkonna](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) juurutamine.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="dc2f9-113">Läbige **Keskkonna ettevalmistamise** viisard.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="dc2f9-114">Veenduge, et valitud rakenduse versioon on 10.0.13 või uuem.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="dc2f9-115">Project Operationsi ettevalmistamiseks valige jaotises **Täpsemad sätted** suvand **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="dc2f9-116">**Common Data Service seadistuse** lubamiseks valige **Jah** ja sisestage seejärel nõutavatele väljadele teave.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="dc2f9-117">Nimetus</span><span class="sxs-lookup"><span data-stu-id="dc2f9-117">Name</span></span>
  - <span data-ttu-id="dc2f9-118">Regioon</span><span class="sxs-lookup"><span data-stu-id="dc2f9-118">Region</span></span>
  - <span data-ttu-id="dc2f9-119">Keel</span><span class="sxs-lookup"><span data-stu-id="dc2f9-119">Language</span></span>
  - <span data-ttu-id="dc2f9-120">Valuuta</span><span class="sxs-lookup"><span data-stu-id="dc2f9-120">Currency</span></span>
 
5. <span data-ttu-id="dc2f9-121">Valige **Common Data Service malli** väljal suvand **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="dc2f9-122">Valige juurutamiseks keskkonna tüüp.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="dc2f9-123">Kordustellimusel põhinev prooviversioon võimaldab teil kasutada CDS-keskkonda 30 päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Juurutamise sätted](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="dc2f9-125">Kasutustingimuste tunnustamiseks valige suvand **Nõustun** ja seejärel valige juurutamise sätetesse naasmiseks **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Juurutuse nõusolek](./media/2DeploymentConsent.png)

7. <span data-ttu-id="dc2f9-127">Täitke viisardi ülejäänud nõutavad väljad ja kinnitage juurutus.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="dc2f9-128">Keskkonna ettevalmistamise aeg varieerub vastavalt keskkonna tüübile.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="dc2f9-129">Ettevalmistamine võib kesta kuni kuus tundi.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="dc2f9-130">Pärast juurutuse edukat lõpuleviimist kuvatakse keskkonna olekuks **Juurutatud**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="dc2f9-131">Kontrollimaks, et keskkond on edukalt juurutatud, valige **Logi sisse** ja logige kontrollimiseks keskkonda sisse.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![i keskkonna üksikasjad](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="dc2f9-133">Project Operations Finance'i demoandmete rakendamine (valikuline etapp)</span><span class="sxs-lookup"><span data-stu-id="dc2f9-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="dc2f9-134">Project Operations Finance'i demoandmete rakendamine 10.0.13 teenuseväljalaske pilvepõhisele keskkonnale, nagu on kirjeldatud [selles artiklis](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="dc2f9-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="dc2f9-135">Värskenduste rakendamine Finance'i keskkonnale</span><span class="sxs-lookup"><span data-stu-id="dc2f9-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="dc2f9-136">Project Operations nõuab Finance'i keskkonda, mille rakenduse versioon on **10.0.13 (10.0.569.20009)** või uuem.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="dc2f9-137">Võimalik, et peate selle versiooni saamiseks rakendama oma Finance'i keskkonnale kvaliteedivärskendusi.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="dc2f9-138">Valige LCS-s lehel **Keskkonna üksikasjad** jaotises **Saadaolevad värskendused** suvand **Kuva värskendus**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Kuva värskendused](./media/5ViewUpdates.png)

2. <span data-ttu-id="dc2f9-140">Valige lehel **Binaarsed värskendused** suvand **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvesta pakett](./media/6SavePackage.png)

3. <span data-ttu-id="dc2f9-142">Valige suvand **Vali kõik** ja seejärel **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-142">Click **Select all** and then select **Save package**.</span></span>

![Vaadake üle ja salvestage värskendused](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="dc2f9-144">Sisestage paketi nimi ja kirjeldus ning seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="dc2f9-145">Olenevalt Internetiühendusest, võib see protsess võtta aega.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-145">Depending on the internet connection, this process might take some time.</span></span>

![Laadiga pakett varateeki üles](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="dc2f9-147">Kui pakett on salvestatud, valige **Valmis** ja salvestage see pakett oma LCS projekti varateeki.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="dc2f9-148">Paketi salvestamine ja valideerimine võib võtta ~ 15 minutit.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="dc2f9-149">Värskenduse rakendamiseks navigeerige LCS-s lehele **Keskkonna üksikasjad** ja valige **Haldus** > **Rakenda värskendused**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Keskkondade haldamine](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="dc2f9-151">Valige värskenduste loendist oma loodud pakett ja valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Värskenduste rakendamine](./media/10ApplyUpdates.png)

<span data-ttu-id="dc2f9-153">Keskkonna teenindamine võtab aega.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-153">Environment servicing will take some time.</span></span> <span data-ttu-id="dc2f9-154">Kui see on lõpule viidud, naaseb keskkond juurutatud olekusse.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-154">After it is complete, the environment will return to a deployed state.</span></span>

![Keskkond juurutatud](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="dc2f9-156">Topeltkirjutuse ühenduse loomine</span><span class="sxs-lookup"><span data-stu-id="dc2f9-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="dc2f9-157">Minge oma LCS-i projektis lehele **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="dc2f9-158">Tehke jaotises **Common Data Service'i keskkonnateave** valik **Lingi lahendusele CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="dc2f9-159">Kui link on valmis, valige uuesti **Lingi lahendusele CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="dc2f9-160">Teid suunatakse ümber Finance'i topeltkirjutusse.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-160">You will be redirected to Dual Write in Finance.</span></span>

![Link CDS-le](./media/12LinktoCDS.png)

4. <span data-ttu-id="dc2f9-162">Valige **Rakenda lahendus**, et avada integreerimisel vastendatavad olemid.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Rakenda lahendused](./media/13ApplySolutions.png)

5. <span data-ttu-id="dc2f9-164">Valige mõlemad lahendused, **Dynamics 365 Finance and Operationsi topeltkirjutusolemi kaart** ja **Dynamics 365 Project Operationsi topeltkirjutusolemi kaardid** ja seejärel valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Lahenduste kinnitamine](./media/14ConfirmSolutions.png)

<span data-ttu-id="dc2f9-166">Pärast lahenduste rakendamist rakendatakse topeltkirjutusolemid keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Lahenduste rakendamine](./media/15ApplyingSolutions.png)

<span data-ttu-id="dc2f9-168">Pärast olemite rakendamist loetletakse keskkonnas kõik saadaolevad vastendused.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Topeltkirjutuse kaardid](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="dc2f9-170">Värskendage andmeüksused pärast värskendamist</span><span class="sxs-lookup"><span data-stu-id="dc2f9-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="dc2f9-171">Minge Finance'i tööruumi **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-171">In Finance, go to the **Data management** workspace.</span></span>

![Andmehalduse tööruum](./media/16DataManagement.png)

2. <span data-ttu-id="dc2f9-173">Valige paan **Raamistiku parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-173">Select the **Framework parameters** tile.</span></span>

![Raamistiku parameetrid](./media/17FrameworkParameters.png)

3. <span data-ttu-id="dc2f9-175">Valige lehel **Olemi sätted** suvand **Värskenda olemiloendit**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Värskenda olemiloendit](./media/18RefreshEntityList.png)

<span data-ttu-id="dc2f9-177">Värskendamine võtab aega umbes 20 minutit.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="dc2f9-178">Teile kuvatakse teade, kui see on valmis.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-178">You will receive an alert when it is complete.</span></span>

![Värskendamise kinnitamine](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="dc2f9-180">Käivitage Project Operationsi topeltkirjutuse kaardid</span><span class="sxs-lookup"><span data-stu-id="dc2f9-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="dc2f9-181">Minge oma LCS-i projektis lehele **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="dc2f9-182">Tehke jaotises **Common Data Service'i keskkonnateave** valik **Lingi lahendusele CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="dc2f9-183">Pärast lingi valimist suunatakse teid vastenduste olemite loendisse.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="dc2f9-184">Käivitage kaardid vastavalt järgmises tabelis kirjeldatule.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="dc2f9-185">Veenduge, et järgite loendis kuvatavat jada.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="dc2f9-186">**Olemikaart**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-186">**Entity Map**</span></span> | <span data-ttu-id="dc2f9-187">**Värskenda olemit**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-187">**Refresh entity**</span></span> | <span data-ttu-id="dc2f9-188">**Algne sünkroonimine**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-188">**Initial sync**</span></span> | <span data-ttu-id="dc2f9-189">**Algse sünkroonimise ülem**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-189">**Master for initial sync**</span></span> | <span data-ttu-id="dc2f9-190">**Käivita eeltingimused**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-190">**Run prerequisites**</span></span> | <span data-ttu-id="dc2f9-191">**Eeltingimuste esialgne sünkroonimine**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="dc2f9-192">**Projekti ressursside rollid kõigile ettevõtetele (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="dc2f9-193">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-193">No</span></span> | <span data-ttu-id="dc2f9-194">Ja</span><span class="sxs-lookup"><span data-stu-id="dc2f9-194">Yes</span></span> | <span data-ttu-id="dc2f9-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dc2f9-195">Common Data Service</span></span> | <span data-ttu-id="dc2f9-196">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-196">No</span></span> | <span data-ttu-id="dc2f9-197">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-197">N\A</span></span> |
| <span data-ttu-id="dc2f9-198">**Juriidilised isikud (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="dc2f9-199">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-199">No</span></span> | <span data-ttu-id="dc2f9-200">Ja</span><span class="sxs-lookup"><span data-stu-id="dc2f9-200">Yes</span></span> | <span data-ttu-id="dc2f9-201">Finance and Operationsi rakendused</span><span class="sxs-lookup"><span data-stu-id="dc2f9-201">Finance and Operations apps</span></span> | <span data-ttu-id="dc2f9-202">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-202">No</span></span> | <span data-ttu-id="dc2f9-203">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-203">N\A</span></span> |
| <span data-ttu-id="dc2f9-204">**Project Operationsi integratsiooni tegelikud näitajad (msdyn\_tegelikud)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="dc2f9-205">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-205">No</span></span> | <span data-ttu-id="dc2f9-206">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-206">No</span></span> | <span data-ttu-id="dc2f9-207">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-207">N\A</span></span> | <span data-ttu-id="dc2f9-208">Ja</span><span class="sxs-lookup"><span data-stu-id="dc2f9-208">Yes</span></span> | <span data-ttu-id="dc2f9-209">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-209">No</span></span> |
| <span data-ttu-id="dc2f9-210">**Projekti lepinguread (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="dc2f9-211">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-211">No</span></span> | <span data-ttu-id="dc2f9-212">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-212">No</span></span> | <span data-ttu-id="dc2f9-213">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-213">N\A</span></span> | <span data-ttu-id="dc2f9-214">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-214">No</span></span> | <span data-ttu-id="dc2f9-215">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-215">No</span></span> |
| <span data-ttu-id="dc2f9-216">**Projekti kande seoste integratsiooni olem (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="dc2f9-217">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-217">No</span></span> | <span data-ttu-id="dc2f9-218">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-218">No</span></span> | <span data-ttu-id="dc2f9-219">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-219">N\A</span></span> | <span data-ttu-id="dc2f9-220">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-220">No</span></span> | <span data-ttu-id="dc2f9-221">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-221">N\A</span></span> |
| <span data-ttu-id="dc2f9-222">**Project Operationsi integreerimise lepingurea vahe-eesmärgid (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="dc2f9-223">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-223">No</span></span> | <span data-ttu-id="dc2f9-224">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-224">No</span></span> | <span data-ttu-id="dc2f9-225">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-225">N\A</span></span> | <span data-ttu-id="dc2f9-226">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-226">No</span></span> | <span data-ttu-id="dc2f9-227">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-227">N\A</span></span> |
| <span data-ttu-id="dc2f9-228">**Project Operationsi integratsiooni olem kuluprognooside jaoks (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="dc2f9-229">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-229">No</span></span> | <span data-ttu-id="dc2f9-230">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-230">No</span></span> | <span data-ttu-id="dc2f9-231">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-231">N\A</span></span> | <span data-ttu-id="dc2f9-232">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-232">No</span></span> | <span data-ttu-id="dc2f9-233">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-233">N\A</span></span> |
| <span data-ttu-id="dc2f9-234">**Project Operationsi integratsiooni olem kestuse prognooside jaoks (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="dc2f9-235">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-235">No</span></span> | <span data-ttu-id="dc2f9-236">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-236">No</span></span> | <span data-ttu-id="dc2f9-237">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-237">N\A</span></span> | <span data-ttu-id="dc2f9-238">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-238">No</span></span> | <span data-ttu-id="dc2f9-239">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-239">N\A</span></span> |
| <span data-ttu-id="dc2f9-240">**Project Operationsi integreerimise projekti kulude ekspordi olem (msdyn\_kulud)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="dc2f9-241">Ja</span><span class="sxs-lookup"><span data-stu-id="dc2f9-241">Yes</span></span> | <span data-ttu-id="dc2f9-242">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-242">No</span></span> | <span data-ttu-id="dc2f9-243">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-243">N\A</span></span> | <span data-ttu-id="dc2f9-244">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-244">No</span></span> | <span data-ttu-id="dc2f9-245">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-245">N\A</span></span> |
| <span data-ttu-id="dc2f9-246">**Project Operationsi integratsiooni olem kestuse prognooside jaoks (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="dc2f9-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="dc2f9-247">Ja</span><span class="sxs-lookup"><span data-stu-id="dc2f9-247">Yes</span></span> | <span data-ttu-id="dc2f9-248">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-248">No</span></span> | <span data-ttu-id="dc2f9-249">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-249">N\A</span></span> | <span data-ttu-id="dc2f9-250">No</span><span class="sxs-lookup"><span data-stu-id="dc2f9-250">No</span></span> | <span data-ttu-id="dc2f9-251">Puudub</span><span class="sxs-lookup"><span data-stu-id="dc2f9-251">N\A</span></span> |

4. <span data-ttu-id="dc2f9-252">Olemi värskendamiseks valige vastenduse nimi ja seejärel valige **Värskenda olemid**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="dc2f9-253">Jätkake vastenduse käitamisega pärast värskendamise lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-253">Proceed with running the map after the refresh is complete.</span></span>

![Kaardi värskendamine](./media/20RefreshMapping.png)

<span data-ttu-id="dc2f9-255">Enne järgmise vastenduse lubamist veenduge, et tabelis olev kaart oleks olekus **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="dc2f9-256">Suurema hulga eeltingimustega kaartide käitamine võib võtta aega.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="dc2f9-257">Eeltingimustega kaartide käivitamiseks lubage ümberlülitusnupp **Kuva seostuvad olemikaardid**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="dc2f9-258">Kui tabel näitab, et **Eeltingimuste esialgne sünkroonimine** on **Ei**, veenduge, et lipp **Esialgne sünkroonimine** oleks enne käivitamist kõigil eeltingimuse kaartidel **Väljas**.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Käita kaart](./media/21RunMap.png)

6. <span data-ttu-id="dc2f9-260">Kontrollige, et kõik projektiga seotud kaardid oleksid töötavad olekus.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-260">Validate all project related maps are in the running state.</span></span>

![Kõik kaardid töötavad](./media/22AllMapsRunning.png)

<span data-ttu-id="dc2f9-262">Teie Project Operationsi keskkond on nüüd ettevalmistatud ja konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="dc2f9-262">Your Project Operations environment is now provisioned and configured.</span></span>
