---
title: Ajakava abi ülevaade
description: Selles teemas antakse teavet ajakava abimehega töötamise kohta ressursside broneerimisel.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125623"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="c320a-103">Ajakava abi ülevaade</span><span class="sxs-lookup"><span data-stu-id="c320a-103">Schedule assistant overview</span></span>

<span data-ttu-id="c320a-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="c320a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c320a-105">Ajakava abimeest kasutatakse selleks, et broneerida ressursse, lähtudes projektijuhi määratud nõuetest.</span><span class="sxs-lookup"><span data-stu-id="c320a-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="c320a-106">Ajakava abimees toetub ressursi leidmiseks ressursinõudes esitatud parameetritele.</span><span class="sxs-lookup"><span data-stu-id="c320a-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="c320a-107">Ajakava abimees soovitab ressursse, mis vastavad asjakohastele nõuetele, nagu vajalikud ajavahemikud või oskused.</span><span class="sxs-lookup"><span data-stu-id="c320a-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="c320a-108">Pärast sobivate ressursside tuvastamist saab ressursihaldur või projektijuht ressursi tööle broneerida.</span><span class="sxs-lookup"><span data-stu-id="c320a-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c320a-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c320a-109">Prerequisites</span></span>

<span data-ttu-id="c320a-110">Ajakava abimees on lahenduse Universal Resource Scheduling osa.</span><span class="sxs-lookup"><span data-stu-id="c320a-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="c320a-111">See lahendus on kaasatud ja installitud rakendustes Dynamics 365 Project Operations, Dynamics 365 Field Service ja Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="c320a-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="c320a-112">Nõuete ja ressursside ühitamine</span><span class="sxs-lookup"><span data-stu-id="c320a-112">Matching requirements and resources</span></span>

<span data-ttu-id="c320a-113">Genereeritud ressursinõue põhineb järgmistel üksikasjadel.</span><span class="sxs-lookup"><span data-stu-id="c320a-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="c320a-114">Tunnused</span><span class="sxs-lookup"><span data-stu-id="c320a-114">Characteristics</span></span>
-   <span data-ttu-id="c320a-115">Rollid</span><span class="sxs-lookup"><span data-stu-id="c320a-115">Roles</span></span>
-   <span data-ttu-id="c320a-116">Äriüksused</span><span class="sxs-lookup"><span data-stu-id="c320a-116">Business units</span></span>
-   <span data-ttu-id="c320a-117">Ressursieelistused</span><span class="sxs-lookup"><span data-stu-id="c320a-117">Resource preferences</span></span>
-   <span data-ttu-id="c320a-118">Tööpanuse kontuurid</span><span class="sxs-lookup"><span data-stu-id="c320a-118">Effort contours</span></span>
-   <span data-ttu-id="c320a-119">Ajavöönd</span><span class="sxs-lookup"><span data-stu-id="c320a-119">Time zone</span></span>

<span data-ttu-id="c320a-120">Ajakava abimees kasutab neid üksikasju ressursside filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="c320a-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="c320a-121">Ajakava abimehe käivitamine</span><span class="sxs-lookup"><span data-stu-id="c320a-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="c320a-122">Ajakava abimehe käivitamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="c320a-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="c320a-123">Kui kasutate hübriidrežiimi, saate meeskonnaliikmete ruudustikus valida mis tahes meeskonnaliikme, kellel on täitmata ressursinõue, ja seejärel valige **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="c320a-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="c320a-124">Kui kasutate keskset režiimi, leiab ja valib ressursi ressursihaldur.</span><span class="sxs-lookup"><span data-stu-id="c320a-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="c320a-125">Ajakavaabilise filtrid</span><span class="sxs-lookup"><span data-stu-id="c320a-125">Schedule assistant filters</span></span>

<span data-ttu-id="c320a-126">Pärast ajakava abimehe käitamist kuvatakse ressursinõude üksikasjad filtreeritud väärtustena vasakpoolsel paanil.</span><span class="sxs-lookup"><span data-stu-id="c320a-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="c320a-127">Ressursihaldur või projektijuht saavad tulemusi viimistleda, kohandades filtreid, et need vastaksid kavandamise vajadustele.</span><span class="sxs-lookup"><span data-stu-id="c320a-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="c320a-128">Filtripaan kuvab järgmisi tööga seotud suvandeid.</span><span class="sxs-lookup"><span data-stu-id="c320a-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="c320a-129">Töö algus ja lõpp</span><span class="sxs-lookup"><span data-stu-id="c320a-129">Work start and end</span></span>
-   <span data-ttu-id="c320a-130">Tunnused</span><span class="sxs-lookup"><span data-stu-id="c320a-130">Characteristics</span></span>
-   <span data-ttu-id="c320a-131">Rollid</span><span class="sxs-lookup"><span data-stu-id="c320a-131">Roles</span></span>
-   <span data-ttu-id="c320a-132">Organisatsiooniüksused</span><span class="sxs-lookup"><span data-stu-id="c320a-132">Organizational units</span></span>
-   <span data-ttu-id="c320a-133">Ressursiettevõte</span><span class="sxs-lookup"><span data-stu-id="c320a-133">Resourcing company</span></span>
-   <span data-ttu-id="c320a-134">Ressursi tüübid</span><span class="sxs-lookup"><span data-stu-id="c320a-134">Resource types</span></span>
-   <span data-ttu-id="c320a-135">Eelistatud ressursid</span><span class="sxs-lookup"><span data-stu-id="c320a-135">Preferred resources</span></span>
