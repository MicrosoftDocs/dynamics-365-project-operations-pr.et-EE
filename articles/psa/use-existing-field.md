---
title: Project Service’is olemasoleva välja kasutamine hinnakujunduse dimensioonina
description: Selles teemas kirjeldatakse, kuidas kasutada Project Service’i olemasolevaid välju hinnakujunduse dimensioonidena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bc3a1df7669dac43b45d781448ed5c795a65be4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144147"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="80629-103">Project Service’is olemasoleva välja kasutamine hinnakujunduse dimensioonina</span><span class="sxs-lookup"><span data-stu-id="80629-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="80629-104">Project Service Automation (PSA) on olemis **Tegelikud näitajad** palju välju, mida saab projekti organisatsioonides ressursil põhineva hinnakujunduse jaoks kasutada hinnakujunduse dimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="80629-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="80629-105">Näiteks üks üldväli on **Broneeritav ressurss**.</span><span class="sxs-lookup"><span data-stu-id="80629-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="80629-106">Väiksemad ettevõtted, millel on vähem kui 20–30 arveldatavat ressurssi, võivad leida, et lihtsam on lihtsalt igale ressursile määrata konkreetsed arveldus- ja kulumäärad.</span><span class="sxs-lookup"><span data-stu-id="80629-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="80629-107">Kuna aga arveldatav töötajaskond kasvab, võib erimäärade säilitamine muutuda ebarealistlikuks, sest ressursi kulu- ja arveldusmäärad hakkavad erinema, kui ressursse edutatakse, nad saavad rohkem kogemust või omandavad erinevaid oskusi.</span><span class="sxs-lookup"><span data-stu-id="80629-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="80629-108">Kuna aga see lähenemine töötab endiselt teatava suurusega ettevõtete puhul, vaadake jaotist [Broneeritava ressursi kasutamine hinnakujunduse dimensioonina](bookable-resource-pricing-dimension.md) ja lugege, kuidas Project Service’i olemasolevat välja saab kasutada hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="80629-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="80629-109">Teine näide on kandekategooria.</span><span class="sxs-lookup"><span data-stu-id="80629-109">Another example is that of transaction category.</span></span> <span data-ttu-id="80629-110">Kliendid ja juurutajad on kasutanud PSA kandekategooriat töö klassifitseerimiseks ning välja hinnakujunduse ja kulude jaoks vastavalt töökategooria järgi.</span><span class="sxs-lookup"><span data-stu-id="80629-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="80629-111">Lisateavet leiate jaotisest [Kandekategooria kasutamine hinnakujunduse dimensioonina](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="80629-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
