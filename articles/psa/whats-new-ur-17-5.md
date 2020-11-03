---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 17.5, Hotfix, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 17.5, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074911"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="580c2-103">Rakenduse Project Service Automation, värskenduse väljaanne 17.5, v3</span><span class="sxs-lookup"><span data-stu-id="580c2-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="580c2-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="580c2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="580c2-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="580c2-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="580c2-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="580c2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="580c2-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="580c2-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="580c2-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="580c2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="580c2-109">Selles teemas loetletakse V3 värskenduse väljalaske 17.5 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="580c2-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="580c2-110">Selle versiooni järgunumber on V3.10.7.32 ja see on märtsis 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="580c2-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="580c2-111">Värskenduste väljalase 17.5</span><span class="sxs-lookup"><span data-stu-id="580c2-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="580c2-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="580c2-112">Bug fixes</span></span>


<span data-ttu-id="580c2-113">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="580c2-113">**Project Management**</span></span>

- <span data-ttu-id="580c2-114">Parandatud: käsitletakse serveripoolse sünkroonimise probleeme, mis ilmnevad pika kestusega tööülesannete korral.</span><span class="sxs-lookup"><span data-stu-id="580c2-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="580c2-115">Parandatud: käsitletakse 24-tunniste töötundide malli poolt ülesandele valesti lisatavat täiendavat päeva.</span><span class="sxs-lookup"><span data-stu-id="580c2-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="580c2-116">Parandatud: käsitletakse +13 GMT töötundide malli ülesannete valet nihutamist päev varemaks.</span><span class="sxs-lookup"><span data-stu-id="580c2-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

