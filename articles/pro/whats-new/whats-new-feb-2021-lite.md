---
title: Mis on uut, veebruaris 2021 – Project Operations Lite juurutamine
description: See teema sisaldab teavet Project Operations Lite’i juurutuse 2021. aasta veebruari väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bfc4c622c423e689938e58666ae47abbe3c23d48
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141304"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a><span data-ttu-id="1817a-103">Mis on uut, veebruaris 2021 – Project Operations Lite juurutamine</span><span class="sxs-lookup"><span data-stu-id="1817a-103">What's new February 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="1817a-104">See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="1817a-104">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

  - <span data-ttu-id="1817a-105">Project Operations Dataverse’i keskkonna versioonis 4.7.0.95</span><span class="sxs-lookup"><span data-stu-id="1817a-105">Project Operations on Dataverse environment version 4.7.0.95</span></span>

## <a name="quality-updates"></a><span data-ttu-id="1817a-106">Kvaliteedi värskendused</span><span class="sxs-lookup"><span data-stu-id="1817a-106">Quality updates</span></span>

| <span data-ttu-id="1817a-107">**Funktsiooni ala**</span><span class="sxs-lookup"><span data-stu-id="1817a-107">**Feature Area**</span></span> | <span data-ttu-id="1817a-108">**Viitenumber**</span><span class="sxs-lookup"><span data-stu-id="1817a-108">**Reference number**</span></span> | <span data-ttu-id="1817a-109">**Kvaliteedi värskendus**</span><span class="sxs-lookup"><span data-stu-id="1817a-109">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1817a-110">**Arveldamine ja hinnakujundus**</span><span class="sxs-lookup"><span data-stu-id="1817a-110">**Billing and Pricing**</span></span> | <span data-ttu-id="1817a-111">2053736</span><span class="sxs-lookup"><span data-stu-id="1817a-111">2053736</span></span> | <span data-ttu-id="1817a-112">Arverea üksikasjad on nüüd juurdepääsetav jaotises **Arve** > **Arvega seotud teave**.</span><span class="sxs-lookup"><span data-stu-id="1817a-112">Invoice line details are now accessible by going to **Invoice** > **Related information**.</span></span> |
| <span data-ttu-id="1817a-113">**Arveldamine ja hinnakujundus**</span><span class="sxs-lookup"><span data-stu-id="1817a-113">**Billing and Pricing**</span></span> | <span data-ttu-id="1817a-114">2122613</span><span class="sxs-lookup"><span data-stu-id="1817a-114">2122613</span></span> | <span data-ttu-id="1817a-115">Toimingud **Aktiveeri** ja **Deaktiveeri** eemaldati **Hinnakirja** seose olemitelt.</span><span class="sxs-lookup"><span data-stu-id="1817a-115">The **Activate** and **Deactivate** actions were removed from the **Price List** association entities.</span></span> |
| <span data-ttu-id="1817a-116">**Arveldamine ja hinnakujundus**</span><span class="sxs-lookup"><span data-stu-id="1817a-116">**Billing and Pricing**</span></span> | <span data-ttu-id="1817a-117">2128606</span><span class="sxs-lookup"><span data-stu-id="1817a-117">2128606</span></span> | <span data-ttu-id="1817a-118">Lahendatud on probleem tõrkega **ullReferenceException** lisandmoodulis **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="1817a-118">Resolved the issue with **ullReferenceException** in the **GetEstimatesForProject** plug-in.</span></span> |
| <span data-ttu-id="1817a-119">**Juurutamine ja konfiguratsioon**</span><span class="sxs-lookup"><span data-stu-id="1817a-119">**Deployment and configuration**</span></span> | <span data-ttu-id="1817a-120">2140569</span><span class="sxs-lookup"><span data-stu-id="1817a-120">2140569</span></span> | <span data-ttu-id="1817a-121">Projekti lahendus ei tohi olla installitud Dataverse'i meeskondade keskkondadesse.</span><span class="sxs-lookup"><span data-stu-id="1817a-121">Project solution must not be installed in the Dataverse Teams environments.</span></span> |
| <span data-ttu-id="1817a-122">**Juurutamine ja konfiguratsioon**</span><span class="sxs-lookup"><span data-stu-id="1817a-122">**Deployment and configuration**</span></span> | <span data-ttu-id="1817a-123">2086991</span><span class="sxs-lookup"><span data-stu-id="1817a-123">2086991</span></span> | <span data-ttu-id="1817a-124">Veebiressursside piiratud kohandamise lokaliseerimine.</span><span class="sxs-lookup"><span data-stu-id="1817a-124">Restricted customizing localization of web resources.</span></span> |
| <span data-ttu-id="1817a-125">**Müügivõimaluse haldus**</span><span class="sxs-lookup"><span data-stu-id="1817a-125">**Opportunity Management**</span></span> | <span data-ttu-id="1817a-126">2136794</span><span class="sxs-lookup"><span data-stu-id="1817a-126">2136794</span></span> | <span data-ttu-id="1817a-127">Saate kuvada õige tõrketeate, kui protsess **Arve kinnitamine** või **Arve tasutuks märkimine** nurjub.</span><span class="sxs-lookup"><span data-stu-id="1817a-127">Display correct error message when **Confirm invoice** or **Mark invoice as paid** process fails,</span></span> |
| <span data-ttu-id="1817a-128">**Müügivõimaluse haldus**</span><span class="sxs-lookup"><span data-stu-id="1817a-128">**Opportunity Management**</span></span> | <span data-ttu-id="1817a-129">2146376</span><span class="sxs-lookup"><span data-stu-id="1817a-129">2146376</span></span> | <span data-ttu-id="1817a-130">Arve kinnituselt luuakse parandatud maksusumma mittearveldatavad tegelikus näitajas.</span><span class="sxs-lookup"><span data-stu-id="1817a-130">Corrected tax amount in a non-chargeable actual is created from invoice confirmation.</span></span> |
| <span data-ttu-id="1817a-131">**Projekti plaanimine ja jälgimine**</span><span class="sxs-lookup"><span data-stu-id="1817a-131">**Project Planning and Tracking**</span></span> | <span data-ttu-id="1817a-132">2099879</span><span class="sxs-lookup"><span data-stu-id="1817a-132">2099879</span></span> | <span data-ttu-id="1817a-133">Dataverse'i keskkonna juurutamine peab looma tehingu vaikekategooria koos staatilise ID-ga ja mitte seda juhuslikult keskkonna kohta looma.</span><span class="sxs-lookup"><span data-stu-id="1817a-133">The Dataverse environment deployment must create a default transaction category with a static ID and not randomly generate one per environment.</span></span> |
| <span data-ttu-id="1817a-134">**Projekti plaanimine ja jälgimine**</span><span class="sxs-lookup"><span data-stu-id="1817a-134">**Project Planning and Tracking**</span></span> | <span data-ttu-id="1817a-135">2128577</span><span class="sxs-lookup"><span data-stu-id="1817a-135">2128577</span></span> | <span data-ttu-id="1817a-136">Parandatud on Project Service'i kasutajaõigused tehingu kategooria värskendamiseks ressursi määramisel.</span><span class="sxs-lookup"><span data-stu-id="1817a-136">Fixed the Project service user privileges to update the transaction category on a resource assignment.</span></span> |
| <span data-ttu-id="1817a-137">**Projekti plaanimine ja jälgimine**</span><span class="sxs-lookup"><span data-stu-id="1817a-137">**Project Planning and Tracking**</span></span> | <span data-ttu-id="1817a-138">2164035</span><span class="sxs-lookup"><span data-stu-id="1817a-138">2164035</span></span> | <span data-ttu-id="1817a-139">Parandatud on probleemid funktsiooniga **Projekti kopeerimine**.</span><span class="sxs-lookup"><span data-stu-id="1817a-139">Fixed issues with the **Copy Project** function.</span></span> |
| <span data-ttu-id="1817a-140">**Ajakirje**</span><span class="sxs-lookup"><span data-stu-id="1817a-140">**Time entry**</span></span> | <span data-ttu-id="1817a-141">2129161</span><span class="sxs-lookup"><span data-stu-id="1817a-141">2129161</span></span> | <span data-ttu-id="1817a-142">Rakendatakse kitsamaid piiranguid tagamaks, et kasutajad ei saaks muuta või värskendada esitatud või kinnitatud ajakirjet.</span><span class="sxs-lookup"><span data-stu-id="1817a-142">Tighter restrictions are applied to ensure users can't change and update a time entry that has been submitted or approved.</span></span> |
| <span data-ttu-id="1817a-143">**Ajakirje**</span><span class="sxs-lookup"><span data-stu-id="1817a-143">**Time entry**</span></span> | <span data-ttu-id="1817a-144">2103572</span><span class="sxs-lookup"><span data-stu-id="1817a-144">2103572</span></span> | <span data-ttu-id="1817a-145">Projektiväliste ajakirjete aja kinnitamine ei pea nõudma projekti kinnitaja rolli.</span><span class="sxs-lookup"><span data-stu-id="1817a-145">Time approval for non-project time entries must not be looking for project approver role.</span></span> |