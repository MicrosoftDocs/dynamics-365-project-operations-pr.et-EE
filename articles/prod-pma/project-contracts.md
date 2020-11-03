---
title: Projektilepingud
description: Selles teemas on toodud näited projektilepingutest, mida saate luua erinevat tüüpi projektide ja rahastamisallikate jaoks, ning seda, kuidas saate hallata lepinguid ja klientide arveprojekte.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075087"
---
# <a name="project-contracts"></a><span data-ttu-id="8bc70-103">Projektilepingud</span><span class="sxs-lookup"><span data-stu-id="8bc70-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bc70-104">Selles artiklis on toodud näited projektilepingutest, mida saate luua erinevat tüüpi projektide ja rahastamisallikate jaoks, ning seda, kuidas saate hallata lepinguid ja klientide arveprojekte.</span><span class="sxs-lookup"><span data-stu-id="8bc70-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="8bc70-105">Projektilepingu jaoks loodav projektitüüp määratleb meetodi, mida kasutatakse projekti osas kliendiga arveldamiseks.</span><span class="sxs-lookup"><span data-stu-id="8bc70-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="8bc70-106">Projektilepingut ja sellega seotud projekti saab muuta, kuid projektitüüpi ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="8bc70-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="8bc70-107">Projektilepingu abil saate korraga arveldada ühe või mitu projekti.</span><span class="sxs-lookup"><span data-stu-id="8bc70-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="8bc70-108">Samuti aitab projektileping tagada iga projekti struktuuri jaoks järjepideva arvete esitamise protseduuri.</span><span class="sxs-lookup"><span data-stu-id="8bc70-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="8bc70-109">Iga arveldatav projekt tuleb seostada projektilepinguga.</span><span class="sxs-lookup"><span data-stu-id="8bc70-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="8bc70-110">Projektilepingu sätted rakenduvad kõigile projektilepinguga seotud projektidele ja projektidele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="8bc70-111">Projektilepinguga saab määrata ühe või mitu rahastamisallikat.</span><span class="sxs-lookup"><span data-stu-id="8bc70-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="8bc70-112">Seega saate jagada arvete vahel mitu rahastajat, seadistades rahastamise piirid, nii et rahastamisallikatelt ei ole arvestata rohkem kui kindlaksmääratud summa, ja konfigureerida rahastamiseeskirju maksustamise kulude osas.</span><span class="sxs-lookup"><span data-stu-id="8bc70-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="8bc70-113">Projektilepingute rahastamine</span><span class="sxs-lookup"><span data-stu-id="8bc70-113">Funding for project contracts</span></span>
<span data-ttu-id="8bc70-114">Mõned projektilepingud täpsustavad, et mitu osapoolt jagavad vastutust projekti kulude rahastamise eest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="8bc70-115">Järgmiselt on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="8bc70-115">Here are some examples:</span></span>

-   <span data-ttu-id="8bc70-116">Suur klient, kellel on mitu allüksust, nõuab projekti rahastamist allüksuse järgi.</span><span class="sxs-lookup"><span data-stu-id="8bc70-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="8bc70-117">Teie ettevõte jagab suure projekti kulusid välise organisatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="8bc70-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="8bc70-118">Teede projekti kaasrahastavad kaks omavalitsust.</span><span class="sxs-lookup"><span data-stu-id="8bc70-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="8bc70-119">Sillaprojekti rahastab valitsuse toetus ja eraettevõte.</span><span class="sxs-lookup"><span data-stu-id="8bc70-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="8bc70-120">Rakenduses Dynamics 365 Finance saate jagada ühe tehingu või kogu projekti arve mitme kliendi, stipendiumi või organisatsiooni vahel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="8bc70-121">Mitme rahastajaga projektides nimetatakse kõiki osapooli, kes toetavad täiustatud rahastamise projekti rahastamist, rahastamisallikateks.</span><span class="sxs-lookup"><span data-stu-id="8bc70-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="8bc70-122">Pärast seda, kui klient, organisatsioon või toetus on määratletud rahastamisallikana, saab selle määrata ühele või mitmele rahastamisreeglile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="8bc70-123">Rahastamise reeglid sisaldavad kriteeriume, mis määratlevad, kuidas kulud eraldatakse projekti erinevatele rahastamisallikatele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="8bc70-124">Kuna varutud kaupa (nt ostutellimustes ja ostutellimustes kuvatavaid kirjeid) ei saa tükeldada, ei saa kulu summat jagada mitme rahastamisallika vahel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="8bc70-125">Seega jääb rahastamisallika väärtuseks 0 (null), kuni sisestatakse varude väljaminek.</span><span class="sxs-lookup"><span data-stu-id="8bc70-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="8bc70-126">Kui varude väljaminek sisestatakse, jaotatakse kulu summa vastavalt projekti konto jaotamise reeglitele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="8bc70-127">Siin on mõned sammud, mida saate teha, et arvete jagamine oleks mitme rahastamisallika vahel hõlpsam.</span><span class="sxs-lookup"><span data-stu-id="8bc70-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="8bc70-128">Määrake, et kõik projekti jaoks sisestatud tehingud kasutavad projekti lepinguna sama müügivaluutat.</span><span class="sxs-lookup"><span data-stu-id="8bc70-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="8bc70-129">Seadistage rahastamise limiidid, nii et rahastamise allikat ei oleks arveldatud üle teatud summa projekti piires.</span><span class="sxs-lookup"><span data-stu-id="8bc70-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="8bc70-130">Konfigureerige iga töötaja, kauba, kategooria, kategooriagrupi ja kandetüübi (või kõigi kandetüübi) jaoks rahastamise reeglid ja rahastamise limiidid.</span><span class="sxs-lookup"><span data-stu-id="8bc70-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="8bc70-131">Valige valikuline algus- ja lõppkuupäev, et määratleda periood, millal mingi rahastamise reegel kehtib.</span><span class="sxs-lookup"><span data-stu-id="8bc70-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="8bc70-132">Määrake protsent, mille eest iga rahastamisallikas vastutab.</span><span class="sxs-lookup"><span data-stu-id="8bc70-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="8bc70-133">Määrake, millist rahastamisallikat rahastatakse saastekvootide eraldamise arvutustest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="8bc70-134">Seadistage reeglid, mis määratlevad, kuidas projekti kulud arveldatakse välisklientidele ja mille eest tuleb tasuda sisemistele organisatsioonidele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="8bc70-135">Kirjendage tehingud ootel rahastamiskontol, kuni saate täiendavaid vahendeid või kuni otsustate kulud sisemiselt kanda.</span><span class="sxs-lookup"><span data-stu-id="8bc70-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="8bc70-136">Tehinguga seostamiseks kasutatava maksurühma määratlemiseks otsitakse projekti jaoks maksurühma määramine.</span><span class="sxs-lookup"><span data-stu-id="8bc70-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="8bc70-137">Kui projekti tasemel ei ole maksurühma määramist tehtud, otsitakse projekti lepingust.</span><span class="sxs-lookup"><span data-stu-id="8bc70-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="8bc70-138">Näide: mitu rahastamisallikat (lihtne)</span><span class="sxs-lookup"><span data-stu-id="8bc70-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="8bc70-139">Järgmises tabelis on toodud stsenaariumid rahastamise jaotamise haldamiseks mitme rahastamisallika vahel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="8bc70-140">Need stsenaariumid põhinevad järgmistel oletustel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="8bc70-141">Esmatähtsad sätted arvestatakse rahaliste vahendite eraldamiseni enne muude rahastamise reegli kriteeriumide rakendamist.</span><span class="sxs-lookup"><span data-stu-id="8bc70-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="8bc70-142">Ajavahemikke pole määratletud kuupäevavahemiku määratlemiseks, mil rahastamise reegel kehtib, pole kuupäevavahemik määratud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bc70-143"><strong>Stsenaarium</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="8bc70-144"><strong>Rahastamise allikas</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="8bc70-145"><strong>Jaotamise protsent</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="8bc70-146"><strong>Eraldamise prioriteet</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-147">Soovite kulud jaotada ühte rahastamisallikasse seni, kuni rahalised vahendid on ammendatud, eraldage kulud teisele rahastamisallikale seni, kuni rahalised vahendid on ammendatud, ning lõpuks eraldatakse ülejäänud kulud kolmandale rahastamisallikale.</span><span class="sxs-lookup"><span data-stu-id="8bc70-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-148">Rahastamisallikas　1</span><span class="sxs-lookup"><span data-stu-id="8bc70-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="8bc70-149">Rahastamisallikas　2</span><span class="sxs-lookup"><span data-stu-id="8bc70-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="8bc70-150">Rahastamisallikas　3</span><span class="sxs-lookup"><span data-stu-id="8bc70-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-151">100%</span><span class="sxs-lookup"><span data-stu-id="8bc70-151">100%</span></span></li>
<li><span data-ttu-id="8bc70-152">100%</span><span class="sxs-lookup"><span data-stu-id="8bc70-152">100%</span></span></li>
<li><span data-ttu-id="8bc70-153">100%</span><span class="sxs-lookup"><span data-stu-id="8bc70-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-154">1</span><span class="sxs-lookup"><span data-stu-id="8bc70-154">1</span></span></li>
<li><span data-ttu-id="8bc70-155">2</span><span class="sxs-lookup"><span data-stu-id="8bc70-155">2</span></span></li>
<li><span data-ttu-id="8bc70-156">3</span><span class="sxs-lookup"><span data-stu-id="8bc70-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bc70-157">Soovite eraldada 75 protsenti kuludest ühele rahastamisallikale ja 25 protsenti teisele rahastamisallikale.</span><span class="sxs-lookup"><span data-stu-id="8bc70-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="8bc70-158">Kui üks nendest rahastamisallikatest on ammendatud, soovite ülejäänud kulud maksta kolmandast rahastamisallikast.</span><span class="sxs-lookup"><span data-stu-id="8bc70-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-159">Rahastamisallikas　1</span><span class="sxs-lookup"><span data-stu-id="8bc70-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="8bc70-160">Rahastamisallikas　2</span><span class="sxs-lookup"><span data-stu-id="8bc70-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="8bc70-161">Rahastamisallikas　3</span><span class="sxs-lookup"><span data-stu-id="8bc70-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-162">75%</span><span class="sxs-lookup"><span data-stu-id="8bc70-162">75%</span></span></li>
<li><span data-ttu-id="8bc70-163">25%</span><span class="sxs-lookup"><span data-stu-id="8bc70-163">25%</span></span></li>
<li><span data-ttu-id="8bc70-164">100%</span><span class="sxs-lookup"><span data-stu-id="8bc70-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-165">1</span><span class="sxs-lookup"><span data-stu-id="8bc70-165">1</span></span></li>
<li><span data-ttu-id="8bc70-166">1</span><span class="sxs-lookup"><span data-stu-id="8bc70-166">1</span></span></li>
<li><span data-ttu-id="8bc70-167">2</span><span class="sxs-lookup"><span data-stu-id="8bc70-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-168">Soovite eraldada 75 protsenti kuludest ühele rahastamisallikale ja 25 protsenti teisele rahastamisallikale.</span><span class="sxs-lookup"><span data-stu-id="8bc70-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="8bc70-169">Kui üks nendest rahastamisallikatest on ammendatud, soovite ülejäänud kulud jagada kolmanda ja neljanda rahastamisallika vahel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-170">Rahastamisallikas　1</span><span class="sxs-lookup"><span data-stu-id="8bc70-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="8bc70-171">Rahastamisallikas　2</span><span class="sxs-lookup"><span data-stu-id="8bc70-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="8bc70-172">Rahastamisallikas　3</span><span class="sxs-lookup"><span data-stu-id="8bc70-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="8bc70-173">Rahastamisallikas　4</span><span class="sxs-lookup"><span data-stu-id="8bc70-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-174">75%</span><span class="sxs-lookup"><span data-stu-id="8bc70-174">75%</span></span></li>
<li><span data-ttu-id="8bc70-175">25%</span><span class="sxs-lookup"><span data-stu-id="8bc70-175">25%</span></span></li>
<li><span data-ttu-id="8bc70-176">50%</span><span class="sxs-lookup"><span data-stu-id="8bc70-176">50%</span></span></li>
<li><span data-ttu-id="8bc70-177">50%</span><span class="sxs-lookup"><span data-stu-id="8bc70-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-178">1</span><span class="sxs-lookup"><span data-stu-id="8bc70-178">1</span></span></li>
<li><span data-ttu-id="8bc70-179">1</span><span class="sxs-lookup"><span data-stu-id="8bc70-179">1</span></span></li>
<li><span data-ttu-id="8bc70-180">2</span><span class="sxs-lookup"><span data-stu-id="8bc70-180">2</span></span></li>
<li><span data-ttu-id="8bc70-181">2</span><span class="sxs-lookup"><span data-stu-id="8bc70-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bc70-182">Soovite eraldada esimese 25 protsenti kuludest ühele rahastamisallikale ja ülejäänud teisele rahastamisallikale.</span><span class="sxs-lookup"><span data-stu-id="8bc70-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-183">Rahastamisallikas　1</span><span class="sxs-lookup"><span data-stu-id="8bc70-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="8bc70-184">Rahastamisallikas　2</span><span class="sxs-lookup"><span data-stu-id="8bc70-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-185">25%</span><span class="sxs-lookup"><span data-stu-id="8bc70-185">25%</span></span></li>
<li><span data-ttu-id="8bc70-186">100%</span><span class="sxs-lookup"><span data-stu-id="8bc70-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8bc70-187">1</span><span class="sxs-lookup"><span data-stu-id="8bc70-187">1</span></span></li>
<li><span data-ttu-id="8bc70-188">2</span><span class="sxs-lookup"><span data-stu-id="8bc70-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="8bc70-189">Näide: mitu rahastamisallikat (keeruline)</span><span class="sxs-lookup"><span data-stu-id="8bc70-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="8bc70-190">Teil on kolm rahastamisallikat, mida soovite kasutada järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="8bc70-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="8bc70-191">Kasutage rahastamisallikat 2 ja rahastamisallikat 3 võrdselt, kuni rahastamisallikas 2 on ammendatud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="8bc70-192">Jätkake rahastamise allika 3 kasutamist, kuni see on ammendatud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="8bc70-193">Kasuta rahastamisallikat 1, kui rahastamisallikas 3 ammendatud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="8bc70-194">Selle eesmärgi saavutamiseks peate esmalt tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="8bc70-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="8bc70-195">Seadistage rahastamise piirmäärad, et rahastada allikat 2 ja allikat 3, nende vastavate summade jaoks.</span><span class="sxs-lookup"><span data-stu-id="8bc70-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="8bc70-196">Looge järgmine rahastamisreegel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="8bc70-197">Reegel 1 (prioriteet 1): eraldada 50 protsenti tehingutest rahastamisallikale 2 ja 50 protsenti rahastamisallikale 3.</span><span class="sxs-lookup"><span data-stu-id="8bc70-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="8bc70-198">Reegel 2 (prioriteet 2): eraldage 100 protsenti tehingutest rahastamisallikale 3.</span><span class="sxs-lookup"><span data-stu-id="8bc70-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="8bc70-199">Reegel 3 (prioriteet 3): eraldage 100 protsenti tehingutest rahastamisallikale 1.</span><span class="sxs-lookup"><span data-stu-id="8bc70-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="8bc70-200">See seadistus töötab, kuna kandeid kontrollitakse reeglite ja piirangute suhtes, et teha kindlaks, kas mõni nendest kannetest rakendub.</span><span class="sxs-lookup"><span data-stu-id="8bc70-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="8bc70-201">Kui tehingu suhtes ei kehti mingeid erieeskirju ega piiranguid, rakendub reegel Kõik tehingud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="8bc70-202">Kõigi reegel Kõik tehingud vastab kõigile tehingutele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="8bc70-203">Kui leitakse reegel, mis vastab tehingule, rakendatakse esmalt selles reeglis eraldatud protsent, kuid alles pärast kõigi seadistatud piirangute kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="8bc70-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="8bc70-204">Kui piirmäär on täidetud ja rahastamisallika vahendid on ammendatud, eiratakse rahastamise reeglit, mis on seotud rahastamise limiidiga, ning programm kontrollib järgmist reeglit, mis kehtib.</span><span class="sxs-lookup"><span data-stu-id="8bc70-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="8bc70-205">Mõnel juhul saab reegli alusel jaotada ainult osa tehingust.</span><span class="sxs-lookup"><span data-stu-id="8bc70-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="8bc70-206">See võib juhtuda, kuna tehingu eraldamisel jõutakse limiidini.</span><span class="sxs-lookup"><span data-stu-id="8bc70-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="8bc70-207">Sel juhul eraldatakse selle reegli järgi ainult teatud summa, nt 50 protsenti iga rahastamisallika kohta.</span><span class="sxs-lookup"><span data-stu-id="8bc70-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="8bc70-208">See kehtib reegli 1 puhul, mida kirjeldatakse käesolevas jaotises varem.</span><span class="sxs-lookup"><span data-stu-id="8bc70-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="8bc70-209">Ülejäänu jaotatakse järjekorras järgmise reegli järgi.</span><span class="sxs-lookup"><span data-stu-id="8bc70-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="8bc70-210">Järgmises tabelis käsitletakse seda stsenaariumi üksikasjalikumalt.</span><span class="sxs-lookup"><span data-stu-id="8bc70-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bc70-211"><strong>Fookus</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="8bc70-212"><strong>Üksikasjad</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-213">Rahastamise eeskirjad</span><span class="sxs-lookup"><span data-stu-id="8bc70-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-214">Eeskiri 1 (prioriteet 1): kõik tehingud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="8bc70-215">Eraldage rahastamise allikale 2 50% ja rahastamise allikale 3 50%.</span><span class="sxs-lookup"><span data-stu-id="8bc70-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="8bc70-216">Eeskiri 2 (prioriteet 2): kõik tehingud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="8bc70-217">Eraldage rahastamisallikale 3 100%.</span><span class="sxs-lookup"><span data-stu-id="8bc70-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="8bc70-218">Eeskiri 3 (prioriteet 2): kõik tehingud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="8bc70-219">Eraldage rahastamisallikale 1 100%.</span><span class="sxs-lookup"><span data-stu-id="8bc70-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bc70-220">Rahastamise limiidid</span><span class="sxs-lookup"><span data-stu-id="8bc70-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-221">Rahastamise allikas 1 piir = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="8bc70-222">Rahastamise allikas 2 piir = 500.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="8bc70-223">Rahastamise allika 3 piir = 750.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-224">Kanne 1</span><span class="sxs-lookup"><span data-stu-id="8bc70-224">Transaction 1</span></span></td>
<td><span data-ttu-id="8bc70-225"><strong>Tehingu summa:</strong> 100.00<strong>Rahastamine:</strong> Tehing makstakse vastavalt reeglile 1 ainult seetõttu, et kanne on pärast reegli 1 rakendamist täielikult tasutud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="8bc70-226">Tehingut rahastatakse võrdselt rahastamisallika 2 ja rahastamisallika 3 vahel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="8bc70-227">Rahastamisallikas 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="8bc70-228">Rahastamisallikas 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bc70-229">Kanne 2</span><span class="sxs-lookup"><span data-stu-id="8bc70-229">Transaction 2</span></span></td>
<td><span data-ttu-id="8bc70-230"><strong>Tehingu summa:</strong>5 000 00<strong>Rahastamine:</strong> Tehing makstakse vastavalt kõigile kolmele reeglile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="8bc70-231"><strong>Eeskiri 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="8bc70-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="8bc70-232">Rahastamisallikas 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="8bc70-233">Rahastamisallikas 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="8bc70-234">
<strong>Eeskiri 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="8bc70-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="8bc70-235">Rahastamisallikas 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="8bc70-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="8bc70-236">
<strong>Eeskiri 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="8bc70-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="8bc70-237">Rahastamisallikas 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="8bc70-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-238">Iga rahastamisallika jaoks jaotatud rahalised vahendid kokku</span><span class="sxs-lookup"><span data-stu-id="8bc70-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-239">Rahastamisallikas 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="8bc70-240">Rahastamisallikas 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="8bc70-241">Rahastamisallikas 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="8bc70-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="8bc70-242">Arvete esitamise reeglid</span><span class="sxs-lookup"><span data-stu-id="8bc70-242">Billing rules</span></span>
<span data-ttu-id="8bc70-243">Kui sõlmite kliendiga projektilepingu, saate määratleda, kuidas ja millal saate kliendile projekti eest arve esitada.</span><span class="sxs-lookup"><span data-stu-id="8bc70-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="8bc70-244">Pärast projekti lepingu ja projekti seadistamist saate projekti jaoks seadistada arvete esitamise reeglid.</span><span class="sxs-lookup"><span data-stu-id="8bc70-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="8bc70-245">Arvete esitamise reeglid põhinevad projekti lepingus määratud projekti tingimustel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="8bc70-246">Saate luua arvete esitamise reeglid, mis sõltuvad projekti lepingu tingimustest ja projekti tüübist (nt aja- ja materjalikulu või fikseeritud hinnaga), mida seostate arveesitamise reegliga.</span><span class="sxs-lookup"><span data-stu-id="8bc70-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="8bc70-247">Projekti lepingu jaoks saate luua rohkem kui ühe arveesitamise reegli.</span><span class="sxs-lookup"><span data-stu-id="8bc70-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="8bc70-248">Samuti saate määrata arvete esitamise reegli mitmele projektile, mis on seotud sama projekti lepinguga ja millel on sarnased arvete esitamise tingimused.</span><span class="sxs-lookup"><span data-stu-id="8bc70-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="8bc70-249">Saate seadistada järgmist tüüpi arvete esitamise reegleid.</span><span class="sxs-lookup"><span data-stu-id="8bc70-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="8bc70-250">**Tarnitav ühik** – arve kliendile, kui olete kauba kohaletoimetamise lõpetanud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="8bc70-251">Saate määratleda lepingus tarnitavad ühikud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="8bc70-252">**Edenemine** – saate kliendile arve esitada, kui olete projekti teatud protsendi lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="8bc70-253">Saate seadistada arvete esitamise reegli, mis arvutaks lõpule viidud töö protsendi või saate käsitsi arvutada lõpuleviidud töö protsendimäära ja kliendile arvestatud summa.</span><span class="sxs-lookup"><span data-stu-id="8bc70-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="8bc70-254">**Vahekokkuvõte** – arve kliendile projekti vahekokkuvõtte täielikus summas, kui vahekokkuvõte on saavutatud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="8bc70-255">**Tasu** – arve kliendile teie teenuste eest, millele lisandub haldustasu, mis on tavaliselt protsent teenuste maksumusest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="8bc70-256">**Aeg ja materjal** – arve kliendile aja ja materjali eest, mida kasutatakse projektis.</span><span class="sxs-lookup"><span data-stu-id="8bc70-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="8bc70-257">Igat tüüpi arvete korral saate määrata kliendiarvest lahutatud säilituse protsendi, kuni projekt jõuab kokkulepitud faasi.</span><span class="sxs-lookup"><span data-stu-id="8bc70-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="8bc70-258">Makse kinnipidamise protsent on määratud projekti lepingus.</span><span class="sxs-lookup"><span data-stu-id="8bc70-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="8bc70-259">Summa arvutatakse kliendi arveridade koguväärtuse põhjal ja lahutatakse sellest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="8bc70-260">**Aja- ja materjalikulu** ning **Edenemise** arveldamise reeglite puhul saate määrata tasustatavad kategooriad.</span><span class="sxs-lookup"><span data-stu-id="8bc70-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="8bc70-261">Tasustatavad kategooriad näitavad tehinguid, mis tuleb kaasata kliendiarvetele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="8bc70-262">Kui olete kliendile arveesitamise lõpetanud, arvutatakse projekti jaoks arvesumma vastavalt arvereeglitele ja luuakse projektiarve soovitus.</span><span class="sxs-lookup"><span data-stu-id="8bc70-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="8bc70-263">Järgmistes jaotistes on toodud näited, mis näitavad projektiarvete seadistamist ja haldamist.</span><span class="sxs-lookup"><span data-stu-id="8bc70-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="8bc70-264">Näide: saate luua arvete esitamise reegli, mis põhineb tarnitud ühikute arvul.</span><span class="sxs-lookup"><span data-stu-id="8bc70-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="8bc70-265">Teie organisatsioon sõlmib lepingu, et pakkuda kliendi töötajatele kokku viit koolitust hinnaga 10 000 ühe koolituse kohta.</span><span class="sxs-lookup"><span data-stu-id="8bc70-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="8bc70-266">Pärast iga koolitust saate kliendile arve esitada.</span><span class="sxs-lookup"><span data-stu-id="8bc70-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="8bc70-267">Lepingu jaoks arveesitamise reeglite seadistamisel saate kasutada järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="8bc70-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="8bc70-268">Tarneühik on üks koolitusseanss.</span><span class="sxs-lookup"><span data-stu-id="8bc70-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="8bc70-269">Ühikuhind on 10 000 koolitusseansi kohta.</span><span class="sxs-lookup"><span data-stu-id="8bc70-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="8bc70-270">Üksuste koguarv on viis koolitusseanssi.</span><span class="sxs-lookup"><span data-stu-id="8bc70-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="8bc70-271">Kui olete ühe koolitusseansi lõpetanud, saate luua arve väärtuses 10 000, esimeste tarnüksuste kohta ja saata arve kliendile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="8bc70-272">Näide: saate luua arveldamise reegli, mis põhineb määratud protsendil projekti lõpuleviimisest (käsitsi arvutamine)</span><span class="sxs-lookup"><span data-stu-id="8bc70-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="8bc70-273">Teie organisatsioon, tarkvara konsultatsioonifirma, sõlmib kliendiga lepingu, et töötada välja osa tootest, mida klient arendab.</span><span class="sxs-lookup"><span data-stu-id="8bc70-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="8bc70-274">Teie organisatsioon nõustub edastama tarkvarakoodi kuue kuu jooksul.</span><span class="sxs-lookup"><span data-stu-id="8bc70-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="8bc70-275">Klient nõustub maksma teie organisatsioonile kokku summa 100 000 töö eest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="8bc70-276">Saate luua arvete esitamise reegli, mis põhineb lepingus määratud projektiga lõpule viidud tööde protsendil.</span><span class="sxs-lookup"><span data-stu-id="8bc70-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="8bc70-277">Esimese kuu lõpus kohtute kliendiga, et teha kindlaks lõpuleviidud töö protsent.</span><span class="sxs-lookup"><span data-stu-id="8bc70-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="8bc70-278">Pärast seda, kui teie ja klient projekti üle vaatate, otsustate, et projekt on lõpule viidud 15 protsenti.</span><span class="sxs-lookup"><span data-stu-id="8bc70-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="8bc70-279">Loote arve 15,000 (15 protsenti 100 000-st) ja saadate selle kliendile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="8bc70-280">Näide: saate luua arveldamise reegli, mis põhineb määratud protsendil projekti lõpuleviimisest (automaatne arvutamine)</span><span class="sxs-lookup"><span data-stu-id="8bc70-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="8bc70-281">Teie organisatsioon, tarkvara arenduse ühing, nõustub looma kliendile palgaarvestusrakenduse väärtuses 30 000.</span><span class="sxs-lookup"><span data-stu-id="8bc70-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="8bc70-282">Klient nõustub maksma teie organisatsioonile lõpetatud töö protsendi alusel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="8bc70-283">Prognoosite, et projekti kulud on 20 000.</span><span class="sxs-lookup"><span data-stu-id="8bc70-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="8bc70-284">Projekti leping määratleb tööde kategooriad, mida te arveldamise protsessis kasutate.</span><span class="sxs-lookup"><span data-stu-id="8bc70-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="8bc70-285">Seadistate arved, mis arvutavad automaatselt arve summad iga kategooria jaoks lõpuleviidud tööde protsendi ulatuses.</span><span class="sxs-lookup"><span data-stu-id="8bc70-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="8bc70-286">Seadistate iga kategooria jaoks eelarve.</span><span class="sxs-lookup"><span data-stu-id="8bc70-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="8bc70-287">**Arendus** – kulu 15 000 ja müügitulu 20 000</span><span class="sxs-lookup"><span data-stu-id="8bc70-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="8bc70-288">**Installimine** – kulu 5000 ja müügitulu 10 000</span><span class="sxs-lookup"><span data-stu-id="8bc70-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="8bc70-289">Kui loote kliendile arve esimest korda, arvutatakse arve summa automaatselt vastavalt järgmisele teabele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="8bc70-290">Pärast ühte kuud esitab projekti töötaja ajatabeli.</span><span class="sxs-lookup"><span data-stu-id="8bc70-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="8bc70-291">Töötaja tööaja kulu on 5000 arenduseks ja 1000 installimiseks.</span><span class="sxs-lookup"><span data-stu-id="8bc70-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="8bc70-292">Arendustöö on 33 protsendi ulatuses lõpetatud (5000 tegelik kulu / 15000 eelarveline kulu) ja installimistööd on 20 protsendi ulatuses lõpetatud (1000 tegelik kulu / 5000 eelarveline kulu).</span><span class="sxs-lookup"><span data-stu-id="8bc70-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="8bc70-293">Arve summa 8667 arvutatakse automaatselt (33 protsenti 20 000-st + 20 protsenti 10 000-st).</span><span class="sxs-lookup"><span data-stu-id="8bc70-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="8bc70-294">Loote arve summas 8667 ja saadate selle kliendile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="8bc70-295">Näide: saate luua arveldamise reegli, mis põhineb kokkulepitud vahekokkuvõttel.</span><span class="sxs-lookup"><span data-stu-id="8bc70-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="8bc70-296">Teie organisatsioon, juhtimise konsultatsioonifirma, nõustub teostama turu-uuringuid tarbija toote kohta, mida klient kavatseb müüa.</span><span class="sxs-lookup"><span data-stu-id="8bc70-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="8bc70-297">Klient on nõus kasutama teie teenuseid kolme kuu jooksul alates märtsist ja nõustub maksma teie organisatsioonile 50 000.</span><span class="sxs-lookup"><span data-stu-id="8bc70-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="8bc70-298">Projektil on kolm vahekokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="8bc70-298">The project has three milestones:</span></span>

-   <span data-ttu-id="8bc70-299">1. tähtaeg: tarbijate andmete kogumine – 31. märts</span><span class="sxs-lookup"><span data-stu-id="8bc70-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="8bc70-300">2. tähtaeg: tarbija andmete analüüsimine – 30. aprill</span><span class="sxs-lookup"><span data-stu-id="8bc70-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="8bc70-301">3. tähtaeg: toote elujõulisuse ettepaneku esitamine – 31. mai</span><span class="sxs-lookup"><span data-stu-id="8bc70-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="8bc70-302">Klient nõustub maksma teie organisatsioonile 10 000 esimese etapi, 20 000 teise etapi ning 20 000 kolmanda etapi eest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="8bc70-303">Projekti lepingu sõlmimisel nõustute kliendi arvega, mis põhineb lõpetatud etapil.</span><span class="sxs-lookup"><span data-stu-id="8bc70-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="8bc70-304">Arvete esitamise reegli seadistamine hõlmab järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="8bc70-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="8bc70-305">Määratlege projekti etapid.</span><span class="sxs-lookup"><span data-stu-id="8bc70-305">Define the project milestones.</span></span>
-   <span data-ttu-id="8bc70-306">Määrake kliendile esitatava arve summa, kui iga etapp on lõpule jõudnud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="8bc70-307">Kui esimene etapp lõpetatakse 31. märtsil, saate märkida, et etapp on lõpetatud ja seejärel luua arve summas 10 000 ja saata see kliendile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="8bc70-308">Etapi eest ei saa arvet luua enne, kui olete etapi lõpetatuks märkinud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="8bc70-309">Näide: saate luua teenustel ja halduskulul põhineva arvete esitamise reegli.</span><span class="sxs-lookup"><span data-stu-id="8bc70-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="8bc70-310">Teie organisatsioon, juhtimise konsultatsioonifirma, nõustub teostama turu-uuringuid, et hinnata toote elujõulisust, mida klient, jaemüügi ettevõte arendab.</span><span class="sxs-lookup"><span data-stu-id="8bc70-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="8bc70-311">Lepingu tingimused määravad, et pakute oma kolme juhtiva konsultandi teenust, kes viib läbi uurimistööd aja- ja materjalipõhiselt.</span><span class="sxs-lookup"><span data-stu-id="8bc70-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="8bc70-312">Klient nõustub maksma 100 tunnis, pluss 10 protsenti haldustasu konsultatsioonide eest, mis on antud projektile.</span><span class="sxs-lookup"><span data-stu-id="8bc70-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="8bc70-313">Projekti lepingu sõlmimisel looge arveldamise reegel, et lisada 10-protsendine haldustasu projektiga seotud konsultatsioonidele.</span><span class="sxs-lookup"><span data-stu-id="8bc70-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="8bc70-314">Kui loote kliendile arve, on kliendile arvestatud 10-protsendise haldamise tasu pluss konsultatsioonide maksumus.</span><span class="sxs-lookup"><span data-stu-id="8bc70-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="8bc70-315">Näiteks kui kolm konsultanti töötasid projekti jaoks kokku 200 tundi, luuakse järgmise arvutuse põhjal arve summas 22 000.</span><span class="sxs-lookup"><span data-stu-id="8bc70-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="8bc70-316">200 tundi tasuga 100 tunnis = 20 000</span><span class="sxs-lookup"><span data-stu-id="8bc70-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="8bc70-317">10 protsenti haldamise tasu = 2000</span><span class="sxs-lookup"><span data-stu-id="8bc70-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="8bc70-318">Arve kogusumma = 22 000</span><span class="sxs-lookup"><span data-stu-id="8bc70-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="8bc70-319">Kui kliendilt võetakse teenustasusid ja te valite projektilepingus käibemaksugrupi, sisestatakse käibemaksugrupp automaatselt ervete esitamise reeglile tasude osas.</span><span class="sxs-lookup"><span data-stu-id="8bc70-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="8bc70-320">Näide: saate luua arvete esitamise reegi aja ja materjalide väärtuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="8bc70-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="8bc70-321">Teie organisatsioon, tarkvara konsultatsioonifirma, nõustub pakkuma teenust viie tehnilise konsultandiga, kes arendavad kliendile tarkvara järgmised kuus kuud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="8bc70-322">Klient nõustub maksma 150 iga konsultatsioonitunni eest, millele lisandub kontoritarvete maksumus.</span><span class="sxs-lookup"><span data-stu-id="8bc70-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="8bc70-323">Teie organisatsioon saadab kliendile arve iga kuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="8bc70-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="8bc70-324">Projektilepingu sõlmimisel nõustute kliendile iga kuu saatma arve aja ja materjalide eest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="8bc70-325">Saate luua arvete esitamise reegli, mis sisaldab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="8bc70-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="8bc70-326">Lepinguperiood on kuus kuud.</span><span class="sxs-lookup"><span data-stu-id="8bc70-326">The contract period is six months.</span></span>
-   <span data-ttu-id="8bc70-327">Konsultatsiooniaeg arvutatakse määraga 150 tunnis.</span><span class="sxs-lookup"><span data-stu-id="8bc70-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="8bc70-328">Kontoritarbed arveldatakse soetusmaksumuses ja projekti kogumaksumus ei tohi ületada 10 000.</span><span class="sxs-lookup"><span data-stu-id="8bc70-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="8bc70-329">Saate luua kliendi arve iga kalendrikuu lõpus projekti jooksul.</span><span class="sxs-lookup"><span data-stu-id="8bc70-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="8bc70-330">Esimesel kuul registreerisid projekti konsultandid kokku 800 tundi.</span><span class="sxs-lookup"><span data-stu-id="8bc70-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="8bc70-331">Projektile arvestatud kontoritarvete kulud on 2000.</span><span class="sxs-lookup"><span data-stu-id="8bc70-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="8bc70-332">Seetõttu saate kuu lõpus luua arve summas 122 000, mis arvutatakse 800 tunnina (150 tunnis), pluss 2000 kontoritarvete eest.</span><span class="sxs-lookup"><span data-stu-id="8bc70-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



