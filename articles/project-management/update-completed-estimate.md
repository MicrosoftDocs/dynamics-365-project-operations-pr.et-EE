---
title: Kogukuluprognoosi värskendamine
description: Selles teemas kirjeldatakse projekti panuse kavandamise uuendamist.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897761"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="46f77-103">Kogukuluprognoosi värskendamine</span><span class="sxs-lookup"><span data-stu-id="46f77-103">Update estimate at completion</span></span>

<span data-ttu-id="46f77-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="46f77-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46f77-105">On tavaline, et projektijuht vaatab ülesande esialgsed prognoosid üle.</span><span class="sxs-lookup"><span data-stu-id="46f77-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="46f77-106">Projekti ümberkavandamine hõlmab projektijuhi ettekujutust prognoosidest, võttes arvesse projekti praegust olekut.</span><span class="sxs-lookup"><span data-stu-id="46f77-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="46f77-107">Kuid me ei soovita projektijuhtidel muuta alusnumbreid, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi kindlaks määratud dokumenti, millega kõik projekti huvirühmad on nõustunud.</span><span class="sxs-lookup"><span data-stu-id="46f77-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="46f77-108">Projektijuht saab ülesannete panust ümber kavandada kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="46f77-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="46f77-109">Alistada vaikimisi prognoos, et lõpetada (ETC) tegeliku järelejäänud panuse uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="46f77-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="46f77-110">Alistada vaikimisi edenemisprotsent ülesande tegeliku edenemise uue prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="46f77-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="46f77-111">Kõik need lähenemised põhjustavad ülesande ETC, lõpus prognoosimise (EAC) ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist.</span><span class="sxs-lookup"><span data-stu-id="46f77-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="46f77-112">Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent, mis annavad panuse hälbe uue prognoosi.</span><span class="sxs-lookup"><span data-stu-id="46f77-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
