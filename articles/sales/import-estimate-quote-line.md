---
title: Projekti prognooside importimine projektpõhise hinnapakkumise reale
description: See teema sisaldab teavet, kuidas importida projekti prognoose hinnapakkumise reale.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908051"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projekti prognooside importimine projektpõhise hinnapakkumise reale

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Kui projekt luuakse müügieelses etapis, saate valida, kas importida projekti finantskalkulatsioonid projektipõhise hinnapakkumise reale.

1. Veenduge, et projektipõhisel hinnapakkumise real oleks projekti teave väljal **Projekt**.
2. Valige vahekaardil **Hinnapakkumise rea üksikasjad** suvand **Impordi projekti prognoosidest**.
3. Avaneval dialoogi lehel valige üks järgmistest kokkuvõtte valikutest.

  - **Kande klass**
  - **Kategooria**
  - **Roll** 
  - **Projekti ülesanne**

Olenevalt teie valikust kopeeritakse üle projekti prognoos kõigi selle hinnapakkumise rea kannete klasside kohta. Kaasatud tehinguklasside kontrollimiseks valige projektipõhisel hinnapakkumise real vahekaart **Üldine** ja kontrollige suvandite **Kaasa aeg**, **Kaasa kulu** ja **Kaasa tasud** väärtuseid.

Prognooside importimisel määrab süsteem vaikimisi hinna, mis põhineb hinnapakkumisele lisatud projekti hinnakirjal ja projektipõhise hinnapakkumise real seadistatud arvelduse tüübil. Kui projektipõhise hinnapakkumise rea rolliks või kategooriaks on määratud, et arvet ei esitata, seatakse imporditud prognoosi rida mittearveldatavaks ja seda ei lisata hinnapakkumise rea hinnapakkumise väärtusele.

Kui hinnapakkumise real on rea üksikasjad, siis hinnapakkumise rea väljad **Hinnapakkumise väärtus** ja **Hinnanguline maks** summeeritakse ja neid ei saa redigeerida.

Kui valitud on mitu summerrimise valikut, proovib summeerimine liita kokku kõik valitud suvandid. See tähendab, et imporditud hinnapakkumise ridade väljund on suurem kui juhul, kui valisite ainult ühe summeerimise suvandi.

Näiteks juhul, kui projektil on kulude jaoks järgmised kalkulatsiooni read.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| Ülesanne A | Lennupiletid | 1.10.2020 | 4 | 400 | 1600 |
| Ülesanne B | Hotell | 1.10.2020 | 4 | 200 | 800 |
| Ülesanne C | Hotell | 1.11.2020 | 2 | 200 | 400 |

Kui kasutaja valib summeerimise tehingu klassi põhjal, siis imporditakse järgmine teave.

| Toiming | Kategooria | Kuupäev | Kogus | Ühiku hind | Summa |
| --- | --- | --- | --- | --- | --- |
| | | 1.10.2020 | 3.34 | 840 | 2800 |

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