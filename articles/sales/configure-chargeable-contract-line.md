---
title: Projekti lepingurea arveldatavate komponentide konfigureerimine
description: Selles artiklis antakse teavet lepinguridade kaasatud, tasuliste ja mittetasustatavate komponentide kohta.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 175b25dbcc43a5954fbbf2d54efdd73e19395907
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928289"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Projekti lepingurea arveldatavate komponentide konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektipõhine lepingurida sisaldab kaasatud, arveldatavaid ja mittearveldatavaid komponente.

Kaasatud komponendid sõltuvad arveldusmeetodist, kliendi jaotamisest, mitteületatavatest limiitidest ja arve sageduse sätetest, mis on määratletud projektipõhisel lepingureal.

Kaasatud komponentide alamhulka saab märkida arveldatavana, muutes välja väärtuseks **Arveldamise tüüp**.

Arveldatavad komponendid saab määratleda rollides ja tehingute kategooriates.

Projekti lepingurea rollile määratud arveldatavuse kehtib ainult tehingu klassile **Aeg**. Kui projekti lepingurea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.

Projekti lepingurea tehingu kategooriate määratud arveldatavuse kehtib ainult tehingu klassile **Kulu**. Kui projekti lepingurea väli **Kaasa kulud** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks

Roll võib olla arveldatav või mittearveldatav kindla projektipõhise lepingurea kohta.

Projektipõhise lepingurea vahekaardil **Arveldatavad rollid** andmeruudustikus **Arveldatavad kategooriad** väljal **Arvelduse tüüp** värskendage rolli arvelduse tüüpi.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks

Tehingu kategooria võib olla arveldatav või mittearveldatav kindla projektipõhise lepingurea kohta.

Projektipõhise lepingurea vahekaardil **Arveldatavad kategooriad** andmeruudustikus **Arveldatavad kategooriad** väljal **Arvelduse tüüp** värskendage tehingu arvelduse tüüpi.

### <a name="resolve-chargeability"></a>Arveldatavuse lahendamine

Aja jaoks loodud prognoosi või tegelikku näitajat käsitletakse arveldatavaks ainult juhul, kui lepingureal on kaasatud aeg ja kui roll konfigureeritakse lepingureal arveldatavana.

Kulu jaoks loodud prognoosi või tegelikku näitajat käsitletakse arveldatavaks ainult juhul, kui lepingureal on kaasatud kulu ja kui tehingu kategooria konfigureeritakse lepingureal arveldatavana.

| Kaasab aja | Kaasab kulu | Roll | Kategooria | Toiming |
| --- | --- | --- | --- | --- |
| Ja | Ja | Arveldatav | Arveldatav | Tegeliku aja arveldamine: Arveldatav </br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| Ja | Ja | Mittearveldatav | Arveldatav | Tegeliku aja arveldamine: Mittearveldatav </br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| Ja | Ja | Mittearveldatav | Mittearveldatav | Tegeliku aja arveldamine: Mittearveldatav </br>Tegeliku kulu arveldamise tüüp: Mittearveldatav |
| No | Ja | Ei saa seadistada | Arveldatav | Tegeliku aja arveldamine: Pole saadaval </br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| No | Ja | Ei saa seadistada | Mittearveldatav | Tegeliku aja arveldamine: Pole saadaval </br>Tegeliku kulu arveldamise tüüp: Mittearveldatav |
| Ja | No | Arveldatav | Ei saa seadistada | Tegeliku aja arveldamine: Arveldatav </br>Tegeliku kulu arveldamise tüüp: Pole saadaval |
| Ja | No | Mittearveldatav | Ei saa seadistada | Tegeliku aja arveldamine: Mittearveldatav </br> Tegeliku kulu arveldamise tüüp: Pole saadaval |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
