---
title: Projekti hankija arve tühistamine
description: See artikkel selgitab, kuidas tühistada projekti hankija arve teenuses Microsoft Dynamics 365 Project Operations ja projekti hankija arve tühistamise finantsmõju.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261085"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekti hankija arve tühistamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Pärast hankija arve kinnitamist ei saa seda muuta ega kustutada. Kui kinnitatud hankija arvel ilmnes viga, saate hankija arve mõju tühistamiseks ja uue hankija arve loomiseks kasutada tegevust Tühista.

Kui valite hankija arvel käsu **Tühista**, ilmneb järgmine käitumine.

1. Hankija arve olekuks värskendatakse **Tühistatud**.
2. Tühistatud hankija arve ja sellega seotud kirjed muutuvad kirjutuskaitstuks ning neid ei saa muuta ega kustutada.
3. Kõik kulu tegelikud näitajad, mis loodi hankija arve ridade alusel hankija arve kinnitamise osana, tühistatakse.
4. Kui mis tahes kulude tegelikud näitajad on lingitud hankija arve ridadega võrdlusprotsessi osana, muutis algse hankija arve kinnitus need ümber. Hankija arve tühistamise ajal luuakse need kulu tegelikud näitajad uuesti. Lähtepunktid viitavad aja-, kulu- või materjalikasutuse kirjetele.
5. Pärast hankija arve tühistamist saate taas luua paranduspäevikuid, töödelda aja sissekannete tagasikutseid ja tühistada esialgse aja, kulu või materjalide tegelike näitajate kinnitamise.

> [!NOTE]
> Tühistada saab ainult kinnitatud projekti hankija arveid. Teiste osariikide hankija arveid ei saa tühistada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
