---
title: Päevarahade kulud
description: See artikkel annab teavet selle kohta, kuidas päevarahadega töötada.
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
> Selles artiklis kirjeldatud funktsionaalsus on sihtkasutajatele saadaval eelvaateväljaande osana.

Päevaraha on fikseeritud ettemääratud päevaraha, mida ettevõte maksab oma töötajatele majutuse (hotellid), toitlustuse ja kõrvalkulude eest, mis nendel töötajatel tööreisil tekivad. Ettevõte maksab seda toetust töötajatele tegelike reisikulude tasumise asemel. Töötajad saavad kasutada oma **Juhuslikud kulud/muu** päevaraha oluliste ärikohtumiste jaoks jootraha, toateeninduse, pesupesemise või keemilise puhastuse teenuste katmiseks. Päevaraha määr võib varieeruda olenevalt sellest, kas tööandja otsustab hüvitada majutuse ja toitlustuse kombineeritud kulud või ainult toitlustuse ja juhuslikud kulud.

Päevarahade määrad võivad põhineda aastaajal, reisisihtkohal või mõlemal. Kui loote päevarahareegli, saate määrata, et teatud protsent päevaraha määrast peetakse kinni, kui töötaja saab tasuta toitlustust või teenuseid. Samuti saate määrata minimaalse tundide arvu ja maksimaalse tundide arvu, mille jooksul saab töötaja reisi päevarahamäära rakendada.

Päevaraha arvutatakse päevaraha kogusummana, millest on lahutatud töötajale makstav toidukorra vähendamine (tasuta toitlustuse maksumus).

## <a name="configure-per-diems"></a>Päevarahade konfigureerimine

Päevaraha kulude konfigureerimiseks toimige järgmiselt.

1. Minge jaotisesse **Kuluhaldus** \> **Seadistus** \> **Üldine** \> **Kuluhalduse parameetrid**.
2. Valige vahekaardil **Päevaraha** väljal **Söögikordade vähendamise arvutamine**, kuidas tuleks päevaraha arvutada.

    - **Toidu tüüp reisi kohta** – päevaraha arvutamine põhineb sisestatud toidukorra tüübil (hommikusöök, lõuna või õhtusöök) ja iga söögi tüübi jaoks määratud söögikordade vähendamisel reisi kestel makstava päevaraha jaoks.
    - **Toidu tüüp päeva kohta** – päevaraha arvutatakse sisestatud toidutüübi ja iga toidutüübi jaoks määratud söögikordade vähendamise alusel päevaraha päeva kohta.
    - **Toidukordade arv päevas** – arvutage päevaraha päeva kohta sisestatud söögikordade arvu ja iga päev pakutavate söögikordade arvu vähendamise alusel.

3. Minge jaotisesse **Kuluhaldus** \> **Seadistus** \> **Arvutused ja koodid** \> **Päevaraha asukohad**.
4. Lisage asukohad, kus saab kasutada päevaraha.
5. Iga lisatava asukoha jaoks valige vahekaardil **Päevarahad** päevaraha määr ja valuuta, mis kehtivad majutuse, toitlustuse ja muude kulude konkreetse algus- ja lõppkuupäeva vahel. Päevaraha määrade ja valuutade konfigureerimiseks minge jaotisesse **Kuluhaldus** \> **Seadistus** \> **Arvutused ja koodid** \> **Päevarahad**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Päevarahad ümberkujundatud kululiideses

Päevaraha funktsiooni toetab ümberkujundatud tööruum **Kuluhaldus** rakenduses Microsoft Dynamics 365 Finance versioonis 10.0.25 ja uuemates versioonides.

Päevarahade lubamiseks järgige järgmisi samme.

1. Tööruumis **Funktsioonihaldus** leidke ja valige loendist funktsioon **Ümberkujundatud kuluaruanded** ning seejärel valige **Luba kohe**.
2. Otsige üles ja valige loendist funktsioon **Kuluaruande päevaraha ümberkujundatud liides** ja seejärel valige **Luba kohe**.

## <a name="how-the-feature-works"></a>Kuidas funktsioon töötab?

See jaotis pakub näiteid kolme konfiguratsioonistsenaariumi kohta. Iga näite puhul on väljal **Toidukordade vähendamise arvutamine** erinev väärtus. Kõigi kolme näite puhul on tasumisele kuuluv kogusumma sama kuni toidukordade vähendamise kohaldamiseni. Pärast seda on tasumisele kuuluv kogusumma iga näite puhul erinev.

Kõigi kolme näite jaoks kasutatava päevarahakulu loomiseks toimige järgmiselt.

1. Minge jaotisesse **Tööruumid** \> **Kuluhaldus**.
2. Valige **Uus kuluaruanne** või valige loendist olemasolev kuluaruanne.
3. Lisage uus kulu. Valige väljal **Kategooria** **Päevaraha**. Valige oma reisi asukoht ning algus- ja lõppkuupäev. Ööbimis-, toitlustus- ja kõrvalkulude (muud kulud) päevaraha arvutatakse valitud asukohas määratud päevaraha alusel.

    Näiteks valite asukohaks **Redmond (USA)**. Selle asukoha päevaraha on 150 USA dollarit (150 USD) majutuse eest, 75 USD söögi eest ja 5 USD ettenägematute kulude eest. Alguskuupäev on 10. jaanuar ja lõppkuupäev 14. jaanuar. Seetõttu on valitud kestuseks viis päeva, kui konfiguratsiooniks on valitud kalendripäevad ajaga ning valitud aeg algab ja lõpeb alguse- ja lõppkuupäeval kell 12.00. Siin on arvutused.

    - Tasumisele kuuluv kogusumma = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
    - Toit ja ettenägematud osad kogusummast = 5 × (75 + 5) = 400 USA dollarit

Kui reisi ajal pakuti hommiku-, lõuna- ja õhtusööki, tuleb need toidukorrad arvesse võtta toidukorra vähendamisena.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Näide 1: päevaraha, mille puhul toidukordade vähendamine põhineb toidukorra tüübil reisi kohta

Selles näites on toidukordade vähendamine hommikusöögi puhul 30 protsenti, lõunasöögi puhul protsenti ja õhtusöögi puhul 40 protsenti. Lehel **Kuluhalduse parameetrid** on väljal **Toidukordade vähendamise arvutamine** määratud **Toidu tüüp reisi kohta**. Siin on arvutused, kui töötajale pakuti kolm hommikusööki, kaks lõunasööki ja null õhtusööki:

- Toidukordade vähendamine = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22.50) + (2 × 22.50) + 0 = 67.50 + 45 + 0 = 112,50 USD
- Toidukorrad ja juhuslikud kulud = 400 – 112,50 = 287,50 USD
- Tasumisele kuuluv kogusumma = Kogu päevaraha – Toidukordade vähendamised = 1150 – 112,50 = 1037,50 USD

![Päevaraha, mille puhul toidukordade vähendamine põhineb toidukorra tüübil reisi kohta.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Näide 2: päevaraha, kus toidukordade vähendamine põhineb toidukorra tüübil päeva kohta

Selles näites on toidukordade vähendamine hommikusöögi puhul 30 protsenti, lõunasöögi puhul protsenti ja õhtusöögi puhul 40 protsenti. Lehel **Kuluhalduse parameetrid** on välja **Toidukordade vähendamise arvutamine** väärtus **Toidu tüüp päeva kohta**. Ruudustikus **Toidukorrad** tühjendate sel juhul dialoogiboksi **Kulude redigeerimine** märkeruudud, et näidata, milliseid toite teile reisi ajal pakuti.

Näiteks siin on arvutused, kui hommikusööki pakuti reisi esimesel kolmel päeval:

- Igapäevane toidukordade vähendamine esimesel kolmel päeval = 75 × 30% = 22,50 USD
- Kogu toidukordade vähendamine = 3 × 22,50 = 67,50 USD
- Toidukorrad ja ettenägematud kulud päevadel 1–3 = 75–22,50 = 57,50 USD
- Toidukordade ja juhuslike kulude kogusumma = toidukordade ja juhuslike kulude summa viie päeva jooksul = 400 – 67,50 = 332,50 USD
- Tasumisele kuuluv kogusumma = Kogu summa – Toidukordade vähendamised = 1150 – 67,50 = 1082,50 USD

![Päevaraha, kui toidukordade vähendamine põhineb toidukorra tüübil päeva kohta.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Näide 3: Päevaraha, kus toidukordade vähendamine põhineb toidukordade arvul päeva kohta

Selles näites arvutatakse söögikordade vähendamine päeva kohta pakutavate söögikordade arvu alusel (st väljal **Toidukordade vähendamise arvutamine** lehel **Kuluhalduse parameetrid** on määratud **Toidukordade arv päevas**). Ruudustikus **Toidukorrad** dialoogiboksis **Kulu redigeerimine** tühjendate märkeruudud, et näidata, milliseid toite pakuti.
Sellisel juhul põhineb toidukordade vähendamine ainult pakutavate toidukordade arvul, mitte aga pakutava toidu liigil (hommikusöök/lõunasöök/õhtusöök).

Siin on päevarahade arvutused, kui päevaraha on 150 USA dollarit majutuse eest, 75 USA dollarit söögi eest ja 5 USA dollarit juhuslike kulude eest:

- **Tasumisele kuuluv kogusumma** = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
- **Üks toidukord:** toidukorra vähendamine = 20% = 15 USD
- **Kaks toidukorda:** toidukorra vähendamine = 50% = 37,50 USD
- **Kolm toidukorda:** toidukorra vähendamine = 100% = 75 USD

Siin on arvutused **toidukordade ja juhuslike kulude päevaraha** kohta, mis sisaldab 5 USD juhuslike kulude katteks:

- 1. päev - Kaks toidukorda = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 2. päev - Kaks toidukorda = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 3. päev – Üks toidukord= (75 –15) + 5 = 60 + 5 = 65 USD
- 4. päev - Null toidukorda = (75 – 0) + 5 = 75 + 5 = 80 USD
- 5. päev - Kolm toidukorda = (75 – 75) + 5 = 0 + 5 = 5 USD

- Toidukordade ja juhuslike kulude kogusumma = Toidukorrad ja juhuslikud 1. päeva + 2. päeva + 3. päeva + 4. päeva + 5. päeva kulud = 235 USD
- Kogu toidukordade vähendamine = Toidukordade vähendamine 1. päeva + 2. päeva + 3. päeva + 4. päeva + 5. päeva kohta = 37,5 + 37,5+ 15 + 0 + 75 = 165 USD
- Tasumisele kuuluv kogusumma = Kogu päevaraha – Toidukordade vähendamised = 1150 USD – 165 USD = 985 USD

![Päevaraha, mille puhul toidukordade vähendamine põhineb toidukordade arvul päeva kohta.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Alates Rahastamisversioonist 10.0.23, ei saa uuendatud kululiidese kasutamisel luua päevarahakulusid, mille kuupäevad kattuvad. Kui proovite, saate tõrketeate.
