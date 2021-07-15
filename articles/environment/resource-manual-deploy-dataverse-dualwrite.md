---
title: Rakenduse Project Operations Dataverse käsitsi juurutamine koos topeltkirjutuse toega
description: Selles teemas selgitatakse, kuidas rakendust Project Operations Dataverse käsitsi juurutada, et see toetaks topeltkirjutamist.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274003"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="ac2d6-103">Rakenduse Project Operations Dataverse käsitsi juurutamine koos topeltkirjutuse toega</span><span class="sxs-lookup"><span data-stu-id="ac2d6-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="ac2d6-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="ac2d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ac2d6-105">Selles teemas selgitatakse, kuidas juurutada käsitsi rakendust Microsoft Dynamics 365 Project Operations teenuses Microsoft Dataverse, et see toetaks topeltkirjutamist.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="ac2d6-106">Project Operations tuvastab keskkonna konfiguratsiooni ja lisab eeltingimuste täitumisel topeltkirjutamise lisatoe.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="ac2d6-107">Kui olete teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu juurutamise ajal järginud selles teemas toodud juhiseid, saate Microsoft Power Platformi integratsiooni juurutamise (varem tuntud kui Common Data Service keskkond) vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="ac2d6-108">Project Operationsi teenuses Dataverse juurutamise protsess, et see toetaks topeltkirjutust, omab nelja peamist etappi.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="ac2d6-109">[Looge teenuses Dataverse uus keskkond, mis toetab topeltkirjutust](#create).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="ac2d6-110">[Lisage keskkonnale topeltkirjutuse eeltingimused](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="ac2d6-111">[Lisage rakendus Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="ac2d6-112">[Siduge oma keskkonnad](#link).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="ac2d6-113">Teenuses Dataverse uue keskkonna loomine, mis toetab topeltkirjutust</span><span class="sxs-lookup"><span data-stu-id="ac2d6-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="ac2d6-114">Selle toimingu lõpuleviimiseks peate administraatorina sisse logima.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="ac2d6-115">Avage [Power Platformi halduskeskus](https://admin.powerplatform.com) ja logige administraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="ac2d6-116">Looge uus keskkond ja pange sellele nimi.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="ac2d6-117">Valige keskkonna tüüp.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-117">Select the environment type.</span></span> <span data-ttu-id="ac2d6-118">Kui registreerusite prooviversiooni jaoks, valige **Prooviversioon (kordustellimusel põhinev)**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="ac2d6-119">Kinnitage juurutuspiirkond.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="ac2d6-120">Lubage suvand **Loo selle keskkonna joaks andmebaas**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="ac2d6-121">Kinnitage keel ja seejärel kontrollige, kas valuuta ühtib teie rakenduste Finance and Operations valuutaga.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="ac2d6-122">Lubage suvand **Dynamics 365 rakendused** ja veenduge, et välja **Juuruta need rakendused automaatselt** väärtuseks oleks seatud **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="ac2d6-123">Lisage turberühm, kui turberühm on nõutav.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="ac2d6-124">Keskkonna loomiseks valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="ac2d6-125">Oodake, kuni juurutamine on lõpule jõudnud ja keskkond jõuab olekusse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="ac2d6-126">Keskkonnale topeltkirjutuse eeltingimuste lisamine</span><span class="sxs-lookup"><span data-stu-id="ac2d6-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="ac2d6-127">Topeltkirjutuse tugi sisaldab lisavälju, mis põhiolemitele lisatakse, näiteks olem **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="ac2d6-128">Kui lisate olemasolevasse keskkonda topeltkirjutamise toe, peate võib-olla toe lubamiseks andmeid värskendama.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="ac2d6-129">Lisateavet andmete alglaadimise kohta vaadake teemast [Ettevõtte andmete alglaadimine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="ac2d6-130">Lisateavet topeltkirjutamise kohta vaadake teemast [Topeltkirjutamise süsteemi nõuded](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="ac2d6-131">Viige see toiming lõpule, et lisada oma keskkonda topeltkirjutuse eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="ac2d6-132">Avage äsja loodud keskkond ja avage seejärel **Ressurss** \> **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="ac2d6-133">Valige rakenduste loendist **Topeltkirjutuse tuumlahendus** ja installige see.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="ac2d6-134">Oodake, kuni installimine on lõpule jõudnud.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-134">Wait until the installation is completed.</span></span> <span data-ttu-id="ac2d6-135">Seejärel valige rakenduste loendist **Topeltkirjutuse rakendamise korraldamise lahendus** ja installige see.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="ac2d6-136">Rakenduse Project Operations Dataverse lisamine</span><span class="sxs-lookup"><span data-stu-id="ac2d6-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="ac2d6-137">Selle toimingu saate teha ainult juhul, kui olete enne Project Operationsi installimist teinud eelnevad toimingud.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="ac2d6-138">Installimise ajal analüüsib süsteem keskkonna konfiguratsiooni ja lisab vajaduse korral topeltkirjutuse toe.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="ac2d6-139">Avage varem loodud keskkond ja avage seejärel **Ressurss** \> **Dynamics 365 rakendused**.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="ac2d6-140">Valige rakenduste loendist **Microsoft Dynamics 365 Project Operations** ja installige see.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="ac2d6-141">Keskkondade sidumine</span><span class="sxs-lookup"><span data-stu-id="ac2d6-141">Link your environments</span></span>

<span data-ttu-id="ac2d6-142">Pärast Dataverse’i keskkonna juurutamist saate häälestada oma Finance and Operationsi rakendustes seose.</span><span class="sxs-lookup"><span data-stu-id="ac2d6-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="ac2d6-143">Järgige juhiseid teemas [Oma keskkondade sidumiseks topeltkirjutuse viisardi kasutamine](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="ac2d6-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
