---
title: Prognooside importimine projektist projekti hinnapakkumise reale
description: Sellest artiklist leiate teavet selle kohta, kuidas importida prognoose projektist projekti hinnapakkumise reale.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824481"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Prognooside importimine projektist projekti hinnapakkumise reale 

_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_

Kui projekt luuakse müügieelses etapis, saate valida, kas importida projekti finantskalkulatsioonid projektipõhise hinnapakkumise reale.

1. Veenduge, et projektipõhisel hinnapakkumise real oleks projekti teave väljal **Projekt**.
2. Valige vahekaardil **Hinnapakkumise rea üksikasjad** suvand **Impordi projekti prognoosidest**.
3. Avaneval dialoogi lehel valige üks järgmistest kokkuvõtte valikutest.

  - **Tehingu klass**
  - **Kategooria**
  - **Roll** 
  - **Projekti ülesanne**

Olenevalt teie valikust kopeeritakse üle projekti prognoos kõigi selle hinnapakkumise rea kannete klasside kohta. Kontrollimaks, millised tehinguklassid on kaasatud, valige projektipõhise hinnapakkumise real vahekaart **Üldine** ja kontrollige väärtusi **Kaasa aeg**, **Kaasa kulud**, **Kaasa materjalid** ja **Kaasa tasud**.  Kui soovite kontrollida, millised tööülesanded on kaasatud, valige hinnapakkumise rea vahekaart **Arveldatavad tööülesanded**.

Olenevalt seotud ülesannetest ja kaasatud tehinguklassidest imporditakse nende tööülesannete ja tehinguklassi kombinatsioonide prognoosid hinnapakkumise reale.

Prognooside importimisel määrab süsteem vaikimisi hinna, mis põhineb hinnapakkumisele lisatud projekti hinnakirjal ja projektipõhise hinnapakkumise real seadistatud arvelduse tüübil. Kui projektipõhise hinnapakkumise rea tööülesandeks, rolliks või kategooriaks on määratud, et arvet ei esitata, seatakse imporditud prognoosi rida mittearveldatavaks ja seda ei lisata hinnapakkumise rea hinnapakkumise väärtusele.

Kui hinnapakkumise real on rea üksikasjad, siis hinnapakkumise rea väljad **Hinnapakkumise väärtus** ja **Hinnanguline maks** summeeritakse ja neid ei saa redigeerida.

Kui valitud on mitu kokkuvõtlikku valikut, proovib süsteem liita kokku kõik valitud suvandid. Tulemuseks on, et imporditud hinnapakkumise ridade väljund on suurem kui juhul, kui valisite ainult ühe summeerimise suvandi.

Näiteks juhul, kui projektil on kulude jaoks järgmised kalkulatsiooni read.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| Ülesanne B | Hotell | 1.10.2020 | 4 | 200 | 800 |
| Ülesanne C | Hotell | 1.11.2020 | 2 | 200 | 400 |

Kui kasutaja valib summeerimise tehingu klassi põhjal, siis imporditakse järgmine teave.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
|||1.10.2020 | 3.34 | 840 | 2800 |

Kui kasutaja valib summeerimise tehingu klassi ja kategooria põhjal, siis imporditakse järgmine teave.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| | Hotell | 1.10.2020 | 6 | 200 | 1200 |

Kui kasutaja valib summeerimise tehingu klassi, kategooria ja lehe ülesande põhjal, siis imporditakse järgmine teave. Pange tähele, et see tulemus on sama, mis oli projektis.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| Ülesanne B | Hotell | 1.10.2020 | 4 | 200 | 800 |
| Ülesanne C | Hotell | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
