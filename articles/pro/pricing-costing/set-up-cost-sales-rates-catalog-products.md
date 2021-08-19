---
title: Kataloogitoodete oma- ja müügihindade seadistamine – liht
description: Selles teemas kirjeldatakse tootekataloogi üksuste kulude ja müügihindade seadistamist.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996026"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kataloogitoodete oma- ja müügihindade seadistamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Tootekataloogi üksuste hinnakujunduse seadistamine rakenduses Dynamics 365 Project Operations on sama nagu rakenduses Dynamics 365 Sales.

Project Operationsis ei saa tooteid hinnata ega projektides kasutada, seega ei pea tootekataloogi hindasid hinnapakkumiste ja lepingute jaoks projekti hinnakirjades seadistama.

Tootekataloogi hindade seadistamiseks kasutage hinnapakkumise, lepingu või konto välja **Toote hind**. Ärge seadistage tootekataloogi hindasid projekti hinnakirjades. Projekti hinnakirjad on eksklusiivsed Project Operationsile. Rakendusepõhine äriloogika kopeerib hinnakirjad hinnapakkumisest lepingusse. Tulemuseks on lepingupõhine projekti hinnakiri. Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks. Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks. Kuna kopeerimist pole kasutatud, siis hinnapakkumise protsessi jõudlust see ei mõjuta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]