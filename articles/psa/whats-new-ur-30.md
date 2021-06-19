---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 30, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 30, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010421"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="8e42a-103">Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 30, V3</span><span class="sxs-lookup"><span data-stu-id="8e42a-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8e42a-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="8e42a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8e42a-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="8e42a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8e42a-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="8e42a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8e42a-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="8e42a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8e42a-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="8e42a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="8e42a-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 30 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="8e42a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="8e42a-110">Selle versiooni järgu number on V3.10.51.61 ja on üldiselt saadaval 2021. a aprilli enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="8e42a-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="8e42a-111">Värskenduste väljalase 30</span><span class="sxs-lookup"><span data-stu-id="8e42a-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8e42a-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="8e42a-112">Bug fixes</span></span>

<span data-ttu-id="8e42a-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="8e42a-113">**Time and Expense**</span></span>

<span data-ttu-id="8e42a-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="8e42a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8e42a-115">Lehel **Kiirloomine** ajakirje loomisel ja salvestamisel esineb tõrge, kui väli **Roll** on eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="8e42a-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="8e42a-116">Ajakirje filter rakendab filtri tehtemärgi valesti.</span><span class="sxs-lookup"><span data-stu-id="8e42a-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="8e42a-117">Kopeeritud ajalehti ei kuvata automaatselt, kui valite ajakirje juhtelemendil suvandi **Kopeeri nädal**.</span><span class="sxs-lookup"><span data-stu-id="8e42a-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="8e42a-118">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="8e42a-118">**Resource Management**</span></span>

<span data-ttu-id="8e42a-119">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="8e42a-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="8e42a-120">Broneeringu pikendamisel on fikseeritud broneeringule määratud broneeringu olek vale.</span><span class="sxs-lookup"><span data-stu-id="8e42a-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="8e42a-121">Broneeringu pikendamine arvestab broneeringu olekuga, mis on määratletud broneeringu häälestamise metaandmetes kui **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="8e42a-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="8e42a-122">Kui kehtivat broneeringu olekut ei määrata, siis tõrketeadet ei lokaliseerita õigesti.</span><span class="sxs-lookup"><span data-stu-id="8e42a-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="8e42a-123">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="8e42a-123">**Project Management**</span></span>

<span data-ttu-id="8e42a-124">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="8e42a-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="8e42a-125">Projekte ei saa luua ühes valuutas ja see ei saa sisaldada seotud ülesandeid teises valuutas.</span><span class="sxs-lookup"><span data-stu-id="8e42a-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="8e42a-126">**Müük**</span><span class="sxs-lookup"><span data-stu-id="8e42a-126">**Sales**</span></span>

<span data-ttu-id="8e42a-127">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="8e42a-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="8e42a-128">Hinnakirja kopeerimisel hindu ei värskendata.</span><span class="sxs-lookup"><span data-stu-id="8e42a-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="8e42a-129">Võidetud hinnapakkumise sulgemine nurjub, kui kulu üksikasjadel on päritolu väärtus.</span><span class="sxs-lookup"><span data-stu-id="8e42a-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="8e42a-130">Olemil **Projekti ülesanne** on suvand **Prognoositav kulu** nimetatud ümber olemiks **Plaanitud kulu (alus)**.</span><span class="sxs-lookup"><span data-stu-id="8e42a-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="8e42a-131">Arvete loomisel ja kustutamisel luuakse nullviite erand.</span><span class="sxs-lookup"><span data-stu-id="8e42a-131">A null reference exception is generated when invoices are created or deleted.</span></span>
