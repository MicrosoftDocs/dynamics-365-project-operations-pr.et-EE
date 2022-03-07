---
title: Kataloogis olevate toodete kulu ja müügihindade seadistamine
description: Selles teemas kirjeldatakse tootekataloogi üksuste kulude ja müügihindade seadistamist.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075023"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Kataloogis olevate toodete kulu ja müügihindade seadistamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Tootekataloogi üksuste hinnakujunduse seadistamine Dynamics 365 Project Operationsis on sama, mis Dynamics 365 Salesis.

Kuna tooteid ei saa prognoosida ega kasutada Project Operationsi projektides, ei pea seadistama tootekataloogi hindu hinnapakkumiste ja lepingute projekti hinnakirjadele.

Tootekataloogi hinnad tuleks seadistada hinnapakkumise, lepingu või konto väljal **Toote hind**. Ärge seadistage tootekataloogi hindu nende olemite projekti hinnakirjades. Projekti hinnakirjad on eksklusiivsed Project Operationsile. Seal on rakendusele omane äriloogika, mis kopeerib hinnakirjad hinnapakkumisest lepingule. Tulemuseks on lepingupõhine projekti hinnakiri. Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks. Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks. See tähendab, et toodete hinnakiri ei mõjuta hinnapakkumise võitmise protsessi tulemuslikkust.
