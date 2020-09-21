---
title: Miks on tegeliku kulu maksumuse vaikeväärtus null?
description: Tõrkeotsing, miks on tegeliku kulu maksumuse vaikeväärtus 0.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750957"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="3bd90-103">Miks on tegeliku kulu maksumuse vaikeväärtus null?</span><span class="sxs-lookup"><span data-stu-id="3bd90-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3bd90-104">See KKK kehtib sellise tegeliku kulu maksumuse puhul, mille kande liigiks on määratud Kulu ja kande tüübiks Kulu.</span><span class="sxs-lookup"><span data-stu-id="3bd90-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="3bd90-105">Tegeliku kulu maksumuse kulumäärade tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="3bd90-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="3bd90-106">Minge seotud kulukirjesse ja veenduge, et kulukirje väljal pole ühtki summat.</span><span class="sxs-lookup"><span data-stu-id="3bd90-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="3bd90-107">Kui algsel kulukirjel polnud summaväli täidetud, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="3bd90-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="3bd90-108">Probleemi lahendamiseks looge kulukirje uuesti koos kehtiva summaga ja kinnitage see.</span><span class="sxs-lookup"><span data-stu-id="3bd90-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
