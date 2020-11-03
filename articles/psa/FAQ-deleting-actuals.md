---
title: Miks ei saa kirjeid tegelike näitajate olemist kustutada?
description: Selles teemas antakse teavet selle kohta, miks te ei saa kirjeid tegelikest olemitest kustutada.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075082"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="87a9b-103">Miks ei saa kirjeid tegelike näitajate olemist kustutada?</span><span class="sxs-lookup"><span data-stu-id="87a9b-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="87a9b-104">Project Service Automation (PSA) ei luba teil tegelikke näitajaid kustutada, kuna need on tõe allikas, mis on finantsmõju allsüsteemidele (nt pearaamat).</span><span class="sxs-lookup"><span data-stu-id="87a9b-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="87a9b-105">Kui tegelikke andmeid saab kustutada, võib kahtluse alla seada finantsaruandluse tervikluse.</span><span class="sxs-lookup"><span data-stu-id="87a9b-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="87a9b-106">Kontrolljälje loomiseks peaksid kliendid kasutama töölehti, et luua kompenseerivad tehingud.</span><span class="sxs-lookup"><span data-stu-id="87a9b-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

