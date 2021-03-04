---
title: Avansimakse
description: Selles teemas antakse teavet avansimaksete kohta.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098879"
---
# <a name="cash-advance"></a>Avansimakse

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Avansimakse võimaldab töötajatel laenata oma ettevõttelt raha enne mis tahes kulude tekkimist. Kui taotletud avansimakse on kinnitatud ja makstud, saab töötaja kasutada raha ärikulude jaoks, mis neil on tekkimas. 

## <a name="create-and-submit-a-cash-advance-request"></a>Avansimakse taotluse loomine ja esitamine
Uue avansimakse loomiseks ja avansimakse taotluse esitamiseks toimige järgmiselt. 

1. Valige jaotises **Minu kulud** valik **Avansimaksed** > **Uus**. 
2. Sisestage lehel **Uus avansimakse taotlus** kulu eesmärk ja valige koht, kus kulu tekib.
3. Sisestage soovitud summa ja valuuta ning valige seejärel **Salvesta**. 
4. Kui olete valmis avansimakse taotlust esitama, valige lehel **Avansimakse taotlus** suvand **Töövoog** > **Esita**.

## <a name="modify-a-cash-advance-request"></a>Avansimakse taotluse muutmine

Kiu avansimakse taotlus ei ole kinnitamiseks esitatud, saate seda muuta.

1. Leidke ja valige jaotises **Minu kulud: avansimaksed** see avansimakse, mida soovite redigeerida.
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

Kui loote ja esitate juba saadud avansimakse jaoks kuluaruande, korrigeeritakse kulud automaatselt avansimakse suhtes. Kui teie avansimakse on suurem kui kulutatud summa, peate tagastama saldo ettevõttele, kasutades kulukategooriat **Tagastatud raha**. Kui ettevõtte makstud avansimakse on väiksem, kui teil kulunud summa, peab ettevõtte saldo teile tagasi maksma. 

### <a name="example"></a>Näide
Plaanite reisida Seattle'ist New Yorki konverentsile. Loote avansitaotluse 3000 USD-le, mis põhineb konverentsi pileti, lendude, hotelli, einestamise ja takso prognoositavatel kuludel. Teile ei maksta, kui teie haldur taotlust ei kinnita. Pärast juhi poolt heaks kiitmist makstakse taotletud avansimakse 600 eurot teie pangaokntole. Te osalete seejärel konverentsil. Pärast reisi lõppemist saate teada, et kulude kogusumma oli vaid 570 eurot. Valige **Raha** väljal **Makseviis** ja sisestage oma kulud summas 2790.00 USD. Teie esitatud kulusummat muudetakse automaatselt teile laenatud avansimakse 600 euro suhtes. Nüüd võlgnete vahe 210.00 USD (3000.00 - 2790.00), mille saate ettevõttele tagastada, kasutades kulukategooriat **Raha tagastamine**.

