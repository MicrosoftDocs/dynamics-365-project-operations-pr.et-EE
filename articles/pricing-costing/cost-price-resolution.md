---
title: Prognooside ja tegelike näitajate omahindade lahendamine
description: Selles teemas antakse teavet prognooside ja tegelike näitajate lahendamise kohta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119684"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Prognooside ja tegelike näitajate omahindade lahendamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Omahindade ja omahinna loendi lahendamiseks prognooside ja tegelike näitajate puhul kasutab süsteem teavet, mis on seotud projekti väljadel **Kuupäev**, **Valuuta** ja **Lepingut sõlmiv üksus**. Pärast omahinnaloendi lahendamist lahendab rakendus omahinna.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Aja tegelike ja prognoositavate ridade kulumäärade lahendamine

Aja prognoositavad read viitavad projekti aja- ja ressursimäärangute hinnapakkumise ja lepingurea üksikasjadele.

Pärast omahinna loendi lahendamist kasutab süsteem aja prognoositaval real välju **Roll**,  **Ressursiettevõte** ja **Ressursi üksus**, et need vastaksid hinnakirja rollihindade ridadele. See vaste eeldab, et kasutate tööjõukulude jaoks hinnakujunduse dimensioone. Kui olete konfigureerinud süsteemi, et see vastaks väljadele või lisaks väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik**, kasutatakse vastava rolli hinna rea toomiseks erinevat kombinatsiooni. Kui rakendus leiab rolli hinna rea, millel on väljade **Roll**, **Ressursiettevõte** ja **Ressursi ühik** kulumäära kombinatsioon, mis on vaikimisi kulumäär. Kui rakendus ei vasta välja **Roll**, **Ressursiettevõte** ja **Ressursi ühik** väärtustele, toob see rolli hinna read, millel on vastav roll, kuid välja **Ressursi ühik** väärtus on null. Pärast vastava rollihinna kirje salvestamist on kulumäär sellest kirjest vaikimisi. 

> [!NOTE]
> Kui konfigureerite väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik** erineva tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub käitumine vastavalt. Süsteem toob rollihinna kirjed väärtustega, mis vastavad igale hinnadimensiooni väärtusele tähtsuse järjekorras ridadega, mille dimensioonide jaoks on viimasena tühiväärtused.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kulu tegelike ja prognoositavate ridade kulumäärade lahendamine

Kulu prognoositavad read viitavad projekti kulu ja kulu prognoositavate ridade hinnapakkumise ja lepingurea üksikasjadele.

Pärast omahinna loendi lahendamist kasutab süsteem prognoositaval real väljade **Kategooria** ja **Üksus** kombinatsiooni, et kulu vastaks lahendatud hinnakirja ridadele **Kategooria hind**. Kui süsteem leiab kategooria hinna rea, millel on väljade **Kategooria** ja **Ühik** kulumäära kombinatsioon, mis on vaikimisi kulumäär. Kui süsteem ei vasta väärtustele **Kategooria** ja **Ühik** või kui see suudab leida vastava kategooria hinnarea, kuid hinnakujundusmeetod ei ole **Ühiku hind**, on omahinna määr vaikimisi null (0).
