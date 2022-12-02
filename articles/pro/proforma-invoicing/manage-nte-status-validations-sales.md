---
title: Mitteületatava oleku ja valideerimiste haldamine
description: See artikkel annab teavet rakenduses Project Operations tehtavatest mitteületatava limiidi kontrollidest.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932751"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Mitteületatava oleku ja valideerimiste haldamine 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

## <a name="not-to-exceed-on-approvals"></a>Mitteületatavad kinnitused

Aja, kulu või materjali kasutuse kirje esitamisel luuakse kinnituskirje. Kui kinnitus on tasustatav ja vastendub aja- ja materjalikulu lepingureaga, teeb süsteem mitteületatava valideerimise kontrolli järgmistel tasemetel.

  - Kontrollige projekti lepingureal kliendi jaoks määratud limiiti
  - Kontrollige lepungureal määratud limiiti
  - Kontrollige kliendi jaoks määratud limiiti
  - Kontrollige lepungul määratud limiiti

Igal tasandil tehtavad kontrollid hõlmavad tagamist, et selle kinnitamise müügiväärtuse summa ei riku pärast juba salvestatud arvelduse võlgnevuse summa arvutamist mitteületatavat limiiti sellel tasemel ega sellel tasemel seni arveldatud summat.

Kui kontroll läbitakse, lisatakse kinnitusele valideerimise olek **Õnnestus**.

Kui kontroll ebaõnnestu, lisatakse kinnitusele valideerimise olek **Nurjus**. Mitteületatava kinnitamise üksikasjad teavitavad kasutajat, millisel tasemel kinnitamine nurjus.

Kui esitatud aja, kulu või materjali kasutuskirjet peetakse mittearveldatavaks, määratakse valideerimisolekuks **Mitte kohaldatav** koos valideerimise üksikasjaga, mis on võrdne valikuga **Mitte kohaldatav**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Mitteületatav arveldamata müügi tegelikel näitajatel

Aja, kulu või materjali kasutuskirje kinnitamisel luuakse kulu ja arveldamata müügi tegelike näitajate kirjed. Kui arveldamata müügi tegelikud näitajad on tasustatavad ja vastenduvad aja- ja materjalikulu lepingureaga, teev rakendus mitteületatava valideerimise kontrolli järgmistel tasemetel.

  - Kontrollige projekti lepingurea kliendi jaoks määratud limiiti
  - Kontrollige lepungureal määratud limiiti
  - Kontrollige kliendi jaoks määratud limiiti
  - Kontrollige lepungul määratud limiiti

Igal tasandil tehtavad kontrollid tagavad, et tegeliku näitaja müügiväärtuse summa ei riku pärast juba salvestatud arvelduse võlgnevuse summa arvutamist mitteületatavat limiiti sellel tasemel ega sellel tasemel seni arveldatud summat.

Kui kontroll läbitakse, lisatakse arveldamata müügi tegelikule näitajale mitteületatav olek **Sooritatud**.

Kui kontroll nurjub, lisatakse arveldamata müügi tegelikule näitajale mitteületatav olek **Nurjunud**. Kinnitamise üksikasjad teavitavad kasutajat, millisel tasemel kinnitamine nurjus.

Kui arveldamata müügi tegelik näitaja loetakse mittearveldatavaks või tasuta, kui ühelgi neljast tasemest pole mitteületatavat limiiti määratud või kui loodab tegelik näitaja on kulu, honorar, ressursi üksus või organisatsioonisisene müük, peavad väljad **Mitteületuse olek** ja **Mitteületuse kinnituse üksikasjad** peavad olema määratud valikule **Pole kohaldatav**.

## <a name="reset-the-not-to-exceed-status"></a>Mitteületatava oleku lähtestamine

Mitteületatavaid olekuid on võimalik lähtestada hulgi. Projektijuhid saavad reguleerida mitte ületatavat valideerimist, et prioriseerida üks kindel töö, aja, kulu või materjali jaotuse kasutuse arveldamine teiste suhtes, mis on juba pühendunud saadaolevast mitte ületatavast summast.

Pärast seda, kui mitteületatavuse olek on lähtestatud arveldamata müügi tegelikele näitajatele, kinnitatud summa vähendatakse. Projektijuht saab valida mõne muu töö, aja, kulu või materjali jaotuse kasutuskirje, mille varasem mitte ületamise valideerimine ja uuesti hindamine nurjus. Kinnitatud summa vähendamisega need tegelikud väärtused läbivad nüüd valideerimise, mis aitab projektijuhil avaldada suuremat mõju ja omada suuremat kontrolli selle perioodi arveldatavate tehingute üle.

Kui te soovite mitteületamise oleku lähtestada, valige vaates **Aja ja materjali arveldamise võlgnevus** või **Tegelikud näitajad** üks või mitu tegelikku näitajat ja valige seejärel **Lähtesta mitteületatavate olek**.

Mitteületamise olek lähtestatakse kõikidel seotud valitud tegelikel näitajatel olekule **Pole hinnatud**. Tegelikud näitajad, mille mitteületamise olek on lähtestatud, on arveldamata müügi tegelikud näitajad, mis ei ole veel arveldatud, pole veel arve mustandil ja on märgitud arvedatavana. Kõiki teisi valitud tegelikke näitajaid ignoreeritakse.

## <a name="reevaluate-not-to-exceed-status"></a>Mitteületatavuse oleku uuesti hindamine

Mitteületatavaid olekuid on võimalik hinnata uuesti hulgi. Mitteületatavuse oleku uuesti hindamine on kasulik järgmistel juhtudel.

  - Mitteületatavuse limiidid räägiti uuesti kliendiga läbi ja tegelikke näitajaid ei hinnata uuesti.
  - Projektijuht tahab arveldamata müügi võlgnevuse arveldamist täpsustada, prioriseerides ühte tööorganit teise ees.

Kui te soovite mitteületamise oleku uuesti hinnata, valige vaates **Aja ja materjali arveldamise võlgnevus** või **Tegelikud näitajad** üks või mitu tegelikku näitajat ja valige seejärel **Hinda mitteületatavate olek uuesti**.

Kõik asjaomased valitud mitteületatava limiidiga tegelikud näitajad hinnatakse uuesti vasatavalt mitteületatavuse piirväärtuse seadistusele. Mitteületatavuse oleku uuesti hindamiseks asjakohased tegelikud näitajad on arveldamata müügi tegelikud näitajad, mis ei ole arveldatud, pole veel arve mustandil ja on märgitud arvedatavana. Kõik muud valitud tegelikud näitajad.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
