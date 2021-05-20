---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 18, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 18, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949179"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="d21ab-103">Rakenduse Project Service Automation, värskenduse väljaanne 18, v3</span><span class="sxs-lookup"><span data-stu-id="d21ab-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d21ab-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="d21ab-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d21ab-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="d21ab-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d21ab-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="d21ab-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d21ab-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="d21ab-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="d21ab-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d21ab-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d21ab-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 18 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="d21ab-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="d21ab-110">Selle versiooni järgu number on V3.10.8.12 ja on üldiselt saadaval 2020. a aprilli enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="d21ab-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="d21ab-111">Värskenduste väljalase 18</span><span class="sxs-lookup"><span data-stu-id="d21ab-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d21ab-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="d21ab-112">Bug fixes</span></span>

<span data-ttu-id="d21ab-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="d21ab-113">**Time and Expense**</span></span>

- <span data-ttu-id="d21ab-114">Parandatud. Suvandid **Võta tagasi**, **Taotle** ja **Tühista kinnitus** liigub läbi erandite koos ebaselgete tõrketeadetega.</span><span class="sxs-lookup"><span data-stu-id="d21ab-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="d21ab-115">Parandatud. Kui kulu suvand **Tühista kinnitus** nurjub, ilmneb vastav erandi tõrge.</span><span class="sxs-lookup"><span data-stu-id="d21ab-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="d21ab-116">Parandatud. Ajakirje ruudustik käsitseb pärast oktoobris suveaja vahetust Austraalias mittetööpäevi valesti.</span><span class="sxs-lookup"><span data-stu-id="d21ab-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="d21ab-117">Parandatud. Vale vaikeloogika takistab kulude esitamist.</span><span class="sxs-lookup"><span data-stu-id="d21ab-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="d21ab-118">Parandatud. Kui aja sisestamise kinnitus nurjub, jääb kinnitus olekusse **Ootel**.</span><span class="sxs-lookup"><span data-stu-id="d21ab-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="d21ab-119">Parandatud. SQL-i tõrked hulgikinnitustes (tupik/aegumine).</span><span class="sxs-lookup"><span data-stu-id="d21ab-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="d21ab-120">Parandatud. Olulised kasutuskeskkonna jõudlusprobleemid, mille põhjustavad värskendusi tegevad meeskonnaliikmed ajakirjete kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="d21ab-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="d21ab-121">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="d21ab-121">**Project Management**</span></span>

- <span data-ttu-id="d21ab-122">Parandatud. Ajavööndi teatis on viidud vaatest **Vastavusse viimine** põhivormile **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d21ab-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="d21ab-123">Parandatud. Kalendrimall ei lähtesta uue projektivormi avamisel õigesti vaikesätetele.</span><span class="sxs-lookup"><span data-stu-id="d21ab-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="d21ab-124">Parandatud. Chromiumi-põhistes brauserites ei saa kasutajad hõlpsalt valida kustutamiseks eelkäija ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="d21ab-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="d21ab-125">Parandatud. Suvandi **Projekt tühjast mallist** loomine või kopeerimine toob seoseta ülesanded.</span><span class="sxs-lookup"><span data-stu-id="d21ab-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="d21ab-126">Parandatud. Konkreetsetes servajuhtumites põhjustab uue ülesande loomine ülesande ruudustikust duplikaatkirjete loomist.</span><span class="sxs-lookup"><span data-stu-id="d21ab-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="d21ab-127">Parandatud. Käsitsi režiimis ei saa kasutajad uuendada ülesande alguskuupäevasi hilisemaks kui praegune salvestatud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d21ab-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="d21ab-128">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="d21ab-128">**Resource Management**</span></span>

- <span data-ttu-id="d21ab-129">Parandatud. Vaate **Vastavusse viimine** vahekokkuvõtte rida arvutab pärast broneeringute pikendamist broneeringute hälbe valesti.</span><span class="sxs-lookup"><span data-stu-id="d21ab-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="d21ab-130">Parandatud. Vaade **Vastavusse viimine** kuvab ressursi ülesanded valesti, kui broneeritaval ressursil on kalender, mis ei ühti projekti kalendriga.</span><span class="sxs-lookup"><span data-stu-id="d21ab-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="d21ab-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d21ab-131">**Sales**</span></span>

- <span data-ttu-id="d21ab-132">Parandatud. Kui ajakirjed kinnitatakse uuesti (**Kinnita > Tühista >** uuesti kinnitamine), luuakse mittearvestatava tegeliku duplikaat.</span><span class="sxs-lookup"><span data-stu-id="d21ab-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]