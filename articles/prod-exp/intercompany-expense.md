---
title: Kontsernisisesed kulud
description: Selles teemas kirjeldatakse, kuidas kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001201"
---
# <a name="intercompany-expenses"></a>Kontsernisisesed kulud

Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks. Saate kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti. Juriidilist olemit, mille jaoks töötaja töötab, nimetatakse laenavaks juriidiliseks olemiks. Juriidilist olemit, mille jaoks töötaja kulusid kannab, nimetatakse laenajast juriidiliseks olemiks. 

Enne töötaja saab luua ja esitada kontsernisiseseid kulusid, peate lubama kontsernisiseste kulude read. Valige laenava juriidilise isiku lehel **Kuluhalduse parameetrid** suvand **Luba kontsernisisesed kuluread**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Kontsernisiseste kulude maksude sisestamine

[!include [banner](../includes/banner.md)]

Enne kui saate kuluaruandes kasutada laenava (allika) juriidilise isikuga seotud maksurühmi, mitte vastuvõtva (siht) juriidilise isiku omi, peate lubama selle funktsionaalsuse pearaamatu käibemaksu seadistuses. Kui parameeter **Juriidiline isik kontsernisisese maksusisestuse jaoks** on määratud olekusse **Allikas** ja **Rakenda käibemaksuga maksustamise reegleid** on määratud olekusse **Ei**, kasutatakse laenava juriidilise üksuse maksukombinatsiooni. Kui sama parameetri väärtuseks on seatud **Lähte**, kasutatakse laenajast juriidilise olemi jaoks maksu kombinatsiooni. Ameerika Ühendriikide juriidilistele olemitele, kui parameetri väärtuseks on seatud **Algne**, peab väli **käibemaks laekumata** olema konfigureeritud ka uuel lehel **Pearaamatusse sisestamise rühmad**. Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamisandmete jaoks.   
Käitumine on kooskõlas projektiga või ilma selleta sisestatud kuluaruannete jaoks.  

## <a name="new-expense-expression-builder"></a>Uus kuluavaldise koostur

Uus kuluavaldise koostur käsitleb projekte kasutatavate kontsernisiseste kulude stsenaariumite probleeme. See funktsioon tagab, et kontsernisisese kulu loomisel valideeritakse kulupoliitika õigesti kulureal valitud projekti suhtes ja et kuluaruannet saab edukalt esitada.

Selleks, et kuluavaldise koosturi funktsioon töötaks, peab see olema sisse lülitatud. Samuti tuleb seadistada projekti ID-ga kulupoliitika.

Kui olete juba konfigureerinud poliitikaid, mis valideerivad kulureal projekti ID, tuleb need poliitikad eemaldada. Seejärel saate funktsiooni sisse lülitada ja poliitikad uuesti konfigureerida.

Funktsiooni sisselülitamiseks järgige allolevaid juhiseid.

1. Minge jaotisse **Tööruumid** \> **Funktsiooni juhtimine**.
2. Valige loendis **Uus kuluavaldise koostur, mis käsitleb projekte kasutatavate kontsernisiseste kulude stsenaariumite probleeme**. Seejärel valige **Luba kohe**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
