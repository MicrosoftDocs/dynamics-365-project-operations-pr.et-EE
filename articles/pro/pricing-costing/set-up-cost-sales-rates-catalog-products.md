---
title: Kataloogitoodete oma- ja müügihindade seadistamine – liht
description: Selles teemas kirjeldatakse tootekataloogi üksuste kulude ja müügihindade seadistamist.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576817"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kataloogitoodete oma- ja müügihindade seadistamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Tootekataloogi üksuste hinnakujunduse seadistamine rakenduses Dynamics 365 Project Operations on sama nagu rakenduses Dynamics 365 Sales.

Project Operationsis ei saa tooteid hinnata ega projektides kasutada, seega ei pea tootekataloogi hindasid hinnapakkumiste ja lepingute jaoks projekti hinnakirjades seadistama.

Tootekataloogi hindade seadistamiseks kasutage hinnapakkumise, lepingu või konto välja **Toote hind**. Ärge seadistage tootekataloogi hindasid projekti hinnakirjades. Projekti hinnakirjad on eksklusiivsed Project Operationsile. Rakendusepõhine äriloogika kopeerib hinnakirjad hinnapakkumisest lepingusse. Tulemuseks on lepingupõhine projekti hinnakiri. Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks. Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks. Kuna kopeerimist pole kasutatud, siis hinnapakkumise protsessi jõudlust see ei mõjuta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]