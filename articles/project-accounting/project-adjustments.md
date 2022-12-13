---
title: Projekti kohandused
description: Selles artiklis antakse teavet projekti korrigeerimiste kohta.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788363"
---
# <a name="project-adjustments"></a>Projekti kohandused

_**Kehtib järgmiste puhul:** Project Operations ladustamise-/tootmispõhiste stsenaariumide jaoks_

## <a name="adjustments-overview"></a>Kohanduste ülevaade

Saate Microsofti Dynamics 365 Project Operations konfigureerida nii, et kasutajad saaksid sisestatud kannetes muudatusi teha. Saate projektikandeid ükshaaval kohandada või valida kõigi projektikannete loendist korraga mitu kannet. Projekti korrigeerimisi kasutatakse näiteks arveldatava oleku massvärskendamiseks, kulu ümberarvutamiseks pärast konfiguratsiooni muutmist või rahastamisallikate värskendamiseks.

Kasutajad pääsevad projekti kohandamise funktsioonile juurde mitmel viisil.

- Kasutades **lehte Kannete** korrigeerimine, millele pääseb juurde projektihalduse ja raamatupidamise **seadistusest** \> **·**.
- Kasutades **lehel Sisestatud projektikanded** nuppu **Korrigeerimine**, millele pääseb juurde projektihalduse ja **raamatupidamiskannete** \> **kaudu**.
- Kasutades **projekti kontekstis nupu Korrigeerimine** lehel Sisestatud projekti **kanded** . Sellele lehele pääseb juurde projektijuhtimisest **ja raamatupidamisest** \> **Kõik projektid**.

Korrigeerimiste lubamiseks peate lubama ühe või mitu kande olekut rakendusest **Projektihaldus ja raamatupidamine Projektijuhtimine ja raamatupidamine** \> **vahekaardil** **Üldine,** jaotises **Luba kande oleku** korrigeerimine. Kannete olekute näideteks on sisestatud kanded, arveldatud kanded või eemaldatud kanded. Mis tahes kande olekus, mille väärtuseks on seatud **Ei**, on selles olekus kandeid, mida korrigeerimisprotsessis korrigeerimiseks valitavatena ei kuvata.

Konfiguratsioonisuvand nimega **Loo korrigeerimiskanne** on praegu saadaval jaotises Projektihaldus ja raamatupidamisparameetrid. Saate selle suvandi keelata, et värskendada algset kannet, selle asemel et luua stsenaariumide alamhulga korrigeerimise ajal uusi kandeid. On teatatud, et see parameeter aegub 1. märtsiks 2023. Pärast 1. märtsi 2023 käitub süsteem alati nii, nagu oleks valik lubatud.

## <a name="adjustments-process-flow"></a>Reguleerimisprotsessi voog

Järgmised sammud näitavad tüüpilist voogu korrigeerimiste töötlemiseks.

1.  **Avage leht Projekti korrigeerimised** .
2. Valige **Vali**, et otsida kandeid, mis vastavad korrigeerimise eeldatavatele kriteeriumidele.
3. Valige kannete loendist korrigeerimiseks kõik kanded või kannete alamhulk.
4. Valige **Reguleeri** ja muutke real olevaid atribuute. Teise võimalusena, kui väärtused määrati kande sisestamise ajal käsitsi, saate valida süsteemi vaikeväärtuste sisestamise.
5. Kannete loend tagastatakse ja veerus **Ootel korrigeerimine** kuvatakse märge, mis näitab, kus muudatused tehti. Kõik parandused, mille muudatused on ootel, kuvatakse lehe alumises pooles. Seal saate teha täiendavaid üksikasjalikke muudatusi lisaks eelmisel lehel näidatule.
6. Korrigeerimiskannete sisestamiseks valige **Postita** .

Sõltuvalt konfiguratsioonist luuakse korrigeerimise jaoks tavaliselt uued kanded.

- Algse **kande välja Arve olek** väärtuseks on määratud **Korrigeeritud**.
- Algse kande tühistamiseks luuakse ümberpööramiskanne ja **välja Olek** väärtuseks on seatud **Korrigeeritud**.
- Luuakse uus kanne, millel on korrigeerimisprotsessi käigus tehtud muudatused.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Mitme sisestatud projektikande valimine korraga korrigeerimiste ja kreeditarvete jaoks

Väljalaskes 10.0.30 kasutusele võetud uus funktsioon võimaldab lehelt Postitatud projektikanded **valida** korraga mitu korrigeerimiseks kannet.

Enne selle funktsiooni kasutamist peab see olema teie süsteemis lubatud. Administraatorid saavad kasutada **tööruumi Funktsioonihaldus**, et kontrollida funktsiooni olekut ja lubada see, kui see on nõutav.  **Otsige tööruumis Funktsioonihaldus** üles ja valige korrigeerimiste ja kreeditarvete **jaoks mitme valikuga sisestatud projektikanded ning seejärel valige** **Luba kohe**.

See funktsioon võimaldab järgmisi põhifunktsioone.

- Sellele pääseb juurde projekti sees postitatud kande lehelt, kasutades olemasolevat **korrigeerimisnuppu** .
- See lubab lehel Postitatud projektikanded **mitmerealise valiku juhtelemendi** . Saate loendilehele filtreid rakendada ja kirjed enne korrigeerimiste alustamist valida.
- See keelab **nupu Korrigeerimine**, kui mõnda üksikut kannet ei saa korrigeerida või kui valite kreeditarvete ja töölehtede kombinatsiooni koos, mitte eraldi.
- Mitme rea valimise juhtelemendi lisamise tõttu pole lindil olev link Pühendunud kulu **enam keelatud,** kui valitud on mitu rida.
- See lisab järgmise hoiatusteate: "Olete valinud korrigeerimiseks rohkem kui (valitud arv) kirjeid. Selle toiminguga jätkamine võib võtta aega. Kas olete kindel, et soovite selle tegevusega jätkata?"

See funktsioon eemaldab ka 2. sammu protsessivoost, mida selles artiklis varem kirjeldati. Seetõttu kaasatakse kõik kanded, mis valiti enne **lehe Korrigeeri kandeid avamist, korrigeeritavate kannete** loendisse. Nende otsimiseks ei pea **te kasutama nuppu Vali** .

> [!NOTE] 
> Isegi kui see funktsioon on keelatud, saate reguleerimiseks siiski valida mitu kirjet. Siiski jääb valituks *ainult üks kirje* ja **dialoogiboks Kannete valimine kuvatakse kohe pärast seda, kui olete valinud korrigeerimiste** avamise.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Korrigeerimiskande olekud, mida saab korrigeerimiste puhul lubada või keelata

Lehe Projektihalduse ja raamatupidamise parameetrid vahekaardil **Üldine** **saab lubada või keelata järgmised olekud** .

- Postitatud
- Arvesoovitus
- Arveldatud
- Hinnanguline
- Kõrvaldada
- Algsaldo (tund)

## <a name="adjustment-parameters"></a>Reguleerimise parameetrid

Need parameetrid on loetletud **lehel Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Üldine** grupi Korrigeerimine **ja** need muudavad korrigeerimiste töötlemise käitumist. 

| Parameetri nimetus | Kirjeldus |
|----------------|-------------
| Korrigeerimiskande loomine alati | Kui see parameeter on lubatud, loob korrigeerimisprotsess alati uue tagurduskande ja uue korrigeeritud kande, kui sellel on finants- või aruandlusmõju. Kui parameeter on keelatud, värskendab korrigeerimisprotsess algset kannet, selle asemel et luua stsenaariumi (nt kande teksti värskenduse) jaoks tagasipööramine ja uus kanne. |
| Automaatvärskenduse väli | Kui see parameeter on lubatud, arvutab süsteem omahinna ja müügihinna ümber. |
| Korrigeerimiskuupäeva kasutamine uue projektina | Seda parameetrit kasutatakse kannete teisaldamiseks tulevikku fiskaalperiood enne, kui süsteem seda funktsiooni toetas. Me ei soovita teil seda kasutada, kuna see muudab kande ärikuupäeva ja on tulevases väljaandes kasutuselt kõrvaldatud. |
| Luba suletud tegevused | Tavaliselt ei saa suletud tegevuste jaoks kandeid luua. Kui see parameeter on lubatud, alistatakse see käitumine. Seetõttu saab suletud tegevuste jaoks luua kohandusi. |
