---
title: Projektipõhise näidisarve kinnitamine
description: See teema sisaldab teavet projektipõhis näidisarve kinnitamise kohta.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 88dccb63247fe6937240921de7bc7a30a3737dad3f62c6c441d732c046aaddc3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985856"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Projektipõhise näidisarve kinnitamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Pärast näidisarve kinnitamist värskendatakse projekti arve olekuks **Kinnitatud**. Kui arve on kinnitatud, muutub see kirjutuskaitstuks. Edaspidi saate arve parandada ainult juhul, kui on olemas kliendiga seotud parandused või krediidid.

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
Arveldamata müügi tegelik näitaja kinnitamiseks kasutatava honorari või ettemaksu negatiivse summaga.
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
Uus arveldamata müügi tegelik väärtus, mis pärast muudetud arve rea üksikasjades parandatud arvude osa lahutamist jääb ülejäänud tundidele ja summale mittearveldatavaks, müügi tegelike näitajate ümberpööramine ja sellega võrdväärse arveldatud müügi tegelik näitaja.
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
Materjali tehingu arveldamine ilma arve mustandit muutmata.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tagasipööramine materjali algsel kasutuse kinnitusel sisalduvale kogusele ja summale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelik näitaja materjali algsel kasutuse kinnitusel sisalduvale kogusele ja summale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Materjali tehingu arveldamine, mida on koguse vähendamiseks muudetud.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tagasipööramine algsel aja kinnitusel sisalduvale kogusele ja summale.
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
Materjali tehingu arveldamine, mida on koguse suurendamiseks muudetud.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müügi tagasipööramine materjali algsel kasutuse kinnitusel sisalduvale kogusele ja summale.
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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
