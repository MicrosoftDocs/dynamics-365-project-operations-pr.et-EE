---
title: Vaikehinnakirjad
description: Selles artiklis antakse teavet project operationsi müügi- ja omahinna vaikehinnaloendite kohta.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410257"
---
# <a name="default-price-lists"></a>Vaikehinnakirjad

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

## <a name="sales-price-lists"></a>Müügihinnakirjad

Iga projekti hinnapakkumine ja leping rakenduses Dynamics 365 Project Operations sisaldab vaikimisi müügi hinnakirja. 

### <a name="price-list-default-on-project-quotes"></a>Projekti hinnapakkumiste vaikehinnakiri
Süsteem lõpetab järgmise protsessi, et teha kindlaks, milline on projekti hinnapakkumise vaikehinnakiri.

1. Süsteem vaatleb hinnakirjasid, mis on seotud konto projekti hinnakirjadega. 
1. Kui kontokirjele ei ole lisatud projekti hinnakirju, vaatab süsteem projekti parameetritele lisatud müügihinnakirju, mis vastavad projekti hinnapakkumise valuutale.
1. Järgmisena kontrollib süsteem projekti hinnapakkumise kuupäevavahemikule vastavate hinnakirjade kehtivuskuupäeva. Eriti kuupäeva, millal hinnapakkumine loodi.
1. Kui projekti hinnapakkumise kuupäeval kehtib mitu hinnakirja, on kõik hinnakirjad projekti hinnapakkumises vaikimisi.
1. Kui projekti hinnapakkumise kuupäeval ei kehti ühtegi hinnakirja, pole projekti hinnapakkumisel projekti vaikehinnakirja. Projekti hinnapakkumises kuvatakse hoiatusteade. Teates on kirjas, et kuna projekti hinnakiri pole lisatud, siis teie prognoositavat ja tegelikku projekti ei hinnastata.

### <a name="price-list-default-on-project-contracts"></a>Projekti lepingu vaikehinnakiri 
Süsteem lõpetab järgmise protsessi, et teha kindlaks, milline on projekti lepingu vaikehinnakiri.

1. Kui leping on loodud hinnapakkumisest, kopeeritakse hinnapakkumise projekti hinnakirjad eraldi ja seotakse projekti lepinguga.
1. Kui leping luuakse nullist, vaatab süsteem hinnakirjasid, mis on konto projekti hinnakirjadega seotud. Kui kontokirjega pole seotud projekti hinnakirjad, vaatleb süsteem projekti parameetritega seotud pakkumise müügi hinnakirjasid, mille valuuta vastab projekti lepingule.
1. Järgmisena kontrollib süsteem projekti lepingu kuupäevavahemikule vastavate hinnakirjade kehtivuskuupäeva. Eriti kuupäeva, millal leping loodi.
1. Kui lepingu kuupäeval kehtib mitu hinnakirja, on kõik hinnakirjad lepingus vaikimisi.
1. Kui lepingu kuupäeval ei kehti ühtegi hinnakirja, pole lepingul projekti vaikehinnakirja. Projekti lepingus kuvatakse hoiatusteade. Teates on kirjas, et kuna projekti hinnakiri pole lisatud, siis teie prognoositavat ja tegelikku projekti ei hinnastata.

## <a name="cost-price-lists"></a>Omahinnakirjad

Omahinnakirjadel ei ole Project Operationsis ühtegi vaikeolemit. Projektikuludeks kasutatava omahinnakirja määramine toimub alati kandepõhiselt. Süsteem lõpetab järgmise protsessi, et teha kindlaks, millist vaikehinnakirja projekti kuludeks kasutada.

1. Süsteem vaatab hinnakirju, mis on lisatud projekti tellija üksusele.
1. Järgmisena vaatab süsteem nende hinnakirjade kuupäevaefektsust, mis vastavad sissetuleva hinnangu konteksti või tegeliku konteksti kuupäevale.

    - *Hinnangu kontekst* viitab ühele kolmest hindamise kontekstist projektitoimingutes.

        - Projekti prognoosi rida
        - Hinnapakkumise rea üksikasjad
        - Lepingurea üksikasjad

    - *Tegelik kontekst* viitab ühele kolmest projektitoimingute tegelike näitajate allikast.

       - Käsitsi loodud tööleheridade sisestamine või parandustöölehel loodud tööleheridade korrigeerimine
       - Töölehe read, mis luuakse aja-, kulu- või materjalikasutuse logide edastamisel
       - Arve rea üksikasjad

    Kui projektioperatsioonid vastavad sissetuleva töölehe rea või arve rea üksikasja kuupäevaefektsusele *tegelikus kontekstis*, kasutab **see välja Kande kuupäev**.

    - Kui sissetuleva prognoosi konteksti või tegeliku konteksti kuupäeval kehtib mitu hinnakirja, valitakse viimati loodud hinnakiri.
    - Kui projekti tellijaorganisatsiooni üksusele ei ole lisatud hinnakirju, vaatab süsteem omahinnakirju, mis on lisatud projekti parameetritele, mis vastavad projekti valuutale.

## <a name="enable-multi-currency-cost-price-list"></a>Luba mitme valuutaga omahinnakiri

Selle sätte leiate jaotisest **Seaded** \> **Parameetrid.** Vaikeväärtus on **Ei**.

Kui see säte on lubatud (st väärtus on seatud väärtusele **Jah**), käitub süsteem järgmiselt:

- See võimaldab organisatsiooniüksusega seostada mis tahes valuutas omahinnakirju. Näiteks saab USD valuutas organisatsiooniüksusele lisada EUR-valuutas omahinnaloendi. Süsteem kinnitab jätkuvalt, et organisatsiooniüksusele lisatud omahinnaloenditel ei ole kattuvat kuupäevaefektsust.
- See kinnitab, et projekti parameetritele lisatud omahinnaloenditel ei ole kattuvat kuupäevaefektsust, isegi kui neil on erinevad valuutad. See käitumine erineb vaikekäitumisest (st käitumisest, kui väärtuseks **on seatud Ei**). Vaikekäitumises valideeritakse ainult sama **valuutaga** omahinnaloendid kuupäeva mittekattuvuse suhtes.
- Sissetuleva kande kontekstis määrab see omahinnaloendi ainult kuupäeva mõjususe põhjal. See käitumine erineb vaikekäitumisest, kus süsteem valib omahinnaloendi, mis vastab nii projekti valuutale kui ka kuupäeva mõjususele.

Nende käitumise muutuste tõttu saavad Project Operationsi kliendid hallata globaalset omahinnaloendit, mis on asjakohane kogu ettevõtte jaoks. Neil ei pea olema hinnakirju igas toimingute valuutas. Ülemaailmsel hinnakirjal on kuupäevaline efektiivsus ja see võimaldab seadistada kulumäärasid mis tahes valuutas konkreetse hinnakujundusmõõtme väärtuste kombinatsiooni jaoks. Omahinnaloendi valuutat kasutatakse ainult vaikeväärtuste **sisestamiseks rollihindade**, **Kategooria hindade** ja **Hinnakirjaüksuse** kirjete loomisel. Seda ei kasutata hinnakirja määramiseks.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
