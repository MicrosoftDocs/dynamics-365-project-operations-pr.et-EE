---
title: Kinnitatud aja- või kulukirjete tagasivõtmine
description: Selles teemas antakse teavet varem kinnitatud aja- või kulukirjete tagasivõtmise kohta.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751047"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="18a79-103">Kinnitatud aja- või kulukirjete tagasivõtmine</span><span class="sxs-lookup"><span data-stu-id="18a79-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="18a79-104">Projektimeeskonna liige või mõni muu isik, kes aja- või kulukirje esitab, saab selle aja- või kulukirje pärast selle kinnitamist tagasi võtta.</span><span class="sxs-lookup"><span data-stu-id="18a79-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="18a79-105">Kinnitatud aja- või kulukirje tagasivõtmisel on kaks etappi.</span><span class="sxs-lookup"><span data-stu-id="18a79-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="18a79-106">Esitaja taotleb tagasivõtmist.</span><span class="sxs-lookup"><span data-stu-id="18a79-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="18a79-107">Kinnitaja kinnitab tagasivõtmise.</span><span class="sxs-lookup"><span data-stu-id="18a79-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="18a79-108">Tagasivõtmise taotlemine</span><span class="sxs-lookup"><span data-stu-id="18a79-108">Request a recall</span></span>

<span data-ttu-id="18a79-109">Kinnitatud aja- või kulukirje tagasivõtmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="18a79-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="18a79-110">Ajakirjete puhul tehke valikud **Projektid** \> **Minu töö** \> **Ajakirje**.</span><span class="sxs-lookup"><span data-stu-id="18a79-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="18a79-111">–või–</span><span class="sxs-lookup"><span data-stu-id="18a79-111">–or–</span></span>

    <span data-ttu-id="18a79-112">Kulukirjete puhul tehke valikud **Projektid** \> **Minu töö** \> **Kulud**.</span><span class="sxs-lookup"><span data-stu-id="18a79-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="18a79-113">Ajakirjete puhul valige kindla projekti ja ülesande kombinatsiooni jaoks kõik ajakirjed.</span><span class="sxs-lookup"><span data-stu-id="18a79-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="18a79-114">Alternatiivina valige ruudustikus kindla projekti kindla kuupäeva aegade üksikud lahtrid.</span><span class="sxs-lookup"><span data-stu-id="18a79-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="18a79-115">–või–</span><span class="sxs-lookup"><span data-stu-id="18a79-115">–or–</span></span>

    <span data-ttu-id="18a79-116">Kulukirjete puhul valige tagasivõtmiseks kulukirje rida.</span><span class="sxs-lookup"><span data-stu-id="18a79-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="18a79-117">Tehke valik **Kutsu tagasi**.</span><span class="sxs-lookup"><span data-stu-id="18a79-117">Select **Recall**.</span></span> <span data-ttu-id="18a79-118">Ilmub kinnituse dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="18a79-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="18a79-119">Kui valitud aja- ja kulukirjed olid juba kinnitatud, palutakse teil sisestada tagasivõtmise põhjus.</span><span class="sxs-lookup"><span data-stu-id="18a79-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="18a79-120">Sisestage tagasivõtmise põhjus ja seejärel klõpsake toimingu kinnitamiseks nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="18a79-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="18a79-121">Süsteem saadab kirje kinnitanud isikule tagasivõtmise kinnitamise taotluse.</span><span class="sxs-lookup"><span data-stu-id="18a79-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="18a79-122">Kuigi kinnitatud aja- ja kulukirjeid saab tagasi võtta, ei saa tagasivõtmise taotlust luua, kui kinnitatud aja või kulu eest on juba kliendile arve esitatud.</span><span class="sxs-lookup"><span data-stu-id="18a79-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="18a79-123">Kasutajale, kes proovib tagasivõtmise taotlust luua, kuvatakse teade, mis teatab, et aega või kulu ei saa tagasi võtta, kuna see on juba arveldatud.</span><span class="sxs-lookup"><span data-stu-id="18a79-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="18a79-124">Tagasivõtmise taotluse kinnitamine või tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="18a79-124">Approve or reject a recall request</span></span>

<span data-ttu-id="18a79-125">Tagasivõtmise taotluse kinnitamiseks või tagasilükkamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="18a79-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="18a79-126">Minge jaotisse **Projektid** \> **Minu töö** \> **Kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="18a79-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="18a79-127">Muutke loendilehel **Kinnitamised** vaade väärtusele **Tagasivõtmistaotlused kinnitamiseks**.</span><span class="sxs-lookup"><span data-stu-id="18a79-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="18a79-128">Kuvatakse esitatud tagasivõtmistaotluste loend.</span><span class="sxs-lookup"><span data-stu-id="18a79-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="18a79-129">Valige üks või mitu kirjet ja seejärel tehke kas valik **Kinnita** või **Hülga**.</span><span class="sxs-lookup"><span data-stu-id="18a79-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="18a79-130">Kui valisite suvandi **Kinnita**, kuvatakse hoiatusteade, mis selgitab kinnitamise mõju.</span><span class="sxs-lookup"><span data-stu-id="18a79-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="18a79-131">Toimingu kinnitamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="18a79-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="18a79-132">Tagasivõtmistaotlus on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="18a79-132">The recall request is approved.</span></span>

    <span data-ttu-id="18a79-133">–või–</span><span class="sxs-lookup"><span data-stu-id="18a79-133">–or–</span></span>

    <span data-ttu-id="18a79-134">Kui valisite suvandi **Hülga**, siis lükatakse tagasivõtmistaotlus tagasi.</span><span class="sxs-lookup"><span data-stu-id="18a79-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="18a79-135">Nagu tagasivõtmise taotlemisel, nii ka tagasivõtmise kinnitamisel kontrollib süsteem aja- või kulukirjetest arveldustegevust.</span><span class="sxs-lookup"><span data-stu-id="18a79-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="18a79-136">Kui kirje eest on juba arve esitatud või kui see on arve mustandis, kuvatakse kinnitajale tõrketeade, mis teatab, et aega või kulu ei saa tagasivõtmiseks kinnitada, kuna see on juba arveldatud.</span><span class="sxs-lookup"><span data-stu-id="18a79-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="18a79-137">Tagasivõtmistaotluse mõju</span><span class="sxs-lookup"><span data-stu-id="18a79-137">Impact of a recall request</span></span>

<span data-ttu-id="18a79-138">Kinnitamise tagasivõtmisel on nii tegevuslik kui ka finantsmõju.</span><span class="sxs-lookup"><span data-stu-id="18a79-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="18a79-139">Mõju tegevusele</span><span class="sxs-lookup"><span data-stu-id="18a79-139">Operational impact</span></span>

<span data-ttu-id="18a79-140">Kui tagasivõtmistaotlus on kinnitatud, märgitakse kinnitamise kirje kui **Hüljatud**.</span><span class="sxs-lookup"><span data-stu-id="18a79-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="18a79-141">Kirje olekuks määratakse kas **Tagastatud** või **Hüljatud**, olenevalt sellest, kas see on aja- või kulukirje.</span><span class="sxs-lookup"><span data-stu-id="18a79-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="18a79-142">Projektimeeskonna liige saab kirjeid vaadata, redigeerida ja seejärel uuesti esitada või kirjeid täielikult kustutada.</span><span class="sxs-lookup"><span data-stu-id="18a79-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="18a79-143">Kui tagasivõtmistaotlus lükatakse tagasi, jääb kirje olekuks **Kinnitatud**ja projektimeeskonna liige ega kinnitaja ei saa kirjet redigeerida.</span><span class="sxs-lookup"><span data-stu-id="18a79-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="18a79-144">Finantsmõju</span><span class="sxs-lookup"><span data-stu-id="18a79-144">Financial impact</span></span>

<span data-ttu-id="18a79-145">Tagasivõtmistaotluse kinnitamisel värskendatakse vastavaid kulude ja müügi tegelikke näitajaid järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="18a79-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="18a79-146">Välja **Korrigeerimise olek** värskendatakse väärtusele **Korrigeeritud**.</span><span class="sxs-lookup"><span data-stu-id="18a79-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="18a79-147">Välja **Arveldusolek** värskendatakse väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="18a79-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="18a79-148">Seejärel luuakse tabelis tegelikud tagasipööramise kirjed.</span><span class="sxs-lookup"><span data-stu-id="18a79-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="18a79-149">Tagasipööratud kirjete loomiseks kopeerib süsteem algsetest tegelikest välja väärtustest üle.</span><span class="sxs-lookup"><span data-stu-id="18a79-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="18a79-150">Ainukesed väärtused, mida ei kopeerita, on koguse väärtused.</span><span class="sxs-lookup"><span data-stu-id="18a79-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="18a79-151">Need väärtused pööratakse hoopis vastupidiseks.</span><span class="sxs-lookup"><span data-stu-id="18a79-151">These values are reversed instead.</span></span> <span data-ttu-id="18a79-152">Tagasipööratud tegelikud luuakse järgmiste tegelike jaoks: **Kulu** ja **Arveldamata müük**.</span><span class="sxs-lookup"><span data-stu-id="18a79-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="18a79-153">Tühistatud tegelike näitajate väli **Korrigeerimise olek** määratakse väärtusele **Korrigeerimatu** ja väli **Arveldusolek** väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="18a79-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="18a79-154">Nende muudatuste tõttu ei võta projekti talletatud kulutused ja tulu mahajäämus enam arvesse summasid, mida need tegelikud näitajad esindavad.</span><span class="sxs-lookup"><span data-stu-id="18a79-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="18a79-155">Kui tagasivõtmisetaotlus lükatakse tagasi, ei ole projektile finantsmõju.</span><span class="sxs-lookup"><span data-stu-id="18a79-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="18a79-156">Ajakirjete kirjete muudatused</span><span class="sxs-lookup"><span data-stu-id="18a79-156">Changes to time entry records</span></span>

<span data-ttu-id="18a79-157">Järgmisel joonisel on kuvatud muudatused, mis toimuvad kinnitatud ajakirjetes nende tagasivõtmisel.</span><span class="sxs-lookup"><span data-stu-id="18a79-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Ajakirje oleku üleminekud](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="18a79-159">Kulukirjete kirjete muudatused</span><span class="sxs-lookup"><span data-stu-id="18a79-159">Changes to expense entry records</span></span>

<span data-ttu-id="18a79-160">Järgmisel joonisel on kuvatud muudatused, mis toimuvad kinnitatud kulukirjetes nende tagasivõtmisel.</span><span class="sxs-lookup"><span data-stu-id="18a79-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Kulukirje oleku üleminekud](media/ExpenseEntryStateTransitions.png)
