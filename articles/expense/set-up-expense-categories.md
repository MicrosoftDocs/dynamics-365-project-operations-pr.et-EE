---
title: Kulukategooriate seadistamine
description: Selles teemas kirjeldatakse kuluarvestuse kulukategooriate ja kuluaruannete ühiskasutuses olevate kategooriate seadistamist.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896681"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="c7b36-103">Kulukategooriate seadistamine</span><span class="sxs-lookup"><span data-stu-id="c7b36-103">Set up expense categories</span></span>

<span data-ttu-id="c7b36-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="c7b36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c7b36-105">Kui töötajad loovad kuluaruandeid, peavad kõik kirjendatud kulud olema seostatud kulukategooriaga.</span><span class="sxs-lookup"><span data-stu-id="c7b36-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="c7b36-106">Kulukategooriate tuletatakse ühiskasutatavatest kategooriatest, mida saab teie organisatsiooni juriidiliste isikutega ühiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="c7b36-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="c7b36-107">Olenevalt sellest, kuidas teie organisatsioon on määratletud, saab neid kulukategooriaid ühiskasutusse anda ka muudes valdkondades.</span><span class="sxs-lookup"><span data-stu-id="c7b36-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="c7b36-108">Vastavalt teie organisatsiooni määratlusele ja juurutuse meeskonna juhistele peate määratlema, kas kuluhalduses kasutatavaid kategooriaid kasutatakse ainult kulude halduses või tuleks neid anda ühiskasutusse muudes valdkondades.</span><span class="sxs-lookup"><span data-stu-id="c7b36-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="c7b36-109">Neid kategooriaid saab kasutada ühiselt projektijuhtimises ja raamatupidamises ning kuluhalduses või projektijuhtimise ning raamatupidamise ja tootmise vahel.</span><span class="sxs-lookup"><span data-stu-id="c7b36-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="c7b36-110">Kuid neid ei saa kasutada ühiselt kuluhalduses ja tootmises.</span><span class="sxs-lookup"><span data-stu-id="c7b36-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="c7b36-111">Enne seadistusprotsessi alustamist tuleb iga kulukategooria kohta teha järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="c7b36-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="c7b36-112">Mis on kulukategooria?</span><span class="sxs-lookup"><span data-stu-id="c7b36-112">What is the expense category?</span></span> <span data-ttu-id="c7b36-113">Näidete hulka kuuluvad lendude, hotelli või kilometraaži kategooria.</span><span class="sxs-lookup"><span data-stu-id="c7b36-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="c7b36-114">Kas kulukategooriat võib kasutada ka projektijuhtimises ja raamatupidamises?</span><span class="sxs-lookup"><span data-stu-id="c7b36-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="c7b36-115">Kui saab, peate langetama ka järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="c7b36-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="c7b36-116">Milliseid kulukontosid kasutatakse järgmistel kulude korral?</span><span class="sxs-lookup"><span data-stu-id="c7b36-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="c7b36-117">Kulu</span><span class="sxs-lookup"><span data-stu-id="c7b36-117">Cost</span></span>
        - <span data-ttu-id="c7b36-118">Palgaarvestuse jaotus</span><span class="sxs-lookup"><span data-stu-id="c7b36-118">Payroll allocation</span></span>
        - <span data-ttu-id="c7b36-119">WIP-kulu väärtus</span><span class="sxs-lookup"><span data-stu-id="c7b36-119">WIP-cost value</span></span>
        - <span data-ttu-id="c7b36-120">Kulu-üksus</span><span class="sxs-lookup"><span data-stu-id="c7b36-120">Cost-item</span></span>
        - <span data-ttu-id="c7b36-121">WIP-kulu väärtuse-üksus</span><span class="sxs-lookup"><span data-stu-id="c7b36-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="c7b36-122">Tekkepõhine kahjum</span><span class="sxs-lookup"><span data-stu-id="c7b36-122">Accrued loss</span></span>
        - <span data-ttu-id="c7b36-123">WIP-tekkepõhine kahjum</span><span class="sxs-lookup"><span data-stu-id="c7b36-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="c7b36-124">Milliseid tulukontosid kasutatakse järgmiste tuluallikate korral?</span><span class="sxs-lookup"><span data-stu-id="c7b36-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="c7b36-125">Arveldatud tulu</span><span class="sxs-lookup"><span data-stu-id="c7b36-125">Invoiced revenue</span></span>
        - <span data-ttu-id="c7b36-126">Viittulu-müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="c7b36-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="c7b36-127">WIP-müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="c7b36-127">WIP-sales value</span></span>
        - <span data-ttu-id="c7b36-128">Viittulu-tootmine</span><span class="sxs-lookup"><span data-stu-id="c7b36-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="c7b36-129">WIP-tootmine</span><span class="sxs-lookup"><span data-stu-id="c7b36-129">WIP-production</span></span>
        - <span data-ttu-id="c7b36-130">Viittulu-kasum</span><span class="sxs-lookup"><span data-stu-id="c7b36-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="c7b36-131">WIP-kasum</span><span class="sxs-lookup"><span data-stu-id="c7b36-131">WIP-profit</span></span>
        - <span data-ttu-id="c7b36-132">Viittulu-kordustellimus</span><span class="sxs-lookup"><span data-stu-id="c7b36-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="c7b36-133">WIP-kordustellimus</span><span class="sxs-lookup"><span data-stu-id="c7b36-133">WIP-subscription</span></span>

- <span data-ttu-id="c7b36-134">Mis on kulutüüp?</span><span class="sxs-lookup"><span data-stu-id="c7b36-134">What is the expense type?</span></span>
- <span data-ttu-id="c7b36-135">Milline on kulukategooria jaoks vaikimisi kasutatav makseviis?</span><span class="sxs-lookup"><span data-stu-id="c7b36-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="c7b36-136">Kas kulukategooria kulud tuleb täpsustada?</span><span class="sxs-lookup"><span data-stu-id="c7b36-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="c7b36-137">Milline on kulukategooria jaoks peamine vaikekonto?</span><span class="sxs-lookup"><span data-stu-id="c7b36-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="c7b36-138">Milline on kulukategooria üksuse vaikimisi käibemaksurühm?</span><span class="sxs-lookup"><span data-stu-id="c7b36-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="c7b36-139">Kas kulukategooria jaoks on lubatud täiendavad makseviisid?</span><span class="sxs-lookup"><span data-stu-id="c7b36-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="c7b36-140">Kui jah, siis millised need on?</span><span class="sxs-lookup"><span data-stu-id="c7b36-140">If so, what are they?</span></span>
- <span data-ttu-id="c7b36-141">Kas selles kulukategoorias pm alamkategooriaid?</span><span class="sxs-lookup"><span data-stu-id="c7b36-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="c7b36-142">Kui on alamkategooriaid, peate langetama ka järgmised otsused.</span><span class="sxs-lookup"><span data-stu-id="c7b36-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="c7b36-143">Kas mõni alamkategooria on maksutagastusest välja jäetud?</span><span class="sxs-lookup"><span data-stu-id="c7b36-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="c7b36-144">Mis on alamkategooria üksuse käibemaksugrupp?</span><span class="sxs-lookup"><span data-stu-id="c7b36-144">What is the item sales tax group of the subcategories?</span></span>
