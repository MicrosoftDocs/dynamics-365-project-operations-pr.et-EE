---
title: Reserveeringud ja määramised
description: Selles teemas antakse teavet ressursside broneerimise ja ressurside määramise erinevuste kohta.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012761"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="b9c07-103">Reserveeringud ja määramised</span><span class="sxs-lookup"><span data-stu-id="b9c07-103">Bookings vs assignments</span></span>

<span data-ttu-id="b9c07-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="b9c07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b9c07-105">Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised.</span><span class="sxs-lookup"><span data-stu-id="b9c07-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="b9c07-106">Fikseeritud broneeringud tarbivad ressursivõimsust.</span><span class="sxs-lookup"><span data-stu-id="b9c07-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="b9c07-107">Reserveeringud annavad meeskondadele korralduslikud kontseptsioonid, et nad mõistaksid, kuidas ressursid erinevate projektide üleselt rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="b9c07-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="b9c07-108">Dynamics 365 Project Operations peab broneeringuid projektitasemel mõisteks.</span><span class="sxs-lookup"><span data-stu-id="b9c07-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="b9c07-109">Erinevalt broneeringutest on määramised ressursside kohustus projekti ülesannete osas projekti ajakavas.</span><span class="sxs-lookup"><span data-stu-id="b9c07-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="b9c07-110">Ressursid võivad olla nimelised või üldised.</span><span class="sxs-lookup"><span data-stu-id="b9c07-110">The resources can be named or generic.</span></span>  <span data-ttu-id="b9c07-111">Kui ressursinõue tuletatakse projekti ülesande määramisest, kasutab Project Operations ressursside määramise panuse kontuure ressursinõude üksikasjade kontuuride loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b9c07-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="b9c07-112">Kuid viidet ressursi määramisele ei säilitata.</span><span class="sxs-lookup"><span data-stu-id="b9c07-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="b9c07-113">Ressursinõudest pärit broneeringute värskendamised ei värskenda ressursi määramisi.</span><span class="sxs-lookup"><span data-stu-id="b9c07-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="b9c07-114">Tavaliselt võrdub ressursi reserveeringute summa ressursi määramiste summaga ühe või mitme ülesande üleselt.</span><span class="sxs-lookup"><span data-stu-id="b9c07-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="b9c07-115">Samas Project Operations ei jõusta seda kokkulepet.</span><span class="sxs-lookup"><span data-stu-id="b9c07-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="b9c07-116">Vaates **Vastavusseviimine** kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.</span><span class="sxs-lookup"><span data-stu-id="b9c07-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]