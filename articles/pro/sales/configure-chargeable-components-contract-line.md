---
title: Projektipõhise lepingurea arveldatavate komponentide konfigureerimine – liht
description: Selles teemas antakse teavet selle kohta, kuidas lisada Project Operationsis lepinguridadele arveldatavaid komponente.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513874"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Projektipõhise lepingurea arveldatavate komponentide konfigureerimine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektipõhine lepingurida *sisaldas* komponente ja *arveldatavaid* komponente.

Kaasatud komponendid on komponendid, mis kuuluvad:

  - Arveldusmeetod ja kliendi jaotamine
  - Mitteületatavad limiidid 
  - Projektipõhise lepingurea määratletud arve sageduse sätted

Kaasatud komponentide alamhulka saab märkida arveldatavana, kasutades välja **Arveldamise tüüp**. Väli **Arveldamise tüüp** on seatud, mis võimaldab lepingurea kontekstis järgmisi väärtusi.

  - Arveldatav
  - Mittearveldatav

Arveldatavad komponendid saab määratleda tööülesannetes, rollides ja tehingute kategooriates.

Arveldatav tegevus määratletakse projekti lepingurea tööülesannetes ja seda rakendatakse kõigile real kaasatud tehingute klassidele. Kui lepingurea väli **Kaasa tööülesanded** on tühi või seatud väärtusele **Kogu projekt**, ei ole vahekaart **Arveldatavad tööülesanded** saadaval.

Projekti lepingurea rollidele määratud arveldatavuse kehtib ainult tehingu klassile **Aeg**. Kui lepingurea väli **Kaasa aeg** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad rollid** saadaval.

Projekti lepingurea tehingu kategooriate määratud arveldatavuse kehtib ainult tehingu klassile **Kulu**. Kui väli **Kaasa kulu** on seatud väärtusele **Ei**, ei ole vahekaart **Arveldatavad kategooriad** saadaval.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekti tööülesande värskendamine arveldatavaks või mittearveldatavaks

Projekti tööülesanne võib olla arveldatav või mittearveldatav kindla lepingurea kohta, mis võimaldab järgmist seadistust.

Kui projektipõhine lepingurida sisaldab väärtust **Aeg** ja teatud ülesannet, siis seostatakse väärtust **T1** sellega kui arveldatav. Kui olemas on teine lepingurida, mis sisaldab väärtust **Kulu**, saate seostada lepingurea väärtuse T1 tööülesannet sellega kui arveldatav. Tulemuseks on, et kogu tööülesande kohta registreeritud aeg on arveldatav ja kõik kulud on mittearveldatavad.

Ülesande arveldamise tüübi saab konfigureerida lepingurea vahekaardil **Arveldatavad ülesanded**, värskendades lepingurea ülesannete andmeruudustikus välja **Arveldamise tüüp**. Teise võimalusena saate värskendada välja **Arvelduse tüüp** ülesande arveldamise seadistuse andmeruudustikus projekti juures, mis näitab ülesandega seotud kontaktiridu.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks

Roll võib olla arveldatav või mittearveldatav kindla lepingurea kohta.

Rolli arveldamise tüüpi saab konfigureerida lepingurea vahekaardil **Arveldatavad rollid**. Selleks värskendage andmeruudustikus **Arveldatavad rollid** välja **Arveldamise tüüp**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks

Tehingu kategooria võib olla arveldatav või mittearveldatav kindla lepingurea kohta.

Tehingu arveldamise tüüpi saab konfigureerida projektipõhise lepingurea vahekaardil **Arveldatavad kategooriad**. Selleks värskendage andmeruudustikus **Arveldatavad kategooriad** välja **Arveldamise tüüp**.

### <a name="resolve-chargeability"></a>Arveldatavuse lahendamine

Aja jaoks loodud prognoosi või tegelikku näitajat käsitletakse arveldatavaks ainult juhul, kui lepingureal on kaasatud väärtus **Aeg** ja kui kategooriaid **Tööülesanne** ja **Roll** konfigureeritakse lepingureal arveldatavana.

Kulu jaoks loodud prognoosi või tegelikku näitajat käsitletakse arveldatavaks ainult juhul, kui lepingureal on kaasatud väärtus **Kulu** ja kui kategooriaid **Tööülesanne** ja **Tehing** konfigureeritakse lepingureal arveldatavana.


| Kaasab aja | Kaasab kulu | Kaasab tööülesanded | Roll           | Kategooria       | Toiming                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ja           | Ja              | Kogu projekt | Arveldatav     | Arveldatav     | Tegeliku aja arveldamine: **Arveldatav** </br> Tegeliku kulu arveldamise tüüp: **Arveldatav**           |
| Ja           | Ja              | Valitud tööülesanded | Arveldatav     | Arveldatav     | Tegeliku aja arveldamine: **Arveldatav** </br> Tegeliku kulu arveldamise tüüp: **Arveldatav**           |
| Ja           | Ja              | Valitud tööülesanded | Mittearveldatav | Arveldatav     | Tegeliku aja arveldamine: **Mittearveldatav** </br> Tegeliku kulu arveldamise tüüp: **Arveldatav**       |
| Ja           | Ja              | Valitud tööülesanded | Arveldatav     | Arveldatav     | Tegeliku aja arveldamine: **Mittearveldatav** </br> Tegeliku kulu arveldamise tüüp: **Mittearveldatav** |
| Ja           | Ja              | Valitud tööülesanded | Mittearveldatav | Arveldatav     | Tegeliku aja arveldamine: **Mittearveldatav** </br> Tegeliku kulu arveldamise tüüp: **Mittearveldatav** |
| Ja           | Ja              | Valitud tööülesanded | Mittearveldatav | Mittearveldatav | Tegeliku aja arveldamine: **Mittearveldatav** </br> Tegeliku kulu arveldamise tüüp: **Mittearveldatav** |
| No            | Ja              | Kogu projekt | Ei saa seadistada   | Arveldatav     | Tegeliku aja arveldamine: **Pole saadaval**</br>Tegeliku kulu arveldamise tüüp: **Arveldatav**          |
| No            | Ja              | Kogu projekt | Ei saa seadistada   | Mittearveldatav | Tegeliku aja arveldamine: **Pole saadaval**</br> Tegeliku kulu arveldamise tüüp: **Mittearveldatav**     |
| Ja           | No               | Kogu projekt | Arveldatav     | Ei saa seadistada   | Tegeliku aja arveldamine: **Arveldatav** </br> Tegeliku kulu arveldamise tüüp: **Pole saadaval**        |
| Ja           | No               | Kogu projekt | Mittearveldatav | Ei saa seadistada   | Tegeliku aja arveldamine: **Mittearveldatav** </br>Tegeliku kulu arveldamise tüüp: **Pole saadaval**   |
