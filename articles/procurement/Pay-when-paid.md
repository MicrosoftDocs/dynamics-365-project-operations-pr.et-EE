---
title: Maksa, kui maksad hankija maksed
description: Selles teemas selgitatakse, kuidas kasutada maksmisel maksmisel (PWP) stsenaariumi.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525381"
---
# <a name="pay-when-paid-vendor-payments"></a>Maksa, kui maksad hankija maksed

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas selgitatakse, kuidas kasutada maksmisel maksmisel (PWP) stsenaariumi.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>PWP-tingimustega ostutellimuse loomine

Kui sisestate hankija arve, kui hankijale kehtivad PWP tingimused, kuvatakse need tingimused ostutellimuse ridadel. PWP tingimustega ostutellimuse loomiseks toimige järgmiselt.

1. Jaotises Microsoft Dynamics 365 Finance tehke ühte järgmistest sammudest.

    - Minge jaotisse **Hanked** \> **Ostutellimused** \> **Kõik ostutellimused**. Valige toimingupaanil suvand **Uus**. **Valige dialoogiboksis Ostutellimuse** loomine hankija, kelle jaoks PWP-tingimused on projektis seadistatud, sisestage muu nõutav teave ja seejärel valige **OK**.
    - Minge jaotisse **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Kõik projektid**. Valige toimingupaani vahekaardil **Haldamine** käsk **Üksuse tööülesanne**. Valige ostutellimus. Valige hankija, kelle jaoks PWP-tingimused on projektis seadistatud, ja seejärel valige **OK**.

2. **Valige lehe Ostutellimus** kiirkaardil **Ostutellimuse read** rida **Lisa,** et luua ostutellimuse rida.
3. Valige kaubakood või hankekategooria ja sisestage muud nõutavad üksikasjad. Vaadake üle hankija ostutellimuse rea üksikasjad.

    Suvand **Maksa kui on makstud** valitakse automaatselt ja välja **PWP läve protsent** väärtus kopeeritakse automaatselt väljalt **PWP läve protsent** lehel **Projektid**.

4. Kui te ei soovi hankijale ostutellimuse rea jaoks PWP tingimusi rakendada, tühjendage valik **Maksa kui on makstud**. Sel juhul **lähtestatakse ostutellimuse rea PWP läve protsendiväli** väärtusele **0** (null).
5. **Valige lehe Ostutellimus**, tegevuspaani vahekaardil **Ost** ostutellimuse kinnitamiseks **Kinnita**.
6. Valige toimingupaani vahekaardil **Arve**, **et** luua ostutellimuse arve.

## <a name="create-a-project-invoice-proposal"></a>Projektiarvesoovituse loomine

Projektiarvete ettepanekuid kasutatakse kliendile projektiarvete loomiseks. PWP stsenaariumi korral sõltuvad hankija maksed kliendimaksetest vastavalt PWP seadetele. Siiski on valikuid, mis võimaldavad teil makseid vabastada ilma kliendimakseteta vastavalt vajadusele. Kliendile projektiarve loomiseks toimige järgmiselt.

1. Minge klientide kaasamise rakendustes jaotisse **Project Projects (Projektiprojektid** \> **)** ja valige projekt.
2. **Valige vahekaardil Tegelikud kogused** tegelik rida, mille loob ostutellimus, mille tüüp On **arveldamata müügikanne**. Seejärel valige **Arve** jaoks valmis.
3. Minge jaotisse **Müügiprojekti** \> **·** \> **leping** ja valige projekti leping.
4. Valige tegevuspaanil Arve **,** et luua kliendiarve.
5. Avage finance **jaotises Projektihaldus ja raamatupidamine** \> **Perioodiline** \> **importimine koondamistabelist** ja valige **OK**, et luua tööleht Projektitoimingute integreerimine.
6. Minge jaotisse **Projektihaldus ja raamatupidamine** \> **Projektiarvete** \> **ettepanek Projektiarvete ettepanek** ja valige **Projekti jaoks loodud arvesoovituse sisestamiseks Postita.**

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliendi makse värskendamine ja hankijale tasumine

Kui hankija lõpetab projektiga töö ja saadab teile arve, peate üle vaatama projekti oleku ja kliendiarved, et teha kindlaks, kas projekti PWP tingimused olid täidetud. Kui hankija PWP tingimused on täidetud, saate tuvastada, millised hankija arve read vastavalt kliendi maksetele projekti eest tuleb tasuda. Kui otsustate hankijale maksta ka juhul, kui PWP tingimusi ei täidetud, saate PWP tingimused lehel **Hankija arve maksa kui on makstud tingimustega** alistada.

1. Avage jaotises Rahandus **jaotis Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja valige projekt.
2. Valige toimingupaanil **Juhtelement** ja seejärel valige **Hankija arved**, et kuvada kõik projekti jaoks loodud hankija arved.
3. Sisestage lehe **Hankija arved maksa kui on makstud tingimustega** otsinguvälja väärtused, et leida hankija arve, mida soovite üle vaadata, ja seejärel valige **Otsi**.
4. **Valige suvand Maksa maksmisel**, et vaadata ainult PWP arveid.
5. **Valige vahekaardil Hankija arve read** read, mille soovite maksmiseks vabastada.
6. Valige **Vabasta hankija makse**. Valik **Maksa kui on makstud** kustutatakse ja välja **Maksmiseks valmis** väärtus muudetakse olekusse **Jah**.
