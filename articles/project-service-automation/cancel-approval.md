---
title: Tühista varem kinnitatud aja- ja kuluarvestuse olemid
description: Selles teemas antakse teavet kinnitatud projekti aja- ja kuluarvestuse tehingute tühistamise kohta.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750879"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Tühista varem kinnitatud aja- ja kuluarvestuse tehingud

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rakenduse Dynamics 365 Project Service Automation viimases versioonis saavad kinnitajad tühistada varem kinnitatud aja- või kuluarvestuse tehinguid.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Varem kinnitatud aja- või kulukirje tühistamine

Varem kinnitatud aja- või kulukirje tühistamiseks tehke järgmist.

1. Minge jaotisse **Projektid** \> **Minu töö** \> **Kinnitused**.
2. Muutke loendilehel **Kinnitused** vaateks **Minu varasemad kinnitused**. Kuvatakse varem kinnitatud aegade ja kulu kirjete loend.
3. Valige üks või mitu kirjet ja seejärel klõpsake käsku **Tühista kinnitamine**. Te saate hoiatusteate.
4. Kinnitamise tühistamiseks valige **OK**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Mõistke aja- või kulukirje kinnitamisest loobumise mõju

Kui kinnitus tühistatakse, on sel mõju nii tegevusele kui ka finantsile.

### <a name="operational-impact"></a>Mõju tegevusele

Tegevuste poolel, kui kinnitamine tühistatakse, lähtestatakse kirje olekuks **Mustand**, ja kinnitust ei kuvata enam vaates **Minu varasemad kinnitused**. Selle asemel kuvatakse tühistatud kinnitus kas vaates **Ajakirjed kinnitamiseks** või vaates **Kulukirjed kinnitamiseks**, olenevalt sellest, kas see oli aja- või kulukirje. Peale selle muudetakse seotud aja- või kulukirje olekuks **Esitatud**, et seotud kirje oleks vastavuses kinnitatutega, mille olek on **Mustand**.

Kinnitajana saate redigeerida mõnda kinnitusvälja, mille olek on **Mustand**. Nende väljade hulka kuuluvad **Arveldamise tüüp** ja **Arveldatavate tundide ajakirjed**. Pärast muudatuste tegemist saate kirje uuesti kinnitada. Soovi korral võite kirje tagasi lükata. Kui lükkate ajakirje kinnitamise tagasi, muudetakse kirje olekuks **Tagastatud**. Kui lükkate ajakirje kinnitamise tagasi, muudetakse olekuks **Tagasi lükatud**. Funktsionaalselt, nii tagasi lükatud kui ka hüljatud kirjed käituvad samamoodi kui kirje, mille olek on **Mustand**. Projekti meeskonnaliige saab kirjes vajalikud muudatused teha ja seejärel uuesti kinnitamiseks esitada või kirje täielikult kustutada.

### <a name="financial-impact"></a>Rahaline mõju

Projekti mõjutatakse ka rahaliselt, kui kinnitus tühistatakse. Esmalt värskendatakse vastavad tegelikud kulud ja müügid järgmiselt.

- Kohandamise olekuks seatakse **Korrigeeritud**.
- Arveldamise olekuks seatakse **Tühistatud**.

Seejärel luuakse tabelis tegelikud tagasipööramise kirjed. Tagasipööratud kirjete loomiseks kopeerib süsteem algsetest tegelikest välja väärtustest üle. Ainukesed väärtused, mida ei kopeerita, on koguse väärtused. Need väärtused pööratakse hoopis vastupidiseks. Tagasipööratud tegelikud luuakse järgmiste tegelike jaoks: **Kulu** ja **Arveldamata müük**. Tagasipööratud tegelike välja **Korrigeerimise olek** väärtuseks seatakse **Pole korrigeeritav** ja arve olekuks seatakse **Tühistatud**.

Pärast nende muudatuste tegemist arvestatakse projektile kulutatud summa ja projekti tulu mahajäämust, mis on seotud nende tegelike näitajate summadega.
