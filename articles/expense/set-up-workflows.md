---
title: Töövoogude seadistamine kuluhalduseks
description: Saate seadistada töövoo protsessi, mida kasutatakse reisi-ja kuludokumentide ülevaatamiseks ja kinnitamiseks.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074983"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="2cb7c-103">Töövoogude seadistamine kuluhalduseks</span><span class="sxs-lookup"><span data-stu-id="2cb7c-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="2cb7c-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="2cb7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2cb7c-105">Saate seadistada töövoo protsessi reisi-ja kuludokumentide ülevaatamiseks ja kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="2cb7c-106">Saate määratleda kuluaruannete, reisidetellimuste ja ettemaksetaotluste töövood.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="2cb7c-107">Töövoog esindab äriprotsessi ja määratleb, kuidas dokument süsteemist läbi liigub.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="2cb7c-108">Töövoog näitab ka, kes peab tööülesande lõpetama või dokumendi kinnitama.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="2cb7c-109">Teie ettevõttes on töövoo süsteemi kasutamisel mitu eelist.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="2cb7c-110">**Järjepidevad protsessid** : saate määratleda konkreetsete dokumentide (nt ostutellimuste ja kuluaruannete) kinnitamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="2cb7c-111">Töövoogude süsteemi kasutamine aitab tagada, et dokumente töödeldakse ja kinnitatakse järjekindlalt ja tõhusalt.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="2cb7c-112">**Protsessi nähtavus** : saate jälgida kindla töövoo eksemplari olekut, ajalugu ja jõudluse mõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="2cb7c-113">See aitab teil kindlaks teha, kas töövoogu tuleb muuta tõhusamaks.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="2cb7c-114">**Tsentraliseeritud tööloend** : kasutajad saavad vaadata tsentraliseeritud tööloendit, et kuvada neile määratud töövoo tööülesandeid ja kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="2cb7c-115">Töövoo tüübid</span><span class="sxs-lookup"><span data-stu-id="2cb7c-115">Workflow types</span></span>

<span data-ttu-id="2cb7c-116">Järgmises tabelis on loetletud töövoogude tüübid, mida saate **Kuluhalduses** luua.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="2cb7c-117"><strong>Tüüp</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="2cb7c-118"><strong>Kasutage seda tüüpi järgnevaks</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="2cb7c-119"><strong>Kuluaruande automaatne kinnitamine</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="2cb7c-120">Kuluaruannete jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="2cb7c-121"><strong>Kuluaruande automaatne sisestamine</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="2cb7c-122">Kuluaruannete jaoks automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="2cb7c-123"><strong>Kulu reaüksus</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="2cb7c-124">Kuluaruannete reaüksuste jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="2cb7c-125"><strong>Kulu reaüksuse automaatne sisestamine</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="2cb7c-126">Kuluaruannete reaüksuste jaoks automaatse sisestamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="2cb7c-127"><strong>Reisitellimus</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="2cb7c-128">Reisitellimuste jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="2cb7c-129"><strong>Ettemakse taotlus</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="2cb7c-130">Ettemakse taotluste jaoks kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="2cb7c-131"><strong>Käibemaksu sissenõudmine</strong></span><span class="sxs-lookup"><span data-stu-id="2cb7c-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="2cb7c-132">Käibemaksu (VAT) sissenõudmise kinnitamise töövoogude loomine.</span><span class="sxs-lookup"><span data-stu-id="2cb7c-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
