---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 24, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 24, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000251"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="6834e-103">Rakenduse Project Service Automation, värskenduse väljaanne 24, v3</span><span class="sxs-lookup"><span data-stu-id="6834e-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6834e-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="6834e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6834e-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="6834e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6834e-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="6834e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6834e-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="6834e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6834e-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6834e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6834e-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 24 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="6834e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="6834e-110">Selle versiooni järgunumber on V 3.10.42.43 ja see on oktoobris 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="6834e-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="6834e-111">Värskenduste väljalase 24</span><span class="sxs-lookup"><span data-stu-id="6834e-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6834e-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="6834e-112">Bug fixes</span></span>

<span data-ttu-id="6834e-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6834e-113">**Sales**</span></span>

<span data-ttu-id="6834e-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="6834e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6834e-115">Toodete vaikehinnakirja määramisel esines probleem.</span><span class="sxs-lookup"><span data-stu-id="6834e-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="6834e-116">Hinnapakkumise võitmise jõudlus on manustatud hinnakirja ja rolli hinnakirjete koopia tõttu aeglane.</span><span class="sxs-lookup"><span data-stu-id="6834e-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="6834e-117">**Projektileping/müügikeskus** > **Tootereaüksuste / tellimuserea kogus** ümardatakse automaatselt lähima täisarvuni.</span><span class="sxs-lookup"><span data-stu-id="6834e-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="6834e-118">Laiendage hinnakirja lugemisel süsteemi õigusteni.</span><span class="sxs-lookup"><span data-stu-id="6834e-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="6834e-119">Kopeerige kliendi aadressiväljad **address1_freighttermscode** ja **address1_shippingmethodcode** hinnapakkumisele/tellimusele.</span><span class="sxs-lookup"><span data-stu-id="6834e-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="6834e-120">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="6834e-120">**Time and Expense**</span></span>

<span data-ttu-id="6834e-121">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="6834e-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="6834e-122">**Ajakirje ruudustik** ei toeta ajafunktsiooni **Ainult kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="6834e-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="6834e-123">**Ajakirjet** ei värskendata automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6834e-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="6834e-124">Nõutav on käsitsi värskendamine.</span><span class="sxs-lookup"><span data-stu-id="6834e-124">A manual refresh is required.</span></span>
- <span data-ttu-id="6834e-125">Ajakirjeid ei saa ülesandest importida, kui ressursi määramistes on paus (0 tundi).</span><span class="sxs-lookup"><span data-stu-id="6834e-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="6834e-126">Ajakirje loomisel määrake algus samale väärtusele kui **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="6834e-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="6834e-127">Lubage uuesti ajakirje hulgiredigeerimine.</span><span class="sxs-lookup"><span data-stu-id="6834e-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="6834e-128">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="6834e-128">**Resource Management**</span></span>

<span data-ttu-id="6834e-129">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="6834e-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="6834e-130">Päevasisese broneeringu oleku värskendamise proovimine ilma vajaduseta annab nullviite erandi.</span><span class="sxs-lookup"><span data-stu-id="6834e-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="6834e-131">Viga suvandi **Vastavusseviimise vaade** laadimisel.</span><span class="sxs-lookup"><span data-stu-id="6834e-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="6834e-132">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="6834e-132">**Project Management**</span></span>

<span data-ttu-id="6834e-133">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="6834e-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="6834e-134">Kui vahetate suvandis **Projekti ajakava** valikult **Käsitsi** valikule **Automaatne**, siis automaatset salvestamist ei viida lõpuni.</span><span class="sxs-lookup"><span data-stu-id="6834e-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="6834e-135">Kulumäära ei tohiks suvandis **Projekti jälgimise ruudustik** arvutada hälbe suunas.</span><span class="sxs-lookup"><span data-stu-id="6834e-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="6834e-136">Veergude **Hinnangute silt** vastuoluline käitumine laadimise ajal võrreldes tüübi **Ajafaas** muutumisega.</span><span class="sxs-lookup"><span data-stu-id="6834e-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="6834e-137">Projekti tegelik kulu ei pruugi kajastada kogusummasid suvandist **Tegelikud summad**.</span><span class="sxs-lookup"><span data-stu-id="6834e-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="6834e-138">**Hinnanguline lõpukuupäev** vahekaardil **Kokkuvõte** ei ühti suvandiga **WBS-i ajakava**.</span><span class="sxs-lookup"><span data-stu-id="6834e-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="6834e-139">**Tegeliku tööaja värskendamine** ei tööta õigesti taandel õigesti.</span><span class="sxs-lookup"><span data-stu-id="6834e-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="6834e-140">Juur-**äriüksusest** väljaspool olev projektijuht ei saa projekti luua.</span><span class="sxs-lookup"><span data-stu-id="6834e-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="6834e-141">Tööülesande või kategooria muudatused suvandis **Kuluhinnangud** ei jää püsima.</span><span class="sxs-lookup"><span data-stu-id="6834e-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="6834e-142">**Lepingu koopia** kopeerib arve ajakavad ja käitamise oleku.</span><span class="sxs-lookup"><span data-stu-id="6834e-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="6834e-143">Nupp **Värskenda tegelikud näitajad** arvutab kokkuvõtte ülesanded valesti.</span><span class="sxs-lookup"><span data-stu-id="6834e-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="6834e-144">Microsoft Projecti lisandmoodul: parandage nullviite tõrge, kui mõnel meeskonnaliikmel on tühi ressursiühik.</span><span class="sxs-lookup"><span data-stu-id="6834e-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]