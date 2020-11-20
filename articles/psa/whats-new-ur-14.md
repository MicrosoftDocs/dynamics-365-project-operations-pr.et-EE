---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 14, V3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 14, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124813"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="ccf8b-103">Rakenduse Project Service Automation, värskenduse väljaanne 14, v3</span><span class="sxs-lookup"><span data-stu-id="ccf8b-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="ccf8b-104">Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="ccf8b-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ccf8b-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ccf8b-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="ccf8b-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ccf8b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ccf8b-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 14 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="ccf8b-110">Selle versiooni järgu number on V3.10.4.21 ja see on saadaval järgmise ajakava järgi.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="ccf8b-111">**Üldine saadavus (automaatvärskendus):** jaanuar 2020</span><span class="sxs-lookup"><span data-stu-id="ccf8b-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="ccf8b-112">**Automaatvärskendus:** veebruar 2020</span><span class="sxs-lookup"><span data-stu-id="ccf8b-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="ccf8b-113">Värskenduste väljalase 14</span><span class="sxs-lookup"><span data-stu-id="ccf8b-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="ccf8b-114">Täiustused</span><span class="sxs-lookup"><span data-stu-id="ccf8b-114">Enhancements</span></span>

- <span data-ttu-id="ccf8b-115">Sales</span><span class="sxs-lookup"><span data-stu-id="ccf8b-115">Sales</span></span>

     - <span data-ttu-id="ccf8b-116">Jaotise **Hinnapakkumise rea üksikasjad** kohandatud välja väärtused kopeeritakse jaotisse **Projektilepingu rea üksikasjad** siis, kui hinnapakkumine värskendatakse olekusse **Suletud võidetuna**.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="ccf8b-117">Kinnitatud projekte saab **sulgeda kaotatuna**.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="ccf8b-118">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="ccf8b-118">Resource Management</span></span>

     - <span data-ttu-id="ccf8b-119">Broneeringute pikendamisel kuvatakse kasutajatele kinnitusega dialoogiakent, et võtta kokku broneeringu tulemused ja anda link broneeringute haldamise juurde.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="ccf8b-120">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="ccf8b-120">Bug fixes</span></span>

- <span data-ttu-id="ccf8b-121">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="ccf8b-121">Time and Expense</span></span>

     - <span data-ttu-id="ccf8b-122">Parandatud: täiustatud kasutajakogemust, kui kasutaja ei ole valinud parandamiseks ühtegi kirjet.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="ccf8b-123">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="ccf8b-123">Resource Management</span></span>

     - <span data-ttu-id="ccf8b-124">Parandatud: ressursi mitmekordne broneerimine ujutab broneeritava ressursi üle.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="ccf8b-125">Sales</span><span class="sxs-lookup"><span data-stu-id="ccf8b-125">Sales</span></span>

     - <span data-ttu-id="ccf8b-126">Parandatud: kogu müügihinda ei arvutata enne, kui kasutaja sisestab ka projekti kuluprognoosi omahinna.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="ccf8b-127">Parandatud: hinnapakkumise sulgemine olekus **Võidetud** ebaõnnestub, kui seotud projekti leping ei ole olekus **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="ccf8b-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

