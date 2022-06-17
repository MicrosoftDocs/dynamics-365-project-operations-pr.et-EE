---
title: Mustandist projekti arve ettepanekute raamatupidamise parandamine
description: Selles artiklis selgitatakse, kuidas arvesoovituses raamatupidamisalast teavet kohandada.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921205"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Mustandist projekti arve ettepanekute raamatupidamise parandamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projekti arvete *toimingu üksikasju* haldab projektijuht näidisarvel. Need üksikasjad hõlmavad otsuseid tundide, kulude, materjalide või vahe-eesmärkide kohta, mille eest tuleb esitada arve, hindade ning avansi- ja honorarisummade taotlemise kohta. Pärast algse näidisarve kinnitamist saate toimingu üksikasju muuta, luues ja kinnitades [korrigeeriva näidisarve](../proforma-invoicing/corrective-invoices.md).

Projekti arvete *raamatupidamise üksikasju* hallatakse kliendile suunatud arvedokumendis. Need üksikasjad hõlmavad arvele rakendatud käibemaksu arvutamist ja finantsdimensioone. Selles artiklis on toodud üksikasjad selle kohta, kuidas neid raamatupidamisandmeid saab projektiarve ettepaneku eelnõuga korrigeerida.

## <a name="adjust-sales-tax"></a>Käibemaksu muutmine

Vaikimisi arveldamise käibemaksurühmasid ja eseme käibemaksurühmasid saab muuta otse arve ettepaneku dokumendis. Nende rühmade muutmiseks valige **Redigeeri** ja sisestage seejärel igal projekti arve ettepaneku real väljale **Käibemaksurühm** või **Eseme käibemaksurühm**.

## <a name="adjust-financial-dimensions"></a>Finantsdimensioonide muutmine

### <a name="header-dimensions"></a>Päise dimensioonid

Vaikimisi tuletatakse arve finantsdimensioonid arveldatavatest sisestamata projektikannete kirjetest. Süsteemisätted võimaldavad teil siiski kasutada projektiarvete ettepanekute päises olevaid finantsdimensioone kliendisaldode konteerimiseks. Selle funktsiooni lubamiseks valige **lehe Projektihaldus- ja raamatupidamisparameetrite vahekaardil** **Finantsid** müügireskontro müügireskontro **dimensioonide luba värskenduste** lubamine.

Arve päiste finantsdimensioone saab redigeerida enne arve konteerimist. Aktiveerige **lehel** Projektiarve ettepanek **vaade Päis** ja seejärel redigeerige väärtusi vahekaardil **Finantsdimensioonid**.

**Päisevaade** on saadaval alles pärast seda, kui süsteemiadministraator lubab funktsioonihalduse **tööruumis funktsiooniga Päise** **ja ridade vaate** funktsiooniga vormid Kasuta projektiarve ettepanekut ja arvežurnaali vorme. See funktsioon nõuab Finance'i värskendust 10.0.25 või uuemat versiooni.

### <a name="line-dimensions"></a>Rea dimensioonid

Finantsdimensioone ei saa muuta otse projekti arve ettepaneku real. Selle asemel järgige neid samme, et kohandada projekti arve ettepaneku finantsdimensioone.

1. Valige arve ettepanekul suvand **Kustuta kõik**, et eemaldada projekti arve ettepaneku read.

    Nupp **Kustuta kõik** on saadaval alles pärast seda, kui süsteemiadministraator lubab funktsiooni **Kustuta arve ettepaneku read ressursipõhiste/mittelaopõhiste stsenaariumide jaoks Project Operationsi kasutamise ajal** tööruumis **Funktsioonihaldus**.

2. Muutke dinantsdimensioone.

    - **Ettemaksukanded (arvelduse vahe-eesmärgid):** avage **Kõik projektid** \> **Haldamine** \> **Ettemaksukanded** ja valige muutmist vajav vahe-eesmärk. Seejärel värskendage vahekaardil **Finantsdimensioonid** vastavalt vajadusele väärtuseid.
    - **Aja-, kulu- ja materjali kanded:** valige lehel **Kirjendatud projekti kanded** suvand **Raamatupidamise muutmine**, et värskendada finantsmõõtmeid.

3. Pärast finantsdimensiooni väärtuste kohandamist avage **Projektihaldus ja raamatupidamine** \> **Perioodiline** \> **Project Operationsi integreerimine** ja valige perioodilise toimingu käitamiseks suvand **Impordi koondtabelist**. See protsess kasutab projekti arve ettepaneku ridade uuesti loomiseks värskendatud finantsdimensiooni väärtusi. Värskendatud väärtusi kasutatakse seejärel projekti arve kirjendamisel projekti alampearaamatus ja pearaamatus.
