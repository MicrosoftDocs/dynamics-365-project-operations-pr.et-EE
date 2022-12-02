---
title: Määrake projektipõhiste hinnangute ja tegelike kulude määrad
description: See artikkel sisaldab teavet projektipõhiste hinnangute ja tegelike kulumäärade määramise kohta.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475268"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Määrake projektipõhiste hinnangute ja tegelike kulude määrad

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Microsoft Dynamics 365 Project Operationsi prognoositud ja hindade tegelike näitajate omahindade määramiseks kasutab süsteem müügihinnakirja määramiseks esmalt kuupäeva ja valuutat sissetulevas hinnangus või tegelikus kontekstis. Tegelikus kontekstis kasutab süsteem kohaldatava hinnakirja määramiseks välja **Tehingu kuupäev**. Sissetuleva prognoositud või tegeliku väärtuse **Tehingu kuupäev** võrreldakse hinnakirja **Tõhus algus (ajavööndist sõltumatu)** ja **Tõhus lõpp (ajavööndist sõltumatu)** väärtustega. Pärast omahinnakirja kindlaksmääramist määrab süsteem kulumäära.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Kulumäärade määramine aja prognoositavas ja tegelikus kontekstis

Prognoositav kontekst **Aeg** viitab:

- Hinnapakkumise rea üksikasjad **Aja** jaoks.
- Lepingurea üksikasjad **Aja** jaoks.
- Ressursiülesanded projektis.

Tegelik kontekst **Aja** jaoks viitab:

- Kirje- ja parandustöölehele kandmise read **Aja** jaoks.
- Töölehe read, mis luuakse aja sissekande edastamisel.

Pärast omahinnakirja kindlaksmääramist viib süsteem vaikekulumäära sisestamiseks läbi järgmised toimingud.

1. Süsteem sobitab väljade **Roll**, **Ressursiettevõte** ja **Ressursiüksus** kombinatsiooni prognoositud või tegelikus kontekstis **Aeg** ja hinnakirja rollide hinnaridadega. Selle vastenduse puhul eeldatakse, et kasutate tööjõukulu jaoks standardseid hinnakujunduse dimensioone. Kui olete konfigureerinud süsteemi nii, et see vastaks väljadele või lisaks väljadele **Roll**, **Ressursiettevõte** ja **Ressursiühik**, kasutatakse vastava rolli hinna rea toomiseks erinevat kombinatsiooni.
1. Kui süsteem leiab rolli hinna rea, millel on kulumäär kombinatsioonide **Roll**, **Ressursiettevõte** ja **Ressursiühik** jaoks, kasutatakse seda kulumäära vaikekulumäärana.
1. Kui süsteem ei suuda vastata väärtustele **Roll**, **Ressursiettevõte** ja **Ressursiühik**, loobub see dimensioonist, millel on madalaim prioriteet, ja otsib rollihinna ridu, mis sobivad kahe ülejäänud dimensiooniväärtusega ja jätkab dimensioonide järkjärgulist langetamist, kuni leitakse sobiv rollihinna rida. Selle kirje kulumäära kasutatakse vaikekulumäärana. Kui süsteem ei leia sobivat rollihinna rida, määratakse vaikimisi hinnaks **0** (null).

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
