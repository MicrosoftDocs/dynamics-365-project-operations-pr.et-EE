---
title: Reserveeringud ja määramised
description: Selles teemas antakse teavet ressursside broneerimise ja ressurside määramise erinevuste kohta.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130213"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="84116-103">Reserveeringud ja määramised</span><span class="sxs-lookup"><span data-stu-id="84116-103">Bookings vs assignments</span></span>

<span data-ttu-id="84116-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="84116-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84116-105">Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised.</span><span class="sxs-lookup"><span data-stu-id="84116-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="84116-106">Fikseeritud broneeringud tarbivad ressursivõimsust.</span><span class="sxs-lookup"><span data-stu-id="84116-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="84116-107">Reserveeringud annavad meeskondadele korralduslikud kontseptsioonid, et nad mõistaksid, kuidas ressursid erinevate projektide üleselt rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="84116-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="84116-108">Dynamics 365 Project Operations loeb reserveeringud projekti tasemel kontseptsiooniks.</span><span class="sxs-lookup"><span data-stu-id="84116-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="84116-109">Erinevalt broneeringutest on määramised ressursside kohustus projekti ülesannete osas projekti ajakavas.</span><span class="sxs-lookup"><span data-stu-id="84116-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="84116-110">Ressursid võivad olla nimelised või üldised.</span><span class="sxs-lookup"><span data-stu-id="84116-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="84116-111">Tavaliselt võrdub ressursi reserveeringute summa ressursi määramiste summaga ühe või mitme ülesande üleselt.</span><span class="sxs-lookup"><span data-stu-id="84116-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="84116-112">Samas Project Operations ei jõusta seda kokkulepet.</span><span class="sxs-lookup"><span data-stu-id="84116-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="84116-113">Vaates **Vastavusseviimine** kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.</span><span class="sxs-lookup"><span data-stu-id="84116-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
