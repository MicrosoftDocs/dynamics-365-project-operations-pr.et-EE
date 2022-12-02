---
title: Määrake projekti prognooside ja tegelike kulude määrad
description: See artikkel sisaldab teavet projekti prognooside ja tegelike näitajate kulumäärade määramise kohta.
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
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Määrake projekti prognooside ja tegelike kulude määrad

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Prognooside ja tegelike kulumäärade määramiseks Microsoft Dynamics 365 Project Operationsi prognoositud ja hindade tegelike näitajate omahindade määramiseks kasutab süsteem hinnakirja määramiseks esmalt kuupäeva ja valuutat sissetulevas prognoosis või tegelikus kontekstis. Tegelikus kontekstis kasutab süsteem kohaldatava hinnakirja määramiseks välja **Tehingu kuupäev**. Sissetuleva prognoositud või tegeliku väärtuse **Tehingu kuupäev** võrreldakse hinnakirja **Tõhus algus (ajavööndist sõltumatu)** ja **Tõhus lõpp (ajavööndist sõltumatu)** väärtustega. Pärast omahinnakirja kindlaksmääramist määrab süsteem kulumäära. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Kulumäärade määramine aja prognoositavas ja tegelikus kontekstis

Prognoositav kontekst **Aeg** viitab:

- Hinnapakkumise rea üksikasjad **Aja** jaoks.
- Lepingurea üksikasjad **Aja** jaoks.
- Ressursiülesanded projektis.

Tegelik kontekst **Aja** jaoks viitab:

- Kirje- ja parandustöölehele kandmise read **Aja** jaoks.
- Töölehe read, mis luuakse aja sissekande edastamisel.

Pärast omahinnakirja kindlaksmääramist viib süsteem vaikekulumäära sisestamiseks läbi järgmised toimingud.

1. Süsteem sobitab väljade **Roll** ja **Ressursiühik** kombinatsiooni prognoositud või tegelikus kontekstis **Aeg** ja hinnakirja rollide hinnaridadega. Selle vastenduse puhul eeldatakse, et kasutate tööjõukulu jaoks standardseid hinnakujunduse dimensioone. Kui olete süsteemi konfigureerinud nii, et see sobiks väljadele, mis ei ole **Roll** ja **Ressursiühik**, või lisaks sellele, kasutatakse sobiva rollihinna rea toomiseks teistsugust kombinatsiooni.
1. Kui süsteem leiab rollihinnarea, millel on kulumäär kombinatsioonide **Roll** ja **Ressursiühik** jaoks, kasutatakse seda kulumäära vaikekulumäärana.
1. Kui süsteem ei suuda väärtusi **Roll** ja **Ressursiühik** vastendada, hangib see rolli hinnaread, millel on väljal **Roll** vastavad väärtused, kuid väljal **Ressursiühik** nullväärtused. Kui süsteemil on sobiv rollihinna kirje, kasutatakse selle kirje kulumäära vaikekulumäärana.

> [!NOTE]
> Kui konfigureerite väljadele **Roll** ja **Ressursiühik** teistsuguse tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub eelnev käitumine vastavalt. Süsteem hangib rolli hinnakirjed, mille väärtused vastavad prioriteetsuse järjekorras igale hinnadimensiooni väärtusele. Nende dimensioonide nullväärtustega read on viimased.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Kulumäärade määramine kulu tegelike ja prognoositavatel ridadel

Prognoositav kontekst **Kulu** viitab:

- Hinnapakkumise rea üksikasjad **Kulu** jaoks.
- Lepingurea üksikasjad **Kulu** jaoks.
- Projekti kuluprognoosid.

Tegelik kontekst **Kulu** viitab:

- Kirje- ja parandustöölehele kandmise read **Kulu** jaoks.
- Töölehele kandmised, mis luuakse aja sissekande edastamisel.

Pärast omahinnakirja kindlaksmääramist viib süsteem vaikekulumäära sisestamiseks läbi järgmised toimingud.

1. Süsteem võrdleb **Kategooria** ja **Ühiku** väljade kombinatsiooni prognoositavas või tegelikus kontekstis **Kulu** ja hinnakirjas olevate kategooriate hinnaridade vahel.
1. Kui süsteem leiab kategooria hinnarea, millel on kulumäär kombinatsiooni **Kategooria** ja **Ühik** jaoks, kasutatakse seda kulumäära vaikimisi kulumäärana.
1. Kui süsteem ei suuda sobitada väärtusi **Kategooria** ja **Ühik** määratakse hinnaks vaikimisi **0** (null).
1. Kui prognoositavas kontekstis leiab süsteem sobiva kategooria hinnarea, kuid hinnakujundusmeetod on midagi muud kui **Hind ühiku kohta**, määratakse kulumääraks vaikimisi **0** (null).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Materjalide tegelike ja prognoositavate kulumäärade määramine

Prognoositav kontekst **Materjal** viitab:

- Hinnapakkumise rea üksikasjad **Materjali** jaoks.
- Lepingurea üksikasjad **Materjali** jaoks.
- Projekti materjali prognoosid.

Tegelik **Materjali** kontekst viitab:

- Kirje- ja parandustöölehele kandmise read **Materjali** jaoks.
- Töölehele kandmised, mis luuakse materjali kasutamise logi edastamisel.

Pärast omahinnakirja kindlaksmääramist viib süsteem vaikekulumäära sisestamiseks läbi järgmised toimingud.

1. Süsteem kasutab **Toode** ja **Ühiku** väljade kombinatsiooni prognoositavas või tegelikus kontekstis **Materjali** hinnakirjas olevate hinnakirjaridade suhtes.
1. Kui süsteem leiab hinnakirja kirje rea, millel on kulumäär kombinatsiooni **Toode** ja **Ühik** jaoks, kasutatakse seda kulumäära vaikimisi kulumäära.
1. Kui süsteem ei suuda sobitada väärtusi **Toode** ja **Ühik**, määratakse ühiku maksumuseks vaikimisi **0** (null).
1. Kui süsteem leiab prognoositava või tegeliku konteksti puhul sobiva hinnakirja kirje rea, kuid hinnakujundusmeetodiks on midagi muud kui **Valuutasumma**, määratakse ühikuhinnaks vaikimisi **0**. Selline käitumine tuleneb sellest, et Project Operations toetab projektis kasutatavate materjalide puhul ainult **Valuutasumma** hinnakujundusmeetodit.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
