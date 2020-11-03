---
title: Näidisarve kinnitamine
description: Selles teemas antakse teavet fiktiivse arve kinnitamise kohta.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074801"
---
# <a name="confirm-a-proforma-invoice"></a>Näidisarve kinnitamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Pärast näidisarve kinnitamist värskendatakse projekti arve olekuks **Kinnitatud**. Kui arve on kinnitatud, muutub see kirjutuskaitstuks. Edaspidi saab arvet parandada ainult juhul, kui on kliendi algatatud parandused või krediidid, või kui see on märgitud tasutuks.

Järgmises tabelis on loetletud süsteemi loodud tegelikud näitajad. Need tegelikud näitajad luuakse teatud toimingute tegemisel projekti arve mustandisse enne selle kinnitamist.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Stsenaarium</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Ajatehingu arveldamine ilma mustandi arvel tehtud muudatusteta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelikud näitaja algse ajakinnituse tundide ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Ajatehingu arveldamine, mida redigeeriti koguse vähendamiseks.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud tundide ja summa eest pärast parandatud arvude mahaarvamist, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Ajatehingu arveldamine, mida redigeeriti koguse suurendamiseks.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse ajakinnituse tundide ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Kulu tehingu arveldamine ilma mustandi arvel tehtud muudatusteta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelik väärtus algse kulukinnituse koguse ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Kulu tehingu arveldamine, mida redigeeriti koguse vähendamiseks.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud koguse ja summa eest pärast parandatud arvude mahaarvamist, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Kulu tehingu arveldamine, mida redigeeriti koguse suurendamiseks.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse kulukinnituse koguse ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade koguse ja summa eest, tegeliku arveldamata müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Arve esitamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tühistamine algse töölehe rea tasude puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelik väärtus algse töölehe rea tasude koguse ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Vahe-eesmärgi esitamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Projekti lepingurea algse vahe-eesmärgi vahe-eesmärgi arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
    </tbody>
</table>