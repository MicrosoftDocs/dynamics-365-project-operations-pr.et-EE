---
title: Ajakava abi ülevaade
description: Selles teemas antakse teavet ajakava abimehega töötamise kohta ressursside broneerimisel.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014111"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="72b6d-103">Ajakava abi ülevaade</span><span class="sxs-lookup"><span data-stu-id="72b6d-103">Schedule assistant overview</span></span>

<span data-ttu-id="72b6d-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="72b6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72b6d-105">Ajakava abimeest kasutatakse selleks, et broneerida ressursse, lähtudes projektijuhi määratud nõuetest.</span><span class="sxs-lookup"><span data-stu-id="72b6d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="72b6d-106">Ajakava abimees toetub ressursi leidmiseks ressursinõudes esitatud parameetritele.</span><span class="sxs-lookup"><span data-stu-id="72b6d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="72b6d-107">Ajakava abimees soovitab ressursse, mis vastavad asjakohastele nõuetele, nagu vajalikud ajavahemikud või oskused.</span><span class="sxs-lookup"><span data-stu-id="72b6d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="72b6d-108">Pärast sobivate ressursside tuvastamist saab ressursihaldur või projektijuht ressursi tööle broneerida.</span><span class="sxs-lookup"><span data-stu-id="72b6d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="72b6d-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="72b6d-109">Prerequisites</span></span>

<span data-ttu-id="72b6d-110">Ajakava abimees on lahenduse Universal Resource Scheduling osa.</span><span class="sxs-lookup"><span data-stu-id="72b6d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="72b6d-111">See lahendus on kaasatud ja installitud rakendusega Dynamics 365 Project Operations, Dynamics 365 Field Service ja Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="72b6d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="72b6d-112">Nõuete ja ressursside ühitamine</span><span class="sxs-lookup"><span data-stu-id="72b6d-112">Matching requirements and resources</span></span>

<span data-ttu-id="72b6d-113">Genereeritud ressursinõue põhineb järgmistel üksikasjadel.</span><span class="sxs-lookup"><span data-stu-id="72b6d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="72b6d-114">Tunnused</span><span class="sxs-lookup"><span data-stu-id="72b6d-114">Characteristics</span></span>
-   <span data-ttu-id="72b6d-115">Rollid</span><span class="sxs-lookup"><span data-stu-id="72b6d-115">Roles</span></span>
-   <span data-ttu-id="72b6d-116">Äriüksused</span><span class="sxs-lookup"><span data-stu-id="72b6d-116">Business units</span></span>
-   <span data-ttu-id="72b6d-117">Ressursieelistused</span><span class="sxs-lookup"><span data-stu-id="72b6d-117">Resource preferences</span></span>
-   <span data-ttu-id="72b6d-118">Tööpanuse kontuurid</span><span class="sxs-lookup"><span data-stu-id="72b6d-118">Effort contours</span></span>
-   <span data-ttu-id="72b6d-119">Ajavöönd</span><span class="sxs-lookup"><span data-stu-id="72b6d-119">Time zone</span></span>

<span data-ttu-id="72b6d-120">Ajakava abimees kasutab neid üksikasju ressursside filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="72b6d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="72b6d-121">Ajakava abimehe käivitamine</span><span class="sxs-lookup"><span data-stu-id="72b6d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="72b6d-122">Ajakava abimehe käivitamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="72b6d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="72b6d-123">Kui kasutate hübriidrežiimi, saate meeskonnaliikmete ruudustikus valida mis tahes meeskonnaliikme, kellel on täitmata ressursinõue, ja seejärel valige **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="72b6d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="72b6d-124">Kui kasutate keskset režiimi, leiab ja valib ressursi ressursihaldur.</span><span class="sxs-lookup"><span data-stu-id="72b6d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="72b6d-125">Ajakavaabilise filtrid</span><span class="sxs-lookup"><span data-stu-id="72b6d-125">Schedule assistant filters</span></span>

<span data-ttu-id="72b6d-126">Pärast ajakava abimehe käitamist kuvatakse ressursinõude üksikasjad filtreeritud väärtustena vasakpoolsel paanil.</span><span class="sxs-lookup"><span data-stu-id="72b6d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="72b6d-127">Ressursihaldur või projektijuht saavad tulemusi viimistleda, kohandades filtreid, et need vastaksid kavandamise vajadustele.</span><span class="sxs-lookup"><span data-stu-id="72b6d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="72b6d-128">Filtripaan kuvab järgmisi tööga seotud suvandeid.</span><span class="sxs-lookup"><span data-stu-id="72b6d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="72b6d-129">Töö algus ja lõpp</span><span class="sxs-lookup"><span data-stu-id="72b6d-129">Work start and end</span></span>
-   <span data-ttu-id="72b6d-130">Tunnused</span><span class="sxs-lookup"><span data-stu-id="72b6d-130">Characteristics</span></span>
-   <span data-ttu-id="72b6d-131">Rollid</span><span class="sxs-lookup"><span data-stu-id="72b6d-131">Roles</span></span>
-   <span data-ttu-id="72b6d-132">Organisatsiooniüksused</span><span class="sxs-lookup"><span data-stu-id="72b6d-132">Organizational units</span></span>
-   <span data-ttu-id="72b6d-133">Ressursiettevõte</span><span class="sxs-lookup"><span data-stu-id="72b6d-133">Resourcing company</span></span>
-   <span data-ttu-id="72b6d-134">Ressursi tüübid</span><span class="sxs-lookup"><span data-stu-id="72b6d-134">Resource types</span></span>
-   <span data-ttu-id="72b6d-135">Eelistatud ressursid</span><span class="sxs-lookup"><span data-stu-id="72b6d-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]