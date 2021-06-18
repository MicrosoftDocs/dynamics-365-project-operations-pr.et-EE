---
title: Projekti etapid
description: Selles teemas antakse teavet nende projektide etappide kohta, mis on saadaval lahenduses Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996921"
---
# <a name="project-stages"></a><span data-ttu-id="4e3c8-103">Projekti etapid</span><span class="sxs-lookup"><span data-stu-id="4e3c8-103">Project stages</span></span>

<span data-ttu-id="4e3c8-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4e3c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4e3c8-105">Projekti etapid kujundatakse, et kajastada projekti edenedes selle olekut.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="4e3c8-106">Kohandusi saab kasutada äriprotsessi voogude, Power Automate’i või lisandmooduli laiendite etappide automaaseks värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="4e3c8-107">Järgmised etapid on määratletud vaikimisi äriprotsessi voos.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="4e3c8-108">Uus</span><span class="sxs-lookup"><span data-stu-id="4e3c8-108">New</span></span>
- <span data-ttu-id="4e3c8-109">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="4e3c8-109">Quote</span></span>
- <span data-ttu-id="4e3c8-110">Leping</span><span class="sxs-lookup"><span data-stu-id="4e3c8-110">Plan</span></span>
- <span data-ttu-id="4e3c8-111">Üleandmine</span><span class="sxs-lookup"><span data-stu-id="4e3c8-111">Deliver</span></span>
- <span data-ttu-id="4e3c8-112">Lõpeta</span><span class="sxs-lookup"><span data-stu-id="4e3c8-112">Complete</span></span>
- <span data-ttu-id="4e3c8-113">Saate dialoogiakna sulgeda</span><span class="sxs-lookup"><span data-stu-id="4e3c8-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="4e3c8-114">Uus</span><span class="sxs-lookup"><span data-stu-id="4e3c8-114">New</span></span>

<span data-ttu-id="4e3c8-115">Projekti loomisel määratakse selle olekuks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="4e3c8-116">Kui projekt loodi mallist, võivad sellel olemas olla ajakava, prognoosi ja meeskonna andmed.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="4e3c8-117">Muul juhul on tegemist projekti kavandiga ja ülejäänud komponendid tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="4e3c8-118">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="4e3c8-118">Quote</span></span>

<span data-ttu-id="4e3c8-119">Kui seostate projekti hinnapakkumisega või kui loote projekti hinnapakkumise põhjal, määratakse projekti olekuks **Hinnapakkumine**, ja eeldatavaid algus- ning lõppkuupäevi värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="4e3c8-120">Kuniks projekt on etapis **Hinnapakkumine**, kuvab lehe **Projektiolem** vahekaart **Müügid** hinnapakkumise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="4e3c8-121">Plaan</span><span class="sxs-lookup"><span data-stu-id="4e3c8-121">Plan</span></span>

<span data-ttu-id="4e3c8-122">Kui võidate projektiga seotud hinnapakkumise ja projekt jõuab etappi **Leping**, värskendatakse projekt olekule **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="4e3c8-123">Kuniks projekt on etapis **Plaan**, kuvab leht **Projektiolem** lepingu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="4e3c8-124">Üleandmine</span><span class="sxs-lookup"><span data-stu-id="4e3c8-124">Deliver</span></span>

<span data-ttu-id="4e3c8-125">Kui olete projektiplaani lõpule viimisel projekti käivitamiseks valmis, peab projektijuht värskendama projekti etapile **Üleandmine**, näitamaks, et projektiga on alustatud.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="4e3c8-126">Lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="4e3c8-126">Complete</span></span> 

<span data-ttu-id="4e3c8-127">Kui projekti töö on lõpule viidud, saab projektijuht värskendada projekti etapile **Lõpuleviimine**.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="4e3c8-128">Projekti määramisega etapile **Lõpuleviimine** näitab projektijuht, et töö on 100% lõpetatud, kuid projekti hoitakse avatuna, et mis tahes ootelolevaid aja- või kulukirjeid saaks talletada.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="4e3c8-129">Sule</span><span class="sxs-lookup"><span data-stu-id="4e3c8-129">Close</span></span>

<span data-ttu-id="4e3c8-130">Kui projekti jaoks on kõik kanded talletatud, saab projektijuht värskendada projekti etapile **Sule**.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="4e3c8-131">Sel hetkel ei saa kandeid enam talletada ja projekt on seatud kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="4e3c8-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]