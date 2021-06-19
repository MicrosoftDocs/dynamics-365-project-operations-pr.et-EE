---
title: Kinnitamiskomplektid
description: Selles teemas antakse teavet kinnituskomplektide, taotluste ja nende toimingute alamkomplektide kohta.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116866"
---
# <a name="approval-sets"></a><span data-ttu-id="e70df-103">Kinnitamiskomplektid</span><span class="sxs-lookup"><span data-stu-id="e70df-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e70df-104">Kinnitamiskomplektid rühmitavad kinnitamise taotlused kokku toimingute väiksemateks alamhulkadeks.</span><span class="sxs-lookup"><span data-stu-id="e70df-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="e70df-105">See rühmitamine võimaldab projektil kinnitusi töödelda tellimuse järgi ja võimaldab neid uuesti teha ja järjestada.</span><span class="sxs-lookup"><span data-stu-id="e70df-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="e70df-106">Rühmitamine parandab suurte kinnituse koguste puhul kinnituse töötlemise usaldusväärsust ja jälgitavust.</span><span class="sxs-lookup"><span data-stu-id="e70df-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="e70df-107">Kinnituskomplektid näitavad nendega seotud kirjete üldist töötlemise olekut.</span><span class="sxs-lookup"><span data-stu-id="e70df-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="e70df-108">Kui kinnituse kirjet töödeldakse kinnituskomplekti abil, liigub kirje olekust **Esitatud** olekusse **Kinnitatud** ja ühendatakse kinnituskomplekti küljest lahti.</span><span class="sxs-lookup"><span data-stu-id="e70df-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="e70df-109">Kui kirje kinnitamiseks esitamine nurjub, jääb kirje olekusse **Esitatud** ja kinnituskomplekt on märgitud nurjunuks.</span><span class="sxs-lookup"><span data-stu-id="e70df-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="e70df-110">Kinnitamiskomplekt logib nurjumise tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="e70df-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="e70df-111">Kinnituste ja kinnituskomplektide töötlemine</span><span class="sxs-lookup"><span data-stu-id="e70df-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="e70df-112">Töötlemiseks järjekorda pandud kinnitused kuvatakse vaates **Kinnituste töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="e70df-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="e70df-113">Süsteem proovib kõiki kirjeid mitu korda asünkroonselt töödelda, sh kui eelmised katsed nurjusid, proovib see uuesti proovida kinnitada.</span><span class="sxs-lookup"><span data-stu-id="e70df-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="e70df-114">Välja **Kinnitamiskomplekti eluiga** salvestab katsete arvu, mis on komplekti töötlemiseks jäänud, enne kui see märgitakse nurjunuks.</span><span class="sxs-lookup"><span data-stu-id="e70df-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="e70df-115">Nurjunud kinnitused ja kinnituskomplektid</span><span class="sxs-lookup"><span data-stu-id="e70df-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="e70df-116">Vaates **Nurjunud kinnitamised** on loetletud kõik kasutaja sekkumist vajavad kinnitused.</span><span class="sxs-lookup"><span data-stu-id="e70df-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="e70df-117">Avage seostatud kinnituskomplekti logid, et tuvastada nurjumise põhjus.</span><span class="sxs-lookup"><span data-stu-id="e70df-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="e70df-118">Valiku "**Proovi uuesti** valimine lisab kinnituskomplekti eluea loenduse, liigutab kinnituse tagasi olekusse **Töötleb** ja proovib töödelda ülejäänud kirjeid.</span><span class="sxs-lookup"><span data-stu-id="e70df-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="e70df-119">Kinnituskomplektide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e70df-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="e70df-120">Funktsiooni Kinnituskomplektid lubamine</span><span class="sxs-lookup"><span data-stu-id="e70df-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="e70df-121">Enne funktsiooni Kinnituskomplektid lubamist veenduge, et praegu ei töödeldaks ühtegi kinnitust.</span><span class="sxs-lookup"><span data-stu-id="e70df-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e70df-122">Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Luba kaasaegsed kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="e70df-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="e70df-123">Funktsiooni Kinnituskomplektid väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="e70df-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="e70df-124">Enne funktsiooni Kinnituskomplektid väljalülitamist veenduge, et praegu ei töödeldaks ühtegi kinnitust.</span><span class="sxs-lookup"><span data-stu-id="e70df-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e70df-125">Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Keela kaasaegsed kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="e70df-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="e70df-126">Asünkroonse lävendi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e70df-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="e70df-127">Kinnituskomplektide loomisel teisaldatakse töötlemine taustale, kui kinnitamiseks valitud kirjete arv ületab määratud läviväärtuse.</span><span class="sxs-lookup"><span data-stu-id="e70df-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="e70df-128">Kasutage välja **Asünkroonne lävi** konfigureerimiseks, millal kinnitamise töötlemist tuleks käitada sünkroonselt või asünkroonselt.</span><span class="sxs-lookup"><span data-stu-id="e70df-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="e70df-129">Kehtivad väärtused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="e70df-129">Valid values are:</span></span>

  - <span data-ttu-id="e70df-130">Null: kõiki taotlusi tuleks töödelda asünkroonselt.</span><span class="sxs-lookup"><span data-stu-id="e70df-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="e70df-131">Nullist suuremad arvud: kinnitusi töödeldakse asünkroonselt ainult juhul, kui esitatud kinnituste arv ületab selle väärtuse.</span><span class="sxs-lookup"><span data-stu-id="e70df-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
