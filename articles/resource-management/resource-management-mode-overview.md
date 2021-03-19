---
title: Ressursihalduse režiimide ülevaade
description: Selles teemas antakse teavet ressursihalduse funktsionaalsuse kohta rakenduses Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279448"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="312a4-103">Ressursihalduse režiimide ülevaade</span><span class="sxs-lookup"><span data-stu-id="312a4-103">Resource management modes overview</span></span>

<span data-ttu-id="312a4-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="312a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="312a4-105">Dynamics 365 Project Operations toetab kahte režiimi, üldise broneerimisvoo käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="312a4-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="312a4-106">Haldusrežiim määratletakse projekti parameetrina ja seda saab muuta juhul, kui teie äritegevus vajab muutmist.</span><span class="sxs-lookup"><span data-stu-id="312a4-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="312a4-107">Keskne režiim</span><span class="sxs-lookup"><span data-stu-id="312a4-107">Central mode</span></span>
<span data-ttu-id="312a4-108">Organisatsioonidele, kes tsentraliseerivad ressursside eraldamise projektidele, pakub keskne režiim võimalust, kuidas tagada, et projektijuhid saavad määratleta ressursinõude projekti tasandil.</span><span class="sxs-lookup"><span data-stu-id="312a4-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="312a4-109">Ressursinõuete täitmine delegeeritakse ressursihaldurile.</span><span class="sxs-lookup"><span data-stu-id="312a4-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="312a4-110">Projektijuhid saavad ressursihalduri poolt pakutud ressursse aktsepteerida või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="312a4-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Keskne režiim](./media/resource-management-central.png)

<span data-ttu-id="312a4-112">Ressursside haldamiseks keskses režiimis vaadake järgmist.</span><span class="sxs-lookup"><span data-stu-id="312a4-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="312a4-113">Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine</span><span class="sxs-lookup"><span data-stu-id="312a4-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="312a4-114">Nimega ressursside broneerimine ressursinõuetest</span><span class="sxs-lookup"><span data-stu-id="312a4-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="312a4-115">Ressursitaotluse esitamine</span><span class="sxs-lookup"><span data-stu-id="312a4-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="312a4-116">Ressursinõude täitmine</span><span class="sxs-lookup"><span data-stu-id="312a4-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="312a4-117">Pakutud projekti ressursi ressursitaotlusest kinnitamine või tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="312a4-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="312a4-118">Hübriidrežiim</span><span class="sxs-lookup"><span data-stu-id="312a4-118">Hybrid mode</span></span>
<span data-ttu-id="312a4-119">Organisatsioonides, kes vajavad ressursside eraldamisel paindlikkust, võimaldab hübriidrežiim nii projektijuhtidele kui ka ressursihalduritele ressursside broneerimist.</span><span class="sxs-lookup"><span data-stu-id="312a4-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hübriidrežiim](./media/resource-management-hybrid.png)

<span data-ttu-id="312a4-121">Lisaks toetatud keskse režiimi protsessile vaadake järgmisi teemasid kõigi teiste toetatud broneerimisvoogude haldamise kohta hübriidrežiimis.</span><span class="sxs-lookup"><span data-stu-id="312a4-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="312a4-122">Ressursi otse projektile broneerimine.</span><span class="sxs-lookup"><span data-stu-id="312a4-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="312a4-123">Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid</span><span class="sxs-lookup"><span data-stu-id="312a4-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="312a4-124">Ressursi broneerimine ressursinõudest.</span><span class="sxs-lookup"><span data-stu-id="312a4-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="312a4-125">Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine</span><span class="sxs-lookup"><span data-stu-id="312a4-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="312a4-126">Nimega ressursside broneerimine ressursinõuetest</span><span class="sxs-lookup"><span data-stu-id="312a4-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]