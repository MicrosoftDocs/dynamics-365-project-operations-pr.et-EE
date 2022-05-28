---
title: Projekti hankija arve tühistamine
description: Selles teemas selgitatakse, kuidas tühistada projekti hankija arve Microsoftis Dynamics 365 Project Operations ja projekti hankija arve tühistamise finantsmõju.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580635"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekti hankija arve tühistamine

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Pärast hankija arve kinnitamist ei saa seda redigeerida ega kustutada. Kui kinnitatud hankija arvel ilmnes tõrge, saate hankija arve mõju ümberpööramiseks ja uue hankijaarve loomiseks kasutada toimingut Tühista.

Kui valite hankija arvel suvandi **Tühista**, ilmneb järgmine käitumine.

1. Hankija arve olek värskendatakse olekusse **Tühistatud**.
2. Tühistatud hankija arve ja sellega seotud kirjed muutuvad kirjutuskaitstuks ning neid ei saa redigeerida ega kustutada.
3. Kõik hankija arve kinnitusel hankija arve ridadel loodud kulu tegelikud andmed tühistatakse.
4. Kui sobitamisprotsessi käigus lingiti hankija arve ridadega mis tahes kulu tegelikud andmed, tühistas algne hankija arve kinnitus need. Hankija arve tühistamise ajal luuakse need kulu tegelikud andmed uuesti. Päritolu viitab aja-, kulu- või materjalikasutuse kannetele.
5. Pärast hankija arve tühistamist saate taas luua parandusžurnaalid, töödelda ajakande tagasikutsumist ja tühistada algse aja, kulu või materjali tegeliku kinnitamise.

> [!NOTE]
> Tühistada saab ainult kinnitatud projekti hankija arveid. Hankija arveid teistes riikides ei saa tühistada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
