---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 25, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 25, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183538"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="05368-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 25, V3</span><span class="sxs-lookup"><span data-stu-id="05368-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="05368-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="05368-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="05368-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="05368-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="05368-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="05368-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="05368-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="05368-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="05368-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="05368-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="05368-109">Selles teemas loetletakse funktsioonid ja parandused, mis on uued või muudetud rakenduse Project Service Automation versiooni 3 jaoks, värskenduses 25. See versiooni järgu number on V 3.10.43.76 ja on üldiselt saadaval ise värskendamise kaudu oktoobris 2020.</span><span class="sxs-lookup"><span data-stu-id="05368-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="05368-110">Värskenduste väljalase 25</span><span class="sxs-lookup"><span data-stu-id="05368-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="05368-111">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="05368-111">Bug fixes</span></span>

<span data-ttu-id="05368-112">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="05368-112">**Time and Expense**</span></span>

<span data-ttu-id="05368-113">Järgmised probleemid on parandatud.</span><span class="sxs-lookup"><span data-stu-id="05368-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="05368-114">Ajakirje diagramm näitas täiendavaid andmeid liiga suure toodud intervalli põhjal.</span><span class="sxs-lookup"><span data-stu-id="05368-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="05368-115">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="05368-115">**Resource Management**</span></span>

<span data-ttu-id="05368-116">Järgmised probleemid on parandatud.</span><span class="sxs-lookup"><span data-stu-id="05368-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="05368-117">Lisatud paki juurutamise kood, et jätta teenuse Universal Resource Scheduling paiga importimine vahele, kui uuema versiooni paik on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="05368-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="05368-118">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="05368-118">**Project Management**</span></span>

<span data-ttu-id="05368-119">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="05368-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="05368-120">Parandatud on ümardamise ja vahetuskursi lahknevusi, mis põhjustasid projekti jälgimise ruudustikus valesti planeeritud kulu.</span><span class="sxs-lookup"><span data-stu-id="05368-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="05368-121">Vormil **Projekt** kahe või rhkema reageerimisruudustiku kuvamise võimaluse tugi.</span><span class="sxs-lookup"><span data-stu-id="05368-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="05368-122">Esitatud valideerimine, et lahendada võime määrata ülesanne, mis on kalendri lõpukuupäevast hilisem, mis põhjustab ressursi määramise nurjumise.</span><span class="sxs-lookup"><span data-stu-id="05368-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="05368-123">Parandatud on vea käsitlemine, et tegeleda null-viite erandiga, mis loodi järgnevast.</span><span class="sxs-lookup"><span data-stu-id="05368-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="05368-124">Lisandmoodul **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="05368-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="05368-125">**PreValidateProjectTaskCreate**, kui projekti ülesanne on loodud ilma seostatud pojektita</span><span class="sxs-lookup"><span data-stu-id="05368-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="05368-126">Lisandmoodul **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="05368-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="05368-127">Lisandmoodul **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="05368-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="05368-128">Lisandmoodul **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="05368-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="05368-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="05368-129">**Sales**</span></span>

<span data-ttu-id="05368-130">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="05368-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="05368-131">Täiustatud vigade käsitlemine, et lahendada null-viite erandid, mis on loodud suvandist **Projekti kopeerimine: prognoosib abiressursi halduse**.</span><span class="sxs-lookup"><span data-stu-id="05368-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="05368-132">Valik **Pole arveldamiseks valmis** suvandis **Aja ja materjali arveldamise võlgnevus** ei tühjenda arveldamise olekut.</span><span class="sxs-lookup"><span data-stu-id="05368-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="05368-133">Parandatud valesti sildistatud nupud **Hinnad** vahekaartidel **Rolli hind** ja **Kataloogi üksus**.</span><span class="sxs-lookup"><span data-stu-id="05368-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
