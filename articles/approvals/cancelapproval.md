---
title: Eelnevalt kinnitatud kirjete kinnitamise tühistamine
description: See artikkel selgitab, kuidas projektijuht saab tühistada varem kinnitatud aja-, kulu- või materjalikasutuse kirjeid.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930451"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Eelnevalt kinnitatud kirjete kinnitamise tühistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projektijuht või kinnitaja, kes on varem kinnitanud aja-, kulu- või materjalikasutuse kirjeid, saab nende kirjete kinnitamise tühistada. 

Järgige järgmisi etappe, et tühistada varem kinnitatud aja-, kulu- või materjalikasutuse kirje kinnitamine.

1. Minge jaotisse **Projektid** \> **Minu töö** \> **Kinnitused**.
2. Loendilehel **Kinnitused** kuvatakse kõik kinnitamist ootavad aja sissekanded. Muutke vaateks **Minu varasemad kinnitused**.
3. Valige tühistamiseks aeg, kulu või materjali kinnitused. Seejärel valige toimingupaanil **Tühista kinnitus**.
4. Ilmuvas kinnitusteate kastis valige toimingu kinnitamiseks **OK**.

> [!IMPORTANT]
> Te ei saa tühistada varem kinnitatud aja-, kulu- ja materjalikasutuse kirje kinnitamist, mille kohta on kliendile juba arve esitatud. Kui proovite seda teha, saate teate, et kinnitamist ei saa tühistada, sest selle eest on juba arve esitatud. Sel juhul saate kinnituse tühistada ainult siis, kui algsel arvel olevale kliendile krediit- või raha tagasimaksmiseks kasutatakse parandusarvet.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Varem kinnitatud kirje kinnitamise tühistamise mõju

Kui kinnitus tühistatakse, on sel mõju nii tegevusele kui ka finantsile.

### <a name="operational-impact"></a>Mõju tegevusele

Kui kirje kinnitamine tühistatakse, märgitakse kinnituskandele **Edastatud**. Kirje olekuks on muudetud **Edastatud**. Selles etapis saab projektimeeskonna liige kirje tagasi kutsuda ilma tagasikutsumise taotlust esitamata.

Kinnitaja saab väärtusi **Arveldatav kogus** ja **Arveldustüüp** muuta ning seejärel kirje veel kord kinnitada.

### <a name="financial-impact"></a>Finantsmõju

Kui kirje kinnitus tühistatakse, värskendatakse vastavaid kulu ja müügi tegelikke näitajaid järgmiselt:

- Välja **Korrigeerimise olek** värskendatakse väärtusele **Korrigeeritud**.
- Välja **Arveldusolek** värskendatakse väärtusele **Tühistatud**.

Seejärel luuakse tabelis tegelikud tagasipööramise kirjed. Tagasipööratud kirjete loomiseks kopeerib süsteem algsetest tegelikest välja väärtustest üle. Ainukesed väärtused, mida ei kopeerita, on koguse väärtused. Need väärtused pööratakse hoopis vastupidiseks. Tagasipööratud tegelikud luuakse järgmiste tegelike jaoks: **Kulu** ja **Arveldamata müük**. Tühistatud tegelike näitajate väli **Korrigeerimise olek** määratakse väärtusele **Korrigeerimatu** ja väli **Arveldusolek** väärtusele **Tühistatud**. Nende muudatuste tõttu ei võta projekti talletatud kulutused ja tulu mahajäämus enam arvesse summasid, mida need tegelikud näitajad esindavad.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
