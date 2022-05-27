---
title: Tegelik mõju fikseeritud hinna kaasamisele
description: Selles teemas antakse teavet selle kohta, millist mõju avaldab microsofti fikseeritud hinnaga seotuse elutsükli jooksul erinevatel üritustel tabelile Actuals Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579223"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Tegelik mõju fikseeritud hinna kaasamisele

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Järgmises tabelis on loetletud erinevate kandetüüpide tegelikud andmed, mis on loodud fikseeritud hinnaga töövõtu erinevatel üritustel.

| Üritus | Tegelik kulu | Arveldamata tegelik müük | Arveldatud müük on tegelik | Näide |
|---|---|---|---|---|
| Aeg on loodud. | Pole rakendatav | Pole rakendatav | Pole rakendatav | <p>Bob Kozack FABRIKAM USA organisatsiooniüksusest, mille kulumäär on 100 USA dollarit (100 USA dollarit) tunnis, töötab projekti kallal, mille nimi on "Arm Installation at Adatum". See projekt on vastendatud fikseeritud hinnaga arveldamismeetodiga lepingureal. Siin on Bob Kozaki näidisaja kirje:</p><p>Bob Kozack - 8 tundi</p> |
| Aeg on esitatud. | Pole rakendatav | Pole rakendatav | Pole rakendatav | Ajakande jaoks luuakse kulužurnaali rida. Vaikekulumäär sisestatakse žurnaalikandesse. |
| Ajakirje kutsutakse tagasi enne selle heakskiitmist. | Pole rakendatav | Pole rakendatav | Pole rakendatav | |
| Aeg on heaks kiidetud. | Luuakse tegelik kulu. | Pole rakendatav | Pole rakendatav | <p>Uus tegelik, mis on loodud:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800</li></ul> |
| Aja kinnitamine tühistatakse. | <p>Algse kulu tegeliku korrigeerimisolek värskendatakse väärtusele **Korrigeeritud**.</p><p>Luuakse tegelik pöördkulu, mille korrigeerimisolek **on Kohandamatu**.</p> | Pole rakendatav | Pole rakendatav | <p>Olemasolev tegelik, mida värskendatakse:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800, *korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju ümberpööramiseks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, (8 tundi), (USD 800), *Kohandamatu*</li></ul> |
| Ajakirje kutsutakse tagasi pärast selle kinnitamist. | <p>Algse kulu tegeliku korrigeerimisolek värskendatakse väärtusele **Korrigeeritud**.</p><p>Luuakse tegelik pöördkulu, mille korrigeerimisolek **on Kohandamatu**.</p> | Pole rakendatav | Pole rakendatav | <p>Olemasolev tegelik, mida värskendatakse:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800, *korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju ümberpööramiseks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, (8 tundi), (USD 800), *Kohandamatu*</li></ul> |
| Leping on kinnitatud. | <p>Vanade kuluarvude korrigeerimisolek värskendatakse väärtusele **Korrigeeritud**.</p><p>Luuakse ümberpööratud kulu tegelikud summad, mille korrigeerimisolek **on Kohandamatu**.</p><p>Uued kulu tegelikud andmed luuakse pärast lepingureeglite ümberhindamist.</p> | Pole rakendatav | Pole rakendatav | <p>Olemasolev tegelik, mida värskendatakse:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800, *korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju ümberpööramiseks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, (8 tundi), (USD 800), *Kohandamatu*</li></ul><p>Uus tegelik, mis luuakse ümberhinnatud finantsmõju jaoks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800</li></ul> |
| Luuakse arve. | Pole rakendatav | Pole rakendatav | Pole rakendatav | |
| Arve kinnitatakse verstapostiga. | Pole rakendatav | Pole rakendatav | Luuakse uued verstapostil põhinevad arveldatud müügi tegelikud andmed. | <p>Olemasolev tegelik, mis jääb muutumatuks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, USD 800</li></ul><p>Uus tegelik, mis luuakse arveldatud müügiväärtuste kirjendamiseks.</p><ul><li>**Arveldatud müük tegelik:** verstapost, USD 5,000</li></ul> |
| Arve parandatakse verstaposti krediteerimiseks. | Pole rakendatav | Pole rakendatav | Luuakse ümberpööratud arveldatud müügi tegelikud andmed. | <p>Olemasolev tegelik, mis jääb muutumatuks:</p><ul><li>**Maksumus tegelik:** Bob Kozack, 8 tundi, 800 USD</li></ul><p>Olemasolev tegelik, mida värskendatakse:</p><ul><li>**Arveldatud müük tegelik:** verstapost, USD 5,000, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmiste arveldatud müügiväärtuste tühistamiseks.</p><ul><li>**Arveldatud müük tegelik:** verstapost (USD 5000), *Korrigeerimatu*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
