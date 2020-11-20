---
title: Kataloogitoodete oma- ja müügihindade seadistamine – liht
description: Selles teemas kirjeldatakse tootekataloogi üksuste kulude ja müügihindade seadistamist.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176696"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kataloogitoodete oma- ja müügihindade seadistamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Tootekataloogi üksuste hinnakujunduse seadistamine Dynamics 365 Project Operationsis on sama, mis Dynamics 365 Salesis.

Kuna tooteid ei saa prognoosida ega kasutada Project Operationsi projektides, ei pea seadistama tootekataloogi hindu hinnapakkumiste ja lepingute projekti hinnakirjadele.

Tootekataloogi hinnad tuleks seadistada hinnapakkumise, lepingu või konto väljal **Toote hind**. Ärge seadistage tootekataloogi hindu nende olemite projekti hinnakirjades. Projekti hinnakirjad on eksklusiivsed Project Operationsile. Seal on rakendusele omane äriloogika, mis kopeerib hinnakirjad hinnapakkumisest lepingule. Tulemuseks on lepingupõhine projekti hinnakiri. Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks. Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks. See tähendab, et toodete hinnakiri ei mõjuta hinnapakkumise võitmise protsessi tulemuslikkust.
