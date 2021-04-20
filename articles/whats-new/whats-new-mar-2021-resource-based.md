---
title: Mis on uut märtsis 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See teema sisaldab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2021. aasta märtsi väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499993"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="30e93-103">Mis on uut märtsis 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="30e93-103">What's new March 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="30e93-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="30e93-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="30e93-105">See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="30e93-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="30e93-106">Project Operations Dataverse’i keskkonna versioonis 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="30e93-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 
- <span data-ttu-id="30e93-107">Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.16</span><span class="sxs-lookup"><span data-stu-id="30e93-107">Project management and accounting on Dynamics 365 Finance environment version 10.0.16</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="30e93-108">Kvaliteedi värskendused</span><span class="sxs-lookup"><span data-stu-id="30e93-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="30e93-109">Project Operations teenuses Dataverse</span><span class="sxs-lookup"><span data-stu-id="30e93-109">Project Operations on Dataverse</span></span>


| <span data-ttu-id="30e93-110">**Funktsiooni ala**</span><span class="sxs-lookup"><span data-stu-id="30e93-110">**Feature area**</span></span> | <span data-ttu-id="30e93-111">**Viitenumber**</span><span class="sxs-lookup"><span data-stu-id="30e93-111">**Reference number**</span></span> | <span data-ttu-id="30e93-112">**Kvaliteedi värskendus**</span><span class="sxs-lookup"><span data-stu-id="30e93-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="30e93-113">Arveldamine ja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="30e93-113">Billing and pricing</span></span> | <span data-ttu-id="30e93-114">2133873</span><span class="sxs-lookup"><span data-stu-id="30e93-114">2133873</span></span> | <span data-ttu-id="30e93-115">Parandatud on **Ühiku müügihinna** valuuta sümbol ruudustikus **Kuluprognoosid**.</span><span class="sxs-lookup"><span data-stu-id="30e93-115">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="30e93-116">Arveldamine ja hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="30e93-116">Billing and pricing</span></span> | <span data-ttu-id="30e93-117">2174616</span><span class="sxs-lookup"><span data-stu-id="30e93-117">2174616</span></span> | <span data-ttu-id="30e93-118">Kui hinnapakkumine võidetakse, viidatakse lepingu kohandatud hinnakirjale lepingurea üksikasjades, mis kopeeritakse hinnapakkumisest.</span><span class="sxs-lookup"><span data-stu-id="30e93-118">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="30e93-119">Müügivõimaluse haldus</span><span class="sxs-lookup"><span data-stu-id="30e93-119">Opportunity Management</span></span> | <span data-ttu-id="30e93-120">2167475</span><span class="sxs-lookup"><span data-stu-id="30e93-120">2167475</span></span> | <span data-ttu-id="30e93-121">Parandatud on maksusumma parandusarves, mis pärines arveldamata tegelikust kirjest.</span><span class="sxs-lookup"><span data-stu-id="30e93-121">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="30e93-122">Müügivõimaluse haldus</span><span class="sxs-lookup"><span data-stu-id="30e93-122">Opportunity Management</span></span> | <span data-ttu-id="30e93-123">2176285</span><span class="sxs-lookup"><span data-stu-id="30e93-123">2176285</span></span> | <span data-ttu-id="30e93-124">Maksusummat ei tohi kopeerida müügilepingu/hinnapakkumise rea üksikasjadest kululepingu/hinnapakkumise rea üksikasjadesse.</span><span class="sxs-lookup"><span data-stu-id="30e93-124">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="30e93-125">Müügivõimaluse haldus</span><span class="sxs-lookup"><span data-stu-id="30e93-125">Opportunity Management</span></span> | <span data-ttu-id="30e93-126">2188079</span><span class="sxs-lookup"><span data-stu-id="30e93-126">2188079</span></span> | <span data-ttu-id="30e93-127">Jagatud arveldamise reeglit ei tohi luua lepingute jaoks, mis ei põhine tööl.</span><span class="sxs-lookup"><span data-stu-id="30e93-127">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="30e93-128">Plaanimine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="30e93-128">Planning and Tracking</span></span> | <span data-ttu-id="30e93-129">2125274</span><span class="sxs-lookup"><span data-stu-id="30e93-129">2125274</span></span> | <span data-ttu-id="30e93-130">Atribuut **Projekti topeltkirjutuse vastendus** atribuudile **Projekti alguskuupäeva vastendus** värskendati väärtuselt **msdyn\_taskearlieststart** väärtusele **msdyn\_actualstart**.</span><span class="sxs-lookup"><span data-stu-id="30e93-130">**Project Dual Write Map** attribute for **Project Start Date Mapping** updated from **msdyn\_taskearlieststart** to **msdyn\_actualstart**.</span></span> |
| <span data-ttu-id="30e93-131">Plaanimine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="30e93-131">Planning and Tracking</span></span> | <span data-ttu-id="30e93-132">2138853</span><span class="sxs-lookup"><span data-stu-id="30e93-132">2138853</span></span> | <span data-ttu-id="30e93-133">Projekti kopeerimise funktsioon värskendati, et tagada tööülesandele viitavate kuluprognoosi ridade kopeerimine sihtprojekti.</span><span class="sxs-lookup"><span data-stu-id="30e93-133">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="30e93-134">Plaanimine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="30e93-134">Planning and Tracking</span></span> | <span data-ttu-id="30e93-135">2154306</span><span class="sxs-lookup"><span data-stu-id="30e93-135">2154306</span></span> | <span data-ttu-id="30e93-136">Parandatud on probleemid kuluprognooside kustutamisega Project Operationsis ressursipõhiste stsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="30e93-136">Fixed issues with deleting expense estimates in Project Operations for resource-based scenarios.</span></span> |
| <span data-ttu-id="30e93-137">Plaanimine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="30e93-137">Planning and Tracking</span></span> | <span data-ttu-id="30e93-138">2173259</span><span class="sxs-lookup"><span data-stu-id="30e93-138">2173259</span></span> | <span data-ttu-id="30e93-139">Projekti kopeerimisfunktsioon on värskendatud, et tagada, et see ei kuvaks teatud stsenaariumite korral tõrketeadet **WBS-i kopeerimine**.</span><span class="sxs-lookup"><span data-stu-id="30e93-139">Project copy function updated to ensure it doesn't display **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="30e93-140">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="30e93-140">Time and Expense</span></span> | <span data-ttu-id="30e93-141">2148910</span><span class="sxs-lookup"><span data-stu-id="30e93-141">2148910</span></span> | <span data-ttu-id="30e93-142">Lahendatud on kuvamisprobleem lehel **Kirje redigeerimine** ruudustikus **Ajakirje**.</span><span class="sxs-lookup"><span data-stu-id="30e93-142">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="30e93-143">Aeg ja kulu</span><span class="sxs-lookup"><span data-stu-id="30e93-143">Time and Expense</span></span> | <span data-ttu-id="30e93-144">2159798</span><span class="sxs-lookup"><span data-stu-id="30e93-144">2159798</span></span> | <span data-ttu-id="30e93-145">Süvendati kontrolli tagamaks, et kinnitatud kulukirjeid ei saaks redigeerida.</span><span class="sxs-lookup"><span data-stu-id="30e93-145">Tightened controls to ensure approved expense entries can't be edited.</span></span> |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a><span data-ttu-id="30e93-146">Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="30e93-146">Project management and accounting on Dynamics 365 Finance</span></span>

<span data-ttu-id="30e93-147">Lisateavet vaadake jaotisest [Mis on uut jaanuaris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks](whats-new-jan-2021-resource-based.md).</span><span class="sxs-lookup"><span data-stu-id="30e93-147">For more information, see [What's new January 2021 - Project Operations for resource/non-stocked based scenarios](whats-new-jan-2021-resource-based.md).</span></span>

## <a name="regulatory-updates"></a><span data-ttu-id="30e93-148">Regulatiivsed uuendused</span><span class="sxs-lookup"><span data-stu-id="30e93-148">Regulatory updates</span></span>

<span data-ttu-id="30e93-149">Lisateavet teenuse Finance and Operations rakenduste regulatiivsete uuenduste kohta vaadake teemast [Regulatiivsed uuendused](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span><span class="sxs-lookup"><span data-stu-id="30e93-149">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="30e93-150">Veel üks võimalus regulatiivsete värskenduste kohta teada saada on logida teenusesse LCS ja vaadata plaanitud regulatiivseid värskendusi, kasutades probleemide otsingu tööriista.</span><span class="sxs-lookup"><span data-stu-id="30e93-150">Another way to learn about regulatory updates is to sign in to LCS and view the planned regulatory updates using the issue search tool.</span></span> <span data-ttu-id="30e93-151">Probleemi otsing võimaldab teil otsida riigi, funktsiooni tüübi ja väljalaske põhjal.</span><span class="sxs-lookup"><span data-stu-id="30e93-151">Issue search lets you search by country, type of feature, and release.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]