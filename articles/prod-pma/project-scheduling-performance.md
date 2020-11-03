---
title: Projekti ressursiplaanimise jõudlus
description: Selles teemas kirjeldatakse suure hulga projektide jaoks ressursside kavandamise jõudluse parandamist.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074939"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="a73da-103">Projekti ressursiplaanimise jõudlus</span><span class="sxs-lookup"><span data-stu-id="a73da-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="a73da-104">Ressursside kavandamisega seotud jõudluse probleemid võib ilmneda juhul, kui projektide arv ulatub üle tuhandete.</span><span class="sxs-lookup"><span data-stu-id="a73da-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="a73da-105">Ressursi ajastamise jõudluse parendamiseks on saadaval funktsioon, mis võimaldab kasutajatel vähendada ressursi kättesaadavuse vormi käivitamiseks kuluvat aega.</span><span class="sxs-lookup"><span data-stu-id="a73da-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="a73da-106">Täpsemalt, see eemaldab ressursi võimsuse ümberarvestuse sünkroonimise protsessi ja kasutab tabelit **ResProjectResource** ressursi otsingu kiirendamiseks.</span><span class="sxs-lookup"><span data-stu-id="a73da-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="a73da-107">Pange tähele, et tabelit **ResRollup** enam ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="a73da-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a73da-108">Kui ressursi võimsuse ümberarvestuse sünkroonimise protsessil või tabelil **ResProjectResource** on sõltuvus, ärge seda funktsiooni kasutage.</span><span class="sxs-lookup"><span data-stu-id="a73da-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a73da-109">Ressursi kavandamise jõudluse suurendamise lubamine</span><span class="sxs-lookup"><span data-stu-id="a73da-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="a73da-110">Ressursi ajastamise jõudluse suurendamise lubamiseks läbige järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="a73da-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="a73da-111">Minge jaotisse **Funktsioonidhaldus** > **Kõik** ja leidke funktsioonide loendist suvand **Luba projekti ressursi kavandamise jõudluse suurendamise funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="a73da-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a73da-112">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="a73da-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="a73da-113">Kui te ei leia loendist funktsiooni, valige loendi värskendamiseks käsk **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="a73da-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="a73da-114">Värskendage oma brauserit ja seejärel minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Projekti ressursid** > **Sünkrooni ressursi kalendrite mahutavus kõigis ettevõtetes**.</span><span class="sxs-lookup"><span data-stu-id="a73da-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="a73da-115">Määrake eelnevate andmete eemaldamiseks suvand **Olemasolevate mahutavuse kirjete eemaldamine** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a73da-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a73da-116">Kui soovite luua täiendavaid andmeid, määrake see väärtusele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="a73da-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="a73da-117">Valige väljal **Perioodi kood** ajavahemik, mille jooksul tuleks andmed luua.</span><span class="sxs-lookup"><span data-stu-id="a73da-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a73da-118">Kui valite perioodi koodi, ei pea algus-ja lõppkuupäeva määratlema.</span><span class="sxs-lookup"><span data-stu-id="a73da-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="a73da-119">Kui jätate välja **Perioodi kood** tühjaks, valige andmete loomiseks konkreetsed algus-ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="a73da-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="a73da-120">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a73da-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a73da-121">See jaotab üldandmed tabelisse **ResCalendarCapacity** kõigile teie keskkonna ettevõtetele, nii et pakett-töö tuleb käivitada ainult ühes juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="a73da-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a73da-122">Selle pakett-töö andmeid on vaja ressursi võimsuse arvutamiseks seostatud kalendri kaudu.</span><span class="sxs-lookup"><span data-stu-id="a73da-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="a73da-123">Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Projekti ressursid** > **Täida projekti ressursid kõigis ettevõtetes** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a73da-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="a73da-124">See on tabelite **ResProjectResource** , **ResCalendarDateTimeRange** ja **ResEffectiveDateTimeRange** üldandmete andmevärskenduste skript.</span><span class="sxs-lookup"><span data-stu-id="a73da-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="a73da-125">Värskendatakse ka väärtusi väljadel **PSAPRojSchedRole.RootActivity**.</span><span class="sxs-lookup"><span data-stu-id="a73da-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="a73da-126">Kui seda ei käivitata, kuvatakse teile hoiatus, kui proovite käivitada ressursside kavandamise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="a73da-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a73da-127">Ressursi kavandamise jõudluse suurendamise väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="a73da-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="a73da-128">Avage jaotis **Funktsioonidhaldus** > **Kõik** ja leidke suvand **Luba projekti ressursi kavandamise jõudluse suurendamise funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="a73da-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a73da-129">Valige funktsioon ja seejärel valige nupp **Keela**.</span><span class="sxs-lookup"><span data-stu-id="a73da-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="a73da-130">Värskendage oma brauser.</span><span class="sxs-lookup"><span data-stu-id="a73da-130">Refresh your browser.</span></span>
4. <span data-ttu-id="a73da-131">Avage jaotis **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Võimsuse sünkroonimine** > **Ressursi võimsuse sünkroonimise ümberarvestused**.</span><span class="sxs-lookup"><span data-stu-id="a73da-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="a73da-132">Määrake eelmiste andmete eemaldamiseks lehel **Võimsuse ümberarvestuse sünkroonimine** suvand **Olemasolevate võimsuse kirjete eemaldamine** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a73da-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a73da-133">Kui soovite luua täiendavaid andmeid, määrake see väärtusele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="a73da-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="a73da-134">Valige väljal **Perioodi kood** ajavahemik, mille jooksul tuleks andmed luua.</span><span class="sxs-lookup"><span data-stu-id="a73da-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a73da-135">Kui valite perioodi koodi, ei pea algus-ja lõppkuupäeva määratlema.</span><span class="sxs-lookup"><span data-stu-id="a73da-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="a73da-136">Kui jätate välja **Perioodi kood** tühjaks, valige andmete loomiseks konkreetsed algus-ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="a73da-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="a73da-137">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a73da-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a73da-138">See jaotab üldandmed tabelisse **ResRollup** kõigile teie keskkonna ettevõtetele, nii et pakett-töö tuleb käivitada ainult ühes juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="a73da-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a73da-139">Seda pakett-tööd on vaja kõigi **Ressursi saadavuse** vaadete jaoks.</span><span class="sxs-lookup"><span data-stu-id="a73da-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="a73da-140">Kui seda pakett-tööd ei käivitata, siis andmed **ResRollup** luuakse lennult, mis võib võtta aega.</span><span class="sxs-lookup"><span data-stu-id="a73da-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
