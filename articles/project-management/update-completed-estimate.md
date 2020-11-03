---
title: Kogukuluprognoosi värskendamine
description: Selles teemas kirjeldatakse projekti panuse kavandamise uuendamist.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075139"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="453cd-103">Kogukuluprognoosi värskendamine</span><span class="sxs-lookup"><span data-stu-id="453cd-103">Update estimate at completion</span></span>

<span data-ttu-id="453cd-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="453cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="453cd-105">On tavaline, et projektijuht vaatab ülesande esialgsed prognoosid üle.</span><span class="sxs-lookup"><span data-stu-id="453cd-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="453cd-106">Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut.</span><span class="sxs-lookup"><span data-stu-id="453cd-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="453cd-107">Kuid me ei soovita projektijuhtidel muuta alusnumbreid, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.</span><span class="sxs-lookup"><span data-stu-id="453cd-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="453cd-108">Projektijuht saab ülesannete panust ümber kavandada kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="453cd-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="453cd-109">Alistada vaikimisi prognoos, et lõpetada (ETC) tegeliku järelejäänud panuse uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="453cd-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="453cd-110">Alistada vaikimisi edenemisprotsent ülesande tegeliku edenemise uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="453cd-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="453cd-111">Kõik need lähenemised põhjustavad ülesande ETC, lõpus prognoosimise (EAC) ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist.</span><span class="sxs-lookup"><span data-stu-id="453cd-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="453cd-112">Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.</span><span class="sxs-lookup"><span data-stu-id="453cd-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
