---
title: Miks on tegeliku kulu maksumuse vaikeväärtus null?
description: Tõrkeotsing, miks on tegeliku kulu maksumuse vaikeväärtus 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122113"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="c2597-103">Miks on tegeliku kulu maksumuse vaikeväärtus null?</span><span class="sxs-lookup"><span data-stu-id="c2597-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c2597-104">See KKK kehtib sellise tegeliku kulu maksumuse puhul, mille kande liigiks on määratud Kulu ja kande tüübiks Kulu.</span><span class="sxs-lookup"><span data-stu-id="c2597-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="c2597-105">Tegeliku kulu maksumuse kulumäärade tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="c2597-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="c2597-106">Minge seotud kulukirjesse ja veenduge, et kulukirje väljal pole ühtki summat.</span><span class="sxs-lookup"><span data-stu-id="c2597-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="c2597-107">Kui algsel kulukirjel polnud summaväli täidetud, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="c2597-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="c2597-108">Probleemi lahendamiseks looge kulukirje uuesti koos kehtiva summaga ja kinnitage see.</span><span class="sxs-lookup"><span data-stu-id="c2597-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
