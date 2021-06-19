---
title: Kuluaruanded ja mitu kinnitajat
description: Selles teemas antakse teavet kuluaruannete kohta, mis vajavad kinnitamist rohkem kui ühe inimese poolt.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002051"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="982fc-103">Kuluaruanded ja mitu kinnitajat</span><span class="sxs-lookup"><span data-stu-id="982fc-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="982fc-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="982fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="982fc-105">Olenevalt teie organisatsiooni kulude kinnitamise poliitikatest, võib olla vajalik, et esitatud kuluaruande kinnitab rohkem kui üks inimene.</span><span class="sxs-lookup"><span data-stu-id="982fc-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="982fc-106">Kui häälestate kuluaruande kinnitamise töövoo protsessi, saate lisada töövoo elemendid, mis hõlmavad ülesandeid või etappe ühe või mitme kuluaruande kinnitaja jaoks.</span><span class="sxs-lookup"><span data-stu-id="982fc-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="982fc-107">Näiteks võite nõuda, et kõik kuluaruanded peab kinnitama kaks eraldi inimest – aruande esitanud töötaja juht ja ostureskontro koordinaator.</span><span class="sxs-lookup"><span data-stu-id="982fc-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="982fc-108">Kui otsustate nõuda mitut kuluaruande kinnitajat, saate lisada töövoo elemendid mõnel järgnevatest viisidest.</span><span class="sxs-lookup"><span data-stu-id="982fc-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="982fc-109">Lisage üks kinnitamise element, millel on üks etapp.</span><span class="sxs-lookup"><span data-stu-id="982fc-109">Add one approval element that has one step.</span></span> <span data-ttu-id="982fc-110">Näiteks võib etapp nõuda, et kuluaruanne määratakse kasutajaterühmale ja 50% rühmaliikmetest peab selle kinnitama.</span><span class="sxs-lookup"><span data-stu-id="982fc-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="982fc-111">Lisage üks kinnitamise element, millel on mitu etappi.</span><span class="sxs-lookup"><span data-stu-id="982fc-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="982fc-112">Näiteks võivad kinnitamise elemendil olla järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="982fc-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="982fc-113">Kuluaruande esitanud töötaja juht kinnitab selle.</span><span class="sxs-lookup"><span data-stu-id="982fc-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="982fc-114">Ostureskontro sekretör kontrollib kviitungeid ja kuluaruande üksuseid.</span><span class="sxs-lookup"><span data-stu-id="982fc-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="982fc-115">Eelarve omanik kinnitab kuluaruande heaks.</span><span class="sxs-lookup"><span data-stu-id="982fc-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="982fc-116">Lisage mitu kinnitamise elementi, millest igal on üks etapp.</span><span class="sxs-lookup"><span data-stu-id="982fc-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="982fc-117">Näiteks võite lisada iga järgmise etapi jaoks eraldi kinnitamise elemendi.</span><span class="sxs-lookup"><span data-stu-id="982fc-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="982fc-118">Töötaja juht kinnitab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="982fc-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="982fc-119">Eelarve omanik kinnitab kuluaruande heaks.</span><span class="sxs-lookup"><span data-stu-id="982fc-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]