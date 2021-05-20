---
title: Projektikalendrite määratlemine
description: Selles teemas antakse teavet selle kohta, kuidas rakendada projektile kalendrimalli projekti ajakava jälgimiseks.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981295"
---
# <a name="define-project-calendars"></a><span data-ttu-id="4cfda-103">Projektikalendrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="4cfda-103">Define project calendars</span></span>

<span data-ttu-id="4cfda-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4cfda-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4cfda-105">Projekti loomiseks ja haldamiseks peate projektile rakendama kalendrimalli.</span><span class="sxs-lookup"><span data-stu-id="4cfda-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="4cfda-106">Kalendrimallis määratletakse järgmised projektiatribuudid.</span><span class="sxs-lookup"><span data-stu-id="4cfda-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="4cfda-107">Tööaeg (sh algus- ja lõppaeg)</span><span class="sxs-lookup"><span data-stu-id="4cfda-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="4cfda-108">Tööpäevad</span><span class="sxs-lookup"><span data-stu-id="4cfda-108">Working days</span></span>
- <span data-ttu-id="4cfda-109">Kalendri erandid (nt mitte-tööpäevad)</span><span class="sxs-lookup"><span data-stu-id="4cfda-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="4cfda-110">Projektile rakendatud kalendrimall on teie organisatsiooni sätetes määratletud kalendrimalli koopia.</span><span class="sxs-lookup"><span data-stu-id="4cfda-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="4cfda-111">Kui muudate kalendrimalli, siis need muudatused ei laiene projekti tööajale.</span><span class="sxs-lookup"><span data-stu-id="4cfda-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="4cfda-112">Projekti tööaja muutmiseks tuleb rakendada uus mall.</span><span class="sxs-lookup"><span data-stu-id="4cfda-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="4cfda-113">Oma organisatsiooni jaoks kalendrimalli loomiseks on kaks põhinõuet.</span><span class="sxs-lookup"><span data-stu-id="4cfda-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="4cfda-114">Määratlege malli soovitud tööaeg, kasutades uut või olemasolevat broneeritavat ressurssi.</span><span class="sxs-lookup"><span data-stu-id="4cfda-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="4cfda-115">Looge uus kalendrimall ja seostage mall broneeritava ressursiga.</span><span class="sxs-lookup"><span data-stu-id="4cfda-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="4cfda-116">**Määratlege malli tööaeg**</span><span class="sxs-lookup"><span data-stu-id="4cfda-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="4cfda-117">Avage **Ressursid** \> **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="4cfda-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="4cfda-118">Looge kalendrimallis viidatav uus ressurss või valige olemasolev ressurss.</span><span class="sxs-lookup"><span data-stu-id="4cfda-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="4cfda-119">Valige ressursi vahekaart **Tööaeg** ja järgige kalendrireeglite konfigureerimiseks [ressursi töötundide](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) konfigureerimine suuniseid.</span><span class="sxs-lookup"><span data-stu-id="4cfda-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="4cfda-120">**Looge uus kalendrimall**</span><span class="sxs-lookup"><span data-stu-id="4cfda-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="4cfda-121">Avage **Sätted** \> **Kalendrimall**.</span><span class="sxs-lookup"><span data-stu-id="4cfda-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="4cfda-122">Valige **Uus** ning sisestage nimi, kirjeldus ja malliressurss.</span><span class="sxs-lookup"><span data-stu-id="4cfda-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="4cfda-123">Kui ressursile viidatakse kalendrimallis, seostatakse kalendrimalliga ressursi kalendri koopia.</span><span class="sxs-lookup"><span data-stu-id="4cfda-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="4cfda-124">Kui kopeeritud malli tööaega muudetakse, ei laiene need muudatused kalendermallile.</span><span class="sxs-lookup"><span data-stu-id="4cfda-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="4cfda-125">Nüüd saate seostada töömalli projektikalendri malliga.</span><span class="sxs-lookup"><span data-stu-id="4cfda-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

