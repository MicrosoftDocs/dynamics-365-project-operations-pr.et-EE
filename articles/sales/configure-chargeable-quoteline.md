---
title: Projektipõhise hinnapakkumise rea arveldatavate komponentide konfigureerimine
description: Selles artiklis antakse teavet projektipõhiste hinnapakkumisridade kaasatud, tasuliste ja mittetasustatavate komponentide kohta.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff409132ef9103641578f9c94f8ea1ff56738a71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915547"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Projektipõhise hinnapakkumise rea arveldatavate komponentide konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projektipõhine hinnapakkumise rida võib sisaldada tasulisi ja tavalisi komponente.

Kaasatud komponentide puhul rakendatakse arveldusmeetodi, kliendi jaotamise, limiitide mitte ületamise ja arve sageduse sätteid, mis on määratletud projektipõhise hinnapakkumise real.
Kaasatud komponentide alamhulka saab märkida arveldatavatena, kasutades atribuuti **Arve tüüp**. Väljal **Arve tüüp** saate hinnapakkumise rea puhul valida ühe järgmistest suvanditest.

   - Arveldatav
   - Mittearveldatav

Arveldatavad komponendid saab määratleda rollides ja kande kategooriates.

Projekti hinnapakkumise rea rollidele määratud arveldatavus kehtib ainult kandeklassile **Aeg**. Kui projekti hinnapakkumise real on atribuut **Kaasa aeg** = **ei**, siis ei ole vahekaart **Arveldatav roll** saadaval.

Projekti hinnapakkumise rea rollidele määratud kande kategooriad kehtivad ainult kandeklassile **Kulu**. Kui projekti hinnapakkumise rea on atribuut **Kulud** = **ei**, siis ei ole vahekaart **Kategooriad**.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolli värskendamine arveldatavaks või mittearveldatavaks
Projektipõhise hinnapakkumise rea roll võib olla arveldatav või mittearveldatav. Rolli arveldamise tüübi saab konfigureerida projektipõhise hinnapakkumise rea vahekaardil **Arveldatavad rollid**. Selleks värskendage andmeruudustikus **Arveldatavad rollid** välja **Arveldamise tüüp**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Tehingu kategooria värskendamine arveldatavaks või mittearveldatavaks
Projektipõhise hinnapakkumise rea kande kategooria võib olla arveldatav või mittearveldatav. Kande arveldamise tüübi saab konfigureerida projektipõhise hinnapakkumise rea vahekaardil **Arveldatavad kategooriad**. Selleks värskendage andmeruudustikus **Arveldatavad kategooriad** välja **Arveldamise tüüp**. 

## <a name="resolve-chargeability"></a>Arveldatavuse lahendamine

Eeldatavat või tegelikku loodud aega käsitletakse tasustatava aja järgi ainult juhul, kui see on hinnapakkumise reale kaasatud ja kui roll on konfigureeritud arveldatavana.
Eeldatavat või tegelikku loodud kulu käsitletakse arveldatava kulu järgi ainult juhul, kui see on hinnapakkumise reale kaasatud ja kui kande kategooria on konfigureeritud arveldatavana. Järgmine tabel näitab, kui palju on igal väärtusel arveldatavaid vaikeväärtusi. Vaikeväärtused põhinevad kaasatud komponentidel ja hinnapakkumise real seadistatud arveldamise tüübil.

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