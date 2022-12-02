---
title: Tegelike näitajate mõju fikseeritud hinna kaasamises
description: See artikkel annab teavet fikseeritud hinnaga tehingu elutsükli jooksul toimunud erinevate sündmuste kohta tegelike näitajate tabelis rakenduses Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918123"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Tegelike näitajate mõju fikseeritud hinna kaasamises

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Järgmises tabelis on loetletud erinevate tehingutüüpide tegelikud näitajad, mis luuakse erinevatel sündmustel fikseeritud hinnaga tehinguga.

| Üritus | Tegelik kulu | Arveldamata tegelik müük | Arveldatud müügi tegelik näitaja | Näide |
|---|---|---|---|---|
| Aeg on loodud. | Pole rakendatav | Pole rakendatav | Pole rakendatav | <p>Bob Kozack USA organisatsiooniüksusest Fabrikam, mille kulumäär on 100 USA dollarit (100 USD) tunnis, töötab projektiga, mille nimi on „Arm Installation at Adatum“. Selle projekti puhul kasutatakse lepingureal fikseeritud hinnaga arveldusmeetodit. Siin on Bob Kozaki näidisaja sissekanne:</p><p>Bob Kozack – 8 tundi</p> |
| Aeg on esitatud. | Pole rakendatav | Pole rakendatav | Pole rakendatav | Kulu töölehele kandmine aja sissekande jaoks. Vaikimisi kulumäär sisestatakse töölehe reale. |
| Aja sissekanne on enne kinnitamist tagasi võetud. | Pole rakendatav | Pole rakendatav | Pole rakendatav | |
| Aeg on kinnitatud. | Kulu tegelik näitaja on loodud. | Pole rakendatav | Pole rakendatav | <p>Uus tegelik, mida luuakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD</li></ul> |
| Aja kinnitus on tühistatud. | <p>Algse kulu tegeliku näitaja korrigeerimise olek on värskendatud väärtusele **Korrigeeritud**.</p><p>Luuakse pöördkulu tegelik näitaja, mille korrigeerimise olek on **Korrigeerimata**.</p> | Pole rakendatav | Pole rakendatav | <p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju tühistamiseks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, (8 tundi), (800 USD), *Korrigeerimata*</li></ul> |
| Aja sissekanne on pärast kinnitamist tagasi võetud. | <p>Algse kulu tegeliku näitaja korrigeerimise olek on värskendatud väärtusele **Korrigeeritud**.</p><p>Luuakse pöördkulu tegelik näitaja, mille korrigeerimise olek on **Korrigeerimata**.</p> | Pole rakendatav | Pole rakendatav | <p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju tühistamiseks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, (8 tundi), (800 USD), *Korrigeerimata*</li></ul> |
| Leping on kinnitatud. | <p>Vana kulu tegelike näitajate korrigeerimise olek on värskendatud väärtusele **Korrigeeritud**.</p><p>Luuakse pöördkulu tegelikud näitajad, mille korrigeerimise olek on **Korrigeerimata**.</p><p>Uue kulu tegelikud näitajad luuakse pärast lepinguliste reeglite ümberhindamist.</p> | Pole rakendatav | Pole rakendatav | <p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju tühistamiseks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, (8 tundi), (800 USD), *Korrigeerimata*</li></ul><p>Uus tegelik näitaja, mis luuakse ümberhinnatud finantsmõju jaoks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD</li></ul> |
| Arve on loodud. | Pole rakendatav | Pole rakendatav | Pole rakendatav | |
| Arve kinnitatakse vahekokkuvõttega. | Pole rakendatav | Pole rakendatav | Luuakse uued vahekokkuvõttepõhiste müügiarvete tegelikud näitajad. | <p>Olemasolev tegelik näitaja, mis jääb muutumatuks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD</li></ul><p>Uus tegelik näitaja, mis luuakse arveldatud müügiväärtuste kirjendamiseks:</p><ul><li>**Arveldatud müügi tegelik näitaja:** vahekokkuvõte, 5000 USD</li></ul> |
| Arvet parandatakse, et krediteerida vahekokkuvõtet. | Pole rakendatav | Pole rakendatav | Ümberarveldatud müügi tegelikud näitajad on loodud: | <p>Olemasolev tegelik näitaja, mis jääb muutumatuks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD</li></ul><p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Arveldatud müügi tegelik näitaja:** vahekokkuvõte, 5000 USD, *korrigeeritud*</li></ul><p>Uus tegelik näitaja, mis luuakse eelmiste arveldatud müügiväärtuste ümberpööramiseks:</p><ul><li>**Arveldatud müügi tegelik näitaja:** vahekokkuvõte, (5000 USD),*korrigeerimatu*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
