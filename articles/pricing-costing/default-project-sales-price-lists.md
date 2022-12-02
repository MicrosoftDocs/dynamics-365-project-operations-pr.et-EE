---
title: Vaikehinnakirjad
description: See artikkel annab teavet rakenduse Project Operations vaike-müügihinnakirjade ja omahinnakirjade kohta.
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
1. Kui kontokirjega ei ole seotud projekti hinnakirjad, vaatleb süsteem projekti parameetritega seotud pakkumise müügi hinnakirjasid, mille valuuta vastab projekti hinnapakkumisele.
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

Omahinnakirjadel ei ole Project Operationsis ühtegi vaikeolemit. Projekti kuludeks kasutatava omahinnakirja määratlemine toimub alati tehingupõhiselt. Süsteem lõpetab järgmise protsessi, et teha kindlaks, millist vaikehinnakirja projekti kuludeks kasutada.

1. Süsteem vaatleb hinnakirju, mis on seotud projekti lepingu organisatsiooni üksusega.
1. Järgmiseks vaatleb süsteem hinnakirjade kehtivat kuupäeva, mis vastab sissetuleva prognoosi konteksti või tegeliku näitaja konteksti kuupäevale.

    - *Prognoosi kontekst* viitab kõigile kolmele rakenduse Project Operations prognoosi kontekstile.

        - Projekti prognoosi rida
        - Hinnapakkumise rea üksikasjad
        - Lepingurea üksikasjad

    - *Prognoosi kontekst* viitab mis tahes kolmele Project Operationsi tegelike näitajate allikatele.

       - Käsitsi loodud kirjete töölehele kandmised või parandustöölehel loodud parandustöölehele kandmised.
       - Töölehele kandmised, mis luuakse aja-, kulu- või materjali kasutuslogide esitamise käigus
       - Arve rea üksikasjad

    Kui rakendus Project Operations ühtib sissetuleva ajakirje rea või arve rea üksikasja kuupäevaga the *tegelik kontekst*, kasutab see välja **Tehingu kuupäev**.

    - Kui sissetuleva prognoosikonteksti või tegeliku näitaja konteksti kuupäeval kehtib mitu hinnakirja, valitakse viimati loodud hinnakiri.
    - Kui projekti tellivale organisatsiooni üksusele hinnakirju lisatud ei ole, vaatab süsteem omahinnakirju, mis on lisatud projekti valuutale vastavatele projektiparameetritele.

## <a name="enable-multi-currency-cost-price-list"></a>Luba mitme valuutaga omahinnakiri

Selle sätte leiate jaotisest **Sätted** \> **Parameetrid**. Vaikeväärtus on **Ei**.

Kui see säte on lubatud (st väärtuseks on seatud **Jah**), käitub süsteem järgmiselt.

- See võimaldab mis tahes valuutas omahinnakirjasid seostada organisatsiooniüksusega. Näiteks saab organisatsiooniüksusele lisada USD valuutas omahinnakirja EUR valuutas. Süsteem kontrollib jätkuvalt, et organisatsiooniüksusele lisatud omahinnakirjadel ei oleks kuupäevade kehtivus kattuv.
- See kinnitab, et projekti parameetritele lisatud omahinnakirjad ei kattu kuupäevaga, isegi kui neil on erinevad valuutad. See käitumine erineb vaikekäitumisest (st käitumisest, kui väärtuseks on seatud **Ei**). Vaikekäitumise korral kinnitatakse ainult need omahinnakirjad, millel on **sama** valuuta.
- Sissetuleva tehingu kontekstis määrab see omahinnakirja ainult kuupäeva kehtivuse alusel. See käitumine erineb vaikekäitumisest, kus süsteem valib omahinnakirja, mis vastab nii projekti valuutale kui ka kuupäeva kehtivusele.

Tänu nendele käitumismuutustele on rakenduse Project Operations klientidel võimalik säilitada globaalset omahinnakirja, mis on asjakohane kogu ettevõtte jaoks. Neil ei pea olema hinnakirju igas tegevusvaluutas. Ülemaailmne hinnakiri hakkab kehtima alates kuupäevast ja võimaldab määrata kulumäärad mis tahes valuutas konkreetse hinnadimensiooni väärtuste kombinatsiooni jaoks. Omahinnakirja valuutat kasutatakse ainult vaikeväärtuste sisestamiseks, kui luuakse kaubakirjed **Rollihinnad**, **Kategooria hinnad** ja **Hinnakiri**. Seda ei kasutata hinnakirja määratlemiseks.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
