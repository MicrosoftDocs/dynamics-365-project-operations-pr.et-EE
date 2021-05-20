---
title: Project Operationsi topeltkirjutamise integreerimine
description: Selles teemas antakse ülevaade Project Operationsi topeltkirjutamise integreerimisest.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955653"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="181b3-103">Project Operationsi topeltkirjutamise integreerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="181b3-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="181b3-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="181b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="181b3-105">Project Operations kasutab [topeltkirjutamise võimalusi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), et sünkroonida andmed rakendustes Microsoft Dataverse ja Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="181b3-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="181b3-106">Järgmisel joonisel on näidatud, kuidas andmeid sünkroonitakse selle Dataverse’i ja Finance’i vahelise integreerimise osana.</span><span class="sxs-lookup"><span data-stu-id="181b3-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operationsi andmevoogude ülevaade](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="181b3-108">Project Operations Dataverse’is pakub tänapäevast kasutajaliidest (UI) ja lihtsat koodita / madala koodiga laiendatavust, kasutades Power Platformi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="181b3-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="181b3-109">Projektijuhid, ressursihaldurid, projektimeeskonna liikmed ja muud peakontori töötajad teevad oma Project Operationsi tegevusi Dataverse’is.</span><span class="sxs-lookup"><span data-stu-id="181b3-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="181b3-110">Finance’i Project Operations pakub projekti raamatupidamist ja tulude kajastamise tuge.</span><span class="sxs-lookup"><span data-stu-id="181b3-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="181b3-111">Project Operationsi lisandmoodulid liidavad finantsraamistiku Finance’is käibemaksu arvutamise, valuutavahetuskursside, finantsdimensioonide aruandluse ja muu jaoks.</span><span class="sxs-lookup"><span data-stu-id="181b3-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="181b3-112">Projekti raamatupidaja kogemused põhinevad enamasti Finance’il.</span><span class="sxs-lookup"><span data-stu-id="181b3-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="181b3-113">Project Operationsi integreerimine koosneb järgmiste komponentide integreerimisest.</span><span class="sxs-lookup"><span data-stu-id="181b3-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="181b3-114">Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine</span><span class="sxs-lookup"><span data-stu-id="181b3-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="181b3-115">Projekti prognooside ja tegelike andmete integreerimine</span><span class="sxs-lookup"><span data-stu-id="181b3-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="181b3-116">Projekti arved</span><span class="sxs-lookup"><span data-stu-id="181b3-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="181b3-117">Kuluhaldus</span><span class="sxs-lookup"><span data-stu-id="181b3-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="181b3-118">Hankija arved</span><span class="sxs-lookup"><span data-stu-id="181b3-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
