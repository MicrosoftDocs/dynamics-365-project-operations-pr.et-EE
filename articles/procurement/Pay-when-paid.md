---
title: Makske hankija maksete tasumisel
description: See teema selgitab, kuidas kasutada tasu maksmise korral (PWP) stsenaariumi.
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
# <a name="pay-when-paid-vendor-payments"></a>Makske hankija maksete tasumisel

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema selgitab, kuidas kasutada tasu maksmise korral (PWP) stsenaariumi.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>PWP tingimustega ostutellimuse loomine

Kui sisestate hankija arve ja kui hankija suhtes kehtivad PWP tingimused, kuvatakse neid tingimusi ostutellimuse (PO) ridadel. PWP tingimustega ostutellimuse loomiseks toimige järgmiselt.

1. Rakenduses Microsoft Dynamics 365 Finance, järgige ühte järgmistest sammudest.

    - Minge jaotisse **Hanked** \> **Ostutellimused** \> **Kõik ostutellimused**. Valige toimingupaanil suvand **Uus**. Valige dialoogiboksis **Ostutellimuse loomine** hankija, kelle jaoks PWP-tingimused on projektis seadistatud, sisestage muu nõutav teave ja seejärel valige **OK**.
    - Minge jaotisse **Projektijuhtimine ja raamatupidamine** \> **Projektid** \> **Kõik projektid**. Valige toimingupaanil vahekaardil **Haldamine** **Kauba ülesanne**. Valige ostutellimus. Valige hankija, kelle jaoks PWP-tingimused on projektis seadistatud, ja seejärel valige **OK**.

2. Valige lehekülje **Ostutellimus** kiirkaardil **Ostutellimuse read** ostutellimuse rea loomiseks käsk **Rea lisamine**.
3. Valige kauba number või hankekategooria ja sisestage muud nõutavad andmed. Vaadake üle hankija ostutellimuse rea üksikasjad.

    Suvand **Maksa kui on makstud** valitakse automaatselt ja välja **PWP läve protsent** väärtus kopeeritakse automaatselt väljalt **PWP läve protsent** lehel **Projektid**.

4. Kui te ei soovi hankijale ostutellimuse rea jaoks PWP tingimusi rakendada, tühjendage valik **Maksa kui on makstud**. Sel juhul lähtestatakse ostutellimuse rea väli **PWP läve protsent** väärtusele **0** (null).
5. Valige lehe **Ostutellimus** toimingupaanil vahekaardil **Ostmine** ostutellimuse kinnitamiseks **Kinnita**.
6. Toimingupaani vahekaardil **Arve** valige **Arve**, et luua ostutellimuse arve.

## <a name="create-a-project-invoice-proposal"></a>Projekti arve ettepaneku loomine

Projekti arveettepanekuid kasutatakse kliendile projektiarvete koostamiseks. PWP stsenaariumi korral sõltuvad hankija maksed kliendi maksetest vastavalt PWP sätetele. Siiski on valikuid, mis võimaldavad teil maksed vabastada ilma kliendimakseteta, nagu soovite. Kliendile projektiarve koostamiseks toimige järgmiselt.

1. Avage Customer Engagementi rakendustes jaotis **Projekt** \> **Projektid** ja valige projekt.
2. Valige vahekaardil **Tegelikud näitajad** tegelik rida, mille loob ostutellimus, mille tehingutüüp on **Arveldamata müük**. Seejärel valige **Arve jaoks valmis**.
3. Minge jaotisesse **Müük** \> **Müügid** \> **Projektileping** ja valige projektileping.
4. Kliendiarve genereerimiseks valige toimingupaanil **Arve**.
5. Avage jaotises Rahandus jaotis **Projektihaldus ja raamatupidamine** \> **Perioodiline** \> **Impordi etapitabelist** ja valige rakenduse Project Operations integreerimise loomiseks **OK**.
6. Minge jaotisesse **Projektihaldus ja raamatupidamine** \> **Projektiarved** \> **Projektiarve ettepanek** ja valige **Postita**, et postitada arve ettepanek, mis oli projekti jaoks loodud.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliendi makse värskendamine ja hankijale tasumine

Kui hankija lõpetab töö projektiga ja saadab teile arve, peate projekti oleku ja klientide arved üle vaatama, et tuvastada, kas projekti PWP tingimused olid täidetud. Kui hankija PWP tingimused on täidetud, saate tuvastada, millised hankija arve read vastavalt kliendi maksetele projekti eest tuleb tasuda. Kui otsustate hankijale maksta ka juhul, kui PWP tingimusi ei täidetud, saate PWP tingimused lehel **Hankija arve maksa kui on makstud tingimustega** alistada.

1. Rahanduses avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid** ja valige projekt.
2. Valige toimingupaanil **Juhtelement** ja seejärel **Hankija arved**, et kuvada kõik projekti jaoks loodud hankija arved.
3. Sisestage lehe **Hankija arved maksa kui on makstud tingimustega** otsinguvälja väärtused, et leida hankija arve, mida soovite üle vaadata, ja seejärel valige **Otsi**.
4. Ainult PWP-arvete vaatamiseks valige suvand **Maksa tasumisel**.
5. Valige kiirkaardil **Hankija arve read** read, mille soovite tasumiseks vabastada.
6. Valige **Tarnija makse vabastamine**. Valik **Maksa kui on makstud** kustutatakse ja välja **Maksmiseks valmis** väärtus muudetakse olekusse **Jah**.
