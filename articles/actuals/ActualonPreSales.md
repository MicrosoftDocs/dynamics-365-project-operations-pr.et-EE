---
title: Tegelike näitajate mõju kaasamise müügieelse etapi ajal
description: See artikkel annab teavet tegelike andmete tabelis toimunud erinevate sündmuste mõju kohta, kui tehing on Microsoft Dynamics 365 Project Operations-i müügitegevuse eelstaadiumis.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922355"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Tegelike näitajate mõju kaasamise müügieelse etapi ajal

_**Rakendub:** Project Operationsi ressursipõhiste/mittelaopõhiste stsenaariumide korral, lihtjuurutamine – tehing näidisarveldusele_

Järgmises tabelis on loetletud erinevate tehingutüüpide tegelikud andmed, mis luuakse erinevatel sündmustel projekti kaasamise müügieelses etapis.

| Üritus | Tegelik kulu | Näide |
|---|---|---|
| Aeg on loodud. | Pole rakendatav | <p>Bob Kozack USA organisatsiooniüksusest Fabrikam, mille kulumäär on 100 USA dollarit (100 USD) tunnis, töötab projektiga, mille nimi on „Arm Installation at Adatum“. Selle projekti puhul kasutatakse lepingureal fikseeritud hinnaga arveldusmeetodit. Siin on Bob Kozaki näidisaja sissekanne:</p><p>Bob Kozack – 8 tundi</p> |
| Aeg on esitatud. | Pole rakendatav | Kulu töölehele kandmine aja sissekande jaoks. Vaikimisi kulumäär sisestatakse töölehe reale. |
| Aja sissekanne on enne kinnitamist tagasi võetud. | Pole rakendatav | |
| Aeg on kinnitatud. | Kulu tegelik näitaja on loodud. | <p>Uus tegelik, mida luuakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD</li></ul> |
| Aja kinnitus on tühistatud. | <p>Algse kulu tegeliku näitaja korrigeerimise olek on värskendatud väärtusele **Korrigeeritud**.</p><p>Luuakse pöördkulu tegelik näitaja, mille korrigeerimise olek on **Korrigeerimata**.</p> | <p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju tühistamiseks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, (8 tundi), (800 USD), *Korrigeerimata*</li></ul> |
| Aja sissekanne on pärast kinnitamist tagasi võetud. | <p>Algse kulu tegeliku näitaja korrigeerimise olek on värskendatud väärtusele **Korrigeeritud**.</p><p>Luuakse pöördkulu tegelik näitaja, mille korrigeerimise olek on **Korrigeerimata**.</p> | <p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju tühistamiseks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, (8 tundi), (800 USD), *Korrigeerimata*</li></ul> |
| Hinnapakkumine võidetakse ja sõlmitakse leping. | <p>Vana kulu tegelike näitajate korrigeerimise olek on värskendatud väärtusele **Korrigeeritud**.</p><p>Luuakse pöördkulu tegelikud näitajad, mille korrigeerimise olek on **Korrigeerimata**.</p><p>Uue kulu tegelikud näitajad luuakse pärast lepinguliste reeglite ümberhindamist.</p> | <p>Olemasolev tegelik näitaja, mida värskendatakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD, *Korrigeeritud*</li></ul><p>Uus tegelik, mis luuakse eelmise finantsmõju tühistamiseks:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, (8 tundi), (800 USD), *Korrigeerimata*</li></ul><p>Uued tegelikud andmed, mis luuakse ümberhinnatud finantsmõju jaoks, kui hinnapakkumine võidetakse ja leping sõlmitakse:</p><ul><li>**Kulu tegelik näitaja:** Bob Kozack, 8 tundi, 800 USD</li><li>**Arveldamata müügi tegelik näitaja:** Bob Kozack, 8 tundi, 1600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
