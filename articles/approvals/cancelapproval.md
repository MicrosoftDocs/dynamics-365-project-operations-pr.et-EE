---
title: Varem kinnitatud kannete kinnitamise tühistamine
description: Selles teemas selgitatakse, kuidas projektijuht saab tühistada varem kinnitatud aja-, kulu- või materjalikasutuskannete kinnitamise.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584775"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Varem kinnitatud kannete kinnitamise tühistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektijuht või kinnitaja, kes on eelnevalt kinnitanud aja-, kulu- või materjalikasutuse kanded, võib tühistada nende kannete kinnitamise. 

Varem kinnitatud aja-, kulu- või materjalikasutuskande kinnitamise tühistamiseks tehke järgmist.

1. Minge jaotisse **Projektid** \> **Minu töö** \> **Kinnitused**.
2. Loendis **Kinnitused** kuvatakse kõik kinnitamist ootavad ajakirjed. Muutke vaade väärtuseks **Minu varasemad kinnitused**.
3. Valige tühistamiseks aeg, kulu või materjali kinnitused. Seejärel valige **toimingupaanil Käsk Tühista kinnitamine**.
4. Operatsiooni kinnitamiseks valige **kuvataval kinnitussõnumiväljal OK**.

> [!IMPORTANT]
> Kliendile juba arveldatud varem kinnitatud aja-, kulu- ja materjalikasutuskande kinnitamist ei saa tühistada. Kui proovite, saate teate, mis ütleb, et kinnitust ei saa tühistada, kuna see oli juba arveldatud. Sellisel juhul saate kinnituse tühistada ainult juhul, kui korrigeerivat arvet kasutatakse kliendile täieliku krediidi või tagasimakse väljastamiseks algsel arvel.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Varem kinnitatud kande kinnitamise tühistamise mõju

Kui kinnitus tühistatakse, on sel mõju nii tegevusele kui ka finantsile.

### <a name="operational-impact"></a>Mõju tegevusele

Kui kande kinnitamine tühistatakse, märgitakse kinnituskirje esitatud **kirjeks**. Kande olek muudetakse olekuks **Esitatud**. Selles etapis saab projektimeeskonna liige kande tagasi kutsuda ilma tagasikutsumise taotlust esitamata.

Kinnitaja saab muuta **arveldatava koguse** ja **arveldustüübi** väärtusi ning seejärel kinnitada kande veel üks kord.

### <a name="financial-impact"></a>Finantsmõju

Kui kande kinnitamine tühistatakse, uuendatakse vastavaid kulu- ja müüginäitajaid järgmiselt:

- Välja **Korrigeerimise olek** värskendatakse väärtusele **Korrigeeritud**.
- Välja **Arveldusolek** värskendatakse väärtusele **Tühistatud**.

Seejärel luuakse tabelis tegelikud tagasipööramise kirjed. Tagasipööratud kirjete loomiseks kopeerib süsteem algsetest tegelikest välja väärtustest üle. Ainukesed väärtused, mida ei kopeerita, on koguse väärtused. Need väärtused pööratakse hoopis vastupidiseks. Tagasipööratud tegelikud luuakse järgmiste tegelike jaoks: **Kulu** ja **Arveldamata müük**. Tühistatud tegelike näitajate väli **Korrigeerimise olek** määratakse väärtusele **Korrigeerimatu** ja väli **Arveldusolek** väärtusele **Tühistatud**. Nende muudatuste tõttu ei võta projekti talletatud kulutused ja tulu mahajäämus enam arvesse summasid, mida need tegelikud näitajad esindavad.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
