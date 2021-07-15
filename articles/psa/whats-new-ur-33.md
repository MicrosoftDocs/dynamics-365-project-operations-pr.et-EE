---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 33, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 33, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334527"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="281a5-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 33, V3</span><span class="sxs-lookup"><span data-stu-id="281a5-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="281a5-104">Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest.</span><span class="sxs-lookup"><span data-stu-id="281a5-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="281a5-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="281a5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="281a5-106">See ühildub rakendusega Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="281a5-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="281a5-107">Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus.</span><span class="sxs-lookup"><span data-stu-id="281a5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="281a5-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="281a5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="281a5-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 33 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="281a5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="281a5-110">Selle versiooni järgunumber on V3.10.54.98 ja see on üldsusele isevärskenduse kaudu kättesaadav juulis 2021.</span><span class="sxs-lookup"><span data-stu-id="281a5-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="281a5-111">Värskenduste väljalase 33</span><span class="sxs-lookup"><span data-stu-id="281a5-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="281a5-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="281a5-112">Bug fixes</span></span>

<span data-ttu-id="281a5-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="281a5-113">**Time and Expense**</span></span>

<span data-ttu-id="281a5-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="281a5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="281a5-115">Kaks lukus välja **msdyn_description** ja **msdyn_externaldescription** on pärast esitamist redigeeritavad.</span><span class="sxs-lookup"><span data-stu-id="281a5-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="281a5-116">Kuvatakse tõrketeade, kui luuakse kulu, mis pole projektiga seotud.</span><span class="sxs-lookup"><span data-stu-id="281a5-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="281a5-117">Ajakirje loomisel muutub ressursi roll passiivseks rolliks.</span><span class="sxs-lookup"><span data-stu-id="281a5-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="281a5-118">Tagasi võetud ja kustutatud kuluga seotud töölehe ridasid ei kustutata.</span><span class="sxs-lookup"><span data-stu-id="281a5-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="281a5-119">Värskendage suvandis **Ajakirje kiirloomisvorm** vaadet **Projktiülesande loend**, et muuta vaikimisi kuvatav kuupäev ülesande algusuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="281a5-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="281a5-120">Kui loote ajakirje broneeritatava ressursi vahekaardil **Seotud**, luuakse ajakirje valesti sisselogitud kasutaja jaoks, mitte broneeritava ülemressursi jaoks.</span><span class="sxs-lookup"><span data-stu-id="281a5-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="281a5-121">Dialoogiboksi **Hulgikinnitamise MDD** jaoks lisatakse uued väljad.</span><span class="sxs-lookup"><span data-stu-id="281a5-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="281a5-122">**Projekti kavandamine**</span><span class="sxs-lookup"><span data-stu-id="281a5-122">**Project planning**</span></span>

<span data-ttu-id="281a5-123">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="281a5-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="281a5-124">Projekti loomise aeglane jõudlus, kui projekti töötunnimalle rakendatakse keerukate kalendritega.</span><span class="sxs-lookup"><span data-stu-id="281a5-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="281a5-125">Kui alguskuupäev on lõpukuupäevast suurem, kuvatakse koopia projektimallis iga välja kellaaja komponendi erinevuse tõttu tõrge.</span><span class="sxs-lookup"><span data-stu-id="281a5-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="281a5-126">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="281a5-126">**Resource management**</span></span>

<span data-ttu-id="281a5-127">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="281a5-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="281a5-128">Ressursikasutuse päringus kasutatakse vale parameetrit ja XML toob ruudustikus **Ressursikasutus** kaasa valed filtritulemused.</span><span class="sxs-lookup"><span data-stu-id="281a5-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="281a5-129">Kinnitus **Broneeringute laiendamne** kuvab broneeringute jaoks vale lõpukuupäeva.</span><span class="sxs-lookup"><span data-stu-id="281a5-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="281a5-130">**Müük**</span><span class="sxs-lookup"><span data-stu-id="281a5-130">**Sales**</span></span>

<span data-ttu-id="281a5-131">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="281a5-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="281a5-132">Kui kategooria hind luuakse puuduvate väärtustega, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="281a5-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="281a5-133">Kui lepingurea vahe-eesmärk luuakse ilma tellimuse reata, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="281a5-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
