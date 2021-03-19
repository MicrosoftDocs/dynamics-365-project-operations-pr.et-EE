---
title: Arvelduse mahajäämuse ülevaatamine projektide ja projektilepingute jaoks
description: Selles teemas antakse teavet aja, kulude ja toote mahajäämuste ülevaatamise ning selle kohta, kuidas neid arveldusvalmiks märkida.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282778"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="6e555-103">Arvelduse mahajäämuse ülevaatamine projektide ja projektilepingute jaoks</span><span class="sxs-lookup"><span data-stu-id="6e555-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6e555-104">Kui kanne on arve koostamiseks ja töötlemiseks valmis, tuleb kanne märkida väärtusele **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="6e555-105">Selles teemas kirjeldatakse, millist tüüpi kandeid saab luua.</span><span class="sxs-lookup"><span data-stu-id="6e555-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="6e555-106">Ajakavast mahajäämuse ja materjali arvete võlgnevuste ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="6e555-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="6e555-107">Kui projekti jaoks esitatakse ja kinnitatakse aja- või kulukirje, loob PSA projekti tegeliku näitaja.</span><span class="sxs-lookup"><span data-stu-id="6e555-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="6e555-108">Kui projekti ja kande klassi kombinatsioon vastendatakse aja- ja materjalikulu projekti puhul lepingureaga, luuakse kirje kinnitamisel kaks tegelikku näitajat.</span><span class="sxs-lookup"><span data-stu-id="6e555-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="6e555-109">Tegelik kulu</span><span class="sxs-lookup"><span data-stu-id="6e555-109">Cost actual</span></span> 
- <span data-ttu-id="6e555-110">Arveldamata tegelik müük</span><span class="sxs-lookup"><span data-stu-id="6e555-110">Unbilled sales actual</span></span>

<span data-ttu-id="6e555-111">Arveldamata tegelikud müügid näitavad arvete võlgnevust ja nende arveldamise olek tuleb määrata väärtusele **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="6e555-112">Projekti arve loomisel kopeeritakse arveldamata tegelikud müügid, mis on märgitud kui **Arveldamiseks valmis**, arverea üksikasjadena.</span><span class="sxs-lookup"><span data-stu-id="6e555-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="6e555-113">Aja ja materjalide arvete võlgnevuse ülevaatamiseks tehke valikud **Müügid** \> **Arveldus** \> **Ajakavast mahajäämus ja materjali arvete võlgnevused**.</span><span class="sxs-lookup"><span data-stu-id="6e555-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="6e555-114">Valige kõik arveldamata tegelikud müügid, mis on arveldamiseks valmis ja seejärel valige **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="6e555-115">Nende tegelike näitajate arveldamise olek muudetakse väärtusele **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Ajakavast mahajäämus ja materjali arvete võlgnevused](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="6e555-117">Toodete arvete võlgnevuste ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="6e555-117">Review the product billing backlog</span></span>

<span data-ttu-id="6e555-118">Kui projektileping sisaldab tootepõhiseid lepinguridu, kaalutakse PSA-s neid ridu arveldamiseks iga kord, kui projektilepingule luuakse arve.</span><span class="sxs-lookup"><span data-stu-id="6e555-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="6e555-119">Kõik tooted, millel on lepinguread väärtusega **Arveldamiseks valmis**, kopeeritakse projekti arveridadena projekti arvesse.</span><span class="sxs-lookup"><span data-stu-id="6e555-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="6e555-120">Toodete arvete võlgnevuse ülevaatamiseks tehke valikud **Müügid** \> **Arveldus** \> **Toodete arvete võlgnevused**.</span><span class="sxs-lookup"><span data-stu-id="6e555-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="6e555-121">Valige kõik tootepõhised lepinguread, mis on arveldamiseks valmis ja seejärel tehke valik **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="6e555-122">Nende ridade arveldamise olek muudetakse väärtusele **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Toodete arvete võlgnevused](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="6e555-124">Arveldamise vahe-eesmärkide ülevaatamine fikseeritud hinnaga lepingutes</span><span class="sxs-lookup"><span data-stu-id="6e555-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="6e555-125">Iga projekti lepingurida, millel on fikseeritud hinnaga arveldusmeetod, peab määratlema lepingu vahe-eesmärgid.</span><span class="sxs-lookup"><span data-stu-id="6e555-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="6e555-126">Neid lepingu vahe-eesmärke saab arveldada ainult juhul, kui need on väärtusel **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="6e555-127">Arveldamise vahe-eesmärkide ülevaatamiseks tehke valikud **Müügid** \> **Arveldus** \> **Fikseeritud hinna vahe-eesmärgid**.</span><span class="sxs-lookup"><span data-stu-id="6e555-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="6e555-128">Valige vahe-eesmärgid, mis on arveldamiseks valmis ja seejärel tehke valik **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="6e555-129">Nende vahe-eesmärkide arveldamise olek muudetakse väärtusele **Arveldamiseks valmis**.</span><span class="sxs-lookup"><span data-stu-id="6e555-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Fikseeritud hinna vahe-eesmärgid](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]