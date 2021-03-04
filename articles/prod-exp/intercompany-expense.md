---
title: Kontsernisisesed kulud
description: Selles teemas kirjeldatakse, kuidas kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960827"
---
# <a name="intercompany-expenses"></a>Kontsernisisesed kulud

Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks. Saate kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti. Juriidilist olemit, mille jaoks töötaja töötab, nimetatakse laenavaks juriidiliseks olemiks. Juriidilist olemit, mille jaoks töötaja kulusid kannab, nimetatakse laenajast juriidiliseks olemiks. 

Enne töötaja saab luua ja esitada kontsernisiseseid kulusid, peate lubama kontsernisiseste kulude read. Valige laenava juriidilise isiku lehel **Kuluhalduse parameetrid** suvand **Luba kontsernisisesed kuluread**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Kontsernisiseste kulude maksude sisestamine

[!include [banner](../includes/banner.md)]

Enne kui saate kuluaruandes kasutada laenava (allika) juriidilise isikuga seotud maksurühmi, mitte vastuvõtva (siht) juriidilise isiku omi, peate lubama selle funktsionaalsuse pearaamatu käibemaksu seadistuses. Kui parameeter **Juriidiline isik kontsernisisese maksusisestuse jaoks** on määratud olekusse **Allikas** ja **Rakenda käibemaksuga maksustamise reegleid** on määratud olekusse **Ei**, kasutatakse laenava juriidilise üksuse maksukombinatsiooni. Kui sama parameetri väärtuseks on seatud **Lähte**, kasutatakse laenajast juriidilise olemi jaoks maksu kombinatsiooni. Ameerika Ühendriikide juriidilistele olemitele, kui parameetri väärtuseks on seatud **Algne**, peab väli **käibemaks laekumata** olema konfigureeritud ka uuel lehel **Pearaamatusse sisestamise rühmad**. Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamisandmete jaoks.   
Käitumine on kooskõlas projektiga või ilma selleta sisestatud kuluaruannete jaoks.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]