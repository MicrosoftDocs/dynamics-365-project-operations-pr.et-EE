---
title: Projekti prognooside ja tegelike näitajate müügihinna määratlemine
description: See artikkel annab teavet projekti prognooside ja müügihindade tegelike näitajate määratlemise kohta.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475179"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Projekti prognooside ja tegelike näitajate müügihinna määratlemine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

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

1. Süsteem sobitab väljade **Roll** ja **Ressursiühik** kombinatsiooni prognoositud või tegelikus kontekstis **Aeg** ja hinnakirja rollide hinnaridadega. See vastendamine, mida te kasutate, eeldab arveldusmäärade jaoks kastivälise hinnakujunduse dimensioone. Kui olete hinna konfigureerinud nii, et see põhineb muul väljal või lisaks väljadele **Roll** ja **Ressursi ühik**, kasutatakse seda väljade kombinatsiooni sobiva rolli hinnarea leidmiseks.
1. Kui süsteem leiab rolli hinna rea, millel on väljade **Roll** ja **Ressursi ühik** kombinatsiooni arvelduskulu, kasutatakse seda arve määra arve vaikemäärana.
1. Kui süsteem ei suuda väärtusi **Roll** ja **Ressursiühik** vastendada, hangib see rolli hinnaread, millel on väljal **Roll** vastavad väärtused, kuid väljal **Ressursiühik** nullväärtused. Kui süsteem leiab sobiva rollihinna kirje, kasutatakse selle kirje arveldusmäära vaikimisi arveldusmäärana. See vastendus eeldab valmiskujul konfiguratsiooni **Rolli** versus **Ressursiühiku** suhtelise prioriteedi jaoks müügi hinnakujunduse dimensioonina.

> [!NOTE]
> Kui konfigureerite väljadele **Roll** ja **Ressursiühik** teistsuguse tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub eelnev käitumine vastavalt. Süsteem hangib rolli hinnakirjed, mille väärtused vastavad prioriteetsuse järjekorras igale hinnadimensiooni väärtusele. Nende dimensioonide nullväärtustega read on viimased.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
