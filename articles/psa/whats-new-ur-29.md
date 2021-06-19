---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 29, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 29, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010466"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="4fb67-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 29, V3</span><span class="sxs-lookup"><span data-stu-id="4fb67-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4fb67-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="4fb67-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4fb67-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="4fb67-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4fb67-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="4fb67-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4fb67-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="4fb67-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4fb67-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4fb67-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4fb67-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 29 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="4fb67-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="4fb67-110">Selle versiooni järgu number on V3.10.47.7 ja see on kõigile kättesaadav 2021. a veebruaris ise värskendamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="4fb67-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="4fb67-111">Värskenduste väljalase 29</span><span class="sxs-lookup"><span data-stu-id="4fb67-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4fb67-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="4fb67-112">Bug fixes</span></span>

<span data-ttu-id="4fb67-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="4fb67-113">**Time and Expense**</span></span>

<span data-ttu-id="4fb67-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="4fb67-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4fb67-115">Kasutajad ei näe ajakirje ruudustikus mitte-tööpäevadel registreeritud töötunne.</span><span class="sxs-lookup"><span data-stu-id="4fb67-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="4fb67-116">Kinnitatud kulukirjeid saab ruudustikus redigeerida.</span><span class="sxs-lookup"><span data-stu-id="4fb67-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="4fb67-117">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="4fb67-117">**Project Management**</span></span>

<span data-ttu-id="4fb67-118">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="4fb67-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="4fb67-119">Puuduvad valideerimisloogikad, mis tagavad, et ressursi määramise panuse tundide arv ei saa olla negatiivne.</span><span class="sxs-lookup"><span data-stu-id="4fb67-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="4fb67-120">Kohandatud toiming **AssignResourcesForTask** värskendab kõiki välja, mitte ainult muudetud välju.</span><span class="sxs-lookup"><span data-stu-id="4fb67-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="4fb67-121">Projekti kopeerimisel lisandmoodulite või töövoogudega keskkonda, mis on registreeritud sündmusele **CreateProject**, ei värskendatud atribuuti **msdyn_bulkgenerationstatus** kui **CopyWBSToProject** nurjub.</span><span class="sxs-lookup"><span data-stu-id="4fb67-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="4fb67-122">Projekti kalendri laiendamisel ei sordita tööpäevi kasvavas järjekorras, põhjustades mõne projekti tööülesande värskenduste nurjumise.</span><span class="sxs-lookup"><span data-stu-id="4fb67-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="4fb67-123">Projektijuhi muutmine olemasolevas projektis käivitab organisatsiooniüksuse vaikeloogika.</span><span class="sxs-lookup"><span data-stu-id="4fb67-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="4fb67-124">**Müük**</span><span class="sxs-lookup"><span data-stu-id="4fb67-124">**Sales**</span></span>

<span data-ttu-id="4fb67-125">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="4fb67-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="4fb67-126">Vahekaart **Lepingu täitmine** lehel **Leping** nurjub lähtestamisel vaikselt, kui lepinguridu pole olemas.</span><span class="sxs-lookup"><span data-stu-id="4fb67-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>