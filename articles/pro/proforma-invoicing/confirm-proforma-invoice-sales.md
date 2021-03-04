---
title: Näidisarve kinnitamine – liht
description: Selles teemas antakse teavet Project Operationsis näidisarvete kinnitamise kohta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176516"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Näidisarve kinnitamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Pärast näidisarve kinnitamist värskendatakse projekti arve olekuks **Kinnitatud**. Kui arve on kinnitatud, muutub see kirjutuskaitstuks. Edaspidi saab arvet parandada ainult juhul, kui on kliendi algatatud parandused või krediidid, või kui arve on märgitud tasutuks.

Järgmises tabelis on loetletud süsteemi loodud tegelikud näitajad. Need tegelikud näitajad luuakse teatud toimingute tegemisel projekti arve mustandisse enne selle kinnitamist.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Stsenaarium</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Kinnitusel loodud tegelikud näitajad</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Ettemaksu või honorari arveldamine </p>
            </td>
            <td width="408" valign="top">
                <p>
Arvestatud müügi tegeliku näitaja tüüp, <strong>Honorar</strong> luuakse ettemakse või honorari summa jaoks.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Pärast honorari või ettemaksu täielikku vastavusseviimist arvega.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks. See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelik näitaja selle arve summa jaoks.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Pärast honorari või ettemaksu osalist vastavusseviimist arvega.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks. See summa on positiivne, kuna selle eesmärk on tühistada negatiivne summa, mis loodi honorari või ettemakse arve esitamisel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelik näitaja selle arve summa jaoks.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.
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
Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, tegeliku müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on mittearveldatav muudetud arverea üksikasjade järelejäänud tundide ja summa eest pärast parandatud arvude mahaarvamist, tegeliku müügi tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
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
Arveldatud müügi tegelik väärtus algse kulukinnituse koguse ja summa puhul </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Tootepõhiste lepinguridade arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Selle toote rea arveldatud tegelik müük, mille kogus ja summa pärineb tootepõhiselt lepingurealt.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]