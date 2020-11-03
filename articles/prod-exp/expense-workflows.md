---
title: Kuluhalduse töövoogude seadistamine
description: Saate seadistada töövoo protsessi reisi-ja kuludokumentide ülevaatamiseks ja kinnitamiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075110"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="e0a51-103">Kuluhalduse töövoogude seadistamine</span><span class="sxs-lookup"><span data-stu-id="e0a51-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0a51-104">Saate seadistada töövoo protsessi, mida kasutatakse reisi-ja kuludokumentide ülevaatamiseks ja kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="e0a51-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="e0a51-105">Dokumendid, mille jaoks saab töövooge määratleda, hõlmavad kuluaruandeid, reisitellimusi ja ettemaksetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="e0a51-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="e0a51-106">Töövoog tähistab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="e0a51-106">A workflow represents a business process.</span></span> <span data-ttu-id="e0a51-107">See määratleb, kuidas dokument süsteemi läbib ja näitab, kes peab tööülesande lõpetama või dokumendi kinnitama.</span><span class="sxs-lookup"><span data-stu-id="e0a51-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e0a51-108">Teie ettevõttes on töövoo süsteemi kasutamisel mitu eelist.</span><span class="sxs-lookup"><span data-stu-id="e0a51-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="e0a51-109">**Järjepidevad protsessid** – saate määratleda konkreetsete dokumentide (nt ostutellimuste ja kuluaruannete) kinnitamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="e0a51-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e0a51-110">Töövoogude süsteemi kasutamine aitab tagada, et dokumente töödeldakse ja kinnitatakse järjekindlalt ja tõhusalt.</span><span class="sxs-lookup"><span data-stu-id="e0a51-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="e0a51-111">Protsessi nähtavus – saate jälgida kindla töövoo eksemplari olekut, ajalugu ja jõudluse mõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="e0a51-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e0a51-112">See aitab teil kindlaks teha, kas töövoogu tuleb muuta tõhusamaks.</span><span class="sxs-lookup"><span data-stu-id="e0a51-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="e0a51-113">Tsentraliseeritud tööloend – kasutajad saavad vaadata tsentraliseeritud tööloendit, et kuvada neile määratud töövoo tööülesandeid ja kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="e0a51-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="e0a51-114">**Töövoogude tüübid, mida saare luua**</span><span class="sxs-lookup"><span data-stu-id="e0a51-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="e0a51-115">Järgmises tabelis on loetletud töövoogude tüübid, mida saate valikus **Kulu** luua.</span><span class="sxs-lookup"><span data-stu-id="e0a51-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="e0a51-116"><strong>Tüüp</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="e0a51-117"><strong>Kasutage seda tüüpi järgnevaks</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="e0a51-118"><strong>Kuluaruanne</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="e0a51-119">Kuluaruannete jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="e0a51-120"><strong>Kuluaruande automaatne sisestamine</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="e0a51-121">Kuluaruannete jaoks automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="e0a51-122"><strong>Kulu reaüksus</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="e0a51-123">Kuluaruannete reaüksuste jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="e0a51-124"><strong>Kulu reaüksuse automaatne sisestamine</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="e0a51-125">Kuluaruannete reaüksuste jaoks automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="e0a51-126"><strong>Reisitellimus</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="e0a51-127">Reisitellimuste jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="e0a51-128"><strong>Ettemakse taotlus</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="e0a51-129">Ettemakse taotluste jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="e0a51-130"><strong>Käibemaksu sissenõudmine</strong></span><span class="sxs-lookup"><span data-stu-id="e0a51-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="e0a51-131">Käibemaksu (VAT) sissenõudmise kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="e0a51-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

