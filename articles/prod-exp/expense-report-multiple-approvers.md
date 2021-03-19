---
title: Kuluaruande mitu kinnitajat
description: Selles teemas antakse teavet kuluaruannete kohta, mis vajavad kinnitamist mitme kinnita poolt.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271708"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="0e340-103">Kuluaruande mitu kinnitajat</span><span class="sxs-lookup"><span data-stu-id="0e340-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="0e340-104">Olenevalt teie organisatsiooni kulude kinnitamise poliitikatest, võib olla vajalik, et töötaja esitatud kuluaruande kinnitab rohkem kui üks inimene.</span><span class="sxs-lookup"><span data-stu-id="0e340-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="0e340-105">Kui häälestate kuluaruande kinnitamise töövoo protsessi, saate lisada töövoo elemendid, mis hõlmavad ülesandeid või etappe ühe või mitme kuluaruande kinnitaja jaoks.</span><span class="sxs-lookup"><span data-stu-id="0e340-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0e340-106">Näiteks võite nõuda, et kõik kuluaruanded peab esmalt kinnitama aruande esitanud töötaja juht ja seejärel ostureskontro koordinaator.</span><span class="sxs-lookup"><span data-stu-id="0e340-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="0e340-107">Kui otsustate nõuda mitut kuluaruande kinnitajat, saate lisada töövoo elemendid mõnel järgnevatest viisidest.</span><span class="sxs-lookup"><span data-stu-id="0e340-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0e340-108">Lisage üks kinnitamise element, millel on üks etapp.</span><span class="sxs-lookup"><span data-stu-id="0e340-108">Add one approval element that has one step.</span></span> <span data-ttu-id="0e340-109">Näiteks võib etapp nõuda, et kuluaruanne määratakse kasutajaterühmale ja 50% rühmaliikmetest peab selle kinnitama.</span><span class="sxs-lookup"><span data-stu-id="0e340-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0e340-110">Lisage üks kinnitamise element, millel on mitu etappi.</span><span class="sxs-lookup"><span data-stu-id="0e340-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0e340-111">Näiteks võivad kinnitamise elemendil olla järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="0e340-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0e340-112">Kuluaruande esitanud töötaja juht kinnitab selle.</span><span class="sxs-lookup"><span data-stu-id="0e340-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0e340-113">Ostureskontro sekretör kontrollib kviitungeid ja kuluaruande üksuseid.</span><span class="sxs-lookup"><span data-stu-id="0e340-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0e340-114">Eelarve omanik kinnitab kuluaruande heaks.</span><span class="sxs-lookup"><span data-stu-id="0e340-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0e340-115">Lisage mitu kinnitamise elementi, millest igal on üks etapp.</span><span class="sxs-lookup"><span data-stu-id="0e340-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0e340-116">Näiteks võite lisada iga järgmise etapi jaoks eraldi kinnitamise elemendi.</span><span class="sxs-lookup"><span data-stu-id="0e340-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0e340-117">Töötaja juht kinnitab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="0e340-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0e340-118">Eelarve omanik kinnitab kuluaruande heaks.</span><span class="sxs-lookup"><span data-stu-id="0e340-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]