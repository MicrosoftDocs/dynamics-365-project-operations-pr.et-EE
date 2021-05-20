---
title: Uue keskkonna ettevalmistamine
description: Selles teemas antakse teavet uue Project Operationsi keskkonna ettevalmistamise kohta.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950529"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="5e5d5-103">Uue keskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="5e5d5-103">Provision a new environment</span></span>

<span data-ttu-id="5e5d5-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="5e5d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5e5d5-105">Selles teemas antakse teavet selle kohta, kuidas juurutada uut rakenduse Dynamics 365 Project Operations keskkonda ressursi-/mittelaopõhiste stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="5e5d5-106">Project Operationsi automaatse ettevalmistamise lubamine LCS projektis</span><span class="sxs-lookup"><span data-stu-id="5e5d5-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="5e5d5-107">Kasutage järgmisi samme, et lubada Project Operationsi automaatse ettevalmistamise voog oma LCS projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="5e5d5-108">Minge jaotisse [LCS](https://lcs.dynamics.com/v2) ja valige paan **Funktsioonide halduse eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="5e5d5-109">Valige loendis **Eelvaate funktsioon** jaotis **Project Operationsi funktsioon** ja valige Project Operationsi lubamiseks suvand **Eelvaate funktsioon lubatud**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="5e5d5-110">Seda sammu teostatakse iga LCS projekti kohta vaid ühe korra.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="5e5d5-111">Project Operationsi keskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="5e5d5-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="5e5d5-112">Avage uue Dynamics 365 Finance [eelvaatekeskkonna](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) või [liivakasti-/töökeskkonna](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) juurutamine.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="5e5d5-113">Läbige **Keskkonna ettevalmistamise** viisard.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="5e5d5-114">Veenduge, et valitud rakenduse versioon on 10.0.13 või uuem.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="5e5d5-115">Project Operationsi ettevalmistamiseks valige jaotises **Täpsemad sätted** suvand **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="5e5d5-116">**Common Data Service seadistuse** lubamiseks valige **Jah** ja sisestage seejärel nõutavatele väljadele teave.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="5e5d5-117">Nimetus</span><span class="sxs-lookup"><span data-stu-id="5e5d5-117">Name</span></span>
  - <span data-ttu-id="5e5d5-118">Regioon</span><span class="sxs-lookup"><span data-stu-id="5e5d5-118">Region</span></span>
  - <span data-ttu-id="5e5d5-119">Keel</span><span class="sxs-lookup"><span data-stu-id="5e5d5-119">Language</span></span>
  - <span data-ttu-id="5e5d5-120">Valuuta</span><span class="sxs-lookup"><span data-stu-id="5e5d5-120">Currency</span></span>
 
5. <span data-ttu-id="5e5d5-121">Valige **Common Data Service malli** väljal suvand **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="5e5d5-122">Valige juurutamiseks keskkonna tüüp.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="5e5d5-123">Kordustellimusel põhinev prooviversioon võimaldab teil kasutada CDS-keskkonda 30 päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Juurutamise sätted](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="5e5d5-125">Kasutustingimuste tunnustamiseks valige suvand **Nõustun** ja seejärel valige juurutamise sätetesse naasmiseks **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Juurutuse nõusolek](./media/2DeploymentConsent.png)

7. <span data-ttu-id="5e5d5-127">Valikuline – demoandmete rakendamine keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="5e5d5-128">Avage **Täpsemad sätted**, valige **SQL-andmebaasi konfiguratsiooni kohandamine** ja määrake üksuse **Määrake rakenduse andmebaasile andmekomplekt** olekuks **Demo**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="5e5d5-129">Täitke viisardi ülejäänud nõutavad väljad ja kinnitage juurutus.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="5e5d5-130">Keskkonna ettevalmistamise aeg oleneb keskkonna tüübist.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="5e5d5-131">Ettevalmistamine võib kesta kuni kuus tundi.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="5e5d5-132">Pärast juurutuse edukat lõpuleviimist kuvatakse keskkonna olekuks **Juurutatud**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="5e5d5-133">Kui soovite veenduda, et keskkond on edukalt juurutatud, valige kinnitamiseks käsk **Logi sisse** ja logige keskkonda sisse.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![i keskkonna üksikasjad](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="5e5d5-135">Värskenduste rakendamine Finance'i keskkonnale</span><span class="sxs-lookup"><span data-stu-id="5e5d5-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="5e5d5-136">Project Operations nõuab Finance'i keskkonda, mille rakenduse versioon on **10.0.13 (10.0.569.20009)** või uuem.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="5e5d5-137">Võimalik, et peate selle versiooni saamiseks rakendama oma Finance'i keskkonnale kvaliteedivärskendusi.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="5e5d5-138">Valige LCS-s lehel **Keskkonna üksikasjad** jaotises **Saadaolevad värskendused** suvand **Kuva värskendus**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Kuva värskendused](./media/5ViewUpdates.png)

2. <span data-ttu-id="5e5d5-140">Valige lehel **Binaarsed värskendused** suvand **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvesta pakett](./media/6SavePackage.png)

3. <span data-ttu-id="5e5d5-142">Valige suvand **Vali kõik** ja seejärel **Salvesta pakett**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-142">Click **Select all** and then select **Save package**.</span></span>

![Vaadake üle ja salvestage värskendused](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="5e5d5-144">Sisestage paketi nimi ja kirjeldus ning seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="5e5d5-145">Olenevalt Internetiühendusest, võib see protsess võtta aega.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-145">Depending on the internet connection, this process might take some time.</span></span>

![Laadiga pakett varateeki üles](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="5e5d5-147">Kui pakett on salvestatud, valige **Valmis** ja salvestage see pakett oma LCS projekti varateeki.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="5e5d5-148">Paketi salvestamine ja valideerimine võib võtta ~ 15 minutit.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="5e5d5-149">Värskenduse rakendamiseks navigeerige LCS-s lehele **Keskkonna üksikasjad** ja valige **Haldus** > **Rakenda värskendused**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Keskkondade haldamine](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="5e5d5-151">Valige värskenduste loendist oma loodud pakett ja valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Värskenduste rakendamine](./media/10ApplyUpdates.png)

<span data-ttu-id="5e5d5-153">Keskkonna teenindamine võtab aega.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-153">Environment servicing will take some time.</span></span> <span data-ttu-id="5e5d5-154">Kui see on lõpule viidud, naaseb keskkond juurutatud olekusse.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-154">After it is complete, the environment will return to a deployed state.</span></span>

![Keskkond juurutatud](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="5e5d5-156">Topeltkirjutuse ühenduse loomine</span><span class="sxs-lookup"><span data-stu-id="5e5d5-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="5e5d5-157">Minge oma LCS-i projektis lehele **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5e5d5-158">Tehke jaotises **Common Data Service'i keskkonnateave** valik **Lingi lahendusele CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="5e5d5-159">Kui link on valmis, valige uuesti **Lingi lahendusele CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="5e5d5-160">Teid suunatakse ümber Finance'i topeltkirjutusse.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-160">You will be redirected to Dual Write in Finance.</span></span>

![Link CDS-le](./media/12LinktoCDS.png)

4. <span data-ttu-id="5e5d5-162">Valige **Rakenda lahendus**, et avada integreerimisel vastendatavad olemid.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Rakenda lahendused](./media/13ApplySolutions.png)

5. <span data-ttu-id="5e5d5-164">Valige mõlemad lahendused, **Rakenduse Dynamics 365 Finance and Operations topeltkirjutamise olemikaart** ja **Rakenduse Dynamics 365 Project Operations topeltkirjutamise olemikaardid** ja valige seejärel suvand **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Lahenduste kinnitamine](./media/14ConfirmSolutions.png)

<span data-ttu-id="5e5d5-166">Pärast lahenduste rakendamist rakendatakse topeltkirjutusolemid keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Lahenduste rakendamine](./media/15ApplyingSolutions.png)

<span data-ttu-id="5e5d5-168">Pärast olemite rakendamist loetletakse keskkonnas kõik saadaolevad vastendused.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Topeltkirjutuse kaardid](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="5e5d5-170">Värskendage andmeüksused pärast värskendamist</span><span class="sxs-lookup"><span data-stu-id="5e5d5-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="5e5d5-171">Minge Finance'i tööruumi **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-171">In Finance, go to the **Data management** workspace.</span></span>

![Andmehalduse tööruum](./media/16DataManagement.png)

2. <span data-ttu-id="5e5d5-173">Valige paan **Raamistiku parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-173">Select the **Framework parameters** tile.</span></span>

![Raamistiku parameetrid](./media/17FrameworkParameters.png)

3. <span data-ttu-id="5e5d5-175">Valige lehel **Olemi sätted** suvand **Värskenda olemiloendit**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Värskenda olemiloendit](./media/18RefreshEntityList.png)

<span data-ttu-id="5e5d5-177">Värskendamine võtab aega umbes 20 minutit.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="5e5d5-178">Teile kuvatakse teade, kui see on valmis.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-178">You will receive an alert when it is complete.</span></span>

![Värskendamise kinnitamine](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="5e5d5-180">Project Operationsi turbesätete värskendamine Dataverse'is</span><span class="sxs-lookup"><span data-stu-id="5e5d5-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="5e5d5-181">Avage Project Operations oma Dataverse'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="5e5d5-182">Avage **Sätted** > **Turve** > **Turberollid**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="5e5d5-183">Valige lehe **Turberollid** rollide loendist **topeltkirjutuse rakenduse kasutaja** ja valige vahekaart **Kohandatud olemid**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="5e5d5-184">Kontrollige, et rollil oleksid õigused **Lugemine** ja **Lisamine** järgmistele üksustele.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="5e5d5-185">**Valuuta vahetuskurssi tüüp**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="5e5d5-186">**Kontoplaan**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="5e5d5-187">**Finantskalender**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="5e5d5-188">**Pearaamat**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-188">**Ledger**</span></span>

5. <span data-ttu-id="5e5d5-189">Pärast turberolli värskendamist avage **Sätted** > **Turvalisus** > **Meeskonnad** ja valige meeskonna vaates **Kohalik äriüksuse omanik** vaikemeeskond.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="5e5d5-190">Valige **Halda rolle** ja kontrollige, et meeskonnale on rakendatud turbeõigus **topeltkirjutuse rakenduse kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="5e5d5-191">Käivitage Project Operationsi topeltkirjutuse kaardid</span><span class="sxs-lookup"><span data-stu-id="5e5d5-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="5e5d5-192">Minge oma LCS-i projektis lehele **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="5e5d5-193">Tehke jaotises **Common Data Service'i keskkonnateave** valik **Lingi lahendusele CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="5e5d5-194">Pärast lingi valimist suunatakse teid vastenduste olemite loendisse.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="5e5d5-195">Käivitage kaardid vastavalt järgmises tabelis kirjeldatule.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="5e5d5-196">Veenduge, et järgite loendis kuvatavat jada.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="5e5d5-197">**Olemikaart**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-197">**Entity Map**</span></span> | <span data-ttu-id="5e5d5-198">**Värskenda olemit**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-198">**Refresh entity**</span></span> | <span data-ttu-id="5e5d5-199">**Algne sünkroonimine**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-199">**Initial sync**</span></span> | <span data-ttu-id="5e5d5-200">**Algse sünkroonimise ülem**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-200">**Master for initial sync**</span></span> | <span data-ttu-id="5e5d5-201">**Käivita eeltingimused**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-201">**Run prerequisites**</span></span> | <span data-ttu-id="5e5d5-202">**Eeltingimuste esialgne sünkroonimine**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="5e5d5-203">**Projekti ressursside rollid kõigile ettevõtetele (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="5e5d5-204">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-204">No</span></span> | <span data-ttu-id="5e5d5-205">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-205">Yes</span></span> | <span data-ttu-id="5e5d5-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5e5d5-206">Common Data Service</span></span> | <span data-ttu-id="5e5d5-207">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-207">No</span></span> | <span data-ttu-id="5e5d5-208">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-208">N\A</span></span> |
| <span data-ttu-id="5e5d5-209">**Juriidilised isikud (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="5e5d5-210">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-210">No</span></span> | <span data-ttu-id="5e5d5-211">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-211">Yes</span></span> | <span data-ttu-id="5e5d5-212">Finance and Operationsi rakendused</span><span class="sxs-lookup"><span data-stu-id="5e5d5-212">Finance and Operations apps</span></span> | <span data-ttu-id="5e5d5-213">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-213">No</span></span> | <span data-ttu-id="5e5d5-214">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-214">N\A</span></span> |
| <span data-ttu-id="5e5d5-215">**Pearaamat (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="5e5d5-216">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-216">No</span></span> | <span data-ttu-id="5e5d5-217">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-217">Yes</span></span> | <span data-ttu-id="5e5d5-218">Finance and Operationsi rakendused</span><span class="sxs-lookup"><span data-stu-id="5e5d5-218">Finance and Operations apps</span></span> | <span data-ttu-id="5e5d5-219">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-219">Yes</span></span> | <span data-ttu-id="5e5d5-220">Jah, teenuse Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="5e5d5-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="5e5d5-221">**Project Operationsi integratsiooni tegelikud näitajad (msdyn\_tegelikud)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="5e5d5-222">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-222">No</span></span> | <span data-ttu-id="5e5d5-223">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-223">No</span></span> | <span data-ttu-id="5e5d5-224">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-224">N\A</span></span> | <span data-ttu-id="5e5d5-225">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-225">Yes</span></span> | <span data-ttu-id="5e5d5-226">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-226">No</span></span> |
| <span data-ttu-id="5e5d5-227">**Projekti lepinguread (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="5e5d5-228">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-228">No</span></span> | <span data-ttu-id="5e5d5-229">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-229">No</span></span> | <span data-ttu-id="5e5d5-230">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-230">N\A</span></span> | <span data-ttu-id="5e5d5-231">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-231">No</span></span> | <span data-ttu-id="5e5d5-232">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-232">No</span></span> |
| <span data-ttu-id="5e5d5-233">**Projekti kande seoste integratsiooni olem (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="5e5d5-234">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-234">No</span></span> | <span data-ttu-id="5e5d5-235">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-235">No</span></span> | <span data-ttu-id="5e5d5-236">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-236">N\A</span></span> | <span data-ttu-id="5e5d5-237">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-237">No</span></span> | <span data-ttu-id="5e5d5-238">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-238">N\A</span></span> |
| <span data-ttu-id="5e5d5-239">**Project Operationsi integreerimise lepingurea vahe-eesmärgid (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="5e5d5-240">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-240">No</span></span> | <span data-ttu-id="5e5d5-241">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-241">No</span></span> | <span data-ttu-id="5e5d5-242">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-242">N\A</span></span> | <span data-ttu-id="5e5d5-243">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-243">No</span></span> | <span data-ttu-id="5e5d5-244">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-244">N\A</span></span> |
| <span data-ttu-id="5e5d5-245">**Project Operationsi integratsiooni olem kuluprognooside jaoks (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="5e5d5-246">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-246">No</span></span> | <span data-ttu-id="5e5d5-247">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-247">No</span></span> | <span data-ttu-id="5e5d5-248">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-248">N\A</span></span> | <span data-ttu-id="5e5d5-249">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-249">No</span></span> | <span data-ttu-id="5e5d5-250">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-250">N\A</span></span> |
| <span data-ttu-id="5e5d5-251">**Project Operationsi integreerimise projekti kulukategooriate ekspordi olem (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="5e5d5-252">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-252">No</span></span> | <span data-ttu-id="5e5d5-253">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-253">No</span></span> | <span data-ttu-id="5e5d5-254">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-254">N\A</span></span> | <span data-ttu-id="5e5d5-255">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-255">No</span></span> | <span data-ttu-id="5e5d5-256">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-256">N\A</span></span> |
| <span data-ttu-id="5e5d5-257">**Project Operationsi integreerimise projekti kulude ekspordi olem (msdyn\_kulud)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="5e5d5-258">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-258">Yes</span></span> | <span data-ttu-id="5e5d5-259">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-259">No</span></span> | <span data-ttu-id="5e5d5-260">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-260">N\A</span></span> | <span data-ttu-id="5e5d5-261">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-261">No</span></span> | <span data-ttu-id="5e5d5-262">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-262">N\A</span></span> |
| <span data-ttu-id="5e5d5-263">**Project Operationsi integratsiooni olem kestuse prognooside jaoks (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="5e5d5-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="5e5d5-264">Ja</span><span class="sxs-lookup"><span data-stu-id="5e5d5-264">Yes</span></span> | <span data-ttu-id="5e5d5-265">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-265">No</span></span> | <span data-ttu-id="5e5d5-266">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-266">N\A</span></span> | <span data-ttu-id="5e5d5-267">No</span><span class="sxs-lookup"><span data-stu-id="5e5d5-267">No</span></span> | <span data-ttu-id="5e5d5-268">Puudub</span><span class="sxs-lookup"><span data-stu-id="5e5d5-268">N\A</span></span> |


4. <span data-ttu-id="5e5d5-269">Olemi värskendamiseks valige vastenduse nimi ja seejärel valige **Värskenda olemid**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Kaardi värskendamine](./media/20RefreshMapping.png)

5. <span data-ttu-id="5e5d5-271">Pärast värskenduse lõpetamist käivitage vastendus.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="5e5d5-272">Enne järgmise vastenduse lubamist veenduge, et tabelis olev kaart oleks olekus **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="5e5d5-273">Suurema hulga eeltingimustega kaartide käitamine võib võtta aega.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="5e5d5-274">Eeltingimustega kaartide käivitamiseks lubage ümberlülitusnupp **Kuva seostuvad olemikaardid**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="5e5d5-275">Kui tabel näitab, et **Eeltingimuste esialgne sünkroonimine** on **Ei**, veenduge, et lipp **Esialgne sünkroonimine** oleks enne käivitamist kõigil eeltingimuse kaartidel **Väljas**.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Käita kaart](./media/21RunMap.png)

6. <span data-ttu-id="5e5d5-277">Kontrollige, et kõik projektiga seotud kaardid oleksid töötavad olekus.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-277">Validate all project related maps are in the running state.</span></span>

![Kõik kaardid töötavad](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="5e5d5-279">CDS-is konfiguratsiooniandmete rakendamine rakenduses Project Operations (valikuline)</span><span class="sxs-lookup"><span data-stu-id="5e5d5-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="5e5d5-280">Kui olete rakenduse Finance keskkonnale rakendanud demoandmeid, lugege jaotist [Teenuse Common Data Service rakenduses Project Operations konfiguratsiooniandmete seadistamine ja rakendamine](resource-apply-pro-setup-config-data.md), et rakendada CDS-i keskkonnale demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="5e5d5-281">Teie Project Operationsi keskkond on nüüd ettevalmistatud ja konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="5e5d5-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]