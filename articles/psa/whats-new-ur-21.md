---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 21, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 21, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074907"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="9c7b5-103">Rakenduse Project Service Automation, värskenduse väljaanne 21, v3</span><span class="sxs-lookup"><span data-stu-id="9c7b5-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="9c7b5-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9c7b5-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9c7b5-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9c7b5-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9c7b5-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9c7b5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9c7b5-109">Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 21 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="9c7b5-110">Selle versiooni järgu number on V 3.10.32.50 ja on üldiselt saadaval 2020. a juuni enesevärskenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="9c7b5-111">Värskenduste väljalase 21</span><span class="sxs-lookup"><span data-stu-id="9c7b5-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9c7b5-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="9c7b5-112">Bug fixes</span></span>

<span data-ttu-id="9c7b5-113">**Aeg ja kulu**</span><span class="sxs-lookup"><span data-stu-id="9c7b5-113">**Time and Expense**</span></span>

<span data-ttu-id="9c7b5-114">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c7b5-115">Armatuurlaudadel **ajakirje ruudustiku juhtelemendi** majutamisel ei kasuta ruudustik armatuurlaua ruudustiku ümbrise täislaiust.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="9c7b5-116">**Ajakirje** ruudustiku juhtelement ei kuva konkreetsete ajavööndite jaoks kirjeid.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="9c7b5-117">Hilisemad ajakirjed kui kl 21.00 ilmuvad valel päeval.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="9c7b5-118">Kasutajad ei saa kulusid esitada, kui kulukategoorial **Nõutav kuludokument** puudub väärtus.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="9c7b5-119">**Ressursihaldus**</span><span class="sxs-lookup"><span data-stu-id="9c7b5-119">**Resource Management**</span></span>

<span data-ttu-id="9c7b5-120">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c7b5-121">Passiivsed broneeringud kuvatakse vaates **Vastavusseviimine**.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="9c7b5-122">Üldisel ressursi täitmisel puudus valideerimine, et tagada kehtiva broneeringu oleku olemasolu.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="9c7b5-123">**Projektijuhtimine**</span><span class="sxs-lookup"><span data-stu-id="9c7b5-123">**Project Management**</span></span>

<span data-ttu-id="9c7b5-124">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c7b5-125">**Projekti** vormi ruudustikud ( **Ressursi määramine** , **Ülesanne** , vaade **Vastavusseviimine** , **Kuluprognoosid** ) jäävad redigeeritavaks ka siis, kui projekt pole aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="9c7b5-126">Dubleeritud kliente ei saa liita klientidega, kes on seotud kinnitatud projektilepingutega.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="9c7b5-127">Kui lisatakse klient, kellel puudub kehtiv kalender, süsteem ei tagasta kasutajasõbralikku tõrketeadet.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="9c7b5-128">Ülesande ruudustiku nupp **Lisa ülesanne** on lubatud, kui projekt on seotud **Microsoft Projecti lisandmooduliga**.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="9c7b5-129">Panus kasvab kontrollimatult juhul, kui kategooria ülesanne määratakse ressursile, millel on roll, millel pole omahinda määratud.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="9c7b5-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9c7b5-130">**Sales**</span></span>

<span data-ttu-id="9c7b5-131">Tehtud on järgmised täiustused.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="9c7b5-132">**Arve sagedus** ja **Arveldamise algus** on teisaldatud vahekaardile **Arve ajakava**.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="9c7b5-133">Lahendatud on järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c7b5-134">**Müügihind kokku** on null (0) suvandi **Kategooria** jaoks, olgugi suvandi **Roll** müügihind kokku ei ole null.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="9c7b5-135">Kliendid ei saa muuta välja **Arve olek** väärtuseks **Arveldamiseks valmis** , kui muu kohandatud protsess värskendab täiendavat välja.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="9c7b5-136">Nupp **Värskenda arve ridu** saab korduval valimisel luua mitu dubleeritud rida.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="9c7b5-137">Nupp **Värskenda hindu** ei tööta alamruudustikuga **Rolli hinnad** vormil **Kiirvaade**.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="9c7b5-138">**Müügihinnakirja resolutsiooni** loogika käsitseb ajavööndeid valesti, mille tulemuseks on hinnakirjade vale valimine.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="9c7b5-139">Projekti suvand **Tegelik kulu kokku** võib pärast ühekordse sisestuse kinnitamist olla murdosa summa võrra vale.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="9c7b5-140">**Hinna lahenduse** loogika ei esita kasutajasõbralikke tõrketeateid, kui **toodud rolli hind** ei oma väärtuseid väljadel **Põhiühik** ja **Hind põhiühikutes**.</span><span class="sxs-lookup"><span data-stu-id="9c7b5-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
