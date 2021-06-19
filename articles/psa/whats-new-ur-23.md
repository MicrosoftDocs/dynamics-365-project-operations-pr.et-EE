---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 23, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 23, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006461"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="359f2-103">Rakenduse Project Service Automation, värskenduse väljaanne 23, v3</span><span class="sxs-lookup"><span data-stu-id="359f2-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="359f2-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="359f2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="359f2-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="359f2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="359f2-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="359f2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="359f2-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="359f2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="359f2-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="359f2-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="359f2-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 23 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="359f2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="359f2-110">Selle versiooni järgunumber on V 3.10.34.30 ja see on augustis 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="359f2-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="359f2-111">Värskenduste väljalase 23</span><span class="sxs-lookup"><span data-stu-id="359f2-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="359f2-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="359f2-112">Bug fixes</span></span>

<span data-ttu-id="359f2-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="359f2-113">**Time and Expense**</span></span>

<span data-ttu-id="359f2-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="359f2-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="359f2-115">Servajuhtumi käsitlemine suvandis **Projektimeeskonnaliikme kustutamine**, et pakkuda mõttekat erandit.</span><span class="sxs-lookup"><span data-stu-id="359f2-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="359f2-116">Ülesande importimise tulemuseks on tühi eemaldamise ekraan.</span><span class="sxs-lookup"><span data-stu-id="359f2-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="359f2-117">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="359f2-117">**Resource Management**</span></span>

<span data-ttu-id="359f2-118">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="359f2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="359f2-119">**Ressursikasutuse ruudustiku ressursi kaardil** kuvatakse valed andmed, kui ajaskaala on pikem kui viis päeva.</span><span class="sxs-lookup"><span data-stu-id="359f2-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="359f2-120">Kui kliendid loovad broneeritava ressursi, siis lisandmoodulil aeg-ajalt ei õnnestu lisada ressurssi automaatselt Microsoft Office 365 rühma.</span><span class="sxs-lookup"><span data-stu-id="359f2-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="359f2-121">Vaade **Vastavusseviimine** kuvab vaates **Nädal** või **Kuu** käsitsi kontuurid valesti.</span><span class="sxs-lookup"><span data-stu-id="359f2-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="359f2-122">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="359f2-122">**Project Management**</span></span>

<span data-ttu-id="359f2-123">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="359f2-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="359f2-124">Liiga suur hulk olemeid **RetrieveMultiple suvandi usersettings jaoks** põhjustab projektide kinnitamiste ja teiste toimingute jõudluse halvenemist.</span><span class="sxs-lookup"><span data-stu-id="359f2-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="359f2-125">Ruudustiku **Ülesande planeerimise** ressursi otsing on piiratud ainult kuni viie projektimeeskonna meeskonnaliikmeni.</span><span class="sxs-lookup"><span data-stu-id="359f2-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="359f2-126">Ruudustiku **Ülesande planeerimine** ressursiotsing ei filtreeri passiivseid ressursse.</span><span class="sxs-lookup"><span data-stu-id="359f2-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="359f2-127">Käsitsi režiim ei tööta projekti planeerimise tööjaotuse struktuuris ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="359f2-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="359f2-128">Ruudustik **Ülesande planeerimine** kuvab **Passiivsed tehingukategooriad**.</span><span class="sxs-lookup"><span data-stu-id="359f2-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="359f2-129">Kui ülesandel on mitu määramist, ümardab ruudustik **Ressursi määramine** valesti.</span><span class="sxs-lookup"><span data-stu-id="359f2-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="359f2-130">Ühe ülesande planeeritud kulu ja tegeliku kulu ümardamise väärtused on erinevad.</span><span class="sxs-lookup"><span data-stu-id="359f2-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="359f2-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="359f2-131">**Sales**</span></span>

<span data-ttu-id="359f2-132">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="359f2-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="359f2-133">Suvandi **Too kõik tehingukategooriad** topeltklõpsamine loob mitu rida.</span><span class="sxs-lookup"><span data-stu-id="359f2-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]