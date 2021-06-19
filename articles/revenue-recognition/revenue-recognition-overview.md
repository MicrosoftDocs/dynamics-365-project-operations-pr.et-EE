---
title: Tulu kajastamise ülevaade
description: Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013751"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="4899b-103">Tulu kajastamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="4899b-103">Revenue recognition overview</span></span>

<span data-ttu-id="4899b-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="4899b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4899b-105">Rakenduses Dynamics 365 Project Operations erinevad tulu kajastamise põhimõtted projekti või projekti osa valitud arveldusmeetodi põhjal.</span><span class="sxs-lookup"><span data-stu-id="4899b-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="4899b-106">Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4899b-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="4899b-107">Aja ja materjali arveldusmeetodi kasutavad arvestatavad kanded</span><span class="sxs-lookup"><span data-stu-id="4899b-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="4899b-108">Kulude ja tulude kajastamine on seotud.</span><span class="sxs-lookup"><span data-stu-id="4899b-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="4899b-109">Tehingu kulu ja arveldamata müük sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="4899b-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="4899b-110">Projekti kulu ja tulu profiil määratlevad, kas arveldamata müügi kanded sisestatakse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="4899b-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="4899b-111">Kui valitud on **Viitlaekumine**, kasutab süsteem sisestamise ajal kontosid **WIP müügiväärtus** ja **Viitlaekumise müügiväärtus**.</span><span class="sxs-lookup"><span data-stu-id="4899b-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="4899b-112">Järgnev on selle meetodi näide.</span><span class="sxs-lookup"><span data-stu-id="4899b-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="4899b-113">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="4899b-113">Transaction type</span></span> | <span data-ttu-id="4899b-114">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-114">Debit/Credit</span></span> | <span data-ttu-id="4899b-115">Summa</span><span class="sxs-lookup"><span data-stu-id="4899b-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="4899b-116">WIP müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="4899b-116">WIP Sales value</span></span> | <span data-ttu-id="4899b-117">Deebet</span><span class="sxs-lookup"><span data-stu-id="4899b-117">Debit</span></span> | <span data-ttu-id="4899b-118">100</span><span class="sxs-lookup"><span data-stu-id="4899b-118">100</span></span> |
  | <span data-ttu-id="4899b-119">Viittulu müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="4899b-119">Accrued revenue sales value</span></span> | <span data-ttu-id="4899b-120">Kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-120">Credit</span></span> | <span data-ttu-id="4899b-121">100</span><span class="sxs-lookup"><span data-stu-id="4899b-121">100</span></span> |

- <span data-ttu-id="4899b-122">Tulu kajastatakse arveldamise ajal.</span><span class="sxs-lookup"><span data-stu-id="4899b-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="4899b-123">Süsteem kasutab kirjendamise ajal kontot **Arveldatud tulu**.</span><span class="sxs-lookup"><span data-stu-id="4899b-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="4899b-124">Järgnev on selle meetodi näide.</span><span class="sxs-lookup"><span data-stu-id="4899b-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="4899b-125">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="4899b-125">Transaction type</span></span> | <span data-ttu-id="4899b-126">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-126">Debit/Credit</span></span> | <span data-ttu-id="4899b-127">Summa</span><span class="sxs-lookup"><span data-stu-id="4899b-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="4899b-128">Kliendi saldo</span><span class="sxs-lookup"><span data-stu-id="4899b-128">Customer balance</span></span> | <span data-ttu-id="4899b-129">Deebet</span><span class="sxs-lookup"><span data-stu-id="4899b-129">Debit</span></span> | <span data-ttu-id="4899b-130">120</span><span class="sxs-lookup"><span data-stu-id="4899b-130">120</span></span> |
  | <span data-ttu-id="4899b-131">Tasutav käibemaks</span><span class="sxs-lookup"><span data-stu-id="4899b-131">Sales tax payable</span></span> | <span data-ttu-id="4899b-132">Kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-132">Credit</span></span> | <span data-ttu-id="4899b-133">20</span><span class="sxs-lookup"><span data-stu-id="4899b-133">20</span></span> |
  | <span data-ttu-id="4899b-134">Arveldatud tulu</span><span class="sxs-lookup"><span data-stu-id="4899b-134">Invoiced Revenue</span></span> | <span data-ttu-id="4899b-135">Kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-135">Credit</span></span> | <span data-ttu-id="4899b-136">100</span><span class="sxs-lookup"><span data-stu-id="4899b-136">100</span></span> |

- <span data-ttu-id="4899b-137">Kui tulu kajastatakse arveldamata müügi kirjendamise ajal, pöörab süsteem arveldamise ajal viitlaekumise ümber.</span><span class="sxs-lookup"><span data-stu-id="4899b-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="4899b-138">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="4899b-138">Transaction type</span></span> | <span data-ttu-id="4899b-139">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-139">Debit/Credit</span></span> | <span data-ttu-id="4899b-140">Summa</span><span class="sxs-lookup"><span data-stu-id="4899b-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="4899b-141">WIP müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="4899b-141">WIP Sales value</span></span> | <span data-ttu-id="4899b-142">Kreedit</span><span class="sxs-lookup"><span data-stu-id="4899b-142">Credit</span></span> | <span data-ttu-id="4899b-143">100</span><span class="sxs-lookup"><span data-stu-id="4899b-143">100</span></span> |
  | <span data-ttu-id="4899b-144">Viittulu müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="4899b-144">Accrued revenue sales value</span></span> | <span data-ttu-id="4899b-145">Deebet</span><span class="sxs-lookup"><span data-stu-id="4899b-145">Debit</span></span> | <span data-ttu-id="4899b-146">100</span><span class="sxs-lookup"><span data-stu-id="4899b-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="4899b-147">Fikseeritud hinnaga arveldusmeetodi kasutavad arvestatavad kanded</span><span class="sxs-lookup"><span data-stu-id="4899b-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="4899b-148">Kulude ja tulude kajastamine on eraldi.</span><span class="sxs-lookup"><span data-stu-id="4899b-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="4899b-149">Tehingu kulu sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="4899b-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="4899b-150">Arveldamata müügitehinguid ei looda.</span><span class="sxs-lookup"><span data-stu-id="4899b-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="4899b-151">Tulu saab kajastada arveldamise ajal, kui projektikulu ja tuluprofiilis on suvand **Projekti lõpule viimise arvutamiseks kasutatud põhimõte** on määratud valikule **Pole WIP**.</span><span class="sxs-lookup"><span data-stu-id="4899b-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="4899b-152">Kasutage seda meetodit ainult lühiajaliste lihtsate projektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="4899b-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="4899b-153">Tulu saab kajastada kasutades fikseeritud hinnaga tulukalkulatsioone kas meetodiga **Lõpetatud leping** või **Tulu kajastamise lõpetamise protsent**.</span><span class="sxs-lookup"><span data-stu-id="4899b-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4899b-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4899b-154">Additional resources</span></span>
[<span data-ttu-id="4899b-155">Arveldatavate projektide raamatupidamise konfigureerimise artikkel</span><span class="sxs-lookup"><span data-stu-id="4899b-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="4899b-156">Fikseeritud hinnaga tulukalkulatsiooni projektid</span><span class="sxs-lookup"><span data-stu-id="4899b-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="4899b-157">Tulukalkulatsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="4899b-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="4899b-158">Kulu meetodi lõpetamiseks</span><span class="sxs-lookup"><span data-stu-id="4899b-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]