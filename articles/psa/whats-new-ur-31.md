---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 31, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 31, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945530"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="c1035-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 31, V3</span><span class="sxs-lookup"><span data-stu-id="c1035-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c1035-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="c1035-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c1035-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="c1035-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c1035-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="c1035-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c1035-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="c1035-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c1035-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c1035-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c1035-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 31 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="c1035-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="c1035-110">Selle versiooni järgu number on V3.10.52.77 ja on üldiselt saadaval 2021. a mai enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="c1035-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="c1035-111">Värskenduste väljalase 31</span><span class="sxs-lookup"><span data-stu-id="c1035-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c1035-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="c1035-112">Bug fixes</span></span>

<span data-ttu-id="c1035-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="c1035-113">**Time and Expense**</span></span>

<span data-ttu-id="c1035-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c1035-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c1035-115">Aja sisestamise juhtelemendi käsunupud lehel **Broneeritav ressurss** olid kõlbmatud.</span><span class="sxs-lookup"><span data-stu-id="c1035-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="c1035-116">Ajasisestuse kinnitamisel loodi väljal **Project.SetTrackingFields** nullviite erand.</span><span class="sxs-lookup"><span data-stu-id="c1035-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="c1035-117">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="c1035-117">**Resource Management**</span></span>

<span data-ttu-id="c1035-118">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c1035-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="c1035-119">**Meeskonna liikme** loomisel ei kuvata broneeringu seadistamise metaandmete sätet **Vaikimisi broneeritud oleku jaoks** õigesti.</span><span class="sxs-lookup"><span data-stu-id="c1035-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="c1035-120">Kui täiendate versioonilt PSA 1.X versioonile 3.X, nurjub versiooniuuendus **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="c1035-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="c1035-121">**Müük**</span><span class="sxs-lookup"><span data-stu-id="c1035-121">**Sales**</span></span>

<span data-ttu-id="c1035-122">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c1035-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="c1035-123">Tegelik tulu teisendab summad jälgimisruudustikus projekti valuutasse.</span><span class="sxs-lookup"><span data-stu-id="c1035-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="c1035-124">Valuuta vaikeväärtus on ebaselge, kui loote töölehe read, hinnapakkumise read ja lepinguread stsenaariumides, kus organisatsiooni baasvaluuta erineb projekti valuutast.</span><span class="sxs-lookup"><span data-stu-id="c1035-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="c1035-125">**Töölehe ootel paranduse valideerimise** päring ei filtreeri projekti alusel.</span><span class="sxs-lookup"><span data-stu-id="c1035-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="c1035-126">Ülejäänud müügid arvutatakse projektis valesti.</span><span class="sxs-lookup"><span data-stu-id="c1035-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="c1035-127">Kontaktil põhinevad hinnapakkumised nurjuvad, kui need luuakse ilma hinnakirjata.</span><span class="sxs-lookup"><span data-stu-id="c1035-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="c1035-128">Kui valite suvandi **Kinnita arve**, ei kuvata töötlemisnäidikut.</span><span class="sxs-lookup"><span data-stu-id="c1035-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="c1035-129">Kui valite suvandi **Loo arve**, ei kuvata töötlemisnäidikut.</span><span class="sxs-lookup"><span data-stu-id="c1035-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="c1035-130">Kaotatud hinnapakkumise sulgemisel broneeringuid ei tühistata.</span><span class="sxs-lookup"><span data-stu-id="c1035-130">Closing a quote as lost doesn't cancel the bookings.</span></span>






