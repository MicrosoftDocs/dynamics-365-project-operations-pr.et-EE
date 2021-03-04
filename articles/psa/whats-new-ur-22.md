---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 22, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 22, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150978"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="c82b2-103">Rakenduse Project Service Automation, värskenduse väljaanne 22, v3</span><span class="sxs-lookup"><span data-stu-id="c82b2-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c82b2-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="c82b2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c82b2-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="c82b2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c82b2-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="c82b2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c82b2-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="c82b2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c82b2-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c82b2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c82b2-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 22 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="c82b2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="c82b2-110">Selle versiooni järgu number on V 3.10.33.48 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="c82b2-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="c82b2-111">Värskenduste väljalase 22</span><span class="sxs-lookup"><span data-stu-id="c82b2-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c82b2-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="c82b2-112">Bug fixes</span></span>



<span data-ttu-id="c82b2-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="c82b2-113">**Time and Expense**</span></span>

<span data-ttu-id="c82b2-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c82b2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c82b2-115">**Ajakirjeid** ei lisata pärast importimist automaatselt ajakirjete ajakavasse.</span><span class="sxs-lookup"><span data-stu-id="c82b2-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="c82b2-116">**Ajakirje** ruudustiku kuupäeva valija ei tuvasta kasutaja piirkondlikke seadistusi.</span><span class="sxs-lookup"><span data-stu-id="c82b2-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="c82b2-117">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="c82b2-117">**Resource Management**</span></span>

<span data-ttu-id="c82b2-118">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c82b2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="c82b2-119">Käsitsi režiimis kontuuride **Ressursi määramine** muudatusi ei tuvastata **ressursi nõuete** loomisel.</span><span class="sxs-lookup"><span data-stu-id="c82b2-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="c82b2-120">**Ressursi päringud** ei toeta kohandatud taotluse olekuid.</span><span class="sxs-lookup"><span data-stu-id="c82b2-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="c82b2-121">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="c82b2-121">**Project Management**</span></span>

<span data-ttu-id="c82b2-122">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c82b2-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="c82b2-123">EstimateGridControl topeltklõpsamine ei sõelu Hollandi vormingu numbreid õigesti.</span><span class="sxs-lookup"><span data-stu-id="c82b2-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="c82b2-124">Määratud tunde ei värskendata õigesti, kui määramisi muudetakse Microsoft Projecti töölaua klientrakenduse lisandmoodulit kasutades.</span><span class="sxs-lookup"><span data-stu-id="c82b2-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="c82b2-125">Ruudustikud Projekti jälgimine ja Prognoosid kuvavad vale müügi valuutakoodi, kui lepingu valuuta erineb kliendi valuutast ja organisatsioon on konfigureeritud kuvama valuutatähiste asemel valuutakoodid.</span><span class="sxs-lookup"><span data-stu-id="c82b2-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="c82b2-126">Meeskonnaliikme lõppkuupäev lisab ühe päeva, kui töö ajakava on 24 tundi päevas.</span><span class="sxs-lookup"><span data-stu-id="c82b2-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="c82b2-127">Projekti ajakavas ülesandele tehingu kategooria lisamine ei käivita automaatset salvestamist.</span><span class="sxs-lookup"><span data-stu-id="c82b2-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="c82b2-128">Projektimalli meeskonnaliikme lisamisel kuvatakse järgmine tõrge: „Ressursinõudeid ei saa seostada projektimallidega”.</span><span class="sxs-lookup"><span data-stu-id="c82b2-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="c82b2-129">Lindireegli skript „msdyn.Approval.CanApproveOrReject” kuvab aegumise tõrke.</span><span class="sxs-lookup"><span data-stu-id="c82b2-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="c82b2-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c82b2-130">**Sales**</span></span>

<span data-ttu-id="c82b2-131">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="c82b2-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="c82b2-132">Valideerimise tõrketeadet ei kuvata, kui vormil/olemis Uus hinnapakkumise projekti hinnakiri on otsingus Hinnakiri valitud suvand Omahinnakiri.</span><span class="sxs-lookup"><span data-stu-id="c82b2-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="c82b2-133">Võidetuna hinnapakkumise sulgemine navigeeri loodud lepingu juurde, kui hinnapakkumisele manustatud BPF on viimases etapis.</span><span class="sxs-lookup"><span data-stu-id="c82b2-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="c82b2-134">Suvandi **Arveldamata müük** tagasipööramine on seotud algse kuluga, kui ajakirje võetakse tagasi.</span><span class="sxs-lookup"><span data-stu-id="c82b2-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="c82b2-135">Pärast nupu **Kinnita** valimist arve olek ei muutu olekule **Kinnitatud** enne, kui arve värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="c82b2-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
