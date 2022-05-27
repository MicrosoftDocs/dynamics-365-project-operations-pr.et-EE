---
title: Tegelik mõju sisemisele projektile
description: Selles teemas antakse teavet microsofti sisemise projekti erinevatel üritustel tabeli Actuals mõju kohta Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579761"
---
# <a name="actuals-impact-for-an-internal-project"></a>Tegelik mõju sisemisele projektile

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Järgmises tabelis on loetletud erinevate kandetüüpide tegelikud andmed, mis on loodud projektisisese töövõtu erinevatel üritustel.

| Üritus | Tegelik kulu | Näide |
|---|---|---|
| Aeg on loodud. | Pole rakendatav | <p>Bob Kozack FABRIKAM USA organisatsiooniüksusest, mille kulumäär on 100 USA dollarit (100 USA dollarit) tunnis, töötab projekti kallal, mille nimi on "Arm Installation at Adatum". See projekt on vastendatud fikseeritud hinnaga arveldamismeetodiga lepingureal. Siin on Bob Kozaki näidisaja kirje:</p><p>Bob Kozack - 8 tundi</p> |
| Aeg on esitatud. | Pole rakendatav | Ajakande jaoks luuakse kulužurnaali rida. Vaikekulumäär sisestatakse žurnaalikandesse. |
| Ajakirje kutsutakse tagasi enne selle heakskiitmist. | Pole rakendatav | |
| Aeg on heaks kiidetud. | Luuakse tegelik kulu. | <p>Uus tegelik, mis on loodud:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800</li></ul> |
| Ajakinnitus tühistatakse. | <p>Algse kulu tegeliku korrigeerimisolek värskendatakse väärtusele **Korrigeeritud**.</p><p>Luuakse tegelik pöördkulu, mille korrigeerimisolek **on Kohandamatu**.</p> | <p>Olemasolev tegelik, mida värskendatakse:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800, *korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju ümberpööramiseks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, (8 tundi), (USD 800), *Kohandamatu*</li></ul> |
| Ajakirje kutsutakse tagasi pärast selle kinnitamist. | <p>Algse kulu tegeliku korrigeerimisolek värskendatakse väärtusele **Korrigeeritud**.</p><p>Luuakse tegelik pöördkulu, mille korrigeerimisolek **on Kohandamatu**.</p> | <p>Olemasolev tegelik, mida värskendatakse:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800, *korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju ümberpööramiseks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, (8 tundi), (USD 800), *Kohandamatu*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
