---
title: Kontsernisisesed kulud
description: Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks. Sellisel juhul saate kasutada kontsernisiseste kulude funktsiooni, et määrata töötaja kulud juriidilisele olemile, mille jaoks tööd tehti.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075107"
---
# <a name="intercompany-expenses"></a>Kontsernisisesed kulud

[!include [banner](../includes/banner.md)]

Töötaja, kelle on organisatsiooni üks juriidiline olem tööle võtnud, võib teha tööd mõne muu sama organisatsiooni juriidilise olemi jaoks. Sellisel juhul saate kasutada kontsernisiseste kulude funktsiooni, et määrata töötaja kulud juriidilisele olemile, mille jaoks tööd tehti. Juriidilist olemit, mille jaoks töötaja töötab, nimetatakse laenavaks juriidiliseks olemiks. Juriidilist olemit, mille jaoks töötaja kulusid kannab, nimetatakse laenajast juriidiliseks olemiks. 

Enne, kui töötaja saab luua ja esitada mõne muu juriidilise olemi jaoks tehtud töö kulud, valige laenava juriidilise olemi jaoks lehel **Kuluhalduse parameetrid** suvand **Luba kontsernisiseste kulude read**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Kontsernisiseste kulude maksude sisestamine

[!include [banner](../includes/banner.md)]

Kui soovite oma kuluaruandes kasutada laenava (algne) juriidilise olemiga seotud maksurühmasid, mitte laenajast (lähte) juriidilise olemiga, peate selle konfigureerima pearaamatu käibemaksu seadistamisel. Kui pearaamatu parameetriks **Kontsernisisese maksu sisestamise juriidiline olem** on seatud **Algne** ja suvandi **Rakenda käibemaksu maksustamise reegleid** väärtuseks on **Ei** , kasutatakse laenava juriidilise olemi jaoks maksu kombinatsiooni. Kui sama parameetri väärtuseks on seatud **Lähte** , kasutatakse laenajast juriidilise olemi jaoks maksu kombinatsiooni. Ameerika Ühendriikide juriidilistele olemitele, kui parameetri väärtuseks on seatud **Algne** , peab väli **käibemaks laekumata** olema konfigureeritud ka uuel lehel **Pearaamatusse sisestamise rühmad**. Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamisandmete jaoks.   
Käitumine on kooskõlas projektiga või ilma selleta sisestatud kuluaruannete jaoks.  
