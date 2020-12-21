---
title: Project Service Automationi ülevaade
description: Selles teemas antakse teavet rakenduse Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance integreerimise lahenduse kohta.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642448"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="d79df-103">Project Service Automationi ülevaade</span><span class="sxs-lookup"><span data-stu-id="d79df-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d79df-104">Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida teenuse Common Data Service kaudu andmeid rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation olemite üleselt.</span><span class="sxs-lookup"><span data-stu-id="d79df-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="d79df-105">Integreerimismallid, mis on saadaval andmete integreerimise funktsiooniga, võimaldavad projektide, projekti lepingute, projekti lepinguridade, projekti lepingurea vahe-eesmärkide, projekti ülesannete, kulu tehingukategooriate, tööaja prognooside ja kuluprognooside voogu Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="d79df-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="d79df-106">Kui kasutate versiooni 7.3.0, peate installima KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="d79df-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="d79df-107">Seejärel saate integreerida fikseeritud hinnaga projekte.</span><span class="sxs-lookup"><span data-stu-id="d79df-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="d79df-108">Kui kasutate versiooni 7.3.0 ja toote tasulised tehingud Project Service Automationist üle, peate installima KB 4345320, et kaasata need tasud projekti arvesse.</span><span class="sxs-lookup"><span data-stu-id="d79df-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="d79df-109">Kui kasutate versiooni 8.0, saate kasutada projekti ülesannete integreerimist, kulu kandekategooriaid, tööaja prognoose, kuluprognoose ja funktsioonide lukustamist.</span><span class="sxs-lookup"><span data-stu-id="d79df-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="d79df-110">Kui kasutate versiooni 8.0.1 või uuemat, on teil võimalik tegelikud näitajad sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="d79df-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="d79df-111">Enne, kui saate integreerida Project Service Automationi rakendusse Finance, peate konfigureerima Project Service Automationi integreerimise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d79df-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="d79df-112">Lisateavet vt: [Project Service Automationi integreerimise parameetrid](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d79df-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="d79df-113">See integratsiooni lahendus võimaldab otsest sünkroonimist järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="d79df-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="d79df-114">Säilitage projektilepingud rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-115">Looge projekte rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-116">Säilitage projekti lepinguread rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-117">Säilitage projekti lepingurea vaheetapid rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-118">Säilitage projekti ülesanded rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-119">Säilitage kulude kandekategooriaid Finance’is ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="d79df-120">Looge projektide kestusprognoose rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-121">Looge projektide kuluprognoose rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d79df-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="d79df-122">Looge Project Service Automationis projekti aja, kulu ja tasu tegelikud näitajad ning looge Project Service Automationi integreerimise töölehel projekti kanded, et neid saaks Finance’i postitada.</span><span class="sxs-lookup"><span data-stu-id="d79df-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="d79df-123">Andmete sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="d79df-123">Data synchronization</span></span>

<span data-ttu-id="d79df-124">Järgmisel joonisel on näidatud, kuidas andmeid integratsiooni osana rakenduste Project Service Automation ja Finance vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="d79df-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="d79df-125">Kõik mallid pole hetkel saadaval.</span><span class="sxs-lookup"><span data-stu-id="d79df-125">Not all templates are currently available.</span></span> <span data-ttu-id="d79df-126">Mallid väljastatakse, kui need lõpetatakse.</span><span class="sxs-lookup"><span data-stu-id="d79df-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="d79df-127">[![Project Service Automationi integreerimine rakendusega Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="d79df-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="d79df-128">Finance’i süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="d79df-128">System requirements for Finance</span></span>

<span data-ttu-id="d79df-129">Rakendusest Project Service Automation rakendusse Finance integreerimise lahenduse kasutamiseks peate installima Enterprise’i versiooni 7.3 koos Platformi värskendusega 12 või uuemaga.</span><span class="sxs-lookup"><span data-stu-id="d79df-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="d79df-130">Project Service Automationi süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="d79df-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="d79df-131">Rakendusest Project Service Automation rakendusse Finance integreerimise lahenduse kasutamiseks peate installima järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="d79df-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="d79df-132">Dynamics 365 Project Service Automation’i versioon 9.0.0.0 või uuem</span><span class="sxs-lookup"><span data-stu-id="d79df-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="d79df-133">Sularahas lahenduse tõenäosus rakenduses Dynamics 365 Sales, versioon 1.14.0.0 (ver 14) või uuem</span><span class="sxs-lookup"><span data-stu-id="d79df-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="d79df-134">Project Service Automationist Finance’i lahendus rakenduse Dynamics 365 Project Service Automation versiooni 1.0.0.0 või hilisema jaoks</span><span class="sxs-lookup"><span data-stu-id="d79df-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="d79df-135">Installige Project Service Automationist Finance’i integreerimise lahendus oma Project Service Automationi olemisse</span><span class="sxs-lookup"><span data-stu-id="d79df-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="d79df-136">Laadige Project Service Automationist Finance’i integreerimise lahendus alla [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=57016) ja järgige juhiseid, mis on lahendusega kaasas.</span><span class="sxs-lookup"><span data-stu-id="d79df-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
