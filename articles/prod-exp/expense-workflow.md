---
title: Kuluhalduse töövoog
description: Selles teemas kirjeldatakse, kuidas kasutada rakenduses Microsoft Dynamics 365 Finance töövoo süsteemi, et seadistada kuluhalduses kuluaruannete ülevaatamise protsessi.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005201"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="31247-103">Kuluhalduse töövoog</span><span class="sxs-lookup"><span data-stu-id="31247-103">Expense management workflow</span></span>

<span data-ttu-id="31247-104">Saate kasutada töövoo süsteemi, et seadistada kuluhalduses kuluaruannete ülevaatamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="31247-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="31247-105">Saate seadistada töövoo, mis kasutab järgmisi kriteeriume, et määratleda, kes võib kuluaruande kinnitada.</span><span class="sxs-lookup"><span data-stu-id="31247-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="31247-106">Töötaja aruannete hierarhia ja eelmääratletud kinnitamise piirid</span><span class="sxs-lookup"><span data-stu-id="31247-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="31247-107">Mitmetasandiline kinnitamine, mis toetab ajutisi kinnitusi ja lõplikku kinnitajat</span><span class="sxs-lookup"><span data-stu-id="31247-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="31247-108">Finantsdimensioonid ja projekti vastutusala</span><span class="sxs-lookup"><span data-stu-id="31247-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="31247-109">Määramine kindlatele kasutajatele või kasutajarühmadele</span><span class="sxs-lookup"><span data-stu-id="31247-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="31247-110">Töövoo kinnitamised saab luua kuluaruannete, reisitellimuste, sularaha ettemaksete ja käibemaksu (VAT) taastamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="31247-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="31247-111">**Näide**</span><span class="sxs-lookup"><span data-stu-id="31247-111">**Example**</span></span>

<span data-ttu-id="31247-112">Järgmine protsess on näiteks kuluaruande kuluhalduse töövoost.</span><span class="sxs-lookup"><span data-stu-id="31247-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="31247-113">Töötaja loob ja salvestab kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="31247-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="31247-114">Töötaja esitab kuluaruande kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="31247-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="31247-115">Kinnitaja tuvastatakse töövoo seadistamisel määratletud reeglite põhjal.</span><span class="sxs-lookup"><span data-stu-id="31247-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="31247-116">Kinnitaja saab teate, et kuluaruanne on kinnitamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="31247-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="31247-117">Kinnitaja vaatab kuluaruande üle ja kontrollib, kas järgmised tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="31247-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="31247-118">Kulud ei riku ühtegi kulupoliitikat.</span><span class="sxs-lookup"><span data-stu-id="31247-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="31247-119">Kui kulu rikub poliitikat, kontrollib kinnitaja, et kuluaruanne sisaldaks kehtivat äriõigustust.</span><span class="sxs-lookup"><span data-stu-id="31247-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="31247-120">Kuluaruandele lisatakse elektroonilised kviitungid.</span><span class="sxs-lookup"><span data-stu-id="31247-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="31247-121">Kinnitaja kinnitab kuluaruande heaks.</span><span class="sxs-lookup"><span data-stu-id="31247-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="31247-122">Kuluaruanne määratakse sisestamiseks ostureskontro koordinaatorile.</span><span class="sxs-lookup"><span data-stu-id="31247-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="31247-123">Olenevalt sellest, kas automaatne sisestamine on konfigureeritud, kuvatakse üks järgmistest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="31247-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="31247-124">Kui automaatne sisestamine on konfigureeritud, töödeldakse kuluaruanne tasumiseks ja värskendatakse kuluaruande olekut.</span><span class="sxs-lookup"><span data-stu-id="31247-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="31247-125">Kui automaatset sisestamist ei konfigureerita, kontrollib ostureskontro koordinaator, et kõik algsed kviitungid oleksid esitatud ja et sissetulekud oleksid joondatud kuluaruande kuludega.</span><span class="sxs-lookup"><span data-stu-id="31247-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="31247-126">Kõigi kuluaruandesse sisestatud maksukoodide õigsust tuleb kontrollida.</span><span class="sxs-lookup"><span data-stu-id="31247-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="31247-127">Pärast nende nõuete kontrollimist sisestatakse kuluaruanne.</span><span class="sxs-lookup"><span data-stu-id="31247-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="31247-128">Pärast kuluaruande sisestamist on kuluaruande jaoks lubatud maksta ja töötajale makstakse hüvitis.</span><span class="sxs-lookup"><span data-stu-id="31247-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]