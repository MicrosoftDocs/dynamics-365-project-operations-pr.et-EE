---
title: Mida on uut rakenduse Project Service Automation värskenduse väljaandes 14, v3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 14, v3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750963"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="4bcb9-103">Rakenduse Project Service Automation V3, värskenduse väljaanne 14</span><span class="sxs-lookup"><span data-stu-id="4bcb9-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="4bcb9-104">Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="4bcb9-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4bcb9-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4bcb9-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="4bcb9-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4bcb9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4bcb9-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 14 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="4bcb9-110">Selle versiooni järgu number on V3.10.4.21 ja see on saadaval järgmise ajakava järgi.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="4bcb9-111">**Üldine saadavus (automaatvärskendus):** jaanuar 2020</span><span class="sxs-lookup"><span data-stu-id="4bcb9-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="4bcb9-112">**Automaatvärskendus:** veebruar 2020</span><span class="sxs-lookup"><span data-stu-id="4bcb9-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="4bcb9-113">Värskenduste väljalase 14</span><span class="sxs-lookup"><span data-stu-id="4bcb9-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="4bcb9-114">Täiustused</span><span class="sxs-lookup"><span data-stu-id="4bcb9-114">Enhancements</span></span>

- <span data-ttu-id="4bcb9-115">Sales</span><span class="sxs-lookup"><span data-stu-id="4bcb9-115">Sales</span></span>

     - <span data-ttu-id="4bcb9-116">Jaotise **Hinnapakkumise rea üksikasjad** kohandatud välja väärtused kopeeritakse jaotisse **Projektilepingu rea üksikasjad** siis, kui hinnapakkumine värskendatakse olekusse **Suletud võidetuna**.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="4bcb9-117">Kinnitatud projekte saab **sulgeda kaotatuna**.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="4bcb9-118">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="4bcb9-118">Resource Management</span></span>

     - <span data-ttu-id="4bcb9-119">Broneeringute pikendamisel kuvatakse kasutajatele kinnitusega dialoogiakent, et võtta kokku broneeringu tulemused ja anda link broneeringute haldamise juurde.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="4bcb9-120">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="4bcb9-120">Bug fixes</span></span>

- <span data-ttu-id="4bcb9-121">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="4bcb9-121">Time and Expense</span></span>

     - <span data-ttu-id="4bcb9-122">Parandatud: täiustatud kasutajakogemust, kui kasutaja ei ole valinud parandamiseks ühtegi kirjet.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="4bcb9-123">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="4bcb9-123">Resource Management</span></span>

     - <span data-ttu-id="4bcb9-124">Parandatud: ressursi mitmekordne broneerimine ujutab broneeritava ressursi üle.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="4bcb9-125">Sales</span><span class="sxs-lookup"><span data-stu-id="4bcb9-125">Sales</span></span>

     - <span data-ttu-id="4bcb9-126">Parandatud: kogu müügihinda ei arvutata enne, kui kasutaja sisestab ka projekti kuluprognoosi omahinna.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="4bcb9-127">Parandatud: hinnapakkumise sulgemine olekus **Võidetud** ebaõnnestub, kui seotud projekti leping ei ole olekus **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

