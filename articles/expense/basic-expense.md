---
title: Kulukirje (liht)
description: Selles teemas sisaldub teave selle kohta, kuidas töötada kulukirjega lihtjuurutuses.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074840"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="e998d-103">Kulukirje (liht)</span><span class="sxs-lookup"><span data-stu-id="e998d-103">Expense entry (lite)</span></span>

<span data-ttu-id="e998d-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="e998d-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e998d-105">Põhiline või lihtne kuluhaldus on võimalus kirjendada lihtkulusid.</span><span class="sxs-lookup"><span data-stu-id="e998d-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="e998d-106">Saate kirjendada kulusid projekti suhtes ja seejärel vaatab projekti kinnitaja need läbi ja kinnitab need.</span><span class="sxs-lookup"><span data-stu-id="e998d-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="e998d-107">Lisateavet rakenduse Dynamics 365 Project Operations kulu võimaluste kohta vaadake teemast [Kulu ülevaade](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e998d-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="e998d-108">Põhikulu jäädvustamine</span><span class="sxs-lookup"><span data-stu-id="e998d-108">Capture a basic expense</span></span>

<span data-ttu-id="e998d-109">Saate oma kulud jäädvustada, et saaksite need kinnitajale edastada.</span><span class="sxs-lookup"><span data-stu-id="e998d-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="e998d-110">Avage suvand **Kulud** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e998d-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="e998d-111">Sisestage lehel **Uus kulu** nõutav kuluga seotud teave ja valige seejärel suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e998d-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="e998d-112">Põhikulu esitamine</span><span class="sxs-lookup"><span data-stu-id="e998d-112">Submit a basic expense</span></span>

<span data-ttu-id="e998d-113">Kui olete lõpetanud kõikide kulude jäädvustamise ja olete valmis need lasta kinnitada, siis te peate need esitama.</span><span class="sxs-lookup"><span data-stu-id="e998d-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="e998d-114">Avage suvand **Kulud** ja valige kulu.</span><span class="sxs-lookup"><span data-stu-id="e998d-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="e998d-115">Või valige kõik kulud, kasutades päises olevat märkeruutu.</span><span class="sxs-lookup"><span data-stu-id="e998d-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="e998d-116">Valige käsk **Esita**.</span><span class="sxs-lookup"><span data-stu-id="e998d-116">Select **Submit**.</span></span> <span data-ttu-id="e998d-117">Süsteem töötleb valitud kirjeid ja loob seejärel kulu kinnitamise taotlused.</span><span class="sxs-lookup"><span data-stu-id="e998d-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="e998d-118">Põhikulu tagasi kutsumine</span><span class="sxs-lookup"><span data-stu-id="e998d-118">Recall a basic expense</span></span>

<span data-ttu-id="e998d-119">Kui esitate kulu eklikult, saate selle tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="e998d-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="e998d-120">Kulukirje tagasikutsumiseks vajalik aeg oleneb selle kinnitamise etapist.</span><span class="sxs-lookup"><span data-stu-id="e998d-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="e998d-121">Kui kinnitaja pole kirjet veel kinnitanud, võib tagasikutsumine toimuda kohe.</span><span class="sxs-lookup"><span data-stu-id="e998d-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="e998d-122">Samas kui kirje on juba kinnitatud, palutakse kinnitajal kinnitada tagasikutsumine ja tühistada tehing.</span><span class="sxs-lookup"><span data-stu-id="e998d-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="e998d-123">Avage **Kulud** ja valige seejärel kulude loendist tagasi kutsumiseks kulu.</span><span class="sxs-lookup"><span data-stu-id="e998d-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="e998d-124">Tehke valik **Kutsu tagasi**.</span><span class="sxs-lookup"><span data-stu-id="e998d-124">Select **Recall**.</span></span> <span data-ttu-id="e998d-125">Kui kulukirjet pole veel kinnitatud, siis kutsub süsteem selle kohe tagasi.</span><span class="sxs-lookup"><span data-stu-id="e998d-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="e998d-126">Kui kulukirje on juba kinnitatud, luuakse tagasikutsumise taotlus, et teavitada kinnitajat, et soovite kulu tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="e998d-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="e998d-127">Kinnitaja kinnitab seejärel, et tagasikutsumine on võimalik, ja kirje tagastatakse.</span><span class="sxs-lookup"><span data-stu-id="e998d-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="e998d-128">Põhikulu kustutamine</span><span class="sxs-lookup"><span data-stu-id="e998d-128">Delete a basic expense</span></span>

<span data-ttu-id="e998d-129">Veel esitamata kulusid on võimalik kustutada.</span><span class="sxs-lookup"><span data-stu-id="e998d-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="e998d-130">Juba esitatud kulu kustutamiseks peate selle esmalt tagasi kutsuma.</span><span class="sxs-lookup"><span data-stu-id="e998d-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="e998d-131">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e998d-131">See also</span></span>

- [<span data-ttu-id="e998d-132">Kinnituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="e998d-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
