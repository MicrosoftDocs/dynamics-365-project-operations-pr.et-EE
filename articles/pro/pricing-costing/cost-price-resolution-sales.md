---
title: Projekti prognooside ja tegelike näitajate omahinna lahendamine
description: Selles teemas antakse teavet selle kohta, kuidas projekti prognooside ja tegelike näitajate omahinda lahendatakse.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9f20631f41c560f1a4047aaaa624fa4e8651c687
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877260"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Projekti prognooside ja tegelike näitajate omahinna lahendamine 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Materjali tegelike ja prognoosiridade kuluhindade lahendamine

Materjalide prognoosiread viitavad projekti materjalide ja materjalide prognoosiridade hinnapakkumise ja lepingurea üksikasjadele.

Kui omahinna hinnakiri on lahendatud, kasutab süsteem hinnangureal olevate väljade **Toode** ja **Ühik** kombinatsiooni, et vastendada materjali prognoosi lahendatud hinnakirja ridadega **Hinnakirjaüksused**. Kui süsteem leiab tootehinna rea, mille väljade **Toode** ja **Ühik** väärtus on kulumäär, siis läheb kulumäär vaikeväärtusele. Kui süsteem ei saa väärtusi **Toode** ja **Üksus** ühitada või kui see on suudab leida sobiva hinnakirjaüksuse rea, kuid hinnakujundusmeetod põhineb standardsel kulul või praegusel kulul ja kumbki pole tootel määratletud, on ühikukulu vaikeväärtuseks null.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
