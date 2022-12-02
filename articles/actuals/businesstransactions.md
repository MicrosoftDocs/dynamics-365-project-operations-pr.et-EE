---
title: Äritehingud rakenduses Project Operations
description: See artikkel annab ülevaate rakenduse Microsoft Dynamics 365 Project Operations äritehingute kontseptsioonist.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923275"
---
# <a name="business-transactions-in-project-operations"></a>Äritehingud rakenduses Project Operations

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Teenuses Microsoft Dynamics 365 Project Operations on *äritehing* abstraktne mõiste, mida ei esinda ükski üksus. Mõned olemite levinumad väljad ja protsessid on aga mõeldud äritehingute mõiste kasutamiseks. Järgmised olemid kasutavad seda ülevaadet.

- Hinnapakkumise rea üksikasjad
- Lepingurea üksikasjad
- Hinnangu read
- Töölehe read
- Tegelikud

Nende olemite, hinnapakkumise rea üksikasjade, lepingurea üksikasjade ja hinnangu read vastendatakse projekti töötsükli *prognoosi etapiga*. Töölehe read ja tegelikud olemid vastendatakse projekti töötsükli *täitmise etapiga*.

Project Operations käsitleb kõigi viie üksuse kirjeid äritehingutena. Ainus erinevus seisneb selles, et üksuste kirjeid, mis on vastendatud hinnangufaasi (hinnapakkumisrea üksikasjad, lepingurea üksikasjad ja hinnanguread), loetakse *finantsprognoosideks*, samas kui kirjeid üksustes, mis on vastendatud täitmisfaasi (Töölehele kandmise read ja tegelikud näitajad) loetakse *finantsfaktideks*, mis on juba toimunud.

Lisateavet leiate teemast [Hinnangud](../project-management/estimating-projects-overview.md) ja [Tegelikud](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Ärikannetele kordumatud mõisted

Järgmised mõisted on äritehingute mõiste jaoks kordumatud.

- Tehingu tüüp
- Tehingu klass
- Tehingu päritolu
- Tehingu seos

### <a name="transaction-type"></a>Tehingu tüüp

Tehingu tüüp tähistab projekti finantsmõju ajastust ja konteksti. See on määratletud suvandikomplektiga, millel on rakenduses Project Operations järgmised toetatud väärtused:

- Kulu
- Projekti leping
- Arveldamata müük
- Arveldatud müük
- Organisatsioonidevaheline müük
- Ressursiühiku maksumus

### <a name="transaction-class"></a>Tehingu klass

Tehingu klass tähistab erinevat tüüpi kulusid, mis on seotud projektidega. See on määratletud suvandikomplektiga, millel on rakenduses Project Operations järgmised toetatud väärtused:

- Aeg
- Kulu
- Materjal
- Tasu
- Vahe-eesmärk
- Maks

> [!NOTE]
> Väärtust **Vahekokkuvõte** kasutab äriloogika tavaliselt Project Operationsis fikseeritud hinnaga arveldamiseks.

### <a name="transaction-origin"></a>Kande päritolu

Tehingu päritolu on üksus, mis salvestab aruandluse ja jälgitavuse hõlbustamiseks iga äritehingu päritolu. Kui projekti täitmine algab, loob iga äritehing uue äritehingu, mis omakorda loob uue äritehingu jne.

### <a name="transaction-connection"></a>Tehingu seos

Tehingu seos on üksus, mis salvestab seose kahe sarnase äritehingu vahel, nagu kulu ja seotud müügi tegelikud näitajad või tehingute tühistamised, mille käivitavad arveldustoimingud, nagu arve kinnitamine või arve parandused.

Tehingu päritolu ja tehingu seose üksused aitavad teil üheskoos jälgida seoseid äritehingute ja tegevuste vahel, mis põhjustasid konkreetse äritehingu tekkimise.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
