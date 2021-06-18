---
title: Hinnapakkumise sulgemine – liht
description: Selles teemas kirjeldatakse hinnapakkumise sulgemist Project Operationsis.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994131"
---
# <a name="close-a-quote---lite"></a>Hinnapakkumise sulgemine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projekti hinnapakkumise saab sulgeda kui võidetu või kaotatuna. Hinnapakkumise mustandi saab sulgeda, kuna Microsoft Dynamics 365 Project Operations ei toeta hinnapakkumiste aktiveerimise ja muutmise toiminguid.

## <a name="close-a-quote-as-won"></a>Hinnapakkumise sulgemine olekus Võidetud

Kui sulgete projekti hinnapakkumise olekuga Võidetud, määratakse olekuks Suletud ja olekuks oleku põhjuseks Võidetud. Hinnapakkumise sulgemine muudab projekti hinnapakkumise kirjutuskaitstuks ja loob projekti lepingu mustandi, mis sisaldab hinnapakkumise teavet. Kuna suletud hinnapakkumist ei saa uuesti avada, kinnitab kinnitusdialoog teie muudatused.

Kui hinnapakkumine on seotud müügivõimalusega, suletakse kõik muud müügivõimaluse projekti hinnapakkumised automaatselt kaotatud kujul.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Hinnapakkumise võidetud olekus sulgemise finantsmõju

Kui projektil on veel aja tegelikke näitajaid, kui see on hinnapakkumise mustandile lisatud, kirjendatakse ainult aja või kulu maksumust. Pärast hinnapakkumise sulgemist olekus Võidetud, refaktoorib rakendus kulud, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud. Rakendus töötleb need tegelikud kulud võttes aluseks seotud projekti lepingurea arveldusmeetodi. Kui kulu tegelikud andmed viitavad aja ja materjali lepingureale, luuakse vastavad arveldamata müügi tegelikud andmed selleks ajaks, kui hinnapakkumine suletakse ja projekti leping luuakse. Kui kulu tegelikud andmed viitavad fikseeritud hinnaga lepingureale, lõpetab rakendus nende kulu tegelike näitajate uuesti töötlemise, mis põhinevad projekti lepingu klientide jagatud arveldamise reeglitel.

## <a name="closing-a-quote-as-lost"></a>Hinnapakkumise sulgemine olekus Kaotatud:

Kui sulgete projekti hinnapakkumise olekuga Kaotatud, määratakse olekuks Suletud ja olekuks oleku põhjuseks Kaotatud. Hinnapakkumise sulgemine teeb projekti hinnapakkumise kirjutuskaitstuks. Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.

Kui projekti hinnapakkumine, mis on suletud kui Kaotatud, viitab projektile mis tahes real, märgitakse ka see projekt kui Suletud. Kõik ressursi broneeringud alates sellest päevast edasi on tühistatud.

> [!NOTE]
> Project Operationsis ei mõjuta hinnapakkumise sulgemine võidetud või kaotatud olekus müügivõimaluse seda olekut, mis jääb avatuks kuni käsitsi sulgemiseni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]