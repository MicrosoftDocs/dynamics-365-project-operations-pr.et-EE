---
title: Parandatud arved – liht
description: Selles teemas antakse teavet Project Operationsis parandatud arvete kohta.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274228"
---
# <a name="corrected-invoices---lite"></a>Parandatud arved – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Kinnitatud projekti arvet saab parandada muudatuste või krediidi töötlemiseks, pidades läbirääkimisi kliendi ja projektijuhiga.

Kinnitatud arve redigeerimiseks avage kinnitatud arve ja valige suvand **Paranda seda arvet**. 

> [!NOTE]
> See valik pole saadaval, kui projekti arve pole kinnitatud.

Uus arve mustand luuakse kinnitatud arvelt. Kõik varem kinnitatud arve arverea üksikasjad kopeeritakse uude mustandisse. Järgnevalt on toodud mõned olulised punktid, et saaksite aru uue parandatud arve rea üksikasjadest.

- Kõigi koguste väärtused muudetakse nulliks. Rakendus eeldab, et kõik arveldatud üksused krediteeritakse täielikult. Vajaduse korral saate neid koguseid käsitsi värskendada, et kajastada arveldatud kogust, mitte krediteeritud kogust. Teie sisestatud koguse põhjal arvutab rakendus krediteeritud koguse. See summa kajastub tegelikes näitajates, mis luuakse parandatud arve kinnitamisel. Kui muudate maksusummat, peate sisestama õige maksusumma, mitte maksusumma, mis krediteeritakse.
- Varem kinnitatud tootepõhiseid lepinguridu ei kopeerita üle. Tootepõhisel projekti arvel ei toetata paranduste töötlemist.
- Vahe-eesmärgi parandused töödeldakse alati täieliku krediidina.
- Honorari või ettemakse summasid saab parandada juhul, kui kliendile esitati arve vale summaga.
- Kui varem kinnitatud arvega vastavusse viimiseks on kasutatud valet summat, siis saate parandada honoraride ja ettemaksete vastavusseviimist.

> [!IMPORTANT]
> Arve rea üksikasjadel, mis on parandustes muude juba arveldatud tasude jaoks, on välja **Parandus** väärtuseks **Jah**. Arvetel, millel on parandatud arve rea üksikasju, on välja **Parandustega** väärtuseks samuti **Jah**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Parandatud arve kinnitamisel loodud tegelikud näitajad.

Allpool on tegelikud näitajad, mis on loodud rakendusega, mis on seotud parandatud arve mustandis tehtud toimingutega, enne kinnituse kinnitamist.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Kinnitage arveldatud ettemakse või honorari parandamine.<strong></strong>
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
Arveldatud müügi tühistamise tegelik näitaja luuakse honorari või ettemakse summa jaoks, et algne arveldatud müük tühistada.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Honorari või ettemakse parandatud arve real luuakse parandatud summa jaoks uus arveldatud müügi tegelik näitaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Honorari või ettemakse parandatud arve rea negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse vastavusseviimiseks.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Kinnitus varem vastavusse viidud honorari või ettemakse parandamise kohta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Arveldamata müük, mis tühistati vastavusseviimiseks loodud honorari või ettemakse jaoks. See summa on positiivne ja selle eesmärk on tühistada negatiivne summa, mis loodi eelmise vastavusseviimise ajal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Arveldatud müügi tegelik näitaja tühistatakse eelmise arve summa jaoks.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uus arveldatud müügi tegelik näitaja parandatud honorari summa jaoks, mis rakendatakse parandatud arvele.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Parandatud järelejäänud honorari või ettemakse negatiivse summa arveldamata müügi tegelik näitaja, mida kasutatakse tulevaste arvete vastavusseviimiseks.
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
Projekti lepingurea vahe-eesmärgi arve või arveldamise olek on muudetud olekuks **Arveldamiseks valmis**.
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
Mittetoetatud </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Varem arveldatud tootepõhise lepingurea krediit ja parandused.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Mittetoetatud </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]