---
title: Läbisõidu seadistamine läbisõidu määra astmeid kasutades
description: Selles teemas antakse teavet nii läbisõidu määrade kui ka läbisõidu määra astmete kohta.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 030c6abca169b712312ad70ed2ac8262f3d0777bcf93dcccfd956f2f9e0ea77c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993056"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Läbisõidu seadistamine läbisõidu määra astmeid kasutades

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kui kulust teatatakse ja valitud kulukategooria on **Läbisõit**, selle kulurea summa arvutatakse vastavalt *läbisõidu määra* summale. See summa tehakse kindlaks kasutades määratletud läbisõidu astmeid või kui läbisõidu määra astmed pole häälestatud, järgides tavalist läbisõidu määra. 

Läbisõidu määra astmed saab häälestada, kui minna jaotisse **Kuluhaldus** > **Häälestamine** > **Üldine** > **Kulukategooriad** > **Läbisõit** > **Kategooria häälestamine**.

Kui pärast versioonile 10.0.18 uuendamist teie organisatsioon kasutab läbisõidu kulukategooriat, kaaluge läbisõidu funktsiooni lubamist pärast allpool kujunduse muudatuste läbivaatamist. 

Uus läbisõidu määra tasemete kujundus mõjutab seda, kuidas väärtust väljal **Kogus** töödeldakse. Enne versiooni 10.0.18 väljaandmist loeti välja **Kogus** väärtust alumiseks piirväärtuseks. Kui koondsuma selle väärtuse ületas, kasutati vastavat määra.  Alates versioonist 10.0.18 loetakse välja **Kogus** väärtust ülempiiriks. Vastavat määra kasutatakse juhul, kui läbisõidu koondarv on väiksem kui väärtus väljal **Kogus**.  Uus läbisõidu astmete mudel aitab läbisõidu astmete ülese ühtsuse ja parema kasutatavusega.   

Kõik kinnitatud kuluaruanded arvutatakse sisestamisel vastavalt uuele kujundusele ümber.

## <a name="example"></a>Näide
 
### <a name="before-version-10018"></a>Enne versiooni 10.0.18
Kahe läbisõidu määra astmega esindas kumbki aste väljal **Kogus** väiksemat läbisõidu piirväärtust. Praegu esimese astme väärtus on null (0) ja määr 0,45 ning teise astme väärtus on 1000 ja määr 0,25. Kui miilide või kilomeetrite koguarv ületab välja väärtuse, kasutatakse seostuvat määra. Kui nullkogusega rida pole, kasutab süsteem kulude halduses määratletud läbisõidu määra. 
 
Kui töötaja esitab kuluaruande 1500 miiliga, siis oleks kaks kuluaruandesse sisestatud kulurida järgmised: 1000 (määr 0,45) + 500 (määr 0,25) = 575,00.

### <a name="after-version-10018"></a>Pärast versiooni 10.0.18
Versioonis 10.0.18 tähistab iga astme väli **Kogus** astme ülempiiri. Praegu esimese astme väärtus on 999 ja määr 0,45 ning teise astme väärtus on 999 999 999,00 ja määr 0,25. Kui miilide või kilomeetrite koguarv ületab välja **Kogus** väärtuse, kasutatakse seostuvat määra. Kui kõik ülemised piirväärtused ületatakse, kasutab süsteem kulude halduses määratletud läbisõidu määra. 
 
Sama stsenaariumi õigeks arvutamiseks tuleb astme häälestust muuta. Esimese astme välja **Kogus** väärtus on 999,00 ja teise väärtus on 999 999 999,00. Kui töötaja ületab esimeses astmes olevate miilide või kilomeetrite koguse, kasutab süsteem läbisõidu määra, mis on määratletud kuluhalduses. 
  
Kui töötaja esitab kuluaruande 1500 miiliga, siis oleks kaks kuluaruandesse sisestatud kulurida järgmised: 1000 (määr 0,45) + 500 (määr 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Mitme saa määra funktsiooniga läbisõidu astme jaoks läbisõidu koguse arvutamise lubamine

Funktsioon **Mitme saa määra funktsiooniga läbisõidu astme jaoks läbisõidu koguse arvutamine** parandab läbisõidu määra arvutamist. Selle funktsiooni lubamiseks tehke järgmist.

1. Minge jaotisse **Tööruumid** > **Funktsiooni juhtimine**. 
2. Otsige loendist üles ja valige suvand **Mitme saa määra funktsiooniga läbisõidu astme jaoks läbisõidu koguse arvutamine** ja valige seejärel nupp **Luba kohe**.

Pärast funktsiooni lubamist lähtestage algsed läbisõidu astmed õigetele, et need kajastaksid välja **Kogus** väärtust õigesti. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
