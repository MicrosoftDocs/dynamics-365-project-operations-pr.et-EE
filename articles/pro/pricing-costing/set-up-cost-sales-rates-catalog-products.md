---
title: Kataloogitoodete oma- ja müügihindade seadistamine – liht
description: Selles artiklis antakse teavet selle kohta, kuidas seadistada tootekataloogi kaupade kulu- ja müügimäärasid.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917387"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kataloogitoodete oma- ja müügihindade seadistamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Tootekataloogi üksuste hinnakujunduse seadistamine rakenduses Dynamics 365 Project Operations on sama nagu rakenduses Dynamics 365 Sales.

Project Operationsis ei saa tooteid hinnata ega projektides kasutada, seega ei pea tootekataloogi hindasid hinnapakkumiste ja lepingute jaoks projekti hinnakirjades seadistama.

Tootekataloogi hindade seadistamiseks kasutage hinnapakkumise, lepingu või konto välja **Toote hind**. Ärge seadistage tootekataloogi hindasid projekti hinnakirjades. Projekti hinnakirjad on eksklusiivsed Project Operationsile. Rakendusepõhine äriloogika kopeerib hinnakirjad hinnapakkumisest lepingusse. Tulemuseks on lepingupõhine projekti hinnakiri. Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks. Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks. Kuna kopeerimist pole kasutatud, siis hinnapakkumise protsessi jõudlust see ei mõjuta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]