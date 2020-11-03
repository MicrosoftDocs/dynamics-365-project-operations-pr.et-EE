---
title: Vaikehinnakirjad
description: Selles teemas antakse teavet Project Operationsi vaike-müügihinnakirjade ja -omahinnakirjade kohta.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074835"
---
# <a name="default-price-lists"></a>Vaikehinnakirjad

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

## <a name="sales-price-lists"></a>Müügihinnakirjad

Iga projekti hinnapakkumine ja leping Dynamics 365 Project Operationsis sisaldab vaike-müügihinnakirja. 

### <a name="price-list-default-on-project-quotes"></a>Projekti hinnapakkumiste vaikehinnakiri
Süsteem lõpetab järgmise protsessi, et teha kindlaks, milline on projekti hinnapakkumise vaikehinnakiri.

1. Süsteem vaatleb hinnakirjasid, mis on seotud konto projekti hinnakirjadega. 
2. Kui kontokirjega on seotud projekti hinnakirjad, vaatleb süsteem projekti parameetritega seotud pakkumise müügi hinnakirjasid, mille valuuta vastab projekti hinnapakkumisele.
3. Järgmisena kontrollib süsteem projekti hinnapakkumise kuupäevavahemikule vastavate hinnakirjade kehtivuskuupäeva. Eriti kuupäeva, millal hinnapakkumine loodi.
4. Kui projekti hinnapakkumise kuupäeval kehtib mitu hinnakirja, on kõik hinnakirjad projekti hinnapakkumises vaikimisi.
5. Kui projekti hinnapakkumise kuupäeval ei kehti ühtegi hinnakirja, pole projekti hinnapakkumisel projekti vaikehinnakirja. Projekti hinnapakkumises kuvatakse hoiatusteade. Teates on kirjas, et kuna projekti hinnakiri pole lisatud, siis teie prognoositavat ja tegelikku projekti ei hinnastata.

### <a name="price-list-default-on-project-contracts"></a>Projekti lepingu vaikehinnakiri 
Süsteem lõpetab järgmise protsessi, et teha kindlaks, milline on projekti lepingu vaikehinnakiri.

1. Kui leping on loodud hinnapakkumisest, kopeeritakse hinnapakkumise projekti hinnakirjad eraldi ja seotakse projekti lepinguga.
2. Kui leping luuakse nullist, vaatab süsteem hinnakirjasid, mis on konto projekti hinnakirjadega seotud. Kui kontokirjega pole seotud projekti hinnakirjad, vaatleb süsteem projekti parameetritega seotud pakkumise müügi hinnakirjasid, mille valuuta vastab projekti lepingule.
4. Järgmisena kontrollib süsteem projekti lepingu kuupäevavahemikule vastavate hinnakirjade kehtivuskuupäeva. Eriti kuupäeva, millal leping loodi.
5. Kui lepingu kuupäeval kehtib mitu hinnakirja, on kõik hinnakirjad lepingus vaikimisi.
6. Kui lepingu kuupäeval ei kehti ühtegi hinnakirja, pole lepingul projekti vaikehinnakirja. Projekti lepingus kuvatakse hoiatusteade. Teates on kirjas, et kuna projekti hinnakiri pole lisatud, siis teie prognoositavat ja tegelikku projekti ei hinnastata.

## <a name="cost-price-lists"></a>Omahinnakirjad

Omahinnakirjadel ei ole Project Operationsis ühtegi vaikeolemit. Projekti kuludeks kasutatava omahinnakirja määratlemine toimub alati hetkega. Süsteem lõpetab järgmise protsessi, et teha kindlaks, millist vaikehinnakirja projekti kuludeks kasutada.

1. Süsteem vaatleb esmalt hinnakirju, mis on seotud projekti lepingu organisatsiooni üksusega.
2. Süsteem vaatleb seejärel hinnakirjade kehtivat kuupäeva, mis vastab sissetuleva prognoosi või tegeliku rea kuupäevale. Sellisel juhul viitab *prognoosi rida* kõigile kolmele Project Operationsi prognoosi kontekstile.

    - Projekti prognoosi rida
    - Hinnapakkumise rea üksikasjad
    - Lepingurea üksikasjad
  
3. Kui sissetuleva prognoosi või tegeliku kuupäeva jaoks kehtivad mitu hinnakirja, siis valitakse viimati loodud hinnakiri.
4. Kui projekti lepingu organisatsiooni üksusega pole seotud ühtegi projekti hinnakirja, vaatleb süsteem projekti parameetritega seotud omahinakirjasid, mille valuuta vastab projektile.
5. Järgmiseks vaatleb süsteem hinnakirjade kehtivat kuupäeva, mis vastab sissetuleva prognoosi või tegeliku rea kuupäevale. 
6. Kui sissetuleva prognoosi või tegeliku kuupäeva jaoks kehtivad mitu hinnakirja, siis valitakse viimati loodud hinnakiri.
7. Kui projekti parameetritega, mis vastavad valuutale ja lõppkuupäevale, ei ole seotud omahinnakirja, määrab süsteem sissetuleva prognoosi või tegeliku rea kulumäära nulliks (0).
