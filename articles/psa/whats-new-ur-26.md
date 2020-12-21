---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643258"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="cff64-102">Rakenduse Project Service Automation, värskenduse väljaanne 26, v3</span><span class="sxs-lookup"><span data-stu-id="cff64-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="cff64-103">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="cff64-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cff64-104">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="cff64-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cff64-105">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="cff64-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cff64-106">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="cff64-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cff64-107">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cff64-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cff64-108">Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 26 ver 3 uused või muudetud funktsioonid ja parandused.</span><span class="sxs-lookup"><span data-stu-id="cff64-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="cff64-109">Selle versiooni järgu number on V3.10.44.59 ja see on kõigile kättesaadav 2020. a detsembris ise värskendamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="cff64-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="cff64-110">Värskenduste väljalase 26</span><span class="sxs-lookup"><span data-stu-id="cff64-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="cff64-111">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="cff64-111">Bug fixes</span></span>

<span data-ttu-id="cff64-112">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="cff64-112">**Time and Expense**</span></span>

<span data-ttu-id="cff64-113">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="cff64-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cff64-114">Kasutajad saavad muuta kinnitatud/esitatud ajakirje ülesannet.</span><span class="sxs-lookup"><span data-stu-id="cff64-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="cff64-115">Tõrge „Objekti viide pole määratud” ajakirje salvestamisel.</span><span class="sxs-lookup"><span data-stu-id="cff64-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="cff64-116">Ajakirje importimine ressursi määramistest loob ajakirjed valede DateTime väärtustega.</span><span class="sxs-lookup"><span data-stu-id="cff64-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="cff64-117">Kui intstallitud on nii rakendus Project Service Automation kui ka Field Service, kuvatakse rakenduse Field Service ajakirjete jaoks nupp **Uus** käsuribal kaks korda.</span><span class="sxs-lookup"><span data-stu-id="cff64-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="cff64-118">Lahtrite **Luba üksus** ja **Ühikurühm** töötavad nüüd ruudustikus **Kuluarvutused**.</span><span class="sxs-lookup"><span data-stu-id="cff64-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="cff64-119">Vorm **Ajakirje redigeerimise värskendus** hõlmab suvandit **Ajajoon**.</span><span class="sxs-lookup"><span data-stu-id="cff64-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="cff64-120">Mitte-projektipõhiste ajakirjete kellaaja kinnitamine blokeerib süsteemi projekti kinnitaja rolli otsimisel.</span><span class="sxs-lookup"><span data-stu-id="cff64-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="cff64-121">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="cff64-121">**Resource Management**</span></span>

<span data-ttu-id="cff64-122">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="cff64-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cff64-123">Lisatud on lisandmooduli **PostProjectCreate** valideerimine, et kontrollida enne selle loomist peamist nõuet.</span><span class="sxs-lookup"><span data-stu-id="cff64-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="cff64-124">Kiirloomisvorm **Projekti meeskonnaliige** esitab nullviite erandi, kui väljad eemaldatakse vormist.</span><span class="sxs-lookup"><span data-stu-id="cff64-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="cff64-125">12-tunniste nõuete loomine üle ühe aasta nurjub.</span><span class="sxs-lookup"><span data-stu-id="cff64-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="cff64-126">Paranenud on veateate nullviite erand ressursinõude loomise ajal.</span><span class="sxs-lookup"><span data-stu-id="cff64-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="cff64-127">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="cff64-127">**Project Management**</span></span>

<span data-ttu-id="cff64-128">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="cff64-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cff64-129">Paranenud on valideerimine nullviite erandi adresseerimiseks, mis on loodud lisandmoodulis **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cff64-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="cff64-130">Microsoft Projecti töölaua lisandmooduli poolt avaldatud projektd kustutavad määramata ülesanded.</span><span class="sxs-lookup"><span data-stu-id="cff64-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="cff64-131">Lisatud uus valideerimine, kui tööülesande projektiviide on kehtetu nullviite erandi tõttu lisandmoodulis **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cff64-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="cff64-132">Meeskonnaliikmete ruudustik ei kuva meeskonnaliikme kirjes eraldi määramisi.</span><span class="sxs-lookup"><span data-stu-id="cff64-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="cff64-133">Lisatud on uus valideerimine ja tõrketeated nullviite erandi tõttu lisandmoodulis **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="cff64-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="cff64-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cff64-134">**Sales**</span></span>

<span data-ttu-id="cff64-135">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="cff64-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cff64-136">Projektipõhise rea hinnapakkumise või lepingu valimisel peaks nupp **Soovitus** olema nähtav ainult siis, kui valite projektipõhise rea, mis on seotud olemasoleva tootega.</span><span class="sxs-lookup"><span data-stu-id="cff64-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="cff64-137">Eraldage õigus **Create_Product** õigusest **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="cff64-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="cff64-138">Arverea kustutamine põhjustab nuppviite tõrget lisandmoodulis **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="cff64-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
