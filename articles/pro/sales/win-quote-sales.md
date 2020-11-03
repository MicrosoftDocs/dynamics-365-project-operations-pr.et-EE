---
title: Hinnapakkumiste sulgemine
description: Selles teemas kirjeldatakse hinnapakkumise sulgemist Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074877"
---
# <a name="close-quotes"></a>Hinnapakkumiste sulgemine 

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projekti hinnapakkumise saab sulgeda kui võidetu või kaotatuna. Rakenduses Microsoft Dynamics 365 Project Operations ei toetata aktiveerimise ja muutmise toiminguid, seega saab hinnapakkumise mustandi sulgeda.

## <a name="close-a-quote-as-won"></a>Hinnapakkumise sulgemine olekus Võidetud

Võidetud projekti hinnapakkumise sulgemine suleb hinnapakkumise olekus Suletud ja oleku põhjuseks on määratud Võidetud. Hinnapakkumise sulgemine muudab projekti hinnapakkumise kirjutuskaitstuks ja loob projekti lepingu mustandi, mis sisaldab hinnapakkumise teavet. Kuna suletud hinnapakkumist ei saa uuesti avada ja muudatused on pöördumatud, kuvatakse kinnitamise dialoogiaken.

Kui hinnapakkumine on seotud müügivõimalusega, suletakse kõik muud müügivõimaluse projekti hinnapakkumised automaatselt kaotatud kujul.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Hinnapakkumise võidetud olekus sulgemise finantsmõju

Kui projektile on salvestatud tegelikke ajanäitajaid, kui see oli veel hinnapakkumise projektile lisatud, kirjendatakse ainult aja või kulutuse kulu. Pärast hinnapakkumise sulgemist olekus Võidetud, refaktoorib rakendus kulud, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud. Rakendus töötleb need tegelikud kulud võttes aluseks seotud projekti lepingurea arveldusmeetodi. Kui tegelik kulu viitab aja- ja materjalikulu lepingureale, loob süsteem hinnapakkumise sulgemisel ja projekti lepingu loomisel automaatselt vastavad arveldamata müügi tegelikud näitajad. Kui tegelik kulu viitab fikseeritud hinnaga lepingureale, peatab rakendus projekti lepingu klientide jaoks jaotatud arvete esitamise reeglitega seotud tegelike kulude ümbertöötlemise.

## <a name="closing-a-quote-as-lost"></a>Hinnapakkumise sulgemine olekus Kaotatud:

Kaotatud projekti hinnapakkumise sulgemine seab hinnapakkumise olekuks Suletud ja oleku põhjuseks Kaotatud. Hinnapakkumise sulgemine teeb projekti hinnapakkumise kirjutuskaitstuks. Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.

Kui kaotatud projekti hinnapakkumise mistahes ridadel on viidatud projektile, märgitakse ka see projekt suletuks ja mistahes ressursside broneeringud alates sellest päevast tühistatakse.

> [!NOTE]
> Project Operationsis ei mõjuta hinnapakkumise sulgemine võidetud või kaotatud olekus müügivõimaluse seda olekut, mis jääb avatuks kuni käsitsi sulgemiseni.
