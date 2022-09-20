---
title: Projekti prognooside ja tegelike kulude määra määramine
description: Selles artiklis antakse teavet selle kohta, kuidas määratakse projekti prognooside ja tegelike kulude määrad.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475226"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Projekti prognooside ja tegelike kulude määra määramine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations prognooside ja tegelike näitajate kulumäärade määramiseks kasutab süsteem esmalt kuupäeva ja valuutat sissetulevas prognoosis või tegelikus kontekstis, et määrata kindlaks omahinnakiri. Konkreetselt tegelikus kontekstis kasutab **süsteem tehingu kuupäeva** välja, et määrata, milline hinnakiri on rakendatav. **Sissetuleva või tegeliku hinnangu tehingukuupäeva** väärtust võrreldakse hinnakirjas olevate **väärtustega Efektiivne algus (sõltumatu ajavöönd)** ja **Efektiivne lõpp (sõltumatu ajavöönd**). Pärast omahinnaloendi määramist määrab süsteem kulumäära. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Kulumäärade määramine aja hinnangulises ja tegelikus kontekstis

Aja **hinnanguline kontekst** viitab:

- Hinnapakkumise rea üksikasjad aja **kohta**.
- Lepingu rea üksikasjad aja **kohta**.
- Projekti ressursside määramised.

Aja **tegelik kontekst** viitab:

- Sissekande ja paranduse töölehe read aja **jaoks**.
- Tööleheread, mis luuakse ajakirje edastamisel.

Pärast omahinnaloendi määramist teeb süsteem vaikekulumäära sisestamiseks järgmised toimingud.

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

Pärast omahinnaloendi määramist teeb süsteem vaikekulumäära sisestamiseks järgmised toimingud.

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

Pärast omahinnaloendi määramist teeb süsteem vaikekulumäära sisestamiseks järgmised toimingud.

1. Süsteem kasutab väljade **Toode** ja **Ühik** kombinatsiooni materjali **hinnangus või tegelikus kontekstis** hinnakirja kaubaridade suhtes hinnakirjas.
1. Kui süsteem leiab hinnakirja kaubarea, millel on toote **ja** ühiku **kombinatsiooni kulumäär**, kasutatakse seda kulumäära vaikekulumäärana.
1. Kui süsteem ei **vasta** toote ja **ühiku** väärtustele, on ühikukuluks **vaikimisi määratud 0** (null).
1. Kui süsteem suudab hinnangus või tegelikus kontekstis leida vastava hinnakirja kaubarea, kuid hinnastamismeetod on midagi muud kui **valuutasumma**, on ühikukuluks vaikimisi seatud **0**. Selline käitumine ilmneb seetõttu, et Project Operations toetab ainult **valuutasumma** hinnastamise meetodit materjalide puhul, mida projektis kasutatakse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
