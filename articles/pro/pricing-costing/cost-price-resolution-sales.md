---
title: Prognooside ja tegelike näitajate omahinna lahendamine – liht
description: Selles teemas antakse teavet prognooside ja tegelike näitajate omahindade lahendamise kohta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764578"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Prognooside ja tegelike näitajate omahinna lahendamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Omahindade ja omahinna loendi lahendamiseks prognooside ja tegelike näitajate puhul kasutab süsteem teavet, mis on seotud projekti väljadel **Kuupäev**, **Valuuta** ja **Lepingut sõlmiv üksus**. Pärast omahinnaloendi lahendamist lahendab rakendus omahinna.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Aja tegelike ja prognoositavate ridade kulumäärade lahendamine

Aja prognoositavad read viitavad projekti aja- ja ressursimäärangute hinnapakkumise ja lepingurea üksikasjadele.

Kui omahinnakiri on lahendatud, vastendatakse aja prognoosi real olevad väljad **Roll** ja **Ressursiühik** hinnakirja rolli hinna ridadega. Selle vaste puhul eeldatakse, et kasutate tööjõukulu jaoks standardseid hinnakujunduse dimensioone. Kui olete konfigureerinud süsteemi, et see vastaks väljadele või lisaks väljadele **Roll** ja **Ressursi üksus**, kasutatakse vastava rolli hinna rea toomiseks erinevat kombinatsiooni. Kui rakendus leiab rolli hinna rea, millel on väljade **Roll** ja **Ressursi ühik** kulumäära kombinatsioon, mis on vaikimisi kulumäär. Kui rakendus ei vasta välja **Roll** ja **Ressursi ühik** väärtustele, toob see rolli hinna read, millel on vastav roll, kuid välja **Ressursi ühik** väärtus on null. Pärast vastava rollihinna kirje salvestamist on kulumäär sellest kirjest vaikimisi. 

> [!NOTE]
> Kui konfigureerite väljadele **Roll** ja **Ressursi ühik** erineva tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub käitumine vastavalt. Süsteem toob rollihinna kirjed väärtustega, mis vastavad igale hinnadimensiooni väärtusele tähtsuse järjekorras ridadega, mille dimensioonide jaoks on viimasena tühiväärtused.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kulu tegelike ja prognoositavate ridade kulumäärade lahendamine

Kulu prognoositavad read viitavad projekti kulu ja kulu prognoositavate ridade hinnapakkumise ja lepingurea üksikasjadele.

Kui kuluhinnakiri on lahendatud, kasutab süsteem kuluprognoosi ridade välju **Kategooria** ja **Üksus**, et vastendada need lahendatud hinnakirja ridadega **Kategooria hind**. Kui süsteem leiab kategooria hinna rea, millel on väljade **Kategooria** ja **Ühik** kulumäära kombinatsioon, mis on vaikimisi kulumäär. Kui süsteem ei suuda vastendada väärtusi **Kategooria** ja **Üksus**, või ei suuda leida vastavat kategooria hinnarida, kuid hinnakujundusmeetodiks ei ole **Hind üksuse kohta**, on kulumääraks vaikimisi null (0).
