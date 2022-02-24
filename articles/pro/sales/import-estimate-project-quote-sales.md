---
title: Projekti prognooside importimine projektipõhise hinapakkumise reale – liht
description: See teema sisaldab teavet, kuidas importida projekti prognoose hinnapakkumise reale.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0aedaa2ec77bb54031fccd0db2872e0aa5fea5e0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858243"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projekti prognooside importimine projektipõhise hinapakkumise reale 

_**Kehtib järgmistele:** lihtjuurutamine – tehing näidisarveldusele, Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks_

Kui projekt luuakse müügieelses etapis, saate valida, kas importida projekti finantskalkulatsioonid projektipõhise hinnapakkumise reale.

1. Veenduge, et projektipõhisel hinnapakkumise real oleks projekti teave väljal **Projekt**.
2. Valige vahekaardil **Hinnapakkumise rea üksikasjad** suvand **Impordi projekti prognoosidest**.
3. Avaneval dialoogi lehel valige üks järgmistest kokkuvõtte valikutest.

  - **Kande klass**
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
