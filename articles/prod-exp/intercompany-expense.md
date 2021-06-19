---
title: Kontsernisisesed kulud
description: Selles teemas kirjeldatakse, kuidas kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005066"
---
# <a name="intercompany-expenses"></a>Kontsernisisesed kulud

Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks. Saate kasutada kontsernisiseseid kulusid töötaja kulude määramiseks juriidilisele isikule, kelle jaoks töö tehti. Juriidilist olemit, mille jaoks töötaja töötab, nimetatakse laenavaks juriidiliseks olemiks. Juriidilist olemit, mille jaoks töötaja kulusid kannab, nimetatakse laenajast juriidiliseks olemiks. 

Enne töötaja saab luua ja esitada kontsernisiseseid kulusid, peate lubama kontsernisiseste kulude read. Valige laenava juriidilise isiku lehel **Kuluhalduse parameetrid** suvand **Luba kontsernisisesed kuluread**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Kontsernisiseste kulude maksude sisestamine

[!include [banner](../includes/banner.md)]

Enne kui saate kuluaruandes kasutada laenava (allika) juriidilise isikuga seotud maksurühmi, mitte vastuvõtva (siht) juriidilise isiku omi, peate lubama selle funktsionaalsuse pearaamatu käibemaksu seadistuses. Kui parameeter **Juriidiline isik kontsernisisese maksusisestuse jaoks** on määratud olekusse **Allikas** ja **Rakenda käibemaksuga maksustamise reegleid** on määratud olekusse **Ei**, kasutatakse laenava juriidilise üksuse maksukombinatsiooni. Kui sama parameetri väärtuseks on seatud **Lähte**, kasutatakse laenajast juriidilise olemi jaoks maksu kombinatsiooni. Ameerika Ühendriikide juriidilistele olemitele, kui parameetri väärtuseks on seatud **Algne**, peab väli **käibemaks laekumata** olema konfigureeritud ka uuel lehel **Pearaamatusse sisestamise rühmad**. Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamisandmete jaoks.   
Käitumine on kooskõlas projektiga või ilma selleta sisestatud kuluaruannete jaoks.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]