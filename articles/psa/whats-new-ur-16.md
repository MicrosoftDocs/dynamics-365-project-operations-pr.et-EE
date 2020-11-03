---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 16, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 16, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074915"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="c7a69-103">Rakenduse Project Service Automation, värskenduse väljaanne 16, v3</span><span class="sxs-lookup"><span data-stu-id="c7a69-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="c7a69-104">Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest.</span><span class="sxs-lookup"><span data-stu-id="c7a69-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c7a69-105">See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.</span><span class="sxs-lookup"><span data-stu-id="c7a69-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="c7a69-106">See väljalase ühildub Dynamics 365 9. x-iga.</span><span class="sxs-lookup"><span data-stu-id="c7a69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c7a69-107">Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks.</span><span class="sxs-lookup"><span data-stu-id="c7a69-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="c7a69-108">Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="c7a69-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="c7a69-109">Selles teemas loetletakse PSA V3 värskenduse väljalaske 16 uusi või muudetud funktsioone ja parandusi.</span><span class="sxs-lookup"><span data-stu-id="c7a69-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="c7a69-110">Selle versiooni järgunumber on V3.10.6.34 ja see on jaanuaris 2020 automaatvärskendusega kõigile saadaval.</span><span class="sxs-lookup"><span data-stu-id="c7a69-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="c7a69-111">Värskenduste väljalase 16</span><span class="sxs-lookup"><span data-stu-id="c7a69-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c7a69-112">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="c7a69-112">Bug fixes</span></span>

-   <span data-ttu-id="c7a69-113">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="c7a69-113">Time and Expense</span></span>

    -   <span data-ttu-id="c7a69-114">Parandatud: kasutajad, kes püüavad kinnitamiseks esitada kustutatud aja- ja kulukirjeid, ei saa nüüd asjakohaseid tõrketeateid.</span><span class="sxs-lookup"><span data-stu-id="c7a69-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="c7a69-115">Projektijuhtimine</span><span class="sxs-lookup"><span data-stu-id="c7a69-115">Project Management</span></span>

    -   <span data-ttu-id="c7a69-116">Parandatud: meeskonnaliikmetele mallides määratud ressursiüksuseid rakendatakse uuele projektile.</span><span class="sxs-lookup"><span data-stu-id="c7a69-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="c7a69-117">Parandatud: kirje omandiõiguste ümbermääramise käsitlemise täiustamine.</span><span class="sxs-lookup"><span data-stu-id="c7a69-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="c7a69-118">Parandatud: kopeeritavaid projekte ei lubata kopeerida enne, kui kõik kopeerimistoimingud on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="c7a69-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="c7a69-119">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="c7a69-119">Resource Management</span></span>

    -   <span data-ttu-id="c7a69-120">Parandatud: broneeringute pikendamine toimib nüüd lühikeste kestustega õigesti ja ei loo enam pikendatud broneeringutele null-tunde.</span><span class="sxs-lookup"><span data-stu-id="c7a69-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="c7a69-121">Parandatud: nüüd renderdatakse vastavusseviimise vaade, kui projekti ajavöönd on + 5:30 GMT ja kasutaja ajavöönd on erinev.</span><span class="sxs-lookup"><span data-stu-id="c7a69-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="c7a69-122">Sales</span><span class="sxs-lookup"><span data-stu-id="c7a69-122">Sales</span></span>

    -   <span data-ttu-id="c7a69-123">Parandatud: kui lepingureale vastendatud projekt eemaldatakse ja uus projekt vastendatakse, siis uue projekti tegelikke kirjeid ei hinnatud uut projekti ümber lepingureal määratletud arvelduse ja hinnakujunduse põhjal.</span><span class="sxs-lookup"><span data-stu-id="c7a69-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="c7a69-124">See on selles väljalaskes parandatud.</span><span class="sxs-lookup"><span data-stu-id="c7a69-124">This has been fixed in this release.</span></span> <span data-ttu-id="c7a69-125">Äsja vastendatud projekti hinnastamine ja tegelikud kirjed pööratakse tagasi ja luuakse uuesti õigesti, vastavalt lepingurea hinnastamis- ja arveldusreeglitele.</span><span class="sxs-lookup"><span data-stu-id="c7a69-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="c7a69-126">Vastendamata projekti tegelikud kirjed hinnatakse samuti ümber ja luuakse selle tulemusel uuesti.</span><span class="sxs-lookup"><span data-stu-id="c7a69-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="c7a69-127">Parandatud: täiendav valideerimine on lisatud prognoosi rea väljale **Summa** , et tagada null-väärtuste säilimine.</span><span class="sxs-lookup"><span data-stu-id="c7a69-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="c7a69-128">Parandatud: kui projekti tegelikud näitajad on värskendatud, on projekti põhivormile lisatud värskendamise nupp, et võimaldata kasutajatele tegelike näitajate uuesti sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="c7a69-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="c7a69-129">Parandatud: kui kasutajad värskendavad versioonilt 2. X versioonile 3. X, lubatakse NULL väärtusega projektinimega projektid.</span><span class="sxs-lookup"><span data-stu-id="c7a69-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

