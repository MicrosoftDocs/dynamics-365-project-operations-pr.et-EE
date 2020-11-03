---
title: Projektipõhise lepingurea arveldatavate komponentide konfigureerimine
description: Selles teemas antakse teavet kaasatud, arveldatavate ja mittearveldatavate komponentide kohta lepinguridadel.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074893"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Projektipõhise lepingurea arveldatavate komponentide konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektipõhine lepingurida sisaldab kaasatud, arveldatavaid ja mittearveldatavaid komponente.

Kaasatud komponendid sõltuvad arveldusmeetodist, kliendi jaotamisest, mitteületatavatest limiitidest ja arve sageduse sätetest, mis on määratletud projektipõhisel lepingureal.

Kaasatud komponentide alamhulka saab märkida arveldatavana, muutes välja väärtuseks **Arveldamise tüüp**.

Arveldatavad komponendid saab määratleda rollides ja tehingute kategooriates.

Projekti lepingurea rollile määratud arveldatavuse kehtib ainult tehingu klassile **Aeg**. Kui projekti lepingurea väli **Kaasa aeg** on seatud väärtusele **Ei** , ei ole vahekaart **Arveldatavad rollid** saadaval.

Projekti lepingurea tehingu kategooriate määratud arveldatavuse kehtib ainult tehingu klassile **Kulu**. Kui projekti lepingurea väli **Kaasa kulud** on seatud väärtusele **Ei** , ei ole vahekaart **Arveldatavad kategooriad** saadaval.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks

Roll võib olla arveldatav või mittearveldatav kindla projektipõhise lepingurea kohta.

Värskendage projektipõhise lepingurea vahekaardil **Arveldatavad rollid** , andmeruudustikus **Arveldatavad kategooriad** väljal **Arveldamise tüüp** rolli arveldamise tüüpi.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks

Tehingu kategooria võib olla arveldatav või mittearveldatav kindla projektipõhise lepingurea kohta.

Värskendage projektipõhise lepingurea vahekaardil **Arveldatavad kategooriad** , andmeruudustikus **Arveldatavad kategooriad** väljal **Arveldamise tüüp** tehingu arveldamise tüüpi.

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