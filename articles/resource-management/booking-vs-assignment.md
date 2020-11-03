---
title: Reserveeringud ja määramised
description: Selles teemas antakse teavet ressursside broneerimise ja ressurside määramise erinevuste kohta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074805"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="2f162-103">Reserveeringud ja määramised</span><span class="sxs-lookup"><span data-stu-id="2f162-103">Bookings vs assignments</span></span>

<span data-ttu-id="2f162-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="2f162-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f162-105">Broneeringud on ressursside fikseeritud või esialgsed projektile eraldamised.</span><span class="sxs-lookup"><span data-stu-id="2f162-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="2f162-106">Fikseeritud broneeringud tarbivad ressursivõimsust.</span><span class="sxs-lookup"><span data-stu-id="2f162-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="2f162-107">Määramised on projekti ajakavas tehtud ressursside määramised projekti ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="2f162-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="2f162-108">Ressursid võivad olla tegelikud või üldised.</span><span class="sxs-lookup"><span data-stu-id="2f162-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="2f162-109">Ideaalis peaksid tegelike ressursside puhul broneeringud ja määramised ühtima, kuna need ei erine üksteisest.</span><span class="sxs-lookup"><span data-stu-id="2f162-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="2f162-110">Samas Microsoft Dynamics Project Operations ei jõusta seda kokkulepet.</span><span class="sxs-lookup"><span data-stu-id="2f162-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="2f162-111">Vaates **Vastavusseviimine** kuvatakse projektijuhile kohti, kus ressursi broneeringud ja määramised ei ühti.</span><span class="sxs-lookup"><span data-stu-id="2f162-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
