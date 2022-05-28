---
title: Projekti näidisarve kinnitamine
description: See teema sisaldab teavet Project Operationsi projekti näidisarvete kinnitamise kohta.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 276f54936ad9fd72fdc7e85196b43463572e6d3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600277"
---
# <a name="confirm-a-proforma-project-invoice"></a>Projekti näidisarve kinnitamine 

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


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
