---
title: Projekti ajasisestuse mobiilne tööruum
description: Selles teemas kirjeldatakse, kuidas kasutada Projecti ajakirjete mobiilset tööruumi. See tööruum võimaldab kasutajatel oma mobiilsideseadme kaudu sisestada ja salvestada aega projekti jaoks.
author: KimANelson
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
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750977"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="c8298-104">Projekti ajasisestuse mobiilne tööruum</span><span class="sxs-lookup"><span data-stu-id="c8298-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8298-105">Selles teemas kirjeldatakse, kuidas kasutada **Projecti ajakirjete** mobiilset tööruumi.</span><span class="sxs-lookup"><span data-stu-id="c8298-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="c8298-106">See tööruum võimaldab kasutajatel oma mobiilsideseadme kaudu sisestada ja salvestada aega projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="c8298-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="c8298-107">See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="c8298-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="c8298-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c8298-108">Overview</span></span>
<span data-ttu-id="c8298-109">Igapäevase töö osana on projekti ressursid sageli kohapeal või reisivad.</span><span class="sxs-lookup"><span data-stu-id="c8298-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="c8298-110">**Projekti ajakirje** mobiilne tööruum võimaldab kasutajatel sisestada enda poolt valitud mobiilsideseadmel oma arveldatav ja mitte-arveldatav aeg projekti kohta.</span><span class="sxs-lookup"><span data-stu-id="c8298-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="c8298-111">Seega saavad projekti ressursid salvestada ajakandeid igal ajal ja kõikjal.</span><span class="sxs-lookup"><span data-stu-id="c8298-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="c8298-112">Nad saavad vaadata ka juba salvestatud ajakirjeid.</span><span class="sxs-lookup"><span data-stu-id="c8298-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="c8298-113">Täpsemalt saavad kasutajad teha mobiilses tööruumis **Projekti ajakirje** teha järgmisi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="c8298-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="c8298-114">Sisestada mis tahes valitud kuupäeva jaoks mõne kindla toimingu jaoks kulutatud tundide arvu.</span><span class="sxs-lookup"><span data-stu-id="c8298-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="c8298-115">Otsida projekti nime või kliendi alusel, et leida aja sisestamiseks projekt.</span><span class="sxs-lookup"><span data-stu-id="c8298-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="c8298-116">Määrata kulutatud aja kategooria ja tegevus.</span><span class="sxs-lookup"><span data-stu-id="c8298-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="c8298-117">Salvestada aeg projekti jaoks arveldatavaks või mitte-arveldatavaks.</span><span class="sxs-lookup"><span data-stu-id="c8298-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="c8298-118">Vajaduse korral sisestada kõik välised ja sisemised kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="c8298-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8298-119">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c8298-119">Prerequisites</span></span>
<span data-ttu-id="c8298-120">Eeltingimused erinevad sõltuvalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonile.</span><span class="sxs-lookup"><span data-stu-id="c8298-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="c8298-121">Eeltingimused, kui kasutate rakendust Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="c8298-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="c8298-122">Kui teie organisatsiooni jaoks on juurutatud Finance, peab süsteemiadministraator avaldama **Projecti aja sisestamise** mobiilse tööruumi.</span><span class="sxs-lookup"><span data-stu-id="c8298-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="c8298-123">Juhiseid vaadake teemast [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="c8298-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="c8298-124">Eeltingimused kui kasutate versiooni 1611 koos Platformi värskendusega 3 või hilisemaga</span><span class="sxs-lookup"><span data-stu-id="c8298-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="c8298-125">Kui teie organisatsioonis on juurutatud versioon 1611 koos Platformi uuendusega 3 või hilisemaga, peab süsteemiadministraator lõpule viima järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="c8298-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8298-126">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="c8298-126">Prerequisite</span></span></th>
<th><span data-ttu-id="c8298-127">Roll</span><span class="sxs-lookup"><span data-stu-id="c8298-127">Role</span></span></th>
<th><span data-ttu-id="c8298-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c8298-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="c8298-129">KB 4018050 rakendamine.</span><span class="sxs-lookup"><span data-stu-id="c8298-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="c8298-130">Süsteemihaldur</span><span class="sxs-lookup"><span data-stu-id="c8298-130">System administrator</span></span></td>
<td><span data-ttu-id="c8298-131">KB 4018050 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Projecti ajakirje</strong></span><span class="sxs-lookup"><span data-stu-id="c8298-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="c8298-132">KB 4018050 rakendamiseks peab teie süsteemiadministraator järgima järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c8298-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="c8298-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige metaandmete kiirparandus alla portaalist Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="c8298-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="c8298-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installige metaandmete kiirparandus</a>.</span><span class="sxs-lookup"><span data-stu-id="c8298-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="c8298-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looge juurutatav pakett</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ja seejärel laadige LCS-i üles juurutatav pakett.</span><span class="sxs-lookup"><span data-stu-id="c8298-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="c8298-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</span><span class="sxs-lookup"><span data-stu-id="c8298-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8298-137">Avaldage <strong>Projecti ajakirje</strong> mobiilne tööruum.</span><span class="sxs-lookup"><span data-stu-id="c8298-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="c8298-138">Süsteemihaldur</span><span class="sxs-lookup"><span data-stu-id="c8298-138">System administrator</span></span></td>
<td><span data-ttu-id="c8298-139">Vt <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</span><span class="sxs-lookup"><span data-stu-id="c8298-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="c8298-140">Mobiilirakenduse allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="c8298-140">Download and install the mobile app</span></span>

<span data-ttu-id="c8298-141">Mobiilirakenduse Finance and Operations allalaadimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="c8298-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="c8298-142">Androidi telefonidele</span><span class="sxs-lookup"><span data-stu-id="c8298-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="c8298-143">iPhone’idele</span><span class="sxs-lookup"><span data-stu-id="c8298-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="c8298-144">Logige mobiilirakendusse sisse</span><span class="sxs-lookup"><span data-stu-id="c8298-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="c8298-145">Käivitage oma mobiilsideseadmes rakendus.</span><span class="sxs-lookup"><span data-stu-id="c8298-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="c8298-146">Sisestage oma Dynamics 365 URL.</span><span class="sxs-lookup"><span data-stu-id="c8298-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="c8298-147">Esmakordsel sisselogimisel küsitakse teilt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="c8298-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="c8298-148">Sisestage oma identimisteave.</span><span class="sxs-lookup"><span data-stu-id="c8298-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="c8298-149">Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid.</span><span class="sxs-lookup"><span data-stu-id="c8298-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="c8298-150">Pange tähele, et kui teie süsteemiadministraator avaldab uue tööruumi hiljem, tuleb teil mobiilsete tööruumide loendit värskendada.</span><span class="sxs-lookup"><span data-stu-id="c8298-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="c8298-151">[![Tõmbeliigutusega värskendamine](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="c8298-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="c8298-152">Sisestage aeg, kasutades Projecti ajakirje mobiilset tööruumi</span><span class="sxs-lookup"><span data-stu-id="c8298-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="c8298-153">Valige oma mobiilsideseadmes tööruum **Projekti aja sisestamise**.</span><span class="sxs-lookup"><span data-stu-id="c8298-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="c8298-154">Valige **Aja sisestus**.</span><span class="sxs-lookup"><span data-stu-id="c8298-154">Select **Time entry**.</span></span> <span data-ttu-id="c8298-155">Näidatud on selle jooksva nädala kalendri kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="c8298-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="c8298-156">Valige valitud kuupäeval suvand **Toimingud**&gt;**Uus kirje**.</span><span class="sxs-lookup"><span data-stu-id="c8298-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="c8298-157">Sisestage salvestatavate tundide arv.</span><span class="sxs-lookup"><span data-stu-id="c8298-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="c8298-158">Valige ajakirje jaoks projekt.</span><span class="sxs-lookup"><span data-stu-id="c8298-158">Select the project for the time entry.</span></span> <span data-ttu-id="c8298-159">Loendis on toodud projektid, mis on laaditud rakendusse võrguühenduseta kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c8298-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="c8298-160">Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="c8298-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="c8298-161">Lisateavet vt: [Mobiilne platvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="c8298-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="c8298-162">Kui teie projekti loendis pole, valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="c8298-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="c8298-163">Otsige nime järgi või vahetage projekti nime või kliendi järgi otsingule.</span><span class="sxs-lookup"><span data-stu-id="c8298-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="c8298-164">Valige kategooria.</span><span class="sxs-lookup"><span data-stu-id="c8298-164">Select a category.</span></span> <span data-ttu-id="c8298-165">Loendis on toodud kategooriad, mis on laaditud rakendusse võrguühenduseta kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c8298-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="c8298-166">Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="c8298-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="c8298-167">Lisateavet vt: [Mobiilne platvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="c8298-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="c8298-168">Kui teie kategooriat loendis pole, valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="c8298-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="c8298-169">Otsige kategooria järgi või vahetage kategooria nime järgi otsingule.</span><span class="sxs-lookup"><span data-stu-id="c8298-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="c8298-170">Valige tegevus.</span><span class="sxs-lookup"><span data-stu-id="c8298-170">Select an activity.</span></span> <span data-ttu-id="c8298-171">Loendis on toodud tegevused, mis on laaditud rakendusse võrguühenduseta kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c8298-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="c8298-172">Vaikimisi laaditakse 50 üksust, kuid arendaja saab seda numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="c8298-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="c8298-173">Lisateavet vt: [Mobiilne platvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="c8298-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="c8298-174">Kui teie tegevust loendis pole, valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="c8298-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="c8298-175">Otsige tegevuse numbri järgi või vahetage otsingule eesmärgi põhjal.</span><span class="sxs-lookup"><span data-stu-id="c8298-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="c8298-176">Valige rea atribuut.</span><span class="sxs-lookup"><span data-stu-id="c8298-176">Select the line property.</span></span>
12. <span data-ttu-id="c8298-177">Valikuline: sisestage kõik välised ja sisemised kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="c8298-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="c8298-178">Valige nupp **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="c8298-178">Select **Done**.</span></span>
