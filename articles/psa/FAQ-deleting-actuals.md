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
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Miks ei saa kirjeid tegelike näitajate olemist kustutada?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ei luba teil tegelikke näitajaid kustutada, kuna need on tõe allikas, mis on finantsmõju allsüsteemidele (nt pearaamat). Kui tegelikke andmeid saab kustutada, võib kahtluse alla seada finantsaruandluse tervikluse. Kontrolljälje loomiseks peaksid kliendid kasutama töölehti, et luua kompenseerivad tehingud.

