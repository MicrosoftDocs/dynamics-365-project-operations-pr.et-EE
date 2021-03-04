---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 21, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 21, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147018"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="94a9d-103">Rakenduse Project Service Automation, värskenduse väljaanne 21, v3</span><span class="sxs-lookup"><span data-stu-id="94a9d-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="94a9d-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="94a9d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="94a9d-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="94a9d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="94a9d-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="94a9d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="94a9d-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="94a9d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="94a9d-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="94a9d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="94a9d-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 21 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="94a9d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="94a9d-110">Selle versiooni järgu number on V 3.10.32.50 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="94a9d-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="94a9d-111">Värskenduste väljalase 21</span><span class="sxs-lookup"><span data-stu-id="94a9d-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="94a9d-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="94a9d-112">Bug fixes</span></span>

<span data-ttu-id="94a9d-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="94a9d-113">**Time and Expense**</span></span>

<span data-ttu-id="94a9d-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="94a9d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="94a9d-115">Armatuurlaudadel **ajakirje ruudustiku juhtelemendi** majutamisel ei kasuta ruudustik armatuurlaua ruudustiku ümbrise täislaiust.</span><span class="sxs-lookup"><span data-stu-id="94a9d-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="94a9d-116">**Ajakirje** ruudustiku juhtelement ei kuva konkreetsete ajavööndite jaoks kirjeid.</span><span class="sxs-lookup"><span data-stu-id="94a9d-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="94a9d-117">Hilisemad ajakirjed kui kl 21.00 ilmuvad valel päeval.</span><span class="sxs-lookup"><span data-stu-id="94a9d-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="94a9d-118">Kasutajad ei saa kulusid esitada, kui kulukategoorial **Nõutav kuludokument** puudub väärtus.</span><span class="sxs-lookup"><span data-stu-id="94a9d-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="94a9d-119">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="94a9d-119">**Resource Management**</span></span>

<span data-ttu-id="94a9d-120">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="94a9d-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="94a9d-121">Passiivsed broneeringud kuvatakse vaates **Vastavusseviimine**.</span><span class="sxs-lookup"><span data-stu-id="94a9d-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="94a9d-122">Üldisel ressursi täitmisel puudus valideerimine, et tagada kehtiva broneeringu oleku olemasolu.</span><span class="sxs-lookup"><span data-stu-id="94a9d-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="94a9d-123">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="94a9d-123">**Project Management**</span></span>

<span data-ttu-id="94a9d-124">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="94a9d-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="94a9d-125">**Projekti** vormi ruudustikud (**Ressursi määramine**, **Ülesanne**, vaade **Vastavusseviimine**, **Kuluprognoosid**) jäävad redigeeritavaks ka siis, kui projekt pole aktiivne.</span><span class="sxs-lookup"><span data-stu-id="94a9d-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="94a9d-126">Dubleeritud kliente ei saa liita klientidega, kes on seotud kinnitatud projektilepingutega.</span><span class="sxs-lookup"><span data-stu-id="94a9d-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="94a9d-127">Kui lisatakse klient, kellel puudub kehtiv kalender, süsteem ei tagasta kasutajasõbralikku tõrketeadet.</span><span class="sxs-lookup"><span data-stu-id="94a9d-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="94a9d-128">Ülesande ruudustiku nupp **Lisa ülesanne** on lubatud, kui projekt on seotud **Microsoft Projecti lisandmooduliga**.</span><span class="sxs-lookup"><span data-stu-id="94a9d-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="94a9d-129">Panus kasvab kontrollimatult juhul, kui kategooria ülesanne määratakse ressursile, millel on roll, millel pole omahinda määratud.</span><span class="sxs-lookup"><span data-stu-id="94a9d-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="94a9d-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="94a9d-130">**Sales**</span></span>

<span data-ttu-id="94a9d-131">Tehtud on järgmised täiustused.</span><span class="sxs-lookup"><span data-stu-id="94a9d-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="94a9d-132">**Arve sagedus** ja **Arveldamise algus** on teisaldatud vahekaardile **Arve ajakava**.</span><span class="sxs-lookup"><span data-stu-id="94a9d-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="94a9d-133">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="94a9d-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="94a9d-134">**Müügihind kokku** on null (0) suvandi **Kategooria** jaoks, olgugi suvandi **Roll** müügihind kokku ei ole null.</span><span class="sxs-lookup"><span data-stu-id="94a9d-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="94a9d-135">Kliendid ei saa muuta välja **Arve olek** väärtuseks **Arveldamiseks valmis**, kui muu kohandatud protsess värskendab täiendavat välja.</span><span class="sxs-lookup"><span data-stu-id="94a9d-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="94a9d-136">Nupp **Värskenda arve ridu** saab korduval valimisel luua mitu dubleeritud rida.</span><span class="sxs-lookup"><span data-stu-id="94a9d-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="94a9d-137">Nupp **Värskenda hindasid** ei tööta vormi **Kiirvaade** andmeruudustikus **Rolli hinnad**.</span><span class="sxs-lookup"><span data-stu-id="94a9d-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="94a9d-138">**Müügihinnakirja resolutsiooni** loogika käsitseb ajavööndeid valesti, mille tulemuseks on hinnakirjade vale valimine.</span><span class="sxs-lookup"><span data-stu-id="94a9d-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="94a9d-139">Projekti suvand **Tegelik kulu kokku** võib pärast ühekordse sisestuse kinnitamist olla murdosa summa võrra vale.</span><span class="sxs-lookup"><span data-stu-id="94a9d-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="94a9d-140">**Hinna lahenduse** loogika ei esita kasutajasõbralikke tõrketeateid, kui **toodud rolli hind** ei oma väärtuseid väljadel **Põhiühik** ja **Hind põhiühikutes**.</span><span class="sxs-lookup"><span data-stu-id="94a9d-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
