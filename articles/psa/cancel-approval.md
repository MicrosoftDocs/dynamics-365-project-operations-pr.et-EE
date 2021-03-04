---
title: Tühista varem kinnitatud aja- ja kuluarvestuse olemid
description: Selles teemas antakse teavet kinnitatud projekti aja- ja kuluarvestuse tehingute tühistamise kohta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150573"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="ce924-103">Tühista varem kinnitatud aja- ja kuluarvestuse tehingud</span><span class="sxs-lookup"><span data-stu-id="ce924-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ce924-104">Rakenduse Dynamics 365 Project Service Automation viimases versioonis saavad kinnitajad tühistada varem kinnitatud aja- või kuluarvestuse tehinguid.</span><span class="sxs-lookup"><span data-stu-id="ce924-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="ce924-105">Varem kinnitatud aja- või kulukirje tühistamine</span><span class="sxs-lookup"><span data-stu-id="ce924-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="ce924-106">Varem kinnitatud aja- või kulukirje tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ce924-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="ce924-107">Minge jaotisse **Projektid** \> **Minu töö** \> **Kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="ce924-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="ce924-108">Muutke loendilehel **Kinnitused** vaateks **Minu varasemad kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="ce924-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="ce924-109">Kuvatakse varem kinnitatud aegade ja kulu kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="ce924-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="ce924-110">Valige üks või mitu kirjet ja seejärel klõpsake käsku **Tühista kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="ce924-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="ce924-111">Te saate hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="ce924-111">You receive a warning message.</span></span>
4. <span data-ttu-id="ce924-112">Kinnitamise tühistamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce924-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="ce924-113">Mõistke aja- või kulukirje kinnitamisest loobumise mõju</span><span class="sxs-lookup"><span data-stu-id="ce924-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="ce924-114">Kui kinnitus tühistatakse, on sel mõju nii tegevusele kui ka finantsile.</span><span class="sxs-lookup"><span data-stu-id="ce924-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="ce924-115">Mõju tegevusele</span><span class="sxs-lookup"><span data-stu-id="ce924-115">Operational impact</span></span>

<span data-ttu-id="ce924-116">Tegevuste poolel, kui kinnitamine tühistatakse, lähtestatakse kirje olekuks **Mustand**, ja kinnitust ei kuvata enam vaates **Minu varasemad kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="ce924-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="ce924-117">Selle asemel kuvatakse tühistatud kinnitus kas vaates **Ajakirjed kinnitamiseks** või vaates **Kulukirjed kinnitamiseks**, olenevalt sellest, kas see oli aja- või kulukirje.</span><span class="sxs-lookup"><span data-stu-id="ce924-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="ce924-118">Peale selle muudetakse seotud aja- või kulukirje olekuks **Esitatud**, et seotud kirje oleks vastavuses kinnitatutega, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="ce924-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="ce924-119">Kinnitajana saate redigeerida mõnda kinnitusvälja, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="ce924-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="ce924-120">Nende väljade hulka kuuluvad **Arveldamise tüüp** ja **Arveldatavate tundide ajakirjed**.</span><span class="sxs-lookup"><span data-stu-id="ce924-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="ce924-121">Pärast muudatuste tegemist saate kirje uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="ce924-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="ce924-122">Soovi korral võite kirje tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="ce924-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="ce924-123">Kui lükkate ajakirje kinnitamise tagasi, muudetakse kirje olekuks **Tagastatud**.</span><span class="sxs-lookup"><span data-stu-id="ce924-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="ce924-124">Kui lükkate ajakirje kinnitamise tagasi, muudetakse olekuks **Tagasi lükatud**.</span><span class="sxs-lookup"><span data-stu-id="ce924-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="ce924-125">Funktsionaalselt, nii tagasi lükatud kui ka hüljatud kirjed käituvad samamoodi kui kirje, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="ce924-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="ce924-126">Projekti meeskonnaliige saab kirjes vajalikud muudatused teha ja seejärel uuesti kinnitamiseks esitada või kirje täielikult kustutada.</span><span class="sxs-lookup"><span data-stu-id="ce924-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="ce924-127">Rahaline mõju</span><span class="sxs-lookup"><span data-stu-id="ce924-127">Financial impact</span></span>

<span data-ttu-id="ce924-128">Projekti mõjutatakse ka rahaliselt, kui kinnitus tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="ce924-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="ce924-129">Esmalt värskendatakse vastavad tegelikud kulud ja müügid järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ce924-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="ce924-130">Kohandamise olekuks seatakse **Korrigeeritud**.</span><span class="sxs-lookup"><span data-stu-id="ce924-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="ce924-131">Arveldamise olekuks seatakse **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="ce924-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="ce924-132">Seejärel luuakse tabelis tegelikud tagasipööramise kirjed.</span><span class="sxs-lookup"><span data-stu-id="ce924-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="ce924-133">Tagasipööratud kirjete loomiseks kopeerib süsteem algsetest tegelikest välja väärtustest üle.</span><span class="sxs-lookup"><span data-stu-id="ce924-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="ce924-134">Ainukesed väärtused, mida ei kopeerita, on koguse väärtused.</span><span class="sxs-lookup"><span data-stu-id="ce924-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="ce924-135">Need väärtused pööratakse hoopis vastupidiseks.</span><span class="sxs-lookup"><span data-stu-id="ce924-135">These values are reversed instead.</span></span> <span data-ttu-id="ce924-136">Tagasipööratud tegelikud luuakse järgmiste tegelike jaoks: **Kulu** ja **Arveldamata müük**.</span><span class="sxs-lookup"><span data-stu-id="ce924-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="ce924-137">Tagasipööratud tegelike välja **Korrigeerimise olek** väärtuseks seatakse **Pole korrigeeritav** ja arve olekuks seatakse **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="ce924-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="ce924-138">Pärast nende muudatuste tegemist arvestatakse projektile kulutatud summa ja projekti tulu mahajäämust, mis on seotud nende tegelike näitajate summadega.</span><span class="sxs-lookup"><span data-stu-id="ce924-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
