---
title: Projekti prognooside importimine projekti hinnapakkumise reale
description: Selles artiklis antakse teavet hinnangute importimise kohta projekti hinnapakkumise reale.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc5b6279a2123604291da35c9da2bf63dbe475b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915041"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Projekti prognooside importimine projekti hinnapakkumise reale

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
