---
title: Avansimakse
description: Selles teemas antakse teavet avansimaksete kohta.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988511"
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

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Valige kuludele rakenduvad sularahaettemaksed
Enne kuluaruande saatmist saate valida sularahaettemakse, mis ühtib aruande kulutehingutega. Selle funktsiooni kasutamiseks tuleb tööruumis **Funktsiooni haldamine** järgmised kaks funktsiooni lubada.

  - Ümberkujundatud kuluaruanded
  - Võime vastendada sularaha ettemaksed kuluridadega
 
 Kui need funktsioonid on lubatud, tehke järgmist.
 
  - Iga kulurea kohta saate ühe või mitu sularahaettemakset.
  - Sularahaettemaks saadaolev saldo on kuluaruande salvestamisel reaalajas nähtav. See võimaldab teil töödelda kulutehinguid ja samal ajal sularahatehinguid tagastada.
  - Ühe kulukande kohta saate valida mitu sularahaettemakset.
  - Sularahaettemakse vastavusandmed on kättesaadavad päringut kasutades. 
 
Kui te neid funktsioone ei kasuta, jäävad funktsioonid samaks, kus olemasolevad sularahaettemaksed vähenevad pärast kulu esitamist automaatselt.

### <a name="example"></a>Näide 
Plaanite reisida Seattle'ist New Yorki konverentsile. Loote avansitaotluse 3000 USD-le, mis põhineb konverentsi pileti, lendude, hotelli, einestamise ja takso prognoositavatel kuludel. Teile ei maksta, kui teie haldur taotlust ei kinnita. Pärast juhi poolt heaks kiitmist makstakse taotletud avansimakse 600 eurot teie pangaokntole. Te osalete seejärel konverentsil. Pärast reisi lõppemist saate teada, et kulude kogusumma oli vaid 570 eurot. Valige **Raha** väljal **Makseviis** ja sisestage oma kulud summas 2790.00 USD. Teie esitatud kulusummat muudetakse automaatselt teile laenatud avansimakse 600 euro suhtes. Nüüd võlgnete vahe 210.00 USD (3000.00 - 2790.00), mille saate ettevõttele tagastada, kasutades kulukategooriat **Raha tagastamine**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
