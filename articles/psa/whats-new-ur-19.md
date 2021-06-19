---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 19, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 19, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 7812bc41f32f9d4116c63990059f7dbc0351cf9e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006596"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="ae3d5-103">Rakenduse Project Service Automation, värskenduse väljaanne 19, v3</span><span class="sxs-lookup"><span data-stu-id="ae3d5-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ae3d5-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ae3d5-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ae3d5-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ae3d5-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ae3d5-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ae3d5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ae3d5-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 19 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="ae3d5-110">Selle versiooni järgu number on V3.10.30.41 ja on üldiselt saadaval 2020. a mai enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="ae3d5-111">Värskenduste väljalase 19</span><span class="sxs-lookup"><span data-stu-id="ae3d5-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ae3d5-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="ae3d5-112">Bug fixes</span></span>

<span data-ttu-id="ae3d5-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="ae3d5-113">**Time and Expense**</span></span>

<span data-ttu-id="ae3d5-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="ae3d5-115">Ajakirjest importimisel tuletatud tõrked pole õigesti esile toodud.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="ae3d5-116">Ajakirje ruudustik ei toeta välja **Ainult kuupäev** käitumist.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="ae3d5-117">Projekti ressursid ei saa projektiga kulu luua.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="ae3d5-118">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="ae3d5-118">**Project Management**</span></span>

<span data-ttu-id="ae3d5-119">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="ae3d5-120">Alamülesande alamülesanne põhjustab vale koormuse prognoosi arvutamise lõpileviimisel (EAC).</span><span class="sxs-lookup"><span data-stu-id="ae3d5-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="ae3d5-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ae3d5-121">**Sales**</span></span>

<span data-ttu-id="ae3d5-122">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="ae3d5-123">**Ümberarvutamine** ei tööta kulude lepingurea üksikasjadega või hinnapakkumise rea üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="ae3d5-124">**Uuendatud hinnad** puuduvad kulude prognoosi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="ae3d5-125">Kliendid ei saa valida lehelt **Projekti leping** kohandatud lepingu oleku põhjust.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="ae3d5-126">Kliendikogemuse nõrgem tulemus, kui luua hinnapakkumisest kohandatud hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="ae3d5-127">Kliendid kogevad vastuolu **ühiku** vaikeväärtustega lehtedel **Hinnapakkumise rea üksikasjad** ja **Lepingu rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="ae3d5-128">Mittearveldatavate kannete kategooria üksuste lisamine arveldatavale lepingureale ei austa kande kategooria **mittearveldatavat** arveldustüüpi.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="ae3d5-129">Kliendid ei saa varem loodud lepingutes kasutada äsja lisatud rolle ja kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="ae3d5-130">Kliendid kogevad ebavajaliku toomise nõrgemat tulemust PreValidateProjectTeamMemberUpdate.cs korral</span><span class="sxs-lookup"><span data-stu-id="ae3d5-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="ae3d5-131">Rollid luuakse kui mittearveldatavad loendis **Ressursikategooriad** tuleb lisada vahekaardile **Arveldatavad rollid** kui **Mittearveldatavad** projekti lepingureas.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="ae3d5-132">Projekti loomisel võivad kliendid halvenenud tulemusi kogeda, kuna **GetBookableResourceIdFromUser** toob esmase ID asemel kõik arvestusliku ressursi veerud.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="ae3d5-133">Olemist **TransactionType** puudub eelvalideerimise uuenduse lisandmoodul, et takistada kasutajatel sisestada **Üksusi** ja **Üksusegruppe**, mis ei kehti kandetüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="ae3d5-134">Etapp **Eemaldamine** ei tööta ajakirje impordi puhul.</span><span class="sxs-lookup"><span data-stu-id="ae3d5-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]