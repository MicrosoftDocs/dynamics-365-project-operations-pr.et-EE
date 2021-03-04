---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 17.5, Hotfix, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 17.5, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: cd4142176258820f4718f457ca8610f19f584a32
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143700"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="bcf09-103">Rakenduse Project Service Automation, värskenduse väljaanne 17.5, v3</span><span class="sxs-lookup"><span data-stu-id="bcf09-103">Project Service Automation Update Release 17.5, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bcf09-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="bcf09-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bcf09-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="bcf09-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="bcf09-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="bcf09-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bcf09-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="bcf09-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="bcf09-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bcf09-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bcf09-109">Selles teemas loetletakse V3 värskenduse väljalaske 17.5 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="bcf09-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="bcf09-110">Selle versiooni järgunumber on V3.10.7.32 ja see on märtsis 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="bcf09-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="bcf09-111">Värskenduste väljalase 17.5</span><span class="sxs-lookup"><span data-stu-id="bcf09-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bcf09-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="bcf09-112">Bug fixes</span></span>


<span data-ttu-id="bcf09-113">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="bcf09-113">**Project Management**</span></span>

- <span data-ttu-id="bcf09-114">Parandatud: käsitletakse serveripoolse sünkroonimise probleeme, mis ilmnevad pika kestusega tööülesannete korral.</span><span class="sxs-lookup"><span data-stu-id="bcf09-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="bcf09-115">Parandatud: käsitletakse 24-tunniste töötundide malli poolt ülesandele valesti lisatavat täiendavat päeva.</span><span class="sxs-lookup"><span data-stu-id="bcf09-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="bcf09-116">Parandatud: käsitletakse +13 GMT töötundide malli ülesannete valet nihutamist päev varemaks.</span><span class="sxs-lookup"><span data-stu-id="bcf09-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

