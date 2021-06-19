---
title: Project Operationsi väljad hinnakujunduse dimensioonidena
description: See teema sisaldab teavet väljade kasutamise kohta hinnakujunduse dimensioonidena rakenduses Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004481"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="aa50c-103">Project Operationsi väljad hinnakujunduse dimensioonidena</span><span class="sxs-lookup"><span data-stu-id="aa50c-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="aa50c-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="aa50c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aa50c-105">**Tegelikel** olemitel on palju välju, mida saab kasutada ressursil põhineva hinnakujunduse dimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="aa50c-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="aa50c-106">Näiteks üks üldväli on **Broneeritav ressurss**.</span><span class="sxs-lookup"><span data-stu-id="aa50c-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="aa50c-107">Väiksemad ettevõtted, millel on vähem kui 20–30 arveldatavat ressurssi, võivad leida, et lihtsam on lihtsalt igale ressursile määrata konkreetsed arveldus- ja kulumäärad.</span><span class="sxs-lookup"><span data-stu-id="aa50c-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="aa50c-108">Kuid kuna tasustatav tööjõud kasvab, võib ressursipõhised määrad muutuda ebarealistlikuks, et neid säilitada.</span><span class="sxs-lookup"><span data-stu-id="aa50c-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="aa50c-109">Ressursi kulu ja arve määrad hakkavad erinema, kui ressursse edutatakse, nad saavad rohkem kogemusi või õpivad juurde uusi oskusi.</span><span class="sxs-lookup"><span data-stu-id="aa50c-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="aa50c-110">Teine näide on kandekategooria.</span><span class="sxs-lookup"><span data-stu-id="aa50c-110">Another example is that of transaction category.</span></span> <span data-ttu-id="aa50c-111">Kliendid ja juurutajad on kasutanud kandekategooriat töö klassifitseerimiseks ning välja hinnakujunduse ja kulude jaoks vastavalt töökategooria järgi.</span><span class="sxs-lookup"><span data-stu-id="aa50c-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]