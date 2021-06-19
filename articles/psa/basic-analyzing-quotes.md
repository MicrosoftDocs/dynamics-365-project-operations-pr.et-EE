---
title: Projekti hinnapakkumiste analüüs
description: Selles teemas antakse teavet projekti hinnapakkumiste analüüsi kohta.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012446"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="edbc2-103">Projekti hinnapakkumiste analüüs</span><span class="sxs-lookup"><span data-stu-id="edbc2-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="edbc2-104">Rakendus Dynamics 365 Project Service Automation analüüsib projekti hinnapakkumisi, et hinnata kasumlikkust.</span><span class="sxs-lookup"><span data-stu-id="edbc2-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="edbc2-105">Samuti analüüsitakse, kui hästi hinnapakkumine on joondatud kliendi ootustega tarnekuupäeva või lõpuleviimise kuupäeva ja eelarve kohta.</span><span class="sxs-lookup"><span data-stu-id="edbc2-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="edbc2-106">Kasumlikkuse analüüs</span><span class="sxs-lookup"><span data-stu-id="edbc2-106">Profitability analysis</span></span>

<span data-ttu-id="edbc2-107">Rakendus Project Service Automation analüüsib kasumlikkust, kasutades kogutulu ja korrigeeritud kogutulu.</span><span class="sxs-lookup"><span data-stu-id="edbc2-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="edbc2-108">Kogutulu arvutatakse järgmise valemi abil.</span><span class="sxs-lookup"><span data-stu-id="edbc2-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="edbc2-109">Korrigeeritud kogutulu arvutatakse järgmise valemi abil.</span><span class="sxs-lookup"><span data-stu-id="edbc2-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="edbc2-110">Kui kogutulu ja korrigeeritud kogutulu väärtused erinevad suurel määral, loetakse suur osa hinnapakkumise töödest tasumata.</span><span class="sxs-lookup"><span data-stu-id="edbc2-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="edbc2-111">Kliendi ootusteanalüüs</span><span class="sxs-lookup"><span data-stu-id="edbc2-111">Analysis of customer expectations</span></span>

<span data-ttu-id="edbc2-112">Saate analüüsida hinnapakkumisi ja luua graafikuid klientide ootustele ajakava ja eelarve kohta, kui sisestate järgmistele väljadele väärtusi.</span><span class="sxs-lookup"><span data-stu-id="edbc2-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="edbc2-113">Hinnapakkumise päise väli **Nõutav tarnekuupäev**.</span><span class="sxs-lookup"><span data-stu-id="edbc2-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="edbc2-114">Iga hinnapakkumise rea (projektil ja tootel põhinevad read) väli **Kliendi eelarve**.</span><span class="sxs-lookup"><span data-stu-id="edbc2-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="edbc2-115">Ajakavaga seotud klientide ootuste analüüs tehakse võrreldes hinnapakkumise rea lõppkuupäeva üksikasju ja nõutavat tarnekuupäeva kõigis hinnapakkumise ridades.</span><span class="sxs-lookup"><span data-stu-id="edbc2-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="edbc2-116">Eelarvega seotud klientide ootuste analüüs tehakse võrreldes kõigi hinnapakkumiste ridasid pakutava summaga kõigis hinnapakkumise ridades.</span><span class="sxs-lookup"><span data-stu-id="edbc2-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]