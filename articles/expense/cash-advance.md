---
title: Avansimakse
description: Selles teemas antakse teavet avansimaksete kohta.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908048"
---
# <a name="cash-advance"></a>Avansimakse

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Avansimakse võimaldab töötajatel laenata oma ettevõttelt raha enne mis tahes kulude tekkimist. Kui taotletud avansimakse on kinnitatud ja makstud, saab töötaja kasutada raha ärikulude jaoks, mis neil on tekkimas. 

## <a name="create-and-submit-a-cash-advance-request"></a>Avansimakse taotluse loomine ja esitamine

1. Uue avansimakse loomiseks valige jaotises **Minu kulud** suvand **Avansimaksed** > **Uus**. 
2. Sisestage lehel **Uus avansimakse taotlus** kulu eesmärk ja valige koht, kus kulu tekib.
3. Sisestage soovitud summa ja valuuta ning valige seejärel **Salvesta**. 
4. Kui olete valmis avansimakse taotlust esitama, valige lehel **Avansimakse taotlus** suvand **Töövoog** > **Esita**.

## <a name="modify-a-cash-advance-request"></a>Avansimakse taotluse muutmine

Kiu avansimakse taotlus ei ole kinnitamiseks esitatud, saate seda muuta.

1. Leidke ja valige jaotises **Minu kulud: avansimaksed** avansimakse, mida soovite muuta.
2. Valige **Redigeeri** ja tehke avansimakse taotlusele vajalikud muudatused. 
3. Valige **Salvesta ja sule**.


## <a name="view-cash-advance-requests"></a>Avansimaksete taotluste vaatamine
Saate vaadata jaotises **Minu kulud: avandimaksed** loendit kõikides avansimaksetes, mis on mustandid, esitatud, läbivaatamisel või makstud. 

## <a name="approve-cash-advance-requests"></a>Avansimaksete taotluste kinnitamine

Juhid või töövoos kinnitajatena konfigureeritud kasutajad saavad neile läbivaatamiseks esitatud avansimakseid kinnitada. 

1. Avansimakse kinnitamiseks valige jaotises **Avansimaksete töötlemine** suvand **Avansimaksed minule läbivaatamiseks**.
2. Valige avansimakse, mille soovite läbi vaadata, ja valige **Kinnita**.  

## <a name="pay-cash-advances"></a>Avansimaksete maksmine 
Järgmise toimingu teeb tavaliselt raamatupidaja või kasutaja, kellel on raamatupidamise õigused.

1. Heaks kiidetud avansimaksete postitamiseks valige **Kinnitatud avansimaksed** ja valige seejärel **Maksmine ja ülekandmine**.  
2. Sisestage avansimaksetele töölehe üksikasjad ja valige seejärel **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Makstud avansimakse kuluaruande esitamine 

Kui loote ja esitate kuluaruande avansimakse jaoks, mille olete juba kätte saanud, muudetakse kulusid automaatselt selle avansimakse suhtes. Kui teie avansimakse on suurem kui kulutatud summa, peate tagastama saldo ettevõttele, kasutades kulukategooriat **Tagastatud raha**. Kui ettevõtte makstud avansimakse on kulutatud summast väiksem, peab ettevõtte saldo teile tagasi maksma. 

### <a name="example"></a>Näide
Plaanite reisida Tartust Tallinnasse konveretsile. Lõite avansimakse taotluse summas 600 eurot, kuna te eeldasite, et konverentsi pileti, transpordi, totelli, toidu ja takso peale kulub umbes selline summa. Teile ei maksta enne, kui juht selle taotluse heaks kiidab. Pärast juhi poolt heaks kiitmist makstakse taotletud avansimakse 600 eurot teie pangaokntole. Te osalete seejärel konverentsil. Pärast reisi lõppemist saate teada, et kulude kogusumma oli vaid 570 eurot. Valige välja **Maksevoos** jaotis **Makse** ja esitage oma kulud 570 eurot. Teie esitatud kulusummat muudetakse automaatselt teile laenatud avansimakse 600 euro suhtes. Nüüd te võlgnete ettevõttele 30 eurot (600–570), mille saate tagastada ettevõttele kulukategooriat **Tagastusraha** kasutades. 
