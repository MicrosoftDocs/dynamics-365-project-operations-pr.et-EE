---
title: Prognooside importimine projektist selle lepingureale
description: See artikkel annab teavet, kuidas importida projekti finantsprognoose lepingureale.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824669"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Prognooside importimine projektist selle lepingureale

_**Kehtib:** Lite’i juurutamine – kokkulepe proforma arveldusega, projektitoimingud ressursi-/laovarudeta stsenaariumide_ jaoks_

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
