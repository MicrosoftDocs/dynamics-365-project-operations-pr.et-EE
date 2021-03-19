---
title: Microsoft Project Clienti integreerimine
description: Projekti ajakava kavandamine ja haldamine võib olla keeruline, seega peavad projektijuhid kasutama tööriistu, mis aitavad neil seda tööülesannet hallata. Integreerimine rakendusega Microsoft Project Client pakub tuge projekti tööjaotuse struktuuri avamiseks ja haldamiseks.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289319"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="34ce5-104">Microsoft Project Clienti integreerimine</span><span class="sxs-lookup"><span data-stu-id="34ce5-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34ce5-105">Projekti ajakava kavandamine ja haldamine võib olla keeruline, seega peavad projektijuhid kasutama tööriistu, mis aitavad neil seda tööülesannet hallata.</span><span class="sxs-lookup"><span data-stu-id="34ce5-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="34ce5-106">Integreerimine rakendusega Microsoft Project Client pakub tuge projekti tööjaotuse struktuuri avamiseks ja haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="34ce5-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="34ce5-107">Projektijuht saab avaldada kõik muudatused uuesti rakenduse Dynamics 365 Finance projekti tööjaotuse struktuuris.</span><span class="sxs-lookup"><span data-stu-id="34ce5-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="34ce5-108">Kui kasutate juuli värskendust (versioon 10.0.4), peate installima versioonid KB 4054797 ja 4055884.</span><span class="sxs-lookup"><span data-stu-id="34ce5-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="34ce5-109">Lisandmooduli Microsoft Project Client konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="34ce5-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="34ce5-110">Rakendusega Microsoft Project Client integreerimise lubamiseks peab lisandmoodul Microsoft Dynamics 365 olema installitud kasutaja kliendi rakendusse Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="34ce5-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="34ce5-111">Seda saab teha, kui avada **Projektihalduse tööruum**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="34ce5-112">•   Klõpsake valikut **Konfigureeri projekti kliendi lisandmoodul** tööruumi jaotises **Lingid** > **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="34ce5-113">•   Klõpsake valikut **Ava**, seejärel klõpsake käsku **Käivita**, kui teilt seda küsitakse.</span><span class="sxs-lookup"><span data-stu-id="34ce5-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="34ce5-114">Olemasoleva mustandi tööjaotuse struktuuri avamine ja redigeerimine Microsoft Project Clientis</span><span class="sxs-lookup"><span data-stu-id="34ce5-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="34ce5-115">Kui projekti jaoks on rakenduses Dynamics 365 Finance tööjaotuse struktuur loodud, saab tööjaotuse struktuuri avada rakenduses Microsoft Project Client, kui tööjaotuse struktuur on mustandi olekus.</span><span class="sxs-lookup"><span data-stu-id="34ce5-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="34ce5-116">Lehelt **Projekt** avamiseks klõpsake linki **Ava rakenduses Microsoft Project** vahekaardil **Plaanimine**. Selle lehe saab avada ka rakenduse Microsoft Project Client seest, klõpsates käsku **Ava** vahekaardil **Microsoft Dynamics 365**. Valige loendist **Juriidiline üksus** ja **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="34ce5-117">Kui kasutate brauserina Internet Explorerit, peate klõpsama nuppu **Salvesta**, et avada käsitsi kohast, kuhu fail on alla laaditud.</span><span class="sxs-lookup"><span data-stu-id="34ce5-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="34ce5-118">Või klõpsake nuppu **Salvesta ja ava**, et avada fail rakenduses Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="34ce5-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="34ce5-119">Ärge nimetage faili salvestamise ajal ümber.</span><span class="sxs-lookup"><span data-stu-id="34ce5-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="34ce5-120">Enne failis mis tahes muudatuste tegemist rakendust Microsoft Project Client kasutades peate selle välja registreerima. Klõpsake valikut **Registreeri välja** vahekaardil **Microsoft Dynamics 365**. See takistab teistel kasutajatel redigeerida samaaegselt tööjaotuse struktuuri rakendusest Finance.</span><span class="sxs-lookup"><span data-stu-id="34ce5-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="34ce5-121">Pärast mis tahes muudatuste tegemist tööjaotuse struktuuri avaldamiseks klõpsake valikut **Registreeri sisse** vahekaardil **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="34ce5-122">Kui projektile on rakenduses Finance juba projekti meeskond lisatud, täidetakse ressursi loend meeskonnaliikmetega.</span><span class="sxs-lookup"><span data-stu-id="34ce5-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="34ce5-123">Kui projekti meeskonda pole veel projektile lisatud, saate valida ressursid ja luua meeskonna rakenduse Microsoft Project Client seest, klõpsates nuppu **Ressursid** vahekaardil **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="34ce5-124">Sisseregistreerimise protsessi osana sünkroonitakse Finance’i järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="34ce5-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="34ce5-125">•   Ülesande nimi</span><span class="sxs-lookup"><span data-stu-id="34ce5-125">•   Task name</span></span>

<span data-ttu-id="34ce5-126">•   Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="34ce5-126">•   Start date</span></span>

<span data-ttu-id="34ce5-127">•   Lõpukuupäev</span><span class="sxs-lookup"><span data-stu-id="34ce5-127">•   Finish date</span></span>

<span data-ttu-id="34ce5-128">•   Eelkäijad</span><span class="sxs-lookup"><span data-stu-id="34ce5-128">•   Predecessors</span></span>

<span data-ttu-id="34ce5-129">•   Ressursside nimed</span><span class="sxs-lookup"><span data-stu-id="34ce5-129">•   Resource names</span></span>

<span data-ttu-id="34ce5-130">•   Kategooria</span><span class="sxs-lookup"><span data-stu-id="34ce5-130">•   Category</span></span>

<span data-ttu-id="34ce5-131">•   Ressursi kategooria</span><span class="sxs-lookup"><span data-stu-id="34ce5-131">•   Resource category</span></span>

<span data-ttu-id="34ce5-132">•   Tööaeg</span><span class="sxs-lookup"><span data-stu-id="34ce5-132">•   Work hours</span></span>

<span data-ttu-id="34ce5-133">•   Märkmed</span><span class="sxs-lookup"><span data-stu-id="34ce5-133">•   Notes</span></span>

<span data-ttu-id="34ce5-134">•   Prioriteet</span><span class="sxs-lookup"><span data-stu-id="34ce5-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="34ce5-135">Kui lisate oma rakenduse Microsoft Project Client failile mõne muu veeru, siis neid ei salvestata faili ja ei kuvata, kui fail uuesti avatakse.</span><span class="sxs-lookup"><span data-stu-id="34ce5-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="34ce5-136">Rakendust Microsoft Project Client kasutades olemasolevale projektile tööjaotuse struktuuri loomine</span><span class="sxs-lookup"><span data-stu-id="34ce5-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="34ce5-137">Rakendust Microsoft Project Client kasutades uue tööjaotuse struktuuri loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="34ce5-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="34ce5-138">Avage Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="34ce5-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="34ce5-139">Vahekaardil **Microsoft Dynamics 365** klõpsake käsku **Ava**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="34ce5-140">Valige projekti jaoks **Juriidiline üksus**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="34ce5-141">Valige **Project**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="34ce5-142">Klõpsake valikut **Registreeri välja** vahekaardil **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="34ce5-143">Kui olete valmis rakendust Finance avaldama, klõpsake **Registreeri sisse** vahekaardil **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="34ce5-144">Rakendust Microsoft Project Client kasutades olemasoleva projekti olemasoleva tööjaotuse struktuuri asendamine</span><span class="sxs-lookup"><span data-stu-id="34ce5-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="34ce5-145">Uue tööjaotuse struktuuri loomiseks rakendust Microsoft Project Client kasutades ja olemasoleva tööjaotuse struktuuri asendamine olemasoleva projekti jaoks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="34ce5-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="34ce5-146">Avage Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="34ce5-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="34ce5-147">Looge rakenduses Microsoft Project Client ajakava.</span><span class="sxs-lookup"><span data-stu-id="34ce5-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="34ce5-148">Vahekaardil **Microsoft Dynamics 365** klõpsake valikut **Salvesta muudatused** > **Olemasoleva projekti asendamine**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="34ce5-149">Valige projekti jaoks **Juriidiline üksus**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="34ce5-150">Valige **Project**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="34ce5-151">Klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="34ce5-152">Uue projekti loomine rakendusest Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="34ce5-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="34ce5-153">Avage Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="34ce5-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="34ce5-154">Looge rakenduses Microsoft Project Client ajakava.</span><span class="sxs-lookup"><span data-stu-id="34ce5-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="34ce5-155">Vahekaardil **Microsoft Dynamics 365** klõpsake valikut **Salvesta muudatused** > **Salvesta uude projekti**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="34ce5-156">Valige projekti jaoks **Juriidiline üksus**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="34ce5-157">Vajaduse korral sisestage **Projekti ID**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="34ce5-158">Sisestage **Projekti nimi**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="34ce5-159">Valige suvandid **Projekti tüüp**, **Projekti rühm** ja **Projekti kontakti ID**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="34ce5-160">Teise võimalusena saate luua uue projekti lepingu, klõpsates valikud **Uus**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="34ce5-161">Valige ressurssidega kasutamiseks suvand **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="34ce5-162">Klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="34ce5-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]