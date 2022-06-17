---
title: Päevarahade kulud
description: See artikkel annab teavet selle kohta, kuidas töötada päevaraha kuludega.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923183"
---
# <a name="per-diem-expenses"></a>Päevarahade kulud

> [!IMPORTANT] 
> Selles artiklis kirjeldatud funktsioonid on sihitud kasutajatele eelvaateväljaande osana saadaval.

Päevaraha on fikseeritud, etteantud päevaraha, mida ettevõte maksab oma töötajatele majutuse (hotellide), söögikordade ja juhuslike kulude eest, mida need töötajad tööreisil kannavad. Ettevõte maksab seda toetust töötajatele, selle asemel et maksta tegelikke reisikulusid. Töötajad saavad kasutada oma **juhuslikke / muid** päevarahasid, et katta näpunäiteid, toateenindust, pesupesemis- või keemilise puhastuse teenuseid oluliste ärikohtumiste jaoks. Päevaraha määr võib varieeruda sõltuvalt sellest, kas tööandja otsustab hüvitada majutuse ja toitmise kombineeritud kulud või ainult söögi- ja juhuslike kulude eest.

Päevarahade määrad võivad põhineda aastaajal, reisisihtkohal või mõlemal. Kui loote päevaraha reegli, saate määrata, et protsent päevaraha määrast peetakse kinni, kui töötaja saab tasuta eineid või teenuseid. Samuti saate määrata minimaalse tundide arvu ja maksimaalse tundide arvu, mida töötaja reisile saab rakendada päevaraha määra kohta.

Päevaraha arvutatakse päevarahana, mida pakutakse päevas, millest on maha arvatud töötajale antav söögikordade vähendamine (tasuta einete maksumus).

## <a name="configure-per-diems"></a>Päevaraha konfigureerimine

Päevaraha kulude konfigureerimiseks tehke järgmist.

1. **Avage kuluhalduse** \> **seadistuse** \> **üldise** \> **kuluhalduse parameetrid.**
2. **Valige vahekaardi Päevaraha** kohta väljal **Toidu vähendamise arvutamine välja alusel**, kuidas arvutada päevaraha kohta.

    - **Söögikord reisi** kohta – arvutage päevaraha vastavalt sisestatud söögikorra tüübile (hommiku-, lõuna- või õhtusöök) ja söögikordade vähendamisele, mis on määratud iga söögikorra tüübi kohta päevaraha eest reisi ajal.
    - **Söögikorra tüüp päevas** – arvutage päevaraha vastavalt sisestatud söögikorra tüübile ja söögikordade vähendamisele, mis on määratud iga söögikorra tüübi kohta päevaraha kohta päevas.
    - **Söögikordade arv päevas** – arvutage päevaraha vastavalt päevas sisestatud söögikordade arvule ja iga päev pakutavate söögikordade arvu vähendamisele.

3. **Avage kuluhalduse** \> **seadistusarvutused** \> **ja tähised** \> **Päevaraha asukohtade kohta.**
4. Lisage asukohad, kus saab kasutada päevaraha.
5. Valige iga lisatava asukoha kohta vahekaardil **Päevaraha** määr ja valuuta, mis kehtivad majutuse, söögikordade ja muude kulude kindlate algus- ja lõppkuupäevade vahel. Päevarahamäärade ja valuutade konfigureerimiseks minge jaotisse **Kuluhalduse** \> **häälestuse** \> **arvutused ja tähised** \> **päevaraha kohta.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Päevarahade kohta ümberkujundatud kululiideses

Päevaraha funktsiooni toetatakse ümberkujutatud **kuluhalduse** tööruumis 365 Finance versioonis 10.0.25 ja uuemas versioonis Microsoft Dynamics.

Päevaraha lubamiseks järgige neid samme.

1. **Otsige ja valige tööruumis Funktsioonihaldus** loendist **funktsioon Kuluaruanded Ümber kujundatud** ja seejärel valige **Luba kohe**.
2. Leidke ja valige loendist **kuluaruande ümberkujutatud liidese** funktsioon Per-diem ja seejärel valige **Luba kohe**.

## <a name="how-the-feature-works"></a>Kuidas funktsioon töötab?

Selles jaotises on toodud näited kolme konfiguratsioonistsenaariumi kohta. Iga näite puhul on välja **arvutamine välja alusel** seatud erinevale väärtusele. Kõigi kolme näite puhul on makstav kogusumma sama kuni toidukordade vähendamise kohaldamiseni. Pärast seda erineb tasumisele kuuluv kogusumma iga näite puhul.

Kõigi kolme näite puhul kasutatava päevaraha kulu loomiseks tehke järgmist.

1. **Avage tööruumide** \> **kuluhaldus.**
2. Valige **Uus kuluaruanne** või valige olemasolev kuluaruanne.
3. Lisage uus kulu. Valige väljal **Kategooria** väärtus **Päevaraha** kohta. Valige reisi asukoht ning algus- ja lõppkuupäevad. Majutuse, einete ja juhuslike kulude (muude kulude) päevaraha arvutatakse valitud asukohale määratud päevaraha alusel.

    Näiteks valite **asukohaks Redmondi (USA).** Selle asukoha päevaraha on 150 USA dollarit (150 USA dollarit) majutuse, söögikordade USD 75 ja juhuslike USD 5 eest. Alguskuupäev on 10. jaanuar ja lõppkuupäev 14. jaanuar. Seetõttu on valitud kestus viis päeva, kui valitud konfiguratsioon on kalendripäevad ajaga ning valitud aeg algab ja lõpeb algus- ja lõppkuupäevadel kell 12.00. Siin on arvutused:

    - Tasumisele kuuluv kogusumma = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Eine ja juhuslik osa kogusummast = 5 × (75 + 5) = USD 400

Kui reisi ajal pakuti hommiku-, lõuna- ja õhtusööki, tuleb neid eineid arvestada söögikordade vähendamisena.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Näide 1: päevaraha kohta, kus söögikordade vähendamine põhineb söögitüübil reisi kohta

Selles näites on söögikordade vähendamine hommikusöögiks 30 protsenti, lõunasöögiks 30 protsenti ja õhtusöögiks 40 protsenti. **Lehel** Kuluhaldusparameetrid on välja arvutamisreeglid **seatud** väärtusele **Eine tüüp reisi kohta**. Siin on arvutused, kui töötajale pakuti kolm hommikusööki, kaks lõunasööki ja null õhtusööki:

- Söögikordade vähendamine = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Söögid ja juhuslikud juhtumid = 400 – 112,50 = USD 287.50
- Makstav kogusumma = Kogutoetus – Toidukordade vähendamine = 1150 – 112,50 = USD 1,037.50

![Päevaraha kulu kohta, kui söögikordade vähendamine põhineb söögitüübil reisi kohta.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Näide 2: päevaraha kohta, kus söögikordade vähendamine põhineb söögitüübil päevas

Selles näites on söögikordade vähendamine hommikusöögiks 30 protsenti, lõunasöögiks 30 protsenti ja õhtusöögiks 40 protsenti. **Lehel** Kuluhalduse parameetrid **on välja Arvuta söögikordade vähendamine välja järgi** seatud väärtusele **Eine tüüp päevas**. Sellisel juhul **tühjendate dialoogiboksi Kulude redigeerimine ruudustikus** Toidukaubad **märkeruudud**, et näidata, milliseid toite teile reisi ajal pakuti.

Näiteks on siin arvutused, kui reisi esimese kolme päeva jooksul pakuti hommikusööki:

- Söögikordade igapäevane vähendamine iga esimese kolme päeva kohta = 75 × 30% = USD 22.50
- Toidukordade vähendamine kokku = 3 × 22,50 = USD 67.50
- Söögid ja juhuslikud päevad 1 kuni 3 = 75 – 22,50 = USD 57.50
- Söögikordade ja juhuslike asjaolude koguarv = söögikordade ja juhuslike kogus viie päeva jooksul = 400 – 67,50 = USD 332.50
- Tasumisele kuuluv kogusumma = Kogusumma – Söögikordade vähendamine = 1150 – 67,50 = USD 1,082.50

![Päevaraha kulu kohta, kui söögikordade vähendamine põhineb söögitüübil päevas.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Näide 3: päevaraha kohta, kus söögikordade vähendamine põhineb söögikordade arvul päevas

Selles näites arvutatakse söögikordade vähendamine päevas pakutavate söögikordade arvu põhjal (see tähendab, **et lehel Kuluhalduse parameetrid on väljade kaupa** **arvutatud söögikordade vähendamine välja järgi** seatud söögikordade arvule **päevas**). Tühjendage **dialoogiboksi Kulu redigeerimine ruudustikus** Toidukaubad **märkeruudud**, et näidata, milliseid toite pakuti.
Sellisel juhul põhineb söögikordade vähendamine ainult pakutavate toitude # alusel, mitte pakutava söögiliigil (hommiku- / lõuna- / õhtusöök).

Siin on arvutused päevaraha kohta, kui päevaraha on USD 150 majutuse, söögi USD 75 ja juhuslike USD 5 jaoks:

- **Makstav** kogusumma = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Üks söögikord:** söögikordade vähendamine = 20% = USD 15
- **Kaks söögikorda:** söögikordade vähendamine = 50% = USD 37.50
- **Kolm söögikorda:** söögikordade vähendamine = 100% = USD 75

Siin on arvutused söögikordade ja juhuslike hüvitiste **kohta**, mis sisaldavad juhuslike USD 5:

- 1. päev - Pakutakse kahte söögikorda = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. päev - Pakutakse kahte söögikorda = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. päev - Pakutakse üks eine = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. päev - Pakutakse null söögikorda = (75-0) + 5 = 75 + 5 = USD 80
- 5. päev - Kolm söögikorda = (75 – 75) + 5 = 0 + 5 = USD 5

- Söögid ja juhuslikud koguarvud = söögid ja juhuslikud juhtumid 1. päevaks + 2. päevaks + 3. päev + 4. päev + 5. päev = USD 235
- Söögikordade vähendamine kokku = Söögi vähendamine 1+ päevaks 2 + 3. päevaks + 4. päev + 5. päev = 37,5+ 37,5+ 15 + 0 + 75 = USD 165
- Makstav kogusumma = Kogutoetus – Toidukordade vähendamine kokku = USD 1,150 – USD 165 = USD 985

![Päevaraha kulu kohta, kus söögikordade vähendamine põhineb söögikordade arvul päevas.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Finance'i versiooni 10.0.23 seisuga ei saa te ümberkujutatud kululiidest kasutades luua päevarahakulusid, millel on kattuvad kuupäevad. Kui proovite, kuvatakse tõrketeade.
