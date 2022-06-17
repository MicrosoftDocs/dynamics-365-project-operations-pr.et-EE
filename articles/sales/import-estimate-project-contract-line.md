---
title: Prognoosi importimine projektipõhisele lepingureale
description: Selles artiklis antakse teavet selle kohta, kuidas importida hinnanguid projektilt lepingureale.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4a298cbcb8d13447c0f6e264d2aa85ad7ed43bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915087"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Prognoosi importimine projektipõhisele lepingureale

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Dynamics 365 Project Operationsis saate importida prognoosid projektist projektipõhisele lepingureale.

1. Kontrollige, kas projektipõhise lepingurea väli **Projekt** on täidetud.
2. Valige andmeruudustiku vahekaardil **Lepingurea üksikasjad** suvand **Impordi projekti prognoosidest**. Avaneb dialoogileht, kus on kokkuvõtlikud suvandid. Saadaolevad kokkuvõtlikud suvandid on **Tehingu klass**, **Kategooria**, **Roll** ja **Projekti tööülesanne**. Olenevalt kokkuvõtte valikust kopeeritakse üle projekti prognoos kõigi selle lepingurea tehinguklasside kohta. 
3. Kaasatud tehinguklasside kontrollimiseks valige lepingureal vahekaart **Üldine** ja kontrollige suvandite **Kaasa aeg**, **Kaasa kulu** ja **Kaasa tasud** väärtuseid.

Prognooside importimisel määrab rakendus vaikimisi hinna, mis põhineb lepingule lisatud projekti hinnakirjadel ja lepingreal seadistatud arvelduse tüübil. Kui lepingurea rolliks või kategooriaks on määratud, et arvet ei esitata, seatakse selle rolli või kategooria imporditud prognoosi rida mittearveldatavaks ja seda ei lisata lepingurea lepingu väärtusele.

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
| &nbsp;  | &nbsp;  | 1.10.2020 | 3.34 | 840 | 2800 |

Kui kasutaja valib kokkuvõtte suvandite **Tehinguklass** ja **Kategooria** põhjal, siis imporditakse järgmine teave.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotell | 1.10.2020 | 6 | 200 | 1200 |

Kui kasutaja valib kokkuvõtte suvandi **Tehinguklass**, **Kategooria** ja **Lehe tööülesanne** põhjal, siis imporditakse järgmine. Pange tähele, et see tulemus on sama, mis oli projektis.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| Ülesanne B | Hotell | 1.10.2020 | 4 | 200 | 800 |
| Ülesanne C | Hotell | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]