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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278863"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="d353e-103">Tulu kajastamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="d353e-103">Revenue recognition overview</span></span>

<span data-ttu-id="d353e-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="d353e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d353e-105">Rakenduses Dynamics 365 Project Operations erinevad tulu kajastamise põhimõtted projekti või projekti osa valitud arveldusmeetodi põhjal.</span><span class="sxs-lookup"><span data-stu-id="d353e-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="d353e-106">Selles teemas antakse teavet tulu kajastamise kohta rakenduses Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d353e-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="d353e-107">Aja ja materjali arveldusmeetodi kasutavad arvestatavad kanded</span><span class="sxs-lookup"><span data-stu-id="d353e-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="d353e-108">Kulude ja tulude kajastamine on seotud.</span><span class="sxs-lookup"><span data-stu-id="d353e-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="d353e-109">Tehingu kulu ja arveldamata müük sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="d353e-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="d353e-110">Projekti kulu ja tulu profiil määratlevad, kas arveldamata müügi kanded sisestatakse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="d353e-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="d353e-111">Kui valitud on **Viitlaekumine**, kasutab süsteem sisestamise ajal kontosid **WIP müügiväärtus** ja **Viitlaekumise müügiväärtus**.</span><span class="sxs-lookup"><span data-stu-id="d353e-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="d353e-112">Järgnev on selle meetodi näide.</span><span class="sxs-lookup"><span data-stu-id="d353e-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="d353e-113">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="d353e-113">Transaction type</span></span> | <span data-ttu-id="d353e-114">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-114">Debit/Credit</span></span> | <span data-ttu-id="d353e-115">Summa</span><span class="sxs-lookup"><span data-stu-id="d353e-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d353e-116">WIP müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="d353e-116">WIP Sales value</span></span> | <span data-ttu-id="d353e-117">Deebet</span><span class="sxs-lookup"><span data-stu-id="d353e-117">Debit</span></span> | <span data-ttu-id="d353e-118">100</span><span class="sxs-lookup"><span data-stu-id="d353e-118">100</span></span> |
  | <span data-ttu-id="d353e-119">Viittulu müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="d353e-119">Accrued revenue sales value</span></span> | <span data-ttu-id="d353e-120">Kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-120">Credit</span></span> | <span data-ttu-id="d353e-121">100</span><span class="sxs-lookup"><span data-stu-id="d353e-121">100</span></span> |

- <span data-ttu-id="d353e-122">Tulu kajastatakse arveldamise ajal.</span><span class="sxs-lookup"><span data-stu-id="d353e-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="d353e-123">Süsteem kasutab kirjendamise ajal kontot **Arveldatud tulu**.</span><span class="sxs-lookup"><span data-stu-id="d353e-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="d353e-124">Järgnev on selle meetodi näide.</span><span class="sxs-lookup"><span data-stu-id="d353e-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="d353e-125">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="d353e-125">Transaction type</span></span> | <span data-ttu-id="d353e-126">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-126">Debit/Credit</span></span> | <span data-ttu-id="d353e-127">Summa</span><span class="sxs-lookup"><span data-stu-id="d353e-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d353e-128">Kliendi saldo</span><span class="sxs-lookup"><span data-stu-id="d353e-128">Customer balance</span></span> | <span data-ttu-id="d353e-129">Deebet</span><span class="sxs-lookup"><span data-stu-id="d353e-129">Debit</span></span> | <span data-ttu-id="d353e-130">120</span><span class="sxs-lookup"><span data-stu-id="d353e-130">120</span></span> |
  | <span data-ttu-id="d353e-131">Tasutav käibemaks</span><span class="sxs-lookup"><span data-stu-id="d353e-131">Sales tax payable</span></span> | <span data-ttu-id="d353e-132">Kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-132">Credit</span></span> | <span data-ttu-id="d353e-133">20</span><span class="sxs-lookup"><span data-stu-id="d353e-133">20</span></span> |
  | <span data-ttu-id="d353e-134">Arveldatud tulu</span><span class="sxs-lookup"><span data-stu-id="d353e-134">Invoiced Revenue</span></span> | <span data-ttu-id="d353e-135">Kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-135">Credit</span></span> | <span data-ttu-id="d353e-136">100</span><span class="sxs-lookup"><span data-stu-id="d353e-136">100</span></span> |

- <span data-ttu-id="d353e-137">Kui tulu kajastatakse arveldamata müügi kirjendamise ajal, pöörab süsteem arveldamise ajal viitlaekumise ümber.</span><span class="sxs-lookup"><span data-stu-id="d353e-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="d353e-138">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="d353e-138">Transaction type</span></span> | <span data-ttu-id="d353e-139">Deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-139">Debit/Credit</span></span> | <span data-ttu-id="d353e-140">Summa</span><span class="sxs-lookup"><span data-stu-id="d353e-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="d353e-141">WIP müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="d353e-141">WIP Sales value</span></span> | <span data-ttu-id="d353e-142">Kreedit</span><span class="sxs-lookup"><span data-stu-id="d353e-142">Credit</span></span> | <span data-ttu-id="d353e-143">100</span><span class="sxs-lookup"><span data-stu-id="d353e-143">100</span></span> |
  | <span data-ttu-id="d353e-144">Viittulu müügiväärtus</span><span class="sxs-lookup"><span data-stu-id="d353e-144">Accrued revenue sales value</span></span> | <span data-ttu-id="d353e-145">Deebet</span><span class="sxs-lookup"><span data-stu-id="d353e-145">Debit</span></span> | <span data-ttu-id="d353e-146">100</span><span class="sxs-lookup"><span data-stu-id="d353e-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="d353e-147">Fikseeritud hinnaga arveldusmeetodi kasutavad arvestatavad kanded</span><span class="sxs-lookup"><span data-stu-id="d353e-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="d353e-148">Kulude ja tulude kajastamine on eraldi.</span><span class="sxs-lookup"><span data-stu-id="d353e-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="d353e-149">Tehingu kulu sisestatakse kasutades [Project Operationsi integreerimise töölehte](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="d353e-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="d353e-150">Arveldamata müügitehinguid ei looda.</span><span class="sxs-lookup"><span data-stu-id="d353e-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="d353e-151">Tulu saab kajastada arveldamise ajal, kui projektikulu ja tuluprofiilis on suvand **Projekti lõpule viimise arvutamiseks kasutatud põhimõte** on määratud valikule **Pole WIP**.</span><span class="sxs-lookup"><span data-stu-id="d353e-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="d353e-152">Kasutage seda meetodit ainult lühiajaliste lihtsate projektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="d353e-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="d353e-153">Tulu saab kajastada kasutades fikseeritud hinnaga tulukalkulatsioone kas meetodiga **Lõpetatud leping** või **Tulu kajastamise lõpetamise protsent**.</span><span class="sxs-lookup"><span data-stu-id="d353e-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d353e-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d353e-154">Additional resources</span></span>
[<span data-ttu-id="d353e-155">Arveldatavate projektide raamatupidamise konfigureerimise artikkel</span><span class="sxs-lookup"><span data-stu-id="d353e-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="d353e-156">Fikseeritud hinnaga tulukalkulatsiooni projektid</span><span class="sxs-lookup"><span data-stu-id="d353e-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="d353e-157">Tulukalkulatsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="d353e-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="d353e-158">Kulu meetodi lõpetamiseks</span><span class="sxs-lookup"><span data-stu-id="d353e-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]