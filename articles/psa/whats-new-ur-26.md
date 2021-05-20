---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 26, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 26, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948819"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="40783-103">Rakenduse Project Service Automation, värskenduse väljaanne 26, v3</span><span class="sxs-lookup"><span data-stu-id="40783-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="40783-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="40783-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="40783-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="40783-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="40783-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="40783-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="40783-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="40783-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="40783-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="40783-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="40783-109">Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 26 ver 3 uused või muudetud funktsioonid ja parandused.</span><span class="sxs-lookup"><span data-stu-id="40783-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="40783-110">Selle versiooni järgu number on V3.10.44.59 ja see on kõigile kättesaadav 2020. a detsembris ise värskendamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="40783-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="40783-111">Värskenduste väljalase 26</span><span class="sxs-lookup"><span data-stu-id="40783-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="40783-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="40783-112">Bug fixes</span></span>

<span data-ttu-id="40783-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="40783-113">**Time and Expense**</span></span>

<span data-ttu-id="40783-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="40783-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="40783-115">Kasutajad saavad muuta kinnitatud/esitatud ajakirje ülesannet.</span><span class="sxs-lookup"><span data-stu-id="40783-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="40783-116">Tõrge „Objekti viide pole määratud” ajakirje salvestamisel.</span><span class="sxs-lookup"><span data-stu-id="40783-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="40783-117">Ajakirje importimine ressursi määramistest loob ajakirjed valede DateTime väärtustega.</span><span class="sxs-lookup"><span data-stu-id="40783-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="40783-118">Kui intstallitud on nii rakendus Project Service Automation kui ka Field Service, kuvatakse rakenduse Field Service ajakirjete jaoks nupp **Uus** käsuribal kaks korda.</span><span class="sxs-lookup"><span data-stu-id="40783-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="40783-119">Lahtrite **Luba üksus** ja **Ühikurühm** töötavad nüüd ruudustikus **Kuluarvutused**.</span><span class="sxs-lookup"><span data-stu-id="40783-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="40783-120">Vorm **Ajakirje redigeerimise värskendus** hõlmab suvandit **Ajajoon**.</span><span class="sxs-lookup"><span data-stu-id="40783-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="40783-121">Mitte-projektipõhiste ajakirjete kellaaja kinnitamine blokeerib süsteemi projekti kinnitaja rolli otsimisel.</span><span class="sxs-lookup"><span data-stu-id="40783-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="40783-122">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="40783-122">**Resource Management**</span></span>

<span data-ttu-id="40783-123">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="40783-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="40783-124">Lisatud on lisandmooduli **PostProjectCreate** valideerimine, et kontrollida enne selle loomist peamist nõuet.</span><span class="sxs-lookup"><span data-stu-id="40783-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="40783-125">Kiirloomisvorm **Projekti meeskonnaliige** esitab nullviite erandi, kui väljad eemaldatakse vormist.</span><span class="sxs-lookup"><span data-stu-id="40783-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="40783-126">12-tunniste nõuete loomine üle ühe aasta nurjub.</span><span class="sxs-lookup"><span data-stu-id="40783-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="40783-127">Paranenud on veateate nullviite erand ressursinõude loomise ajal.</span><span class="sxs-lookup"><span data-stu-id="40783-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="40783-128">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="40783-128">**Project Management**</span></span>

<span data-ttu-id="40783-129">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="40783-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="40783-130">Paranenud on valideerimine nullviite erandi adresseerimiseks, mis on loodud lisandmoodulis **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="40783-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="40783-131">Microsoft Projecti töölaua lisandmooduli poolt avaldatud projektd kustutavad määramata ülesanded.</span><span class="sxs-lookup"><span data-stu-id="40783-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="40783-132">Lisatud uus valideerimine, kui tööülesande projektiviide on kehtetu nullviite erandi tõttu lisandmoodulis **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="40783-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="40783-133">Meeskonnaliikmete ruudustik ei kuva meeskonnaliikme kirjes eraldi määramisi.</span><span class="sxs-lookup"><span data-stu-id="40783-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="40783-134">Lisatud on uus valideerimine ja tõrketeated nullviite erandi tõttu lisandmoodulis **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="40783-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="40783-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="40783-135">**Sales**</span></span>

<span data-ttu-id="40783-136">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="40783-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="40783-137">Projektipõhise rea hinnapakkumise või lepingu valimisel peaks nupp **Soovitus** olema nähtav ainult siis, kui valite projektipõhise rea, mis on seotud olemasoleva tootega.</span><span class="sxs-lookup"><span data-stu-id="40783-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="40783-138">Eraldage õigus **Create_Product** õigusest **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="40783-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="40783-139">Arverea kustutamine põhjustab nuppviite tõrget lisandmoodulis **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="40783-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]