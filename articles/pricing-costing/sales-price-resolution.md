---
title: Projektipõhiste prognooside ja tegelike näitajate müügihinna määratlemine
description: See artikkel annab teavet projektipõhiste hinnangute ja tegelike müügihindade määratlemise kohta.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475364"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Projektipõhiste prognooside ja tegelike näitajate müügihinna määratlemine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Microsoft Dynamics 365 Project Operationsi prognoositud ja hindade tegelike näitajate müügihindade määramiseks kasutab süsteem müügihinnakirja määramiseks esmalt kuupäeva ja valuutat sissetulevas hinnangus või tegelikus kontekstis. Tegelikus kontekstis kasutab süsteem kohaldatava hinnakirja määramiseks välja **Tehingu kuupäev**. Sissetuleva prognoositud või tegeliku väärtuse **Tehingu kuupäev** võrreldakse hinnakirja **Tõhus algus (ajavööndist sõltumatu)** ja **Tõhus lõpp (ajavööndist sõltumatu)** väärtustega. Pärast müügi hinnakirja kindlaks määramist määrab süsteem müügi või arvelduskulu.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Aja tegelike ja prognoositavate ridade kulumäärade määramine

Prognoositav kontekst **Aeg** viitab:

- Hinnapakkumise rea üksikasjad **Aja** jaoks.
- Lepingurea üksikasjad **Aja** jaoks.
- Ressursiülesanded projektis.

Tegelik kontekst **Aja** jaoks viitab:

- Kirje- ja parandustöölehele kandmise read **Aja** jaoks.
- Töölehe read, mis luuakse aja sissekande edastamisel.
- Arverea üksikasjad **Aja** jaoks. 

Pärast müügi hinnakirja kindlaks määramist täidab süsteem järgmised etapid vaikimisi arveldusmäära sisestamiseks.

1. Süsteem sobitab väljade **Roll**, **Ressursiettevõte** ja **Ressursiüksus** kombinatsiooni prognoositud või tegelikus kontekstis **Aeg** ja hinnakirja rollide hinnaridadega. See vastendamine, mida te kasutate, eeldab arveldusmäärade jaoks kastivälise hinnakujunduse dimensioone. Kui olete hinna konfigureerinud nii, et see põhineb muul väljal või lisaks väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik**, kasutatakse seda väljade kombinatsiooni sobiva rolli hinnarea leidmiseks.
1. Kui süsteem leiab rolli hinnarea, millel on arve määr kombinatsiooni **Roll**, **Ressursiettevõte** ja **Ressursi ühik** jaoks, kasutatakse seda arve määra vaikimisi arve määrana.

> [!NOTE]
> Kui konfigureerite väljad **Roll**, **Ressursiettevõte** ja **Ressursi ühik** erinevalt, või kui teil on muid dimensioone, millel on kõrgem prioriteet, muutub eelnev käitumine vastavalt. Süsteem hangib rolli hinnakirjed, mille väärtused vastavad prioriteetsuse järjekorras igale hinnadimensiooni väärtusele. Nende dimensioonide nullväärtustega read on viimased.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Kulu tegelike ja prognoositavate ridade müügihindade kindlaks määramine

Prognoositav kontekst **Kulu** viitab:

- Hinnapakkumise rea üksikasjad **Kulu** jaoks.
- Lepingurea üksikasjad **Kulu** jaoks.
- Projekti kuluprognoosiread.

Tegelik kontekst **Kulu** viitab:

- Kirje- ja parandustöölehele kandmise read **Kulu** jaoks.
- Töölehele kandmised, mis luuakse aja sissekande edastamisel.
- Arverea üksikasjad **Kulu** jaoks. 

Pärast müügi hinnakirja kindlaks määramist täidab süsteem järgmised etapid vaikimisi ühiku müügihinna sisestamiseks.

1. Süsteem sobitab väljade **Kategooria** ja **Ühik** kombinatsiooni **Kulu** hinnangureal hinnakirja kategooria hinnaridadega.
1. Kui süsteem leiab kategooria hinnarea, millel on kombinatsioonide **Kategooria** ja **Ühik** müügimäär, kasutatakse seda müügimäära vaikemüügimäärana.
1. Kui süsteem leiab sobiva kategooria hinnarea, võidakse vaikemüügihinna sisestamiseks kasutada hinnakujundusmeetodit. Järgmises tabelis on näidatud rakenduse Project Operations kuluhindade vaikekäitumine.

    | Kontekst | Hinnakujundusmeetod | Vaikehind |
    | --- | --- | --- |
    | Hinnang | Ühiku hind | Vastavalt kategooria hinnareale. |
    |        | Omahinnaga | 0.00 |
    |        | Juurdehindlus üle omahinna | 0.00 |
    | Tegelik | Ühiku hind | Vastavalt kategooria hinnareale. |
    |        | Omahinnaga | Vastavalt seotud tegelikule kulule. |
    |        | Juurdehindlus üle omahinna | Seotud kulu tegeliku näitaja ühikukulu määrale rakendatakse kategooria hinnareal määratletud hinnalisandit. |

1. Kui süsteem ei suuda väärtusi **Kategooria** ja **Ühik** ühtida, määratakse müügimääraks vaikimisi **0** (null).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Materjali tegelike ja prognoosiridade müügihindade kindlaks määramine

Prognoositav kontekst **Materjal** viitab:

- Hinnapakkumise rea üksikasjad **Materjali** jaoks.
- Lepingurea üksikasjad **Materjali** jaoks.
- Projekti materjali prognoosiread.

Tegelik **Materjali** kontekst viitab:

- Kirje- ja parandustöölehele kandmise read **Materjali** jaoks.
- Töölehele kandmised, mis luuakse materjali kasutamise logi edastamisel.
- Arverea üksikasjad **Materjal** jaoks. 

Pärast müügi hinnakirja kindlaks määramist täidab süsteem järgmised etapid vaikimisi ühiku müügihinna sisestamiseks.

1. Süsteem sobitab väljade **Toode** ja **Ühik** kombinatsiooni hinnangureal **Materjal** ja hinnakirjas olevaid kaubaridasid.
1. Kui süsteem leiab hinnakirja kaubarea, millel on müügimäär kombinatsioonile **Toode** ja **Ühik**, ja kui hinnakujundusmeetodiks on **Valuutasumma**, on müügihind, mida kasutatakse hinnakirja märgitud real. 
1. Kui väljade **Toode** ja **Ühik** väärtused ei ühti või kui hinnakujundusmeetod on midagi muud kui **Valuutasumma**, määratakse müügikursi väärtuseks **0** (null) vaikimisi. Selline käitumine tuleneb sellest, et Project Operations toetab projektis kasutatavate materjalide puhul ainult **Valuutasumma** hinnakujundusmeetodit.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
