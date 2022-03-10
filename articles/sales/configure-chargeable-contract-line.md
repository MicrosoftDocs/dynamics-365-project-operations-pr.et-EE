---
title: Projekti lepingurea arveldatavate komponentide konfigureerimine
description: Selles teemas antakse teavet kaasatud, arveldatavate ja mittearveldatavate komponentide kohta lepinguridadel.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 51151089df67e2d164fc6315c1291f880917f43f1fba189304cb305ea973cecb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004036"
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
