---
title: Hinnapakkumise rea arveldatavate komponentide konfigureerimine – liht
description: Selles teemas antakse teavet arveldatavate ja mittearveldatavate komponentide seadistamise kohta projektipõhise hinnapakkumise real.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177101"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Hinnapakkumise rea arveldatavate komponentide konfigureerimine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektipõhine hinnapakkumise rida sisaldab *kaasatud* komponente ja *arveldatavaid* komponente.

Kaasatud komponente võidakse:

  - Arveldusmeetod ja kliendi jaotamine
  - Mitteületatavad limiidid 
  - Projektipõhise hinnapakkumise rea määratletud arve sageduse sätted

Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**. Väli **Arveldamise tüüp** on seatud, mis võimaldab hinnapakkumise rea kontekstis järgmisi väärtusi.

  - Arveldatav
  - Mittearveldatav

Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.

Arveldatav tegevus määratletakse hinnapakkumise rea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele. Kui väli **Kaasa tööülesanded** on seatud väärtusele **Kogu projekt** või see on tühjaks jäetud, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.

Hinnapakkumise rea rollidele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Aeg**. Kui projekti hinnapakkumise rea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.

Hinnapakkumise rea tehingu kategooriatele on määratud arveldatavus ja see kehtib ainult tehingu klassile **Kulu**. Kui projekti hinnapakkumise rea väli **Kaasa kulud** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks

Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla projektipõhise hinnapakkumise rea kohta, mis võimaldab järgmist seadistust.

Kui projektipõhise hinnapakkumise rida sisaldab väärtust **Aeg** ja tööülesannet **T1**, seostatakse tööülesanne hinnapakkumise reaga kui arveldatav. Kui olemas on teine hinnapakkumise rida, mis sisaldab väärtust **Kulud**, saate seostada hinnapakkumise rea tööülesannet **T1** sellega kui arveldatav. Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.

Ülesande arveldamise tüübi saab konfigureerida projektipõhise hinnapakkumise rea vahekaardil **Arveldatavad ülesanded**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Hinnapakkumise rea ülesanded**. Teise võimalusena saate värskendada projekti ülesande arveldamise tüüpi väljal **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud hinnapakkumise ridu.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks

Roll võib konkreetse projektipõhise hinnapakkumise rea puhul olla arveldatav või mittearveldatav.

Rolli arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad rollid**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad rollid**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks

Tehingu kategooria võib olla arveldatav või mittearveldatav kindla hinnapakkumise rea kohta.

Tehingu arveldamise tüübi saab konfigureerida hinnapakkumise rea vahekaardil **Arveldatavad kategooriad**, värskendades välja **Arveldamise tüüp** andmeruudustikus **Arveldatavad kategooriad**.

### <a name="resolve-chargeability"></a>Arveldatavuse lahendamine
Aja jaoks loodud prognoosi või tegelikku näitajat käsitletakse arveldatavaks ainult juhul, kui hinnapakkumise real on kaasatud väärtus **Aeg** ja kui kategooriaid **Tööülesanne** ja **Roll** konfigureeritakse hinnapakkumise real arveldatavana.

Kulu jaoks loodud prognoosi või tegelikku näitajat käsitletakse arveldatavaks ainult juhul, kui hinnapakkumise real on kaasatud väärtus **Kulu** ja kui väärtused **Tööülesanne** ja **Tehingu kategooria** konfigureeritakse hinnapakkumise real arveldatavana.

| Kaasab aja | Kaasab kulu | Kaasatud ülesanded | Roll | Kategooria | Toiming | Arveldamine |
| --- | --- | --- | --- | --- | --- | --- |
| Ja | Ja | Kogu projekt | Arveldatav | Arveldatav | Ei saa seadistada | Tegeliku aja arveldamine: Arveldatav </br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| Ja | Ja | Ainult valitud ülesanded | Arveldatav | Arveldatav | Arveldatav | Tegeliku aja arveldamine: Arveldatav</br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| Ja | Ja | Ainult valitud ülesanded | Mittearveldatav | Arveldatav | Arveldatav | Tegeliku aja arveldamine: Mittearveldatav</br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| Ja | Ja | Ainult valitud ülesanded | Arveldatav | Arveldatav | Mittearveldatav | Tegeliku aja arveldamine: Mittearveldatav</br> Tegeliku kulu arveldamise tüüp: Mittearveldatav |
| Ja | Ja | Ainult valitud ülesanded | Mittearveldatav | Arveldatav | Mittearveldatav | Tegeliku aja arveldamine: Mittearveldatav</br> Tegeliku kulu arveldamise tüüp: Mittearveldatav |
| Ja | Ja | Ainult valitud ülesanded | Mittearveldatav | Mittearveldatav | Arveldatav | Tegeliku aja arveldamine: Mittearveldatav</br> Tegeliku kulu arveldamise tüüp: Mittearveldatav |
| No | Ja | Kogu projekt | Ei saa seadistada | Arveldatav | Ei saa seadistada | Tegeliku aja arveldamine: Pole saadaval </br>Tegeliku kulu arveldamise tüüp: Arveldatav |
| No | Ja | Kogu projekt | Ei saa seadistada | Mittearveldatav | Ei saa seadistada | Tegeliku aja arveldamine: Pole saadaval </br>Tegeliku kulu arveldamise tüüp: Mittearveldatav |
| Ja | No | Kogu projekt | Arveldatav | Ei saa seadistada | Ei saa seadistada | Tegeliku aja arveldamine: Arveldatav</br>Tegeliku kulu arveldamise tüüp: Pole saadaval |
| Ja | No | Kogu projekt | Mittearveldatav | Ei saa seadistada | Ei saa seadistada | Tegeliku aja arveldamine: Mittearveldatav </br>Tegeliku kulu arveldamise tüüp: Pole saadaval |
