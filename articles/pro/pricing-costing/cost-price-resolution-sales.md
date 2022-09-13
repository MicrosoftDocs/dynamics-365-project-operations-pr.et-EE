---
title: Projekti prognooside ja tegelike kulude määra määramine
description: Selles artiklis antakse teavet selle kohta, kuidas määratakse projekti prognooside ja tegelike kulude määrad.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410144"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Projekti prognooside ja tegelike kulude määra määramine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Omahinnaloendi ja kulumäärade määramiseks prognoosis ja tegelikes kontekstides kasutab süsteem seotud projekti väljadel Kuupäev, Valuuta ja Lepinguühik **olevat teavet**.**·** **·**

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Kulumäärade määramine aja hinnangulises ja tegelikus kontekstis

Aja **hinnanguline kontekst** viitab:

- Hinnapakkumise rea üksikasjad aja **kohta**.
- Lepingu rea üksikasjad aja **kohta**.
- Projekti ressursside määramised.

Aja **tegelik kontekst** viitab:

- Sissekande ja paranduse töölehe read aja **jaoks**.
- Tööleheread, mis luuakse ajakirje edastamisel.

Pärast omahinnaloendi määramist täidab süsteem vaikekulumäära sisestamiseks järgmised toimingud.

1. Süsteem sobitab väljade **Roll** ja **Ressursiüksus** kombinatsiooni aja hinnangus või tegelikus kontekstis **hinnakirjas** olevate rolli hinnaridade suhtes. See vaste eeldab, et kasutate tööjõukulude jaoks standardseid hinnadimensioone. Kui olete konfigureerinud süsteemi vastendama muid välju peale rolli **- ja** ressursiüksuse **või lisaks** sellele, kasutatakse vastava rolli hinnarea toomiseks teist kombinatsiooni.
1. Kui süsteem leiab rolli hinnarea, millel on rolli ja **ressursiüksuse** kombinatsiooni **kulumäär**, kasutatakse seda kulumäära vaikekulumäärana.
1. Kui süsteem ei vasta rolli ja ressursiüksuse **väärtustele**, toob see rolli hinnaread, millel on vastavad väärtused väljale **Roll**, kuid tühised väärtused väljale **Ressursiüksus**.**·** Kui süsteemil on vastav rolli hinnakirje, kasutatakse selle kirje kulumäära vaikekulumäärana.

> [!NOTE]
> Kui konfigureerite väljade **Rolli** - ja **ressursiüksus** erineva prioriseerimise või kui teil on muid kõrgema prioriteediga dimensioone, muutub eelnev käitumine vastavalt. Süsteem toob rolli hinnakirjed, mille väärtused vastavad igale hinnadimensiooni väärtusele prioriteedi järjekorras. Read, millel on nende dimensioonide jaoks nullväärtused, jäävad viimaseks.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kulumäärade määramine tegelikel ja hinnangulisel kuluridadel

Hinnanguline kulukontekst **viitab**:

- Hinnapakkumise rea üksikasjad kulu **kohta**.
- Lepingu rea üksikasjad kulu **jaoks**.
- Projekti kuluprognoosid.

Kulu **tegelik kontekst** viitab järgmisele:

- Sissekande ja paranduse töölehe read kulu **jaoks**.
- Töölehe read, mis luuakse kulukirje esitamisel.

Pärast omahinnaloendi määramist täidab süsteem vaikekulumäära sisestamiseks järgmised toimingud.

1. Süsteem sobitab väljade **Kategooria** ja **Ühik** kombinatsiooni kulu hinnangus või tegelikus kontekstis **hinnakirja** kategooria hinnaridade suhtes.
1. Kui süsteem leiab kategooria hinnarea, millel on kategooria **ja** ühiku **kombinatsiooni kulumäär**, kasutatakse seda kulumäära vaikekulumäärana.
1. Kui süsteem ei **vasta kategooria** ja **ühiku** väärtustele, määratakse hinnaks **vaikimisi 0** (null).
1. Kui süsteem suudab hindamise kontekstis leida vastava kategooria hinnarea, kuid hinnakujundusmeetod on midagi muud kui **ühiku** hind, määratakse kulumääraks **vaikimisi 0** (null).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Kulumäärade määramine materjali tegelikel ja hinnangulistel ridadel

Materjali **hinnanguline kontekst** viitab:

- Hinnapakkumise rea üksikasjad materjali **jaoks**.
- Lepingu rea üksikasjad materjali **jaoks**.
- Projekti materiaalsed hinnangud.

Materjali **tegelik kontekst** viitab:

- Sissekande ja paranduse töölehe read materjali **jaoks**.
- Tööleheread, mis luuakse materjali kasutamise logi esitamisel.

Pärast omahinnaloendi määramist täidab süsteem vaikekulumäära sisestamiseks järgmised toimingud.

1. Süsteem kasutab väljade **Toode** ja **Ühik** kombinatsiooni materjali **hinnangus või tegelikus kontekstis** hinnakirja kaubaridade suhtes hinnakirjas.
1. Kui süsteem leiab hinnakirja kaubarea, millel on toote **ja** ühiku **kombinatsiooni kulumäär**, kasutatakse seda kulumäära vaikekulumäärana.
1. Kui süsteem ei **vasta** toote ja **ühiku** väärtustele, on ühikukuluks **vaikimisi määratud 0** (null).
1. Kui süsteem suudab hinnangus või tegelikus kontekstis leida vastava hinnakirja kaubarea, kuid hinnastamismeetod on midagi muud kui **valuutasumma**, on ühikukuluks vaikimisi seatud **0**. Selline käitumine ilmneb seetõttu, et Project Operations toetab ainult **valuutasumma** hinnastamise meetodit materjalide puhul, mida projektis kasutatakse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
