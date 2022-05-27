---
title: Mustandist projekti arve ettepanekute raamatupidamise parandamine
description: Selles teemas selgitatakse, kuidas muuta mustandist arve ettepanekul raamatupidamisega seotud teavet.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575069"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Mustandist projekti arve ettepanekute raamatupidamise parandamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projekti arvete *toimingu üksikasju* haldab projektijuht näidisarvel. Need üksikasjad hõlmavad otsuseid tundide, kulude, materjalide või vahe-eesmärkide kohta, mille eest tuleb esitada arve, hindade ning avansi- ja honorarisummade taotlemise kohta. Pärast algse näidisarve kinnitamist saate toimingu üksikasju muuta, luues ja kinnitades [korrigeeriva näidisarve](../proforma-invoicing/corrective-invoices.md).

Projekti arvete *raamatupidamise üksikasju* hallatakse kliendile suunatud arvedokumendis. Need üksikasjad hõlmavad arvele rakendatud käibemaksu arvutamist ja finantsdimensioone. Selles teemas on toodud üksikasjad selle kohta, kuidas neid raamatupidamise üksikasju saab mustandi projekti arve ettepanekus muuta.

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
