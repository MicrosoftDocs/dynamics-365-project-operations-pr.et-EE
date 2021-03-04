---
title: Projekti etappide tüübid
description: Selles teemas antakse teavet projektiga seotud etappide kohta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148098"
---
# <a name="project-stage-types"></a><span data-ttu-id="09bbd-103">Projekti etappide tüübid</span><span class="sxs-lookup"><span data-stu-id="09bbd-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="09bbd-104">Projekti etapid kujundatakse, et kajastada projekti edenedes selle olekut.</span><span class="sxs-lookup"><span data-stu-id="09bbd-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="09bbd-105">Kohandusi saab kasutada äriprotsessi voogude, Power Automate’i või lisandmooduli laiendite etappide automaaseks värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="09bbd-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="09bbd-106">Järgmised etapid on määratletud vaikimisi BPF-is.</span><span class="sxs-lookup"><span data-stu-id="09bbd-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="09bbd-107">Uus</span><span class="sxs-lookup"><span data-stu-id="09bbd-107">New</span></span>
- <span data-ttu-id="09bbd-108">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="09bbd-108">Quote</span></span>
- <span data-ttu-id="09bbd-109">Plaan</span><span class="sxs-lookup"><span data-stu-id="09bbd-109">Plan</span></span>
- <span data-ttu-id="09bbd-110">Üleandmine</span><span class="sxs-lookup"><span data-stu-id="09bbd-110">Deliver</span></span>
- <span data-ttu-id="09bbd-111">Lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="09bbd-111">Complete</span></span>
- <span data-ttu-id="09bbd-112">Sule</span><span class="sxs-lookup"><span data-stu-id="09bbd-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="09bbd-113">Uus</span><span class="sxs-lookup"><span data-stu-id="09bbd-113">New</span></span>

<span data-ttu-id="09bbd-114">Projekti loomisel määratakse selle olekuks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="09bbd-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="09bbd-115">Kui projekt loodi mallist, võivad sellel olemas olla ajakava, prognoosi ja meeskonna andmed.</span><span class="sxs-lookup"><span data-stu-id="09bbd-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="09bbd-116">Muul juhul on tegemist lihtsalt projekti kavandiga ja ülejäänud komponendid tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="09bbd-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="09bbd-117">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="09bbd-117">Quote</span></span>

<span data-ttu-id="09bbd-118">Kui seostate projekti hinnapakkumisega või kui loote projekti hinnapakkumise põhjal, määratakse projekti olekuks **Hinnapakkumine**, ja eeldatavaid algus- ning lõppkuupäevi värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="09bbd-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="09bbd-119">Kuniks projekt on etapis **Hinnapakkumine**, kuvab lehe **Projektiolem** vahekaart **Müügid** hinnapakkumise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="09bbd-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="09bbd-120">Plaan</span><span class="sxs-lookup"><span data-stu-id="09bbd-120">Plan</span></span>

<span data-ttu-id="09bbd-121">Kui võidate projektiga seotud hinnapakkumise ja projekt jõuab etappi **Leping**, värskendatakse projekt olekule **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="09bbd-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="09bbd-122">Kuniks projekt on etapis **Plaan**, kuvab leht **Projektiolem** lepingu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="09bbd-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="09bbd-123">Üleandmine</span><span class="sxs-lookup"><span data-stu-id="09bbd-123">Deliver</span></span>

<span data-ttu-id="09bbd-124">Kui olete projektiplaani lõpule viimisel projekti käivitamiseks valmis, peab projektijuht värskendama projekti etapile **Üleandmine**, näitamaks, et projektiga on alustatud.</span><span class="sxs-lookup"><span data-stu-id="09bbd-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="09bbd-125">Lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="09bbd-125">Complete</span></span> 

<span data-ttu-id="09bbd-126">Kui projekti töö on lõpule viidud, saab projektijuht värskendada projekti etapile **Lõpuleviimine**.</span><span class="sxs-lookup"><span data-stu-id="09bbd-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="09bbd-127">Projekti määramisega etapile **Lõpuleviimine** näitab projektijuht, et töö on 100% lõpetatud, kuid projekti hoitakse avatuna, et mis tahes ootelolevaid aja- või kulukirjeid saaks talletada.</span><span class="sxs-lookup"><span data-stu-id="09bbd-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="09bbd-128">Sule</span><span class="sxs-lookup"><span data-stu-id="09bbd-128">Close</span></span>

<span data-ttu-id="09bbd-129">Kui projekti jaoks on kõik kanded talletatud, saab projektijuht värskendada projekti etapile **Sule**.</span><span class="sxs-lookup"><span data-stu-id="09bbd-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="09bbd-130">Sel hetkel ei saa kandeid enam talletada ja projekt on seatud kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="09bbd-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
