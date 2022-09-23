---
title: Kuluaruannete postitamine
description: Selles artiklis selgitatakse, kuidas kuluaruandeid sisestada.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524864"
---
# <a name="post-expense-reports"></a>Kuluaruannete postitamine

Kui kuluaruanne on kinnitatud ja peažurnaali üle kantud, saab selle sisestada. Kuluaruande sisestamisel tuvastatakse kulud, mis millele saab kohaldada käibemaksutagastust. Käibemaksu maksete kontrollimise ja tagasinõudmise ülesanne määratakse töötajale, kes vastutab kuluaruande kontrollimise eest.

Kui kuluaruande kulud kanna mõni muu ettevõte, mis ei ole ettevõte, kus töötab töötaja, peate kinnitama mõlemad ettevõtted, kellele need kulud võlgnetakse, ja ettevõte, kellelt nad võlgnetakse. Näiteks töötaja, kes esitas kuluaruande, töötab DAT-ettevõtte heaks, kuid kulu kattis ettevõte DIR. Sel juhul on DAT ettevõte, kuhu kulu võlgnetakse, ja DIR on ettevõte, kellelt kulu on võlgnetakse. Pärast nende tööleheridade kinnitamist saate kuluread pearaamatusse sisestada.

Kuluaruande sisestamiseks lehele **Kinnitatud kuluaruanded** valige kuluaruanne ja seejärel valige tegevuspaanil suvand **Sisesta**.

Korraga saate sisestada ka kõik loendi kuluaruanded. Valige kõik kuluaruanded ja seejärel valige **Sisesta**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Luba funktsioon Võime sisestada kulukohustust hankija valuutas sularaha makseviisi jaoks

Funktsioon **Võimalus sisestada kulukohustust sularaha makseviisi** hankija valuutas võimaldab kuluaruandeid sisestada sularaha makseviisi hankija valuutasse.

Praegu sisestatakse sularahakulude esitamisel kuluaruanded arvestusvaluutas. Kandevaluuta, arvestusvaluuta ja hankija valuuta vahelise summa teisendamise tõttu makstakse hankijatele vale summa, kui kulu kandekuupäeval ja tegelikul maksepäeval on erinevad vahetuskursid.

See funktsioon tagab, et hankija saldo kajastatakse kuluaruande sisestamisel hankija valuutas.

1. Minge jaotisse **Tööruumid** \> **Funktsiooni juhtimine**.
2. Leidke loendist võimalus **sisestada kulukohustus hankija valuutas sularahamakse meetodi** jaoks ja seejärel valige **Luba kohe**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
