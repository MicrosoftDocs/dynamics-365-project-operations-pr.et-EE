---
title: Project Operationsi väljad hinnakujunduse dimensioonidena
description: Selles teemas antakse teavet Dynamics 365 Project Operationsi hinnakujunduse dimensioonidena väljade kasutamise kohta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896411"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="445d6-103">Project Operationsi väljad hinnakujunduse dimensioonidena</span><span class="sxs-lookup"><span data-stu-id="445d6-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="445d6-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="445d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="445d6-105">**Tegelikel** olemitel on palju välju, mida saab kasutada ressursil põhineva hinnakujunduse dimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="445d6-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="445d6-106">Näiteks üks üldväli on **Broneeritav ressurss**.</span><span class="sxs-lookup"><span data-stu-id="445d6-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="445d6-107">Väiksemad ettevõtted, millel on vähem kui 20–30 arveldatavat ressurssi, võivad leida, et lihtsam on lihtsalt igale ressursile määrata konkreetsed arveldus- ja kulumäärad.</span><span class="sxs-lookup"><span data-stu-id="445d6-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="445d6-108">Kuid kuna tasustatav tööjõud kasvab, võib ressursipõhised määrad muutuda ebarealistlikuks, et neid säilitada.</span><span class="sxs-lookup"><span data-stu-id="445d6-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="445d6-109">Ressursi kulu ja arve määrad hakkavad erinema, kui ressursse edutatakse, nad saavad rohkem kogemusi või õpivad juurde uusi oskusi.</span><span class="sxs-lookup"><span data-stu-id="445d6-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="445d6-110">Teine näide on kandekategooria.</span><span class="sxs-lookup"><span data-stu-id="445d6-110">Another example is that of transaction category.</span></span> <span data-ttu-id="445d6-111">Kliendid ja juurutajad on kasutanud kandekategooriat töö klassifitseerimiseks ning välja hinnakujunduse ja kulude jaoks vastavalt töökategooria järgi.</span><span class="sxs-lookup"><span data-stu-id="445d6-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
