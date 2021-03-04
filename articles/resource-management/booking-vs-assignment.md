---
title: Reserveeringud ja määramised
description: Selles teemas antakse teavet ressursside broneerimise ja ressurside määramise erinevuste kohta.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841167"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="b024d-103">Reserveeringud ja määramised</span><span class="sxs-lookup"><span data-stu-id="b024d-103">Bookings vs assignments</span></span>

<span data-ttu-id="b024d-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="b024d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b024d-105">Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised.</span><span class="sxs-lookup"><span data-stu-id="b024d-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="b024d-106">Fikseeritud broneeringud tarbivad ressursivõimsust.</span><span class="sxs-lookup"><span data-stu-id="b024d-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="b024d-107">Reserveeringud annavad meeskondadele korralduslikud kontseptsioonid, et nad mõistaksid, kuidas ressursid erinevate projektide üleselt rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="b024d-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="b024d-108">Dynamics 365 Project Operations peab broneeringuid projektitasemel mõisteks.</span><span class="sxs-lookup"><span data-stu-id="b024d-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="b024d-109">Erinevalt broneeringutest on määramised ressursside kohustus projekti ülesannete osas projekti ajakavas.</span><span class="sxs-lookup"><span data-stu-id="b024d-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="b024d-110">Ressursid võivad olla nimelised või üldised.</span><span class="sxs-lookup"><span data-stu-id="b024d-110">The resources can be named or generic.</span></span>  <span data-ttu-id="b024d-111">Kui ressursinõue tuletatakse projekti ülesande määramisest, kasutab Project Operations ressursside määramise panuse kontuure ressursinõude üksikasjade kontuuride loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b024d-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="b024d-112">Kuid viidet ressursi määramisele ei säilitata.</span><span class="sxs-lookup"><span data-stu-id="b024d-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="b024d-113">Ressursinõudest pärit broneeringute värskendamised ei värskenda ressursi määramisi.</span><span class="sxs-lookup"><span data-stu-id="b024d-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="b024d-114">Tavaliselt võrdub ressursi reserveeringute summa ressursi määramiste summaga ühe või mitme ülesande üleselt.</span><span class="sxs-lookup"><span data-stu-id="b024d-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="b024d-115">Samas Project Operations ei jõusta seda kokkulepet.</span><span class="sxs-lookup"><span data-stu-id="b024d-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="b024d-116">Vaates **Vastavusseviimine** kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.</span><span class="sxs-lookup"><span data-stu-id="b024d-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


