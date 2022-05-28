---
title: Ärikanded projektitoimingutes
description: Selles teemas antakse ülevaade Microsofti äritehingute kontseptsioonist Dynamics 365 Project Operations.
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
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582199"
---
# <a name="business-transactions-in-project-operations"></a>Ärikanded projektitoimingutes

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Microsoftis Dynamics 365 Project Operations *on äritehing* abstraktne mõiste, mida ükski olem ei esinda. Mõned olemite levinumad väljad ja protsessid on aga mõeldud äritehingute mõiste kasutamiseks. Järgmised olemid kasutavad seda ülevaadet.

- Hinnapakkumise rea üksikasjad
- Lepingurea üksikasjad
- Hinnangu read
- Töölehe read
- Tegelikud

Nendest olemitest vastendatakse *pakkumise rea üksikasjad, Lepingu rea üksikasjad ja Hinnanguread projekti elutsükli hinnangufaasi*. Olemid Žurnaalrid ja Tegelikud arvud vastendatakse *projekti elutsükli täitmisfaasiga*.

Project Operations käsitleb kõigi viie olemi kirjeid ärikannetena. Ainus erinevus on see, et hinnangufaasiga vastendatud olemite kirjeid (pakkumise rea üksikasjad, lepingurea üksikasjad ja hinnanguread) loetakse *finantsprognoosideks*, samas kui täitmisfaasiga vastendatud olemite kirjeid (žurnaaliread ja tegelikud) loetakse juba toimunud *finantsfaktideks*.

Lisateavet leiate teemast [Hinnangud](../project-management/estimating-projects-overview.md) ja [Tegelikud](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Ärikannetele kordumatud mõisted

Järgmised mõisted on äritehingute mõiste jaoks kordumatud.

- Tehingu tüüp
- Tehingu klass
- Tehingu päritolu
- Tehingu seos

### <a name="transaction-type"></a>Tehingu tüüp

Tehingu tüüp tähistab projekti finantsmõju ajastust ja konteksti. Selle määratleb suvandikomplekt, millel on Project Operationsis järgmised toetatud väärtused.

- Kulu
- Projekti leping
- Arveldamata müük
- Arveldatud müük
- Organisatsioonidevaheline müük
- Ressursiühiku maksumus

### <a name="transaction-class"></a>Tehingu klass

Tehingu klass tähistab erinevat tüüpi kulusid, mis on seotud projektidega. Selle määratleb suvandikomplekt, millel on Project Operationsis järgmised toetatud väärtused.

- Aeg
- Kulu
- Materjal
- Tasu
- Vahe-eesmärk
- Maks

> [!NOTE]
> **Verstaposti** väärtust kasutab tavaliselt äriloogika fikseeritud hinnaga arveldamiseks Project Operationsis.

### <a name="transaction-origin"></a>Kande päritolu

Kande päritolu on olem, mis salvestab iga äritehingu päritolu, et aidata aruandlust ja jälgitavust. Projekti käivitamise alguses loob iga äritehing teise äritehingu, mis omakorda loob teise äritehingu jne.

### <a name="transaction-connection"></a>Tehingu seos

Tehinguühendus on olem, mis salvestab seose kahe sarnase äritehingu vahel, näiteks kulu ja seotud müügi tegelikud andmed või kande tühistamised, mis käivitatakse arveldustegevuste, näiteks arve kinnitamise või arve paranduste kaudu.

Olemid Transaction origin ja Transaction connection aitavad teil üheskoos jälgida seoseid äritehingute ja toimingute vahel, mis põhjustasid konkreetse ärikande loomise.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
