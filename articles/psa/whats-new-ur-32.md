---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 32, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 32, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129661"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="10835-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 32, V3</span><span class="sxs-lookup"><span data-stu-id="10835-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="10835-104">Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest.</span><span class="sxs-lookup"><span data-stu-id="10835-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="10835-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="10835-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="10835-106">See ühildub rakendusega Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="10835-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="10835-107">Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus.</span><span class="sxs-lookup"><span data-stu-id="10835-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="10835-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="10835-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="10835-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 32 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="10835-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="10835-110">Selle versiooni järgu number on V3.10.53.108 ja see on üldiselt saadaval isevärskenduse kaudu 2021. aasta juunis.</span><span class="sxs-lookup"><span data-stu-id="10835-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="10835-111">Värskenduste väljalase 32</span><span class="sxs-lookup"><span data-stu-id="10835-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="10835-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="10835-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="10835-113">Üldist</span><span class="sxs-lookup"><span data-stu-id="10835-113">General</span></span>

- <span data-ttu-id="10835-114">Kui oluline värskendus nurjub, tuleks blokeerida ainult rakenduse peamised sisestuspunktid, et tagada ühiskasutuses olemite juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="10835-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="10835-115">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="10835-115">Time and Expense</span></span>

<span data-ttu-id="10835-116">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="10835-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="10835-117">**TimeEntriesImportFromResourceAssignment** ei säilita ressursi määramise kontuuri sektori algus- ja lõpuaega.</span><span class="sxs-lookup"><span data-stu-id="10835-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="10835-118">Kui valite ruudustikus **Ajakirje** suvandi **Avatud kirje**, võib teiste vormide valimine olla teile takistatud.</span><span class="sxs-lookup"><span data-stu-id="10835-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="10835-119">Kuigi impordite määramised ajakirjetele, võib kliendikoodi päring luua pika URL-i, mis põhjustab päringu nurjumist.</span><span class="sxs-lookup"><span data-stu-id="10835-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="10835-120">Ruudustikus **Ajakirje** ei jää fookus pärast väärtuse lahtrist kustutamist ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="10835-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="10835-121">Nupp **Hülga** on kaasaegse kinnitamine vaatest **Kinnitamise töötlemine** eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="10835-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="10835-122">Ajakirje hulgikinnituse stabiilsust ja jõudlust mõjutavad blokeeringud ja olemiga **Ajakirje** seotud kohanduste sobiva käsitsemise nurjumine.</span><span class="sxs-lookup"><span data-stu-id="10835-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="10835-123">Projekti kavandamine</span><span class="sxs-lookup"><span data-stu-id="10835-123">Project Planning</span></span>

- <span data-ttu-id="10835-124">Null-viite erand luuakse juhul, kui värskendate projekti, mille väljal **Lepinguüksus** on tühi väärtus.</span><span class="sxs-lookup"><span data-stu-id="10835-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="10835-125">**Värskenda projekti kogusummasid** arvutab projekti allesjäänud kulud ja ülejäänud müügid valesti.</span><span class="sxs-lookup"><span data-stu-id="10835-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="10835-126">Ülearused hinnaarvutused mõjutavad jõudlust, mis on seotud ressursi määramise kontuuride värskendustega.</span><span class="sxs-lookup"><span data-stu-id="10835-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="10835-127">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="10835-127">Resource Management</span></span>

<span data-ttu-id="10835-128">Järgmised probleemid on parandatud.</span><span class="sxs-lookup"><span data-stu-id="10835-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="10835-129">Kui broneeritava ressursi kalendrivõimsus on suurem kui 1, tuvastab Project Service Automation võimsuse valesti kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="10835-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="10835-130">Seega leiab ajakavavaates aset lõputu tsükkel.</span><span class="sxs-lookup"><span data-stu-id="10835-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="10835-131">Müük</span><span class="sxs-lookup"><span data-stu-id="10835-131">Sales</span></span>

<span data-ttu-id="10835-132">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="10835-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="10835-133">Kohandatud tehingutüübiga töölehe rea loomisel luuakse järgmine nullviite erand: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="10835-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="10835-134">Rolle ja kategooriaid, mis on inaktiveeritud enne hinnapäringu kopeerimist, ei tohiks vastkopeeritud hinnapakkumise laaditavatesse rollidesse ega kategooriatesse lisada.</span><span class="sxs-lookup"><span data-stu-id="10835-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="10835-135">Dokumendi kuupäeva ja raamatupidamiskuupäeva ei joondatud alguskuupäevaga, mis on toodud otse mustandarvel loodud arve rea üksikasjades.</span><span class="sxs-lookup"><span data-stu-id="10835-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="10835-136">Nullviite erandid luuakse stsenaariumides, mis on seotud rollide ja kategooriate inaktiveerimisega enne hinnapakkumise kopeerimist.</span><span class="sxs-lookup"><span data-stu-id="10835-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="10835-137">Toiming **Värskenda hinnad** lehel **Projektid** ei värskenda kuluprognoose ega materjalide hinnanguid.</span><span class="sxs-lookup"><span data-stu-id="10835-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
