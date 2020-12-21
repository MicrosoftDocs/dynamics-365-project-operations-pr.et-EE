---
title: Tulu kajastamise ülevaade
description: Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531404"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="0121a-103">Tulu kajastamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="0121a-103">Revenue recognition overview</span></span>

<span data-ttu-id="0121a-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="0121a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0121a-105">Rakenduses Dynamics 365 Project Operations erinevad tulu kajastamise põhimõtted projekti või projekti osa valitud arveldusmeetodi põhjal.</span><span class="sxs-lookup"><span data-stu-id="0121a-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="0121a-106">Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0121a-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="0121a-107">Aja ja materjali arveldusmeetodi kasutavad arvestatavad kanded</span><span class="sxs-lookup"><span data-stu-id="0121a-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="0121a-108">Kulude ja tulude kajastamine on seotud.</span><span class="sxs-lookup"><span data-stu-id="0121a-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="0121a-109">Tehingu kulu ja arveldamata müük sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="0121a-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="0121a-110">Projekti kulu ja tulu profiil määratlevad, kas arveldamata müügi kanded sisestatakse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="0121a-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="0121a-111">Kui valitud on **Viitlaekumine**, kasutab süsteem sisestamise ajal kontosid **WIP müügiväärtus** ja **Viitlaekumise müügiväärtus**.</span><span class="sxs-lookup"><span data-stu-id="0121a-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="0121a-112">Järgnev on selle meetodi näide.</span><span class="sxs-lookup"><span data-stu-id="0121a-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="0121a-113">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="0121a-113">Transaction type</span></span> | <span data-ttu-id="0121a-114">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-114">Debit/Credit</span></span> | <span data-ttu-id="0121a-115">Summa</span><span class="sxs-lookup"><span data-stu-id="0121a-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0121a-116">WIP müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="0121a-116">WIP Sales value</span></span> | <span data-ttu-id="0121a-117">Deebet</span><span class="sxs-lookup"><span data-stu-id="0121a-117">Debit</span></span> | <span data-ttu-id="0121a-118">100</span><span class="sxs-lookup"><span data-stu-id="0121a-118">100</span></span> |
  | <span data-ttu-id="0121a-119">Viittulu müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="0121a-119">Accrued revenue sales value</span></span> | <span data-ttu-id="0121a-120">Kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-120">Credit</span></span> | <span data-ttu-id="0121a-121">100</span><span class="sxs-lookup"><span data-stu-id="0121a-121">100</span></span> |

- <span data-ttu-id="0121a-122">Tulu kajastatakse arveldamise ajal.</span><span class="sxs-lookup"><span data-stu-id="0121a-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="0121a-123">Süsteem kasutab kirjendamise ajal kontot **Arveldatud tulu**.</span><span class="sxs-lookup"><span data-stu-id="0121a-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="0121a-124">Järgnev on selle meetodi näide.</span><span class="sxs-lookup"><span data-stu-id="0121a-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="0121a-125">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="0121a-125">Transaction type</span></span> | <span data-ttu-id="0121a-126">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-126">Debit/Credit</span></span> | <span data-ttu-id="0121a-127">Summa</span><span class="sxs-lookup"><span data-stu-id="0121a-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0121a-128">Kliendi saldo</span><span class="sxs-lookup"><span data-stu-id="0121a-128">Customer balance</span></span> | <span data-ttu-id="0121a-129">Deebet</span><span class="sxs-lookup"><span data-stu-id="0121a-129">Debit</span></span> | <span data-ttu-id="0121a-130">120</span><span class="sxs-lookup"><span data-stu-id="0121a-130">120</span></span> |
  | <span data-ttu-id="0121a-131">Tasutav käibemaks</span><span class="sxs-lookup"><span data-stu-id="0121a-131">Sales tax payable</span></span> | <span data-ttu-id="0121a-132">Kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-132">Credit</span></span> | <span data-ttu-id="0121a-133">20</span><span class="sxs-lookup"><span data-stu-id="0121a-133">20</span></span> |
  | <span data-ttu-id="0121a-134">Arveldatud tulu</span><span class="sxs-lookup"><span data-stu-id="0121a-134">Invoiced Revenue</span></span> | <span data-ttu-id="0121a-135">Kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-135">Credit</span></span> | <span data-ttu-id="0121a-136">100</span><span class="sxs-lookup"><span data-stu-id="0121a-136">100</span></span> |

- <span data-ttu-id="0121a-137">Kui tulu kajastatakse arveldamata müügi kirjendamise ajal, pöörab süsteem arveldamise ajal viitlaekumise ümber.</span><span class="sxs-lookup"><span data-stu-id="0121a-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="0121a-138">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="0121a-138">Transaction type</span></span> | <span data-ttu-id="0121a-139">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-139">Debit/Credit</span></span> | <span data-ttu-id="0121a-140">Summa</span><span class="sxs-lookup"><span data-stu-id="0121a-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0121a-141">WIP müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="0121a-141">WIP Sales value</span></span> | <span data-ttu-id="0121a-142">Kreedit</span><span class="sxs-lookup"><span data-stu-id="0121a-142">Credit</span></span> | <span data-ttu-id="0121a-143">100</span><span class="sxs-lookup"><span data-stu-id="0121a-143">100</span></span> |
  | <span data-ttu-id="0121a-144">Viittulu müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="0121a-144">Accrued revenue sales value</span></span> | <span data-ttu-id="0121a-145">Deebet</span><span class="sxs-lookup"><span data-stu-id="0121a-145">Debit</span></span> | <span data-ttu-id="0121a-146">100</span><span class="sxs-lookup"><span data-stu-id="0121a-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="0121a-147">Fikseeritud hinnaga arveldusmeetodi kasutavad arvestatavad kanded</span><span class="sxs-lookup"><span data-stu-id="0121a-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="0121a-148">Kulude ja tulude kajastamine on eraldi.</span><span class="sxs-lookup"><span data-stu-id="0121a-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="0121a-149">Tehingu kulu sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="0121a-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="0121a-150">Arveldamata müügitehinguid ei looda.</span><span class="sxs-lookup"><span data-stu-id="0121a-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="0121a-151">Tulu saab kajastada arveldamise ajal, kui projektikulu ja tuluprofiilis on suvand **Projekti lõpule viimise arvutamiseks kasutatud põhimõte** on määratud valikule **Pole WIP**.</span><span class="sxs-lookup"><span data-stu-id="0121a-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="0121a-152">Kasutage seda meetodit ainult lühiajaliste lihtsate projektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="0121a-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="0121a-153">Tulu saab kajastada kasutades fikseeritud hinnaga tulukalkulatsioone kas meetodiga **Lõpetatud leping** või **Tulu kajastamise lõpetamise protsent**.</span><span class="sxs-lookup"><span data-stu-id="0121a-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0121a-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0121a-154">Additional resources</span></span>
[<span data-ttu-id="0121a-155">Arveldatavate projektide raamatupidamise konfigureerimise artikkel</span><span class="sxs-lookup"><span data-stu-id="0121a-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="0121a-156">Fikseeritud hinnaga tulukalkulatsiooni projektid</span><span class="sxs-lookup"><span data-stu-id="0121a-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="0121a-157">Tulukalkulatsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="0121a-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="0121a-158">Kulu meetodi lõpetamiseks</span><span class="sxs-lookup"><span data-stu-id="0121a-158">Cost to complete methods</span></span>](cost-complete-methods.md)
