---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 15, V3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 15, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 2112e70d7359e7f30725ef3069a18570da651c06
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119908"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="f6514-103">Rakenduse Project Service Automation, värskenduse väljaanne 15, v3</span><span class="sxs-lookup"><span data-stu-id="f6514-103">Project Service Automation Update Release 15, V3</span></span>

<span data-ttu-id="f6514-104">Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest.</span><span class="sxs-lookup"><span data-stu-id="f6514-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f6514-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="f6514-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f6514-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="f6514-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f6514-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht.</span><span class="sxs-lookup"><span data-stu-id="f6514-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f6514-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f6514-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f6514-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 15 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="f6514-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="f6514-110">Selle versiooni järgunumber on V3.10.5.28 ja see on jaanuaris 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="f6514-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="f6514-111">Värskenduste väljalase 15</span><span class="sxs-lookup"><span data-stu-id="f6514-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="f6514-112">Täiustused</span><span class="sxs-lookup"><span data-stu-id="f6514-112">Enhancements</span></span>

- <span data-ttu-id="f6514-113">Projektijuhtimine</span><span class="sxs-lookup"><span data-stu-id="f6514-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f6514-114">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="f6514-114">Bug fixes</span></span>

- <span data-ttu-id="f6514-115">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="f6514-115">Time and Expense</span></span>

  - <span data-ttu-id="f6514-116">Parandatud: lisada laadimise tõrke käsitlemine vastavusseviimise vaatesse.</span><span class="sxs-lookup"><span data-stu-id="f6514-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="f6514-117">Parandatud: projekti ressursside keskus: nimetada ebaselguse vähendamiseks ümber **Summa**.</span><span class="sxs-lookup"><span data-stu-id="f6514-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="f6514-118">Parandatud: reguleerida vaadet **Ajakirje kopeerimise veerud**, et see sisaldaks tüüpi.</span><span class="sxs-lookup"><span data-stu-id="f6514-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="f6514-119">Parandatud: aja kirje kestuse redigeerimine ruudustiku vaates põhjustab kümnendnumbreid kasutades mõne arvu korral tundmatu vea.</span><span class="sxs-lookup"><span data-stu-id="f6514-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="f6514-120">Projektijuhtimine</span><span class="sxs-lookup"><span data-stu-id="f6514-120">Project Management</span></span>

  - <span data-ttu-id="f6514-121">Parandatud: **Kasuta jälgimise aknas** suvandi rippmenüü laieneb nüüd vastavalt valikute laiusele.</span><span class="sxs-lookup"><span data-stu-id="f6514-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="f6514-122">Parandatud: projektide haldamisel +13 ajavööndis võivad ülesannete arvutused kuvada ebatäpseid tulemusi.</span><span class="sxs-lookup"><span data-stu-id="f6514-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="f6514-123">Parandatud: **Meeskonnaliikme lõpuaeg** 24-tunnise kalendri kasutamisel on parandatud.</span><span class="sxs-lookup"><span data-stu-id="f6514-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="f6514-124">Parandatud: **BPF** uuesti aktiveeritud **msdyn_project** põhivormis.</span><span class="sxs-lookup"><span data-stu-id="f6514-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="f6514-125">Parandatud: määramiste arvestamine ei ignoreeri enam ühte päeva.</span><span class="sxs-lookup"><span data-stu-id="f6514-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="f6514-126">Parandatud: projekti vormile on lisatud uus teavituste bänner, kui kasutaja ja projekti ajavöönd erineb.</span><span class="sxs-lookup"><span data-stu-id="f6514-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="f6514-127">Sales</span><span class="sxs-lookup"><span data-stu-id="f6514-127">Sales</span></span>

  - <span data-ttu-id="f6514-128">Parandatud: kulude prognoosi kategooria otsingut saab kasutada duplikaatide filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="f6514-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="f6514-129">Parandatud: kood **PluginDomain. ExecuteInTryCatchBlock(..)**-is ei peida enam erandi päritolu.</span><span class="sxs-lookup"><span data-stu-id="f6514-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="f6514-130">Parandatud: ei saa enam veateadet **Projekti otsingus** vormil **Hinnapakkumise rida**, kui projekte on rohkem kui 1000.</span><span class="sxs-lookup"><span data-stu-id="f6514-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="f6514-131">Parandatud: **Prognooside** ruudustik tööprognooside ja kuluprognooside kohta näitab nüüd õiget valuuta sümbolit.</span><span class="sxs-lookup"><span data-stu-id="f6514-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="f6514-132">Parandatud: kui organisatsioon värskendab PSA-d värskenduse väljaandega 14 või värskenduse väljaandega 15, ei ole vahekaart **Kavandamine** enam vormil **Projekt** tühi.</span><span class="sxs-lookup"><span data-stu-id="f6514-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
