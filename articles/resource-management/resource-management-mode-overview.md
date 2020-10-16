---
title: Ressursihalduse režiimide ülevaade
description: Selles teemas antakse teavet ressursihalduse funktsionaalsusest Dynamics 365 Project Operationsis.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930086"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="0be9f-103">Ressursihalduse režiimide ülevaade</span><span class="sxs-lookup"><span data-stu-id="0be9f-103">Resource management modes overview</span></span>

<span data-ttu-id="0be9f-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="0be9f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0be9f-105">Dynamics 365 Project Operations toetab kahte režiimi, et saaksite kogu reserveeringu voogu käivitada.</span><span class="sxs-lookup"><span data-stu-id="0be9f-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="0be9f-106">Haldusrežiim määratletakse projekti parameetrina ja seda saab muuta juhul, kui teie äritegevus vajab muutmist.</span><span class="sxs-lookup"><span data-stu-id="0be9f-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="0be9f-107">Keskne režiim</span><span class="sxs-lookup"><span data-stu-id="0be9f-107">Central mode</span></span>
<span data-ttu-id="0be9f-108">Organisatsioonidele, kes tsentraliseerivad ressursside eraldamise projektidele, pakub keskne režiim võimalust, kuidas tagada, et projektijuhid saavad määratleta ressursinõude projekti tasandil.</span><span class="sxs-lookup"><span data-stu-id="0be9f-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="0be9f-109">Ressursinõuete täitmine delegeeritakse ressursihaldurile.</span><span class="sxs-lookup"><span data-stu-id="0be9f-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="0be9f-110">Projektijuhid saavad ressursihalduri poolt pakutud ressursse aktsepteerida või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="0be9f-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Keskne režiim](./media/resource-management-central.png)

<span data-ttu-id="0be9f-112">Ressursside haldamiseks keskses režiimis vaadake järgmist.</span><span class="sxs-lookup"><span data-stu-id="0be9f-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="0be9f-113">Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine</span><span class="sxs-lookup"><span data-stu-id="0be9f-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="0be9f-114">Nimega ressursside broneerimine ressursinõuetest</span><span class="sxs-lookup"><span data-stu-id="0be9f-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="0be9f-115">Ressursitaotluse esitamine</span><span class="sxs-lookup"><span data-stu-id="0be9f-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="0be9f-116">Ressursinõude täitmine</span><span class="sxs-lookup"><span data-stu-id="0be9f-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="0be9f-117">Pakutud projekti ressursi ressursitaotlusest kinnitamine või tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="0be9f-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="0be9f-118">Hübriidrežiim</span><span class="sxs-lookup"><span data-stu-id="0be9f-118">Hybrid mode</span></span>
<span data-ttu-id="0be9f-119">Organisatsioonides, kes vajavad ressursside eraldamisel paindlikkust, võimaldab hübriidrežiim nii projektijuhtidele kui ka ressursihalduritele ressursside broneerimist.</span><span class="sxs-lookup"><span data-stu-id="0be9f-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hübriidrežiim](./media/resource-management-hybrid.png)

<span data-ttu-id="0be9f-121">Lisaks toetatud keskse režiimi protsessile vaadake järgmisi teemasid kõigi teiste toetatud broneerimisvoogude haldamise kohta hübriidrežiimis.</span><span class="sxs-lookup"><span data-stu-id="0be9f-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="0be9f-122">Ressursi otse projektile broneerimine.</span><span class="sxs-lookup"><span data-stu-id="0be9f-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="0be9f-123">Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid</span><span class="sxs-lookup"><span data-stu-id="0be9f-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="0be9f-124">Ressursi broneerimine ressursinõudest.</span><span class="sxs-lookup"><span data-stu-id="0be9f-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="0be9f-125">Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine</span><span class="sxs-lookup"><span data-stu-id="0be9f-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="0be9f-126">Nimega ressursside broneerimine ressursinõuetest</span><span class="sxs-lookup"><span data-stu-id="0be9f-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
