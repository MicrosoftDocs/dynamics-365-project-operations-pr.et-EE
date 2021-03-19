---
title: Projekti ajasisestuse mobiilne tööruum
description: Selles teemas kirjeldatakse, kuidas kasutada Projecti ajakirjete mobiilset tööruumi. See tööruum võimaldab kasutajatel oma mobiilsideseadme kaudu sisestada ja salvestada aega projekti jaoks.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288869"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="281cd-104">Projekti ajasisestuse mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="281cd-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="281cd-105">Selles teemas kirjeldatakse, kuidas kasutada **Projecti ajakirjete** mobiilset tööruumi.</span><span class="sxs-lookup"><span data-stu-id="281cd-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="281cd-106">See tööruum võimaldab kasutajatel oma mobiilsideseadme kaudu sisestada ja salvestada aega projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="281cd-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="281cd-107">See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="281cd-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="281cd-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="281cd-108">Overview</span></span>
<span data-ttu-id="281cd-109">Igapäevase töö osana on projekti ressursid sageli kohapeal või reisivad.</span><span class="sxs-lookup"><span data-stu-id="281cd-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="281cd-110">**Projekti ajakirje** mobiilne tööruum võimaldab kasutajatel sisestada enda poolt valitud mobiilsideseadmel oma arveldatav ja mitte-arveldatav aeg projekti kohta.</span><span class="sxs-lookup"><span data-stu-id="281cd-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="281cd-111">Seega saavad projekti ressursid salvestada ajakandeid igal ajal ja kõikjal.</span><span class="sxs-lookup"><span data-stu-id="281cd-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="281cd-112">Nad saavad vaadata ka juba salvestatud ajakirjeid.</span><span class="sxs-lookup"><span data-stu-id="281cd-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="281cd-113">Täpsemalt saavad kasutajad teha mobiilses tööruumis **Projekti ajakirje** teha järgmisi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="281cd-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="281cd-114">Sisestada mis tahes valitud kuupäeva jaoks mõne kindla toimingu jaoks kulutatud tundide arvu.</span><span class="sxs-lookup"><span data-stu-id="281cd-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="281cd-115">Otsida projekti nime või kliendi alusel, et leida aja sisestamiseks projekt.</span><span class="sxs-lookup"><span data-stu-id="281cd-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="281cd-116">Määrata kulutatud aja kategooria ja tegevus.</span><span class="sxs-lookup"><span data-stu-id="281cd-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="281cd-117">Salvestada aeg projekti jaoks arveldatavaks või mitte-arveldatavaks.</span><span class="sxs-lookup"><span data-stu-id="281cd-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="281cd-118">Vajaduse korral sisestada kõik välised ja sisemised kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="281cd-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="281cd-119">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="281cd-119">Prerequisites</span></span>
<span data-ttu-id="281cd-120">Eeltingimused erinevad sõltuvalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonile.</span><span class="sxs-lookup"><span data-stu-id="281cd-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="281cd-121">Eeltingimused, kui kasutate rakendust Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="281cd-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="281cd-122">Kui teie organisatsiooni jaoks on juurutatud Finance, peab süsteemiadministraator avaldama **Projecti aja sisestamise** mobiilse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="281cd-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="281cd-123">Juhiseid vaadake teemast [Mobiilse tööruumi avaldamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="281cd-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="281cd-124">Eeltingimused kui kasutate versiooni 1611 koos Platformi värskendusega 3 või hilisemaga</span><span class="sxs-lookup"><span data-stu-id="281cd-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="281cd-125">Kui teie organisatsioonis on juurutatud versioon 1611 koos Platformi uuendusega 3 või hilisemaga, peab süsteemiadministraator lõpule viima järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="281cd-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="281cd-126">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="281cd-126">Prerequisite</span></span></th>
<th><span data-ttu-id="281cd-127">Roll</span><span class="sxs-lookup"><span data-stu-id="281cd-127">Role</span></span></th>
<th><span data-ttu-id="281cd-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="281cd-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="281cd-129">KB 4018050 rakendamine.</span><span class="sxs-lookup"><span data-stu-id="281cd-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="281cd-130">Süsteemihaldur</span><span class="sxs-lookup"><span data-stu-id="281cd-130">System administrator</span></span></td>
<td><span data-ttu-id="281cd-131">KB 4018050 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Projecti ajakirje</strong></span><span class="sxs-lookup"><span data-stu-id="281cd-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="281cd-132">KB 4018050 rakendamiseks peab teie süsteemiadministraator järgima järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="281cd-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="281cd-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige metaandmete kiirparandus alla portaalist Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="281cd-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="281cd-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installige metaandmete kiirparandus</a>.</span><span class="sxs-lookup"><span data-stu-id="281cd-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="281cd-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Looge juurutatav pakett</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ja seejärel laadige LCS-i üles juurutatav pakett.</span><span class="sxs-lookup"><span data-stu-id="281cd-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="281cd-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</span><span class="sxs-lookup"><span data-stu-id="281cd-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="281cd-137">Avaldage <strong>Projecti ajakirje</strong> mobiilne tööruum.</span><span class="sxs-lookup"><span data-stu-id="281cd-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="281cd-138">Süsteemihaldur</span><span class="sxs-lookup"><span data-stu-id="281cd-138">System administrator</span></span></td>
<td><span data-ttu-id="281cd-139">Vt <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="281cd-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="281cd-140">Mobiilirakenduse allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="281cd-140">Download and install the mobile app</span></span>

<span data-ttu-id="281cd-141">Mobiilirakenduse Finance and Operations allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="281cd-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="281cd-142">Androidi telefonidele</span><span class="sxs-lookup"><span data-stu-id="281cd-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="281cd-143">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="281cd-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="281cd-144">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="281cd-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="281cd-145">Käivitage oma mobiilsideseadmes rakendus.</span><span class="sxs-lookup"><span data-stu-id="281cd-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="281cd-146">Sisestage oma Dynamics 365 URL.</span><span class="sxs-lookup"><span data-stu-id="281cd-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="281cd-147">Esmakordsel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="281cd-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="281cd-148">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="281cd-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="281cd-149">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="281cd-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="281cd-150">Pange tähele, et kui teie süsteemiadministraator avaldab uue tööruumi hiljem, tuleb teil mobiilsete tööruumide loendit värskendada.</span><span class="sxs-lookup"><span data-stu-id="281cd-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="281cd-151">[![Tõmbeliigutusega värskendamine](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="281cd-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="281cd-152">Sisestage aeg, kasutades Projecti ajakirje mobiilset tööruumi</span><span class="sxs-lookup"><span data-stu-id="281cd-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="281cd-153">Valige oma mobiilsideseadmes tööruum **Projekti aja sisestamise**.</span><span class="sxs-lookup"><span data-stu-id="281cd-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="281cd-154">Valige **Aja sisestus**.</span><span class="sxs-lookup"><span data-stu-id="281cd-154">Select **Time entry**.</span></span> <span data-ttu-id="281cd-155">Näidatud on selle jooksva nädala kalendri kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="281cd-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="281cd-156">Valige valitud kuupäeval suvand **Toimingud**&gt;**Uus kirje**.</span><span class="sxs-lookup"><span data-stu-id="281cd-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="281cd-157">Sisestage salvestatavate tundide arv.</span><span class="sxs-lookup"><span data-stu-id="281cd-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="281cd-158">Valige ajakirje jaoks projekt.</span><span class="sxs-lookup"><span data-stu-id="281cd-158">Select the project for the time entry.</span></span> <span data-ttu-id="281cd-159">Loendis on toodud projektid, mis on laaditud rakendusse võrguühenduseta kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="281cd-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="281cd-160">Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="281cd-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="281cd-161">Lisateavet vt: [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="281cd-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="281cd-162">Kui teie projekti loendis pole, valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="281cd-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="281cd-163">Otsige nime järgi või vahetage projekti nime või kliendi järgi otsingule.</span><span class="sxs-lookup"><span data-stu-id="281cd-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="281cd-164">Valige kategooria.</span><span class="sxs-lookup"><span data-stu-id="281cd-164">Select a category.</span></span> <span data-ttu-id="281cd-165">Loendis on toodud kategooriad, mis on laaditud rakendusse võrguühenduseta kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="281cd-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="281cd-166">Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="281cd-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="281cd-167">Lisateavet vt: [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="281cd-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="281cd-168">Kui teie kategooriat loendis pole, valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="281cd-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="281cd-169">Otsige kategooria järgi või vahetage kategooria nime järgi otsingule.</span><span class="sxs-lookup"><span data-stu-id="281cd-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="281cd-170">Valige tegevus.</span><span class="sxs-lookup"><span data-stu-id="281cd-170">Select an activity.</span></span> <span data-ttu-id="281cd-171">Loendis on toodud tegevused, mis on laaditud rakendusse võrguühenduseta kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="281cd-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="281cd-172">Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="281cd-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="281cd-173">Lisateavet vt: [Mobiilne platvorm](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="281cd-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="281cd-174">Kui teie tegevust loendis pole, valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="281cd-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="281cd-175">Otsige tegevuse numbri järgi või vahetage otsingule eesmärgi põhjal.</span><span class="sxs-lookup"><span data-stu-id="281cd-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="281cd-176">Valige rea atribuut.</span><span class="sxs-lookup"><span data-stu-id="281cd-176">Select the line property.</span></span>
12. <span data-ttu-id="281cd-177">Valikuline: sisestage kõik välised ja sisemised kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="281cd-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="281cd-178">Valige nupp **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="281cd-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]