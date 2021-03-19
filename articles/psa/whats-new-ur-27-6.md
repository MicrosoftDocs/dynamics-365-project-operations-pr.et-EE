---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 27.6, Hotfix, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 27.6 V3 funktsioonid ja parandused.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/17/2021
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
ms.openlocfilehash: f6576c6c5660ff6e8e53286ae226c8278a33f2be
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481245"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="55964-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 27.6, V3</span><span class="sxs-lookup"><span data-stu-id="55964-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="55964-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="55964-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="55964-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="55964-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="55964-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="55964-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="55964-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="55964-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="55964-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="55964-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="55964-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 27.6 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="55964-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="55964-110">Selle versiooni järgunumber on V3.10.45.120 ja see on jaanuaris 2021 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="55964-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="55964-111">Värskenduste väljalase 27.6</span><span class="sxs-lookup"><span data-stu-id="55964-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="55964-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="55964-112">Bug fixes</span></span>


<span data-ttu-id="55964-113">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="55964-113">**Resource Management**</span></span>

<span data-ttu-id="55964-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="55964-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="55964-115">Ressursi saadavuse otsimisel kutsutakse **ExpandCalendar** iga ressursi jaoks, mille jaoks pole kalendri reegleid rakendatud.</span><span class="sxs-lookup"><span data-stu-id="55964-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
