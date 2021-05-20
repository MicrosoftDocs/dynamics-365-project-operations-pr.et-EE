---
title: Töötundide malli loomine
description: Selles teemas kirjeldatakse, kuidas luua Project Service’is tööaja malli.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981250"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="75ae6-103">Töötundide malli loomine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="75ae6-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="75ae6-104">Projekti loomiseks ja haldamiseks peate projektile rakendama kalendrimalli.</span><span class="sxs-lookup"><span data-stu-id="75ae6-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="75ae6-105">Kalendrimallis määratletakse järgmised projektiatribuudid.</span><span class="sxs-lookup"><span data-stu-id="75ae6-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="75ae6-106">Tööaeg (sh algus- ja lõppaeg)</span><span class="sxs-lookup"><span data-stu-id="75ae6-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="75ae6-107">Tööpäevad</span><span class="sxs-lookup"><span data-stu-id="75ae6-107">Working days</span></span>
- <span data-ttu-id="75ae6-108">Kalendri erandid (nt mitte-tööpäevad)</span><span class="sxs-lookup"><span data-stu-id="75ae6-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="75ae6-109">Projektile rakendatud kalendrimall on teie organisatsiooni sätetes määratletud kalendrimalli koopia.</span><span class="sxs-lookup"><span data-stu-id="75ae6-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="75ae6-110">Kui muudate kalendrimalli, siis need muudatused ei laiene projekti tööajale.</span><span class="sxs-lookup"><span data-stu-id="75ae6-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="75ae6-111">Projekti tööaja muutmiseks tuleb rakendada uus mall.</span><span class="sxs-lookup"><span data-stu-id="75ae6-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="75ae6-112">Oma organisatsiooni jaoks kalendrimalli loomiseks on kaks põhinõuet.</span><span class="sxs-lookup"><span data-stu-id="75ae6-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="75ae6-113">Määratlege malli soovitud tööaeg, kasutades uut või olemasolevat broneeritavat ressurssi.</span><span class="sxs-lookup"><span data-stu-id="75ae6-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="75ae6-114">Looge uus kalendrimall ja seostage mall broneeritava ressursiga.</span><span class="sxs-lookup"><span data-stu-id="75ae6-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="75ae6-115">**Määratlege malli tööaeg**</span><span class="sxs-lookup"><span data-stu-id="75ae6-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="75ae6-116">Avage **Ressursid** \> **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="75ae6-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="75ae6-117">Looge kalendrimallis viidatav uus ressurss või valige olemasolev ressurss.</span><span class="sxs-lookup"><span data-stu-id="75ae6-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="75ae6-118">Valige ressursi vahekaart **Tööaeg** ja järgige kalendrireeglite konfigureerimiseks [ressursi töötundide](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) konfigureerimine suuniseid.</span><span class="sxs-lookup"><span data-stu-id="75ae6-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="75ae6-119">**Looge uus kalendrimall**</span><span class="sxs-lookup"><span data-stu-id="75ae6-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="75ae6-120">Avage **Sätted** \> **Kalendrimall**.</span><span class="sxs-lookup"><span data-stu-id="75ae6-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="75ae6-121">Valige **Uus** ning sisestage nimi, kirjeldus ja malliressurss.</span><span class="sxs-lookup"><span data-stu-id="75ae6-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="75ae6-122">Kui ressursile viidatakse kalendrimallis, seostatakse kalendrimalliga ressursi kalendri koopia.</span><span class="sxs-lookup"><span data-stu-id="75ae6-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="75ae6-123">Kui kopeeritud malli tööaega muudetakse, ei laiene need muudatused kalendermallile.</span><span class="sxs-lookup"><span data-stu-id="75ae6-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="75ae6-124">Vt ka</span><span class="sxs-lookup"><span data-stu-id="75ae6-124">See Also</span></span>  
 [<span data-ttu-id="75ae6-125">Ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="75ae6-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
