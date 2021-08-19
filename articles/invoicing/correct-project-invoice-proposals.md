---
title: Mustandist projekti arve ettepanekute raamatupidamise parandamine
description: Selles teemas selgitatakse, kuidas muuta mustandist arve ettepanekul raamatupidamisega seotud teavet.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999311"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Mustandist projekti arve ettepanekute raamatupidamise parandamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projekti arvete *toimingu üksikasju* haldab projektijuht näidisarvel. Need üksikasjad hõlmavad otsuseid tundide, kulude, materjalide või vahe-eesmärkide kohta, mille eest tuleb esitada arve, hindade ning avansi- ja honorarisummade taotlemise kohta. Pärast algse näidisarve kinnitamist saate toimingu üksikasju muuta, luues ja kinnitades [korrigeeriva näidisarve](../proforma-invoicing/corrective-invoices.md).

Projekti arvete *raamatupidamise üksikasju* hallatakse kliendile suunatud arvedokumendis. Need üksikasjad hõlmavad arvele rakendatud käibemaksu arvutamist ja finantsdimensioone. Selles teemas on toodud üksikasjad selle kohta, kuidas neid raamatupidamise üksikasju saab mustandi projekti arve ettepanekus muuta.

## <a name="adjust-sales-tax"></a>Käibemaksu muutmine

Vaikimisi arveldamise käibemaksurühmasid ja eseme käibemaksurühmasid saab muuta otse arve ettepaneku dokumendis. Nende rühmade muutmiseks valige **Redigeeri** ja sisestage seejärel igal projekti arve ettepaneku real väljale **Käibemaksurühm** või **Eseme käibemaksurühm**.

## <a name="adjust-financial-dimensions"></a>Finantsdimensioonide muutmine

Finantsdimensioone ei saa muuta otse projekti arve ettepaneku real. Selle asemel järgige neid samme, et kohandada projekti arve ettepaneku finantsdimensioone.

1. Valige arve ettepanekul suvand **Kustuta kõik**, et eemaldada projekti arve ettepaneku read.

    > [!NOTE]
    > Nupp **Kustuta kõik** on saadaval alles pärast seda, kui süsteemiadministraator lubab funktsiooni **Kustuta arve ettepaneku read ressursipõhiste/mittelaopõhiste stsenaariumide jaoks Project Operationsi kasutamise ajal** tööruumis **Funktsioonihaldus**.

2. Muutke dinantsdimensioone.

    - **Ettemaksukanded (arvelduse vahe-eesmärgid):** avage **Kõik projektid** \> **Haldamine** \> **Ettemaksukanded** ja valige muutmist vajav vahe-eesmärk. Seejärel värskendage vahekaardil **Finantsdimensioonid** vastavalt vajadusele väärtuseid.
    - **Aja-, kulu- ja materjali kanded:** valige lehel **Kirjendatud projekti kanded** suvand **Raamatupidamise muutmine**, et värskendada finantsmõõtmeid.

3. Pärast finantsdimensiooni väärtuste kohandamist avage **Projektihaldus ja raamatupidamine** \> **Perioodiline** \> **Project Operationsi integreerimine** ja valige perioodilise toimingu käitamiseks suvand **Impordi koondtabelist**. See protsess kasutab projekti arve ettepaneku ridade uuesti loomiseks värskendatud finantsdimensiooni väärtusi. Värskendatud väärtusi kasutatakse seejärel projekti arve kirjendamisel projekti alampearaamatus ja pearaamatus.
