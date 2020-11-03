---
title: Projekti prognooside importimine projektipõhise hinnapakkumise reale
description: See teema sisaldab teavet, kuidas importida projekti prognoose hinnapakkumise reale.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 224c2265cfcc38dfc2ed74664d38c095feefaca7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074858"
---
# <a name="importing-estimates-for-a-project-to-a-project-based-quote-line"></a>Projekti prognooside importimine projektipõhise hinnapakkumise reale

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Kui projekt luuakse müügieelses etapis, saate valida, kas importida projekti finantskalkulatsioonid projektipõhise hinnapakkumise reale.

1. Veenduge, et projektipõhisel hinnapakkumise real oleks projekti teave väljal **Projekt**.
2. Valige vahekaardil **Hinnapakkumise rea üksikasjad** suvand **Impordi projekti prognoosidest**.
3. Avaneval dialoogi lehel valige üks järgmistest kokkuvõtte valikutest.

  - **Kande klass**
  - **Kategooria**
  - **Roll** 
  - **Projekti ülesanne**

Olenevalt teie valikust kopeeritakse üle projekti prognoos kõigi selle hinnapakkumise rea kannete klasside kohta. Kaasatud tehinguklasside kontrollimiseks valige projektipõhisel hinnapakkumise real vahekaart **Üldine** ja kontrollige suvandite **Kaasa aeg** , **Kaasa kulu** ja **Kaasa tasud** väärtuseid.  Kui soovite kontrollida, millised tööülesanded on kaasatud, valige hinnapakkumise rea vahekaart **Arveldatavad tööülesanded**.

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
