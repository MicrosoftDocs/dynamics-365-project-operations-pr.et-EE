---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 28, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 28, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280213"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="d0f92-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 28, V3</span><span class="sxs-lookup"><span data-stu-id="d0f92-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d0f92-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="d0f92-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d0f92-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="d0f92-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d0f92-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="d0f92-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d0f92-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="d0f92-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d0f92-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d0f92-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d0f92-109">Selles teemas loetletakse funktsioonid ja parandused, mis on uued või muudetud rakenduse Project Service Automation V3 väljalaske 28 jaoks. See versiooni järgu number on V3.10.46.32 ja on üldiselt saadaval ise värskendamise kaudu jaanuaris 2021.</span><span class="sxs-lookup"><span data-stu-id="d0f92-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="d0f92-110">Värskenduste väljalase 28</span><span class="sxs-lookup"><span data-stu-id="d0f92-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d0f92-111">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="d0f92-111">Bug fixes</span></span>

<span data-ttu-id="d0f92-112">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="d0f92-112">**Time and Expense**</span></span>

<span data-ttu-id="d0f92-113">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="d0f92-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="d0f92-114">Kasutajad saavad kinnitatud ja esitatud ajakirjete värskendamiseks kasutada funktsiooni **Hulgiredigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="d0f92-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="d0f92-115">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="d0f92-115">**Project Management**</span></span>

<span data-ttu-id="d0f92-116">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="d0f92-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d0f92-117">Juhtudel, kui toimingu GUID-d tõlgendatakse arvuna, ei saa tööülesandeid redigeerimiseks avada lehe **Tööjaotuse struktuur** riba **Tööülesande redigeerimine** abil.</span><span class="sxs-lookup"><span data-stu-id="d0f92-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="d0f92-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d0f92-118">**Sales**</span></span>

<span data-ttu-id="d0f92-119">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="d0f92-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d0f92-120">Null-viite erand genereeritakse lisandmooduli **GetEstimatesForProject** käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="d0f92-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="d0f92-121">Suvand **Märgi arveldamiseks valmis** osamaksete ruudustikus värskendab atribuute ainult osaliselt, välja arvatud atribuut **InvoiceStatus**, mida värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="d0f92-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]