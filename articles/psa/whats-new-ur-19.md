---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 19, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 19, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126832"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="4cd65-103">Rakenduse Project Service Automation, värskenduse väljaanne 19, v3</span><span class="sxs-lookup"><span data-stu-id="4cd65-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="4cd65-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="4cd65-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4cd65-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="4cd65-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4cd65-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="4cd65-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4cd65-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="4cd65-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4cd65-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4cd65-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4cd65-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 19 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="4cd65-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="4cd65-110">Selle versiooni järgu number on V3.10.30.41 ja on üldiselt saadaval 2020. a mai enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="4cd65-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="4cd65-111">Värskenduste väljalase 19</span><span class="sxs-lookup"><span data-stu-id="4cd65-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4cd65-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="4cd65-112">Bug fixes</span></span>

<span data-ttu-id="4cd65-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="4cd65-113">**Time and Expense**</span></span>

<span data-ttu-id="4cd65-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="4cd65-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="4cd65-115">Ajakirjest importimisel tuletatud tõrked pole õigesti esile toodud.</span><span class="sxs-lookup"><span data-stu-id="4cd65-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="4cd65-116">Ajakirje ruudustik ei toeta välja **Ainult kuupäev** käitumist.</span><span class="sxs-lookup"><span data-stu-id="4cd65-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="4cd65-117">Projekti ressursid ei saa projektiga kulu luua.</span><span class="sxs-lookup"><span data-stu-id="4cd65-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="4cd65-118">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="4cd65-118">**Project Management**</span></span>

<span data-ttu-id="4cd65-119">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="4cd65-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="4cd65-120">Alamülesande alamülesanne põhjustab vale koormuse prognoosi arvutamise lõpileviimisel (EAC).</span><span class="sxs-lookup"><span data-stu-id="4cd65-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="4cd65-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4cd65-121">**Sales**</span></span>

<span data-ttu-id="4cd65-122">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="4cd65-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="4cd65-123">**Ümberarvutamine** ei tööta kulude lepingurea üksikasjadega või hinnapakkumise rea üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="4cd65-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="4cd65-124">**Uuendatud hinnad** puuduvad kulude prognoosi jaoks.</span><span class="sxs-lookup"><span data-stu-id="4cd65-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="4cd65-125">Kliendid ei saa valida lehelt **Projekti leping** kohandatud lepingu oleku põhjust.</span><span class="sxs-lookup"><span data-stu-id="4cd65-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="4cd65-126">Kliendikogemuse nõrgem tulemus, kui luua hinnapakkumisest kohandatud hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="4cd65-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="4cd65-127">Kliendid kogevad vastuolu **ühiku** vaikeväärtustega lehtedel **Hinnapakkumise rea üksikasjad** ja **Lepingu rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4cd65-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="4cd65-128">Mittearveldatavate kannete kategooria üksuste lisamine arveldatavale lepingureale ei austa kande kategooria **mittearveldatavat** arveldustüüpi.</span><span class="sxs-lookup"><span data-stu-id="4cd65-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="4cd65-129">Kliendid ei saa varem loodud lepingutes kasutada äsja lisatud rolle ja kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="4cd65-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="4cd65-130">Kliendid kogevad ebavajaliku toomise nõrgemat tulemust PreValidateProjectTeamMemberUpdate.cs korral</span><span class="sxs-lookup"><span data-stu-id="4cd65-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="4cd65-131">Rollid luuakse kui mittearveldatavad loendis **Ressursikategooriad** tuleb lisada vahekaardile **Arveldatavad rollid** kui **Mittearveldatavad** projekti lepingureas.</span><span class="sxs-lookup"><span data-stu-id="4cd65-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="4cd65-132">Projekti loomisel võivad kliendid halvenenud tulemusi kogeda, kuna **GetBookableResourceIdFromUser** toob esmase ID asemel kõik arvestusliku ressursi veerud.</span><span class="sxs-lookup"><span data-stu-id="4cd65-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="4cd65-133">Olemist **TransactionType** puudub eelvalideerimise uuenduse lisandmoodul, et takistada kasutajatel sisestada **Üksusi** ja **Üksusegruppe**, mis ei kehti kandetüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="4cd65-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="4cd65-134">Etapp **Eemaldamine** ei tööta ajakirje impordi puhul.</span><span class="sxs-lookup"><span data-stu-id="4cd65-134">The **Remove** step does not work for time entry import.</span></span>
