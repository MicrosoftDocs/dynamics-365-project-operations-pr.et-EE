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
ms.openlocfilehash: 829f0941f255aab11a37cacd90c0dca6f99bc2d2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948729"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="b3cb0-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 27.6, V3</span><span class="sxs-lookup"><span data-stu-id="b3cb0-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="b3cb0-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b3cb0-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b3cb0-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b3cb0-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b3cb0-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b3cb0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b3cb0-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 27.6 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="b3cb0-110">Selle versiooni järgunumber on V3.10.45.120 ja see on jaanuaris 2021 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="b3cb0-111">Värskenduste väljalase 27.6</span><span class="sxs-lookup"><span data-stu-id="b3cb0-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b3cb0-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="b3cb0-112">Bug fixes</span></span>


<span data-ttu-id="b3cb0-113">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="b3cb0-113">**Resource Management**</span></span>

<span data-ttu-id="b3cb0-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b3cb0-115">Ressursi saadavuse otsimisel kutsutakse **ExpandCalendar** iga ressursi jaoks, mille jaoks pole kalendri reegleid rakendatud.</span><span class="sxs-lookup"><span data-stu-id="b3cb0-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]