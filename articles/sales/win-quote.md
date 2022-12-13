---
title: Projektipõhiste hinnapakkumiste sulgemine
description: See artikkel annab teavet hinnapakkumiste sulgemise kohta rakenduses Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b35417d4258a1e837fdf7a61bbcc303ec04a900
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824211"
---
# <a name="close-project-based-quotes"></a>Projektipõhiste hinnapakkumiste sulgemine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Projekti hinnapakkumise saab sulgeda kui **võidetud või** kaotatud **·**. 

## <a name="close-a-quote-as-won"></a>Hinnapakkumise sulgemine olekus Võidetud

Võidetud projekti hinnapakkumise sulgemine seab hinnapakkumise olekuks **Suletud** ja oleku põhjuseks **Võidetud**. Hinnapakkumiste sulgemine muudab selle kirjutuskaitstuks ja loob projekti lepingu mustandi koos kogu hinnapakkumise teabega. Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.

Projekti hinnapakkumise põhjal loodud projekti leping tehakse kättesaadavaks ka Project Operationsi Projektijuhtimise ja raamatupidamise moodulis. Kui projekti lepingut pole vastendatud projektiga ühelgi selle real, tehakse selle projekti leping passiivse projekti lepinguna saadaolevaks ja aktiveeritakse kohe, kui projekt on vastendatud vähemalt ühele selle lepingureale.

Kui hinnapakkumine on seotud müügivõimalusega, suletakse kõik muud müügivõimaluse projekti hinnapakkumised automaatselt kaotatud kujul.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Hinnapakkumise võidetud olekus sulgemise finantsmõju

Kui projektile on salvestatud tegelikke ajanäitajaid, kui see oli veel hinnapakkumise projektile lisatud, kirjendatakse ainult aja või kulutuse kulu. Pärast hinnapakkumise sulgemist olekus Võidetud, refaktoorib rakendus kulud, pöörates tagasi vanemad tegelikud kulud ja luues uued tegelikud kulud. Rakendus töötleb need tegelikud kulud võttes aluseks seotud projekti lepingurea arveldusmeetodi. Kui tegelik kulu viitab aja- ja materjalikulu lepingureale, loob süsteem hinnapakkumise sulgemisel ja projekti lepingu loomisel automaatselt vastavad arveldamata müügi tegelikud näitajad. Kui tegelik kulu viitab fikseeritud hinnaga lepingureale, peatab rakendus projekti lepingu klientide jaoks jaotatud arvete esitamise reeglitega seotud tegelike kulude ümbertöötlemise.

Kõik ümbertöödeldud tegelikud näitajad on saadaval Projektijuhtimise ja raamatupidamise moodulis projekti raamatupidajale ülevaatamiseks, värskendamiseks ja pearaamatusse sisestamiseks. 

## <a name="close-a-quote-as-lost"></a>Hinnapakkumise sulgemine olekus Kaotatud

Kaotatud projekti hinnapakkumise sulgemine seab hinnapakkumise olekuks **Suletud** ja oleku põhjuseks **Kaotatud**. Hinnapakkumise sulgemine muudab selle kirjutuskaitstuks. Kuna suletud hinnapakkumist ei saa uuesti avada, siis palutakse hinnapakkumise sulgemisel muudatused kinnitada.

Kui kaotatud projekti hinnapakkumise mistahes ridadel on viidatud projektile, märgitakse ka see projekt suletuks ja mistahes ressursside broneeringud alates sellest päevast tühistatakse.

> [!NOTE]
> Project Operationsis ei mõjuta hinnapakkumise sulgemine võidetud või kaotatud olekus müügivõimaluse seda olekut, mis jääb avatuks kuni käsitsi sulgemiseni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
