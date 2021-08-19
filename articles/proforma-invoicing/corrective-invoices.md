---
title: Projektipõhised parandusarved
description: See teema sisaldab teavet selle kohta, kuidas luua ja kinnitada Project Operationsis projektipõhiseid parandusarveid.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997151"
---
# <a name="corrective-project-based-invoices"></a>Projektipõhised parandusarved

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kinnitatud projekti arvet saab parandada muudatuste või krediidi töötlemiseks, pidades läbirääkimisi kliendi ja projektijuhiga.

Kinnitatud arve redigeerimiseks avage kinnitatud arve ja valige suvand **Paranda seda arvet**. 

> [!NOTE]
> See valik pole saadaval, kui projekti arve ei ole kinnitatud või kui projektipõhisel arvel avansid või honorarid või avansside või honoraride vastavusseviimised.

Uus arve mustand luuakse kinnitatud arvelt. Kõik varem kinnitatud arve arverea üksikasjad kopeeritakse uude mustandisse. Järgnevalt on toodud mõned olulised punktid, et saaksite aru uue parandatud arve rea üksikasjadest.

- Kõigi koguste väärtused muudetakse nulliks. Dynamics 365 Project Operations eeldab, et kõik arveldatud üksused on täielikult krediteeritud. Vajaduse korral saate neid koguseid käsitsi värskendada, et kajastada arveldatud kogust, mitte krediteeritud kogust. Teie sisestatud koguse põhjal arvutab rakendus krediteeritud koguse. See summa kajastub tegelikes näitajates, mis luuakse parandatud arve kinnitamisel. Kui muudate maksusummat, peate sisestama õige maksusumma, mitte maksusumma, mis krediteeritakse.
- Vahe-eesmärgi parandused töödeldakse alati täieliku krediidina.


> [!IMPORTANT]
> Arverea üksikasjadel, mis on muude juba arveldatud kulude parandused, on välja **Parandus** väärtuseks seatud **Jah**. Arvetel, millel on parandatud arve rea üksikasjad, on välja **Sisaldab parandusi** väärtuseks seatud **Jah**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Parandusarve kinnitamisel loodavad tegelikud näitajad

Järgmises tabelis on loetletud tegelikud andmed, mis luuakse, kui parandusarve on kinnitatud.

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
Varem arveldatud ajatehingu täieliku krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uue arveldamata müügi tegeliku näitaja tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Osalise krediidi arveldamine ajatehinguga.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse aja jaoks mõeldud arverea üksikasjad tundide ja arveldatud summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav muudetud arverea üksikasjade tundide ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud tundide ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Varem arveldatud kulutehingu täieliku krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik näitaja algse kulu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Varem arveldatud kulutehingu osalise krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse kulu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Varem arveldatud materjali kande täieliku krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Esitatud arvega müügi tagasipööramine materjali algsel arverea üksikasjal sisalduvale kogusele ja summale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Esitatud uus arveldamata müügi tegelik väärtus materjali algsel arverea üksikasjal sisalduvale kogusele ja summale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Materjali tehingu osalise krediidi eest arve esitamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Esitatud arvega müügi tagasipööramine materjali algse arverea üksikasjal sisalduvale arveldatud kogusele ja summale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mille eest esitatakse arve muudetud arve rea üksikasjades oleva koguse ja summa eest, selle ümberpööramine ja sellega võrdväärse arveldatud müügi tegelik summa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik näitaja, mis on arveldatud järelejäänud koguste ja summade eest pärast seda, kui parandatud arvud on arve rea üksikasjades lahutatud.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Varem arveldatud tasutehingu täieliku krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik näitaja algse tasu jaoks mõeldud arverea üksikasjad koguste ja summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Varem arveldatud tasutehingu osalise krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse tasu jaoks mõeldud arverea üksikasjad koguste ja arveldatud summa puhul.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldamata müügi tegelik väärtus, mis on arveldatav redigeeritud parandatud arverea üksikasjade koduste ja summa eest, selle tühistamine ja samaväärne arveldatud müügi tegelik väärtus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Varem arveldatud vahe-eesmärgi täieliku krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tühistamine algse vahe-eesmärgi jaoks mõeldud arverea üksikasjad summa puhul.
                </p>
                <p>
Vahe-etapi arve olek värskendatakse valikult <b>Kliendi arve on sisestatud</b> valikule <b>Arveldamiseks valmis</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Varem arveldatud vahe-eesmärgi osalise krediidi arveldamine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Seda stsenaariumi ei toetata.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
