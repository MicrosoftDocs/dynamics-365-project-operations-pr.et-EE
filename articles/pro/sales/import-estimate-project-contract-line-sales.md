---
title: Prognoosi importimine projektipõhisele lepingureale – liht
description: See teema sisaldab teavet, kuidas importida projekti finantsprognoose lepingureale.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177461"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Prognoosi importimine projektipõhisele lepingureale – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations saate projekti prognoose projektipõhisele lepingureale importida.

1. Kontrollige, kas projektipõhise lepingurea väli **Projekt** on täidetud.
2. Valige andmeruudustiku vahekaardil **Lepingurea üksikasjad** suvand **Impordi projekti prognoosidest**. Avaneb dialoogileht, kus on kokkuvõtlikud suvandid. Saadaolevad kokkuvõtlikud suvandid on **Tehingu klass**, **Kategooria**, **Roll** ja **Projekti tööülesanne**.
3. Olenevalt kokkuvõtte valikust kopeeritakse üle projekti prognoos kõigi selle lepingurea tehinguklasside ja tööülesannete kohta. Kaasatud tehinguklasside kontrollimiseks valige projektipõhisel lepingureal vahekaart **Üldine** ja kontrollige suvandite **Kaasa aeg**, **Kaasa kulu** ja **Kaasa tasud** väärtuseid. 
4. Kui soovite vaadata, millised tööülesanded on kaasatud, valige lepingurea vahekaart **Arveldatavad tööülesanded**. Põhinedes seotud tööülesannetele, mille välja **Kaasatud tehinguklassid** väärtuseks on määratud **Jah**, imporditakse kõik nende tööülesannete ja tehinguklassi kombinatsioonide prognoosid lepingureale.

Prognooside importimisel määrab süsteem vaikimisi hinna, mis põhineb lepingule lisatud projekti hinnakirjadel ja lepingreal seadistatud arvelduse tüübil. Kui lepingurea tööülesandeks, rolliks või kategooriaks on määratud, et arvet ei esitata, seatakse imporditud prognoosi rida mittearveldatavaks ja seda ei lisata lepingurea lepingu väärtusele.

Kui lepingureal on rea üksikasjad, siis lepingurea väljad **Lepingu väärtus** ja **Prognoositav maks** summeeritakse ja neid ei saa redigeerida.

Kui valitud on mitu kokkuvõtlikku valikut, proovib süsteem liita kokku kõik valitud suvandid. Kokkuvõtte tulemuseks on rohkem imporditud lepinguridu kui ainult ühe kokkuvõtte suvandi valimisel.

Näiteks juhul, kui projektil on kulude jaoks järgmised kalkulatsiooni read.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| Ülesanne B | Hotell | 1.10.2020 | 4 | 200 | 800 |
| Ülesanne C | Hotell | 1.11.2020 | 2 | 200 | 400 |

Kui kasutaja valib kokkuvõtte suvandi **Tehinguklass** põhjal, siis imporditakse järgmine teave.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1.10.2020 | 3.34 | 840 | 2800 |

Kui kasutaja valib kokkuvõtte suvandite **Tehinguklass** ja **Kategooria** põhjal, siis imporditakse järgmine teave.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;| Hotell | 1.10.2020 | 6 | 200 | 1200 |

Kui kasutaja valib kokkuvõtte suvandi **Tehinguklass**, **Kategooria** ja **Lehe tööülesanne** põhjal, siis imporditakse järgmine. Pange tähele, et see tulemus on sama, mis on projektis.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| Ülesanne B | Hotell | 1.10.2020 | 4 | 200 | 800 |
| Ülesanne C | Hotell | 1.11.2020 | 2 | 200 | 400 |
