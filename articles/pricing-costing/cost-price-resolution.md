---
title: Prognooside ja tegelike näitajate omahindade lahendamine
description: Selles teemas antakse teavet prognooside ja tegelike näitajate lahendamise kohta.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003676"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Prognooside ja tegelike näitajate omahindade lahendamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Omahindade ja omahinna loendi lahendamiseks prognooside ja tegelike näitajate puhul kasutab süsteem teavet, mis on seotud projekti väljadel **Kuupäev**, **Valuuta** ja **Lepingut sõlmiv üksus**. Pärast omahinnaloendi lahendamist lahendab rakendus omahinna.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Aja tegelike ja prognoositavate ridade kulumäärade lahendamine

Aja prognoositavad read viitavad projekti aja- ja ressursimäärangute hinnapakkumise ja lepingurea üksikasjadele.

Pärast omahinna loendi lahendamist kasutab süsteem aja prognoositaval real välju **Roll**,  **Ressursiettevõte** ja **Ressursi üksus**, et need vastaksid hinnakirja rollihindade ridadele. See vaste eeldab, et kasutate tööjõukulude jaoks hinnakujunduse dimensioone. Kui olete konfigureerinud süsteemi, et see vastaks väljadele või lisaks väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik**, kasutatakse vastava rolli hinna rea toomiseks erinevat kombinatsiooni. Kui rakendus leiab rolli hinna rea, millel on väljade **Roll**, **Ressursiettevõte** ja **Ressursi ühik** kulumäära kombinatsioon, mis on vaikimisi kulumäär. Kui rakendus ei saa väärtuste **Roll**, **Ressursi ettevõte** ja **Ressursiüksus** kombinatsiooni täpselt vastendada, toob see rolli hinnaread kattuva rolliväärtusega, kuid millel on nullväärtused suvanditel **Ressursiüksus** ja **Ressursi ettevõte**. Pärast leitakse ühtiv rolli ühikukirje, millel on ühtiv rolli hinnaväärtus, tuuakse kulumäär vaikimisi sellest kirjest. 

> [!NOTE]
> Kui konfigureerite väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik** erineva tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub käitumine vastavalt. Süsteem toob rolli hinnakirjed väärtustega, mis vastavad igale hinnakujunduse dimensioonile prioriteedi järjestuses, koos ridadega, millel on prioriteedi järjestuses viimasel kohal olevatel dimensioonidel nullväärtus.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kulu tegelike ja prognoositavate ridade kulumäärade lahendamine

Kulu prognoositavad read viitavad projekti kulu ja kulu prognoositavate ridade hinnapakkumise ja lepingurea üksikasjadele.

Pärast omahinna loendi lahendamist kasutab süsteem prognoositaval real väljade **Kategooria** ja **Üksus** kombinatsiooni, et kulu vastaks lahendatud hinnakirja ridadele **Kategooria hind**. Kui süsteem leiab kategooria hinna rea, millel on väljade **Kategooria** ja **Ühik** kulumäära kombinatsioon, mis on vaikimisi kulumäär. Kui süsteem ei vasta väärtustele **Kategooria** ja **Ühik** või kui see suudab leida vastava kategooria hinnarea, kuid hinnakujundusmeetod ei ole **Ühiku hind**, on omahinna määr vaikimisi null (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Materjali tegelike ja prognoosiridade kuluhindade lahendamine

Materjalide prognoosiread viitavad projekti materjalide ja materjalide prognoosiridade hinnapakkumise ja lepingurea üksikasjadele.

Kui omahinna hinnakiri on lahendatud, kasutab süsteem hinnangureal olevate väljade **Toode** ja **Ühik** kombinatsiooni, et vastendada materjali prognoosi lahendatud hinnakirja ridadega **Hinnakirjaüksused**. Kui süsteem leiab tootehinna rea, mille väljade **Toode** ja **Ühik** väärtus on kulumäär, siis läheb kulumäär vaikeväärtusele. Kui süsteem ei saa väljade **Toode** ja **Ühik** väärtuseid ühitada, on üksuse hinna vaikeväärtuseks null. See vaikeväärtus juhtub ka siis, kui hinnakirjaüksuse rida on ühtiv, kuid hinnakujundusmeetod põhineb standardsel kulul või praegusel kulul, mis pole tootes määratletud.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
