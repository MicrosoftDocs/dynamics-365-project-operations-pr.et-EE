---
title: Mitteületatava oleku ja valideerimiste haldamine
description: See teema anna teavet rakenduses Project Operations tehtavatest mitteületatava limiidi kontrollidest.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129988"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Mitteületatava oleku ja valideerimiste haldamine 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

## <a name="not-to-exceed-on-approvals"></a>Mitteületatavad kinnitused

Aja- või kulukirje esitamisel luuakse kinnitamise kirje. Kui kinnitus on tasustatav ja vastendub aja- ja materjalikulu lepingureaga, teeb süsteem mitteületatava valideerimise kontrolli järgmistel tasemetel.

  - Kontrollige projekti lepingureal kliendi jaoks määratud limiiti
  - Kontrollige lepungureal määratud limiiti
  - Kontrollige kliendi jaoks määratud limiiti
  - Kontrollige lepungul määratud limiiti

Igal tasandil tehtavad kontrollid hõlmavad tagamist, et selle kinnitamise müügiväärtuse summa ei riku pärast juba salvestatud arvelduse võlgnevuse summa arvutamist mitteületatavat limiiti sellel tasemel ega sellel tasemel seni arveldatud summat.

Kui kontroll läbitakse, lisatakse kinnitusele valideerimise olek **Õnnestus**.

Kui kontroll ebaõnnestu, lisatakse kinnitusele valideerimise olek **Nurjus**. Mitteületatava kinnitamise üksikasjad teavitavad kasutajat, millisel tasemel kinnitamine nurjus.

Kui esitatud aja- või kulukirje loetakse mittetasustatavaks, seatakse mitteületatava kinnitamise olekuks **Pole kohaldatav** koos kinnitamise üksikasjadega, mis on võrdsed väärtusega **Pole kohaldatav**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Mitteületatav arveldamata müügi tegelikel näitajatel

Kui aja- või kulukirje kinnitatakse, luuakse kulu ja arveldamata müügi tegelike näitajate kirjed. Kui arveldamata müügi tegelikud näitajad on tasustatavad ja vastenduvad aja- ja materjalikulu lepingureaga, teev rakendus mitteületatava valideerimise kontrolli järgmistel tasemetel.

  - Kontrollige projekti lepingurea kliendi jaoks määratud limiiti
  - Kontrollige lepungureal määratud limiiti
  - Kontrollige kliendi jaoks määratud limiiti
  - Kontrollige lepungul määratud limiiti

Igal tasandil tehtavad kontrollid tagavad, et tegeliku näitaja müügiväärtuse summa ei riku pärast juba salvestatud arvelduse võlgnevuse summa arvutamist mitteületatavat limiiti sellel tasemel ega sellel tasemel seni arveldatud summat.

Kui kontroll läbitakse, lisatakse arveldamata müügi tegelikule näitajale mitteületatav olek **Sooritatud**.

Kui kontroll nurjub, lisatakse arveldamata müügi tegelikule näitajale mitteületatav olek **Nurjunud**. Kinnitamise üksikasjad teavitavad kasutajat, millisel tasemel kinnitamine nurjus.

Kui arveldamata müügi tegelik näitaja loetakse mittearveldatavaks või tasuta, kui ühelgi neljast tasemest pole mitteületatavat limiiti määratud või kui loodab tegelik näitaja on kulu, honorar, ressursi üksus või organisatsioonisisene müük, peavad väljad **Mitteületuse olek** ja **Mitteületuse kinnituse üksikasjad** peavad olema määratud valikule **Pole kohaldatav**.

## <a name="reset-the-not-to-exceed-status"></a>Mitteületatava oleku lähtestamine

Mitteületatavaid olekuid on võimalik lähtestada hulgi. See võimaldab projektijuhtidel reguleerida mitteületavuse kinnitust, et prioriseerida üje kindla töö-, aja- või kuluorgani arveldamist üle teiste, mis on juba saadaolevate mitteületatavate summade seast pühendatud.

Pärast seda, kui mitteületatavuse olek on lähtestatud arveldamata müügi tegelikele näitajatele, kinnitatud summa vähendatakse. Projektijuht saab valida mõne muu töö-, aja- või kuluorgani, millel eelnevalt mitteületamise kinnitumin nurjus, ja hinnata need uuesti. Kinnitatud summa vähendamisega need tegelikud näitajad kinnitamist ei läbi. See aitab projektijuhil rakendada suuremat mõjuvõimu ja kontrolli selle perioodi arveldatavate tehingute üle.

Kui te soovite mitteületamise oleku lähtestada, valige vaates **Aja ja materjali arveldamise võlgnevus** või **Tegelikud näitajad** üks või mitu tegelikku näitajat ja valige seejärel **Lähtesta mitteületatavate olek**.

Mitteületamise olek lähtestatakse kõikidel seotud valitud tegelikel näitajatel olekule **Pole hinnatud**. Tegelikud näitajad, mille mitteületamise olek on lähtestatud, on arveldamata müügi tegelikud näitajad, mis ei ole veel arveldatud, pole veel arve mustandil ja on märgitud arvedatavana. Kõiki teisi valitud tegelikke näitajaid ignoreeritakse.

## <a name="reevaluate-not-to-exceed-status"></a>Mitteületatavuse oleku uuesti hindamine

Mitteületatavaid olekuid on võimalik hinnata uuesti hulgi. Mitteületatavuse oleku uuesti hindamine on kasulik järgmistel juhtudel.

  - Mitteületatavuse limiidid räägiti uuesti kliendiga läbi ja tegelikke näitajaid ei hinnata uuesti.
  - Projektijuht tahab arveldamata müügi võlgnevuse arveldamist täpsustada, prioriseerides ühte tööorganit teise ees.

Kui te soovite mitteületamise oleku uuesti hinnata, valige vaates **Aja ja materjali arveldamise võlgnevus** või **Tegelikud näitajad** üks või mitu tegelikku näitajat ja valige seejärel **Hinda mitteületatavate olek uuesti**.

Kõik asjaomased valitud mitteületatava limiidiga tegelikud näitajad hinnatakse uuesti vasatavalt mitteületatavuse piirväärtuse seadistusele. Mitteületatavuse oleku uuesti hindamiseks asjakohased tegelikud näitajad on arveldamata müügi tegelikud näitajad, mis ei ole arveldatud, pole veel arve mustandil ja on märgitud arvedatavana. Kõik muud valitud tegelikud näitajad.
