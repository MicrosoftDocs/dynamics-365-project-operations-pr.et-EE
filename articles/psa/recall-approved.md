---
title: Kinnitatud aja- või kulukirjete tagasivõtmine
description: Selles teemas antakse teavet varem kinnitatud aja- või kulukirjete tagasivõtmise kohta.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e90b84bbfcd007e97e96b294144f058ac73746e3d358437692f0a8e6e92b8de3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998321"
---
# <a name="recall-approved-time-or-expense-entries"></a>Kinnitatud aja- või kulukirjete tagasivõtmine

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektimeeskonna liige või mõni muu isik, kes aja- või kulukirje esitab, saab selle aja- või kulukirje pärast selle kinnitamist tagasi võtta. Kinnitatud aja- või kulukirje tagasivõtmisel on kaks etappi.

1. Esitaja taotleb tagasivõtmist.
2. Kinnitaja kinnitab tagasivõtmise.

## <a name="request-a-recall"></a>Tagasivõtmise taotlemine

Kinnitatud aja- või kulukirje tagasivõtmiseks toimige järgmiselt.

1. Ajakirjete puhul tehke valikud **Projektid** \> **Minu töö** \> **Ajakirje**.

    –või–

    Kulukirjete puhul tehke valikud **Projektid** \> **Minu töö** \> **Kulud**.

2. Ajakirjete puhul valige kindla projekti ja ülesande kombinatsiooni jaoks kõik ajakirjed. Alternatiivina valige ruudustikus kindla projekti kindla kuupäeva aegade üksikud lahtrid.

    –või–

    Kulukirjete puhul valige tagasivõtmiseks kulukirje rida.

3. Tehke valik **Kutsu tagasi**. Ilmub kinnituse dialoogiboks. Kui valitud aja- ja kulukirjed olid juba kinnitatud, palutakse teil sisestada tagasivõtmise põhjus.
4. Sisestage tagasivõtmise põhjus ja seejärel klõpsake toimingu kinnitamiseks nuppu **OK**. Süsteem saadab kirje kinnitanud isikule tagasivõtmise kinnitamise taotluse.

> [!NOTE]
> Kuigi kinnitatud aja- ja kulukirjeid saab tagasi võtta, ei saa tagasivõtmise taotlust luua, kui kinnitatud aja või kulu eest on juba kliendile arve esitatud. Kasutajale, kes proovib tagasivõtmise taotlust luua, kuvatakse teade, mis teatab, et aega või kulu ei saa tagasi võtta, kuna see on juba arveldatud.

## <a name="approve-or-reject-a-recall-request"></a>Tagasivõtmise taotluse kinnitamine või tagasilükkamine

Tagasivõtmise taotluse kinnitamiseks või tagasilükkamiseks toimige järgmiselt.

1. Minge jaotisse **Projektid** \> **Minu töö** \> **Kinnitused**.
2. Muutke loendilehel **Kinnitamised** vaade väärtusele **Tagasivõtmistaotlused kinnitamiseks**. Kuvatakse esitatud tagasivõtmistaotluste loend.
3. Valige üks või mitu kirjet ja seejärel tehke kas valik **Kinnita** või **Hülga**.
4. Kui valisite suvandi **Kinnita**, kuvatakse hoiatusteade, mis selgitab kinnitamise mõju. Toimingu kinnitamiseks klõpsake nuppu **OK**. Tagasivõtmistaotlus on kinnitatud.

    –või–

    Kui valisite suvandi **Hülga**, siis lükatakse tagasivõtmistaotlus tagasi.

> [!NOTE]
> Nagu tagasivõtmise taotlemisel, nii ka tagasivõtmise kinnitamisel kontrollib süsteem aja- või kulukirjetest arveldustegevust. Kui kirje eest on juba arve esitatud või kui see on arve mustandis, kuvatakse kinnitajale tõrketeade, mis teatab, et aega või kulu ei saa tagasivõtmiseks kinnitada, kuna see on juba arveldatud.

## <a name="impact-of-a-recall-request"></a>Tagasivõtmistaotluse mõju

Kinnitamise tagasivõtmisel on nii tegevuslik kui ka finantsmõju.

### <a name="operational-impact"></a>Mõju tegevusele

Kui tagasivõtmistaotlus on kinnitatud, märgitakse kinnitamise kirje kui **Hüljatud**. Kirje olekuks määratakse kas **Tagastatud** või **Hüljatud**, olenevalt sellest, kas see on aja- või kulukirje.

Projektimeeskonna liige saab kirjeid vaadata, redigeerida ja seejärel uuesti esitada või kirjeid täielikult kustutada.

Kui tagasivõtmistaotlus lükatakse tagasi, jääb kirje olekuks **Kinnitatud** ja projektimeeskonna liige ega kinnitaja ei saa kirjet redigeerida.

### <a name="financial-impact"></a>Finantsmõju

Tagasivõtmistaotluse kinnitamisel värskendatakse vastavaid kulude ja müügi tegelikke näitajaid järgmisel viisil.

- Välja **Korrigeerimise olek** värskendatakse väärtusele **Korrigeeritud**.
- Välja **Arveldusolek** värskendatakse väärtusele **Tühistatud**.

Seejärel luuakse tabelis tegelikud tagasipööramise kirjed. Tagasipööratud kirjete loomiseks kopeerib süsteem algsetest tegelikest välja väärtustest üle. Ainukesed väärtused, mida ei kopeerita, on koguse väärtused. Need väärtused pööratakse hoopis vastupidiseks. Tagasipööratud tegelikud luuakse järgmiste tegelike jaoks: **Kulu** ja **Arveldamata müük**. Tühistatud tegelike näitajate väli **Korrigeerimise olek** määratakse väärtusele **Korrigeerimatu** ja väli **Arveldusolek** väärtusele **Tühistatud**. Nende muudatuste tõttu ei võta projekti talletatud kulutused ja tulu mahajäämus enam arvesse summasid, mida need tegelikud näitajad esindavad.

Kui tagasivõtmisetaotlus lükatakse tagasi, ei ole projektile finantsmõju.

## <a name="changes-to-time-entry-records"></a>Ajakirjete kirjete muudatused

Järgmisel joonisel on kuvatud muudatused, mis toimuvad kinnitatud ajakirjetes nende tagasivõtmisel.

![Ajakirje oleku üleminekud.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Kulukirjete kirjete muudatused

Järgmisel joonisel on kuvatud muudatused, mis toimuvad kinnitatud kulukirjetes nende tagasivõtmisel.

![Kulukirje oleku üleminekud.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]