---
title: Prognoosi importimine projektipõhisele lepingureale – liht
description: See teema sisaldab teavet, kuidas importida projekti finantsprognoose lepingureale.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 52abaa785b50b914e7813aaf4660504ee99129d6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582061"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Prognoosi importimine projektipõhisele lepingureale – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Dynamics 365 Project Operationsis saate importida prognoosid projektist projektipõhisele lepingureale.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]