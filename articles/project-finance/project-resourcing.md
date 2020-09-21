---
title: Projektide ressursid
description: Selles teemas antakse teavet projekti ressursside kohta.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750901"
---
# <a name="project-resourcing"></a>Projektide ressursid

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet projekti ressursside kohta.

Üks projektijuhtide ja ressursi haldajatele väljakutse projekti kavandamise etapis on ressursside eraldamine, kus nad peavad määratlema ja reserveerima õige ressursi projektiga töötamiseks. Rakenduses Dynamics 365 Finance võimaldab projektide ressursside võimekus teil määratleda rolle, mida käsitletakse ajutiste ressurssidena, mida saab reserveerida konkreetsele tegevusele või tegevuse osale. Seda tüüpi ressurss võimaldab projektihalduritel ja ressursi halduritel täita järgmisi tööülesandeid.

- Määrata roll, millel on nõutav pädevus, et ressursse oleks hõlbus vastendada.
- Rollide kasutamine algse kaasamise graafiku määratlemiseks, mis põhineb reserveeritud ressurssidel.
- Prognoosida kulusid ja määrata esialgne eelarve, lähtudes projekti määratud rollidest ja ressurssidest.
- Kasutage rolle, et prognoosida iga tegevuse jaoks vajalike ressursside broneerimiste arvu.
- Prognoosige projekti kogu elutsükli jooksul nõutavate ressursside arvu.
- Looge tööjaotuse struktuuri (WBS) mustand, kasutades algseid ressursimääramisi.

[![Projekti elutsükkel](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Projekti kavandamise edenemisel saab planeeritud ressursse asendada töötajate ressurssidega. Projektijuht saab tagasi minna ja uuendada ressursi reserveerimisi mis tahes projekti etapis.

## <a name="set-up-project-resources"></a>Projekti ressursside seadistamine
Peate seadistama kalendri ja seostama selle töövõtja või töötajaga. Kalendrit kasutatakse projekti kavandamiseks ja projekti jaoks reserveeritavate ressursside tööaegade jaoks. Kalendri seadistamisel saavad projektijuhid ressursi optimeerimise raames teha ressursi tasandamist. Kalendri ajakava põhjal saab ressurssidele lisada piiranguid. Kalendri saate seadistada lehel **Kalendrid**.

Kui te seadistate projekti ressursina töötaja, saate valida töötajate seast, kes töötavad ettevõttes, kelle jaoks ressurssi seadistate. Teise võimalusena saate valida töötajad teistest ettevõtetest oma organisatsioonis. Neid töötajaid nimetatakse kontsernisisesteks ressurssideks.

Järgmised protseduurid selgitavad, kuidas seadistada töötajat oma ettevõttes projekti ressursina ja kuidas seadistada kontsernisisene projekti ressurss.

### <a name="set-up-a-worker-as-a-project-resource"></a>Töötaja seadistamine projekti ressursina

1. Lehel **Töötajad** loendis **Töötajad** valige töötaja, kelle projekti ressursina lisate, ja avage töötaja kirje.
2. Paanil Toiming valige **Projekt** &gt; **Seadistamine** &gt; **Projekti seadistamine**.
3. Valige kalender ja sulgege seejärel leht.

Saate määrata ka ressursi jaoks eelmääramise tüübina vaikeprojektid. Eelmääramisi saab kasutada juhul, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss hakkab tööle. Eelmääramised võivad põhineda ka projekti sponsori või kliendi taotlusel. Projekti eelmääramiseks lehel **Projektide määramine** vahekaardil **Projektid** loendis **Ülejäänud projektid** valige vastav projekt.

### <a name="set-up-an-intercompany-resource"></a>Kontsernisisese ressursi seadistamine

Kui seadistate töötaja kontsernisisese ressursina, peate seadistamise lõpetama nii laenu andvale ettevõttele kui ka laenavale ettevõttele.

**Laenu andvas ettevõttes**

1. Rakenduses Finance kontrollige, kas laenu andev ettevõte on valitud, ja täitke seejärel toiming eelmises jaotises „Töötaja projekti ressursina häälestamine”.
2. Valige lehel **Kontsernisisene raamatupidamine** suvand **Uus**.
3. Valige väljal **Juriidilise üksuse ID** laenu andev ettevõte. Täitke ülejäänud väljad vajaduse järgi ja valige käsk **Salvesta**.
4. Valige lehel **Ülekandehind** suvand **Uus**.
5. Valige väljal **Laenu võttev juriidiline olem** vastav ettevõte.
6. Laenavale ettevõttele ainult selle jaotise alguses loodud ressursi laenamiseks valige väljal **Ressurss** loodud ressursi nimi. Laenavas ettevõttes laenavala ettevõttele kõikide ressursside kättesaadavaks tegemiseks jätke väli **Ressurss** tühjaks.
7. Lehel **Projektihalduse ja raamatupidamise parameetrid**vahekaardil **Kontsernisisesed** määrake suvand **Luba kontsernisisesed ressursiplaneerimine ja ajatabelid** valikule **Jah**.

**Laenu võtvas ettevõttes**

- Sisestage lehel **Ressursside loend** otsingufiltrisse ressursi nimi, mille laenava ettevõtte jaoks lõite, et kontrollida, kas nimi sisaldub laenu võtva ettevõtte ressursside loendis.

## <a name="manage-resource-competencies"></a>Ressursi pädevuste haldamine
Ressursi pädevused on ressursi haldamise olulised osad. Pädevusi saab kasutada algtasemena, et määratleda ressursid, millel on õige oskuste, hariduse, sertifitseerimise ja projektide kogemuse tasakaal. Peaksite selle teabe häälestama iga ressursi jaoks ja seda regulaarselt värskendama. Sel viisil saate maksimeerida võimalusi, kui teatud ressursi pädevused projekti ressursi määramise käigus vastenduvad.

[![Oskuste, sertifitseerimise, hariduse ja projektide kogemuse näited](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Järgmistest toimingutest leiate teavet selle kohta, kuidas teatud ressursi pädevusi seadistada.

Töötaja pädevuste seadistamiseks saate kasutada kas inimressurssides loendi lehte **Töötajad** või projektihalduses ja raamatupidamises loendilehte **Ressursid**. Järgmiste protseduuride puhul kasutatakse inimressursside loendilehte **Töötajad**.

### <a name="set-up-competencies-certificates"></a>Pädevuste seadistamine: sertifikaadid

1. Loendi lehel **Töötajad** valige töötaja rida, et lisada sertifikaadi teave.
2. Valige toimingupaanil vahekaardil **Töötaja** rühmas **Pädevused** suvand **Sertifikaadid**.
3. Valige **Uus** ja seejärel väljal **Sertifikaadi tüüp** valige **PMP**.
4. Väljal **Alguskuupäev** valige **1.10.2015** ja valige **Salvesta**.

### <a name="set-up-competencies-skills"></a>Pädevuste seadistamine: oskused

1. Veenduge, et loendilehel **Töötajad** oleks endiselt valitud töötaja, keda kasutasite eelmises toimingus. Seejärel valige toimingupaanil vahekaardil **Töötaja** rühmas **Pädevused** suvand **Oskused**.
2. Tehke valik **Uus**.
3. Väljal **Oskus** valige **Projektihaldus**.
4. Väljal **Tase** valige **5 Ekspert**.
5. Väljal **Taseme kuupäev** valige **14.1.2014**.
6. Väljale **Kogemus aastates** sisestage **10**.
7. Valige käsk **Salvesta** ja sulgege seejärel leht.

## <a name="create-a-new-project"></a>Uue projekti loomine
1. Lehel **Projektihaldus** valige **Uus projekt** ja sisestage järgmised väärtused.

    - **Projekti tüüp:** aeg ja materjal
    - **Projekti nimi:** XYZ värskenduse 2. etapp
    - **Projekti rühm:** TM\_WIP
    - **Projekti lepingu ID:** 00000002

2. Valige käsk **Loo projekt**.

### <a name="assign-a-resource-to-a-project"></a>Ressursi määramine projektile

1. Lehel **Töötajad** loendis **Töötajad** valige töötaja, kelle jaoks oskuseid seadistasite, ja avage töötaja kirje.
2. Valige toimingupaanil vahekaardil **Projekt** rühmas **Seadistamine** suvand **Määra projekt**.
3. Vahekaardi **Ressursi valideerimise projekti ülesanded** vahekaardi **Projektid** väljal **Lisa projekt valitud projektide hulka** filtreerige projektil **XYZ värskenduse 2. etapp**.
4. Paanil **Ülejäänud projektid** valige projekt ja valige seejärel noolenupp, et lisada see paanile **Valitud projektid** .

Saate ressursile määrata kategooriaid ka vastavalt vajadusele. Kategooria tüüp on kas **Kulu** või **Tulu**. Kategooria tüübi määrab teie organisatsioon. Kui ühtegi kategooriat pole ressursi jaoks määratud, otsib rakendus Finance vaikimisi kategooriat tunnihinna ja tulu kohta.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekti ressursi ja rolli omaduste seadistamine

Projektijuht saab projekti jaoks vajalike rollide loomiseks kasutada projekti ressursside funktsiooni. Rolle saab kasutada juhul, kui kinnitatud ressursid on ressursside reserveerimisel endiselt tundmatud. Rolle saab ajutiselt reserveerida plaanitud ressurssidena, et saaksite projekti kavandamise etappidega jätkata.

[![Rolli näide](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Stsenaarium:** Contoso palgati lõpetama aja- ja materjalikulu projekti, millel on kinnitatud projekti põhikiri. Noorem-projektijuht endiselt lõpetab projekti ulatust. Ressursihaldur määratleb praegu konkreetsed ressursid, mis reserveeritakse uue projektiga töötamiseks. Projekti kriitilise iseloomu tõttu taotles projekti sponsor ühe rollina vanem-projektijuhti. Ressursihaldur peab hankima uue ressursi ja määrama süsteemis rolli juhul, kui noorem-projektijuht vajab projekti kavandamise ajal ressursi teavet.

Järgmised juhised näitavad, kuidas ressursihaldur saab seadistada vanem-projektijuhi rolli ja seostada ressursi omadused sellega. Hiljem saab rolli kasutada saadaolevate ressursside otsimiseks, mis vastavad ressursi nõutavatele pädevustele.

1. Lehel **Seadistamise rollid** valige **Uus projekt** ja sisestage järgmised väärtused.

    - **Rolli ID:** vanem-projektijuht
    - **Kirjeldus:** vanem-projektijuht

2. Valige käsk **Loo**.
3. Valige roll **Vanem-projektijuht** ja valige seejärel **Konfigureeri tunnused**.
4. Väljal **Tunnuste tüüp** valige **Oskus**.
5. Väljale **Saadaolevad tunnused** sisestage otsitav oskus.
6. Väljal **Tunnuse tüüp** valige **Sertifikaat**.
7. Väljale **Saadaolevad tunnused** sisestage otsitav sertifikaadi tüüp.

### <a name="assign-a-project-resource-to-a-project"></a>Projekti ressursi määramine projektile

1. Lehel **Kõik projektid** valige projekt **XYZ värskenduse 2. etapp**.
2. Vahekaardil **Projektimeeskond ja kavandamine** valige suvand **Lisa**.
3. Väljale **Roll** sisestage **Meeskonnaliige**.
4. Valige suvand **Broneeri kalendrist**.
5. Lehel **Ressursi saadavus** valige **Kuva sätted**.
6. Lehel **Redigeeri kuvamissätted** sisestage järgmised väärtused.

    - **Kuupäeva vahemiku vaate vorming:** päev
    - **Kuva saadaolevad kirjeldused:** jah
    - **Kuva allesjäänud võimsus:** jah

7. Valige ressursside loendist ressurss.
8. Valige **Fikseeritud reserveering** ja **Täisvõimsus**.


### <a name="assign-a-resource-to-a-default-role"></a>Ressursi määramine vaikerollile

Projekti või ressursi haldamisega abistamiseks võivad juhid veelgi rohkem minna süvitsi ressursside puhul, mida saab projekti jaoks broneerida. Saate seostada vaike-rolli olemasoleva ressursiga või värskelt omandatud ressursiga. Näiteks, kui Daniel palgati, olid tal kogemus ja oskused täita ärianalüütiku rolli. Ressursihaldur määras selle rolli Danielile vaike-rolliks. Seega lisaks ressursihaldur Daneli ärianalüütikute kogumile, kes olid saadaval projektidega töötamiseks.

Ressursi reserveerimise ajal saavad projektijuhid filtreerida projektidega töötamiseks saadaolevate rollidega ressursse. Nad saavad kasutada seda teavet ühe kriteeriumina, kui nad teostavad ressursi täitmisel mitme tunnusega otsuste analüüsimist. Nad saavad lisada filtrile ka teisi ressursi omadusi, et otsida teatud projekti jaoks konkreetsete oskuste, hariduse ja kogemusega ressursse.

**Stsenaarium:** kinnitatud projekt on käivitatud ja vanem-projektijuhi roll oli reserveeritud planeeritud ressursina projekti kavandamise etapis. Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.

1. Lehel **Ressursside loend** valige **Daniel Kangur**.
2. Lehel **Ressursi roll** valige **Uus projekt** ja sisestage järgmised väärtused.

    - **Jõustub:** sisestage praegune kuupäev.
    - **Aegub:** sisestage **Mitte kunagi**.
    - **Roll:** sisestage **Vanem-projektijuht**.

3. Valige käsk **Salvesta** ja sulgege seejärel leht.
4. Vahekaardil **Pädevused** lisage oskus **Projektihaldus** ja sertifikaat **PMP**.

## <a name="set-up-role-based-pricing"></a>Rollipõhise hinnakujunduse seadistamine
Rollide jaoks saab seadistada kõiki kulusid, müügi ja ülekande hindu.

1. Lehel **Müügihind (tund)** valige **Uus** ja sisestage jõustumiskuupäev.
2. Veerus **Roll** valige roll.
3. Veerus **Hinnakujundus** sisestage valitud ressursi rolli jaoks hind.

## <a name="form-a-project-team"></a>Projektimeeskonna loomine
Varem projektis seadistatud rollide kasutamiseks peab projektijuht seostama rollid projektiga. Projektile võib määrata mitu rolli. Segaduse vältimiseks sildistatakse need rollid reserveerimise ajal automaatselt. Näiteks kui projektijuht nõuab kolme tarkvarainseneri, luuakse automaatselt kolm rolli Tarkvarainsener, millel on sildid **tarkvarainsener 1**, **tarkvarainsener 2** ja **tarkvarainsener 3**, kuna nende sildid luuakse automaatselt. Kui rolli omadused olid varem rollile määratud, rakendatakse need ressursi otsingu ajal justkui filter. Otsingu veelgi täpsemaks muutmiseks saab lisada vastavalt vajadusele täiendavaid tunnuseid.

Kuvamissätteid saab samuti kohandada, et anda ressursi saadavusest parem vaade. Saadavust võib kuvada tundide, päevade, nädalate, kuude, kvartalite ja aastate lõikes. Lisaks on olemas võimalus kuvada ressursside saadaolev ja allesjäänud võimsus. See suvand on kasulik ajahalduse jaoks, kui prognoosite saadaolevat aega tegevuste või ressursi kättesaadavuse kohta.

Projektijuht saab valida lehel rolli ja seejärel vaba ressursi olemasolul, mis nõudega ühtib, valida ressursi reserveerimine rolli täitmiseks. Pange tähele, et ressursse ei pea kavandamise etapis sellel hetkel reserveerima. WBS-i loomisel saate rolle asendada projekti töötajate ressurssidega. Kui rollid asendatakse WBS-is töötajatest ressurssidega, siis ressursi seadistus värskendab automaatselt projektimeeskonda loendit ja ajakava.

[![Projektimeeskonna loend, mis sisaldab nii rolle kui ka tegelikke ressursse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektijuhil on mitmeid võimalusi projekti jaoks ressursi broneerimiseks, nagu **Järelejäänud võimsus**, **Täisvõimsus**, **Võimsuse protsent** ja **Konkreetsed tunnid**. Kui ressursi määramised muutuvad, saab neid broneeringu võimalusi igal ajal tühistada. Toetatud on kahte tüüpi broneeringud.

- **Fikseeritud broneering** – ressursi broneerimine kiideti heaks ja kinnitati, et teatud aja jooksul töötab seal.
- **Esialge broneerimine** – ressursi broneerimised määrati esialgu töötama konkreetse aja jooksul.

Järgmises toimingus kirjeldatakse, kuidas luua projektimeeskonda.

### <a name="create-a-project-team"></a>Projektimeeskonna loomine

1. Loendi lehel **Kõik projektid** valige projekt ja valige seejärel **Redigeeri**.
2. Vahekaardil **Projektimeeskond ja ajastamine** väljal **Ajakava lõpukuupäev** sisestage ajakava algusaeg pluss üks kuu. Näiteks kui ajakava alguskuupäev on 24. juuni 2017 (24.6.2017), sisestage **24/07/2017**.
3. Valige suvand **Lisa**.
4. Paanil **Projektile rollide lisamine** väljal **Roll** valige **Vanem-projektihaldur**.
5. Valige **Nõutav pädevus**.
6. Lehel **Omaduste valimine** valitakse vaikimisi eelnevalt vanem-projektijuhi rollile määratud omadused. Valige **OK**.
7. Lehel **Projektile rollide lisamine** väljale **Ressursside arv** sisestage **1**.
8. Väljal **Ressurss** näitab otsing kõiki ressursse, millel on nõutavad omadused olemas. Valige suvad **Daniel Kangur** ja seejärel valige käsk **Loo**.
9. Lehel **Projekt** valige **Lisa**.
10. Paanil **Projektile rollide lisamine** väljal **Roll** valige **Meeskonnaliige**. Väljale **Ressursside arv** sisestage **5**.
11. Valige käsk **Loo**.
12. Lehel **Projektid** valige **Täida ressurss**.

## <a name="resource-capacity-synchronization"></a>Ressursi võimsuse sünkroonimine
Ressursi sünkroonimise protsess aitab tagada, et teave kalendrist ja põhikalendrist liiguks alla projekti ressursi ajastamisse. Kui kalendrit muudetakse, teevad protsessid projekti ressursside ajastamisse nõutavaid värskendusi. Protsessid aitavad ka parandada jõudlust, kuna kalendri ressursi teave sünkroonitakse eelnevalt. Seetõttu toimuvad ressursside kavandamise teabe värskendused kiiremini. Soovitame ajastada protsessid partiidena, mitte üks korraga. Vastasel juhul on oht, et keegi unustab kaasavad kuupäevad, millal teavet viimati sünkrooniti. Kui kaasavaid kuupäevi ei kasutata, võib kuupäevade sünkroonimise ajal esineda vahesid.

![Kalendri sünkroonimine](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Ressursi võimsuse sünkroonimise ümberarvestused

Sünkroniseerimisprotsess on loodud sünkroonima kogu ressursi kalendri teabe. See teave hõlmab põhikalendri teavet mis tahes muudatuste kohta projekti ressursi kalendri võimsuse tabelis. Kui projekti lisatakse uusi ressursse, aitab sünkroonimine tagada, et saadaval oleks värskendatud kalendri teave. Seda sünkroonimist saab teha igal ajal.

Me soovitame kasutada partiid. Valikud on võimsuse reserveeringute sünkroonimise ajal saadaval.

1. Valige **Projektihaldus ja raamatupidamine** &gt; **Perioodiline** &gt; **Võimsuse sünkroonimine** &gt; **Ressursside võimsuse sünkroonimise ümberarvestused**.
2. Määrake järgmises tabelis valikud.

    | Suvand      | Kirjeldus |
    |-------------|-------------|
    | Perioodi kood | Võite ka valida pearaamatu kuupäevaintervalli koodi, et määrata sünkroniseerimisprotsessi algus- ja lõpukuupäevad ressursi võimsuse ümberarvestuste jaoks. |
    | Alguskuupäev  | Sisestage ressursi võimsuse ümberarvestuse sünkroniseerimisprotsessi alguskuupäev. |
    | Lõppkuupäev    | Sisestage ressursi võimsuse ümberarvestuse sünkroniseerimisprotsessi lõpukuupäev. |

[![Sünkroonimisprotsess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>WBS-i mallide rollide seadistamine
Projektijuhid saavad seadistada WBS-i malle, mida nad saavad rakendada, kui nad loovad uute projektide jaoks WBS-i. Projektijuhid saavad malli luues lisada rolle. Kasutage WBS-i mallile rolli määramiseks järgmist toimingut.

1. Valige **Projektihaldus ja raamatupidamine** &gt; **Seadistamine** &gt; **Projektid** &gt; **Tööjaotuse struktuuri mallid**.
2. Valige valitud WBS-i malli jaoks suvand **Üksikasjad**.
3. Valige loendist tööülesanne ja seejärel väljal **Roll** valige ülesandele määramiseks roll.

### <a name="work-with-a-wbs"></a>WBS-iga töötamine

Saate luua uue WBS-i või kopeerida WBS-i olemasolevast WBS-i mallist. Projektijuht saab ressursse hõlpsalt hallata, määrates WBS-is uutele ülesannetele rollid. Rolle saab asendada kas pärast ressursi hankimist või pärast seda, kui kinnitatud ülesandega töötav ressurss on tuvastatud. See paindlikkus võimaldab projektijuhtidel teha järgmisi ülesandeid.

- Tuvastada ressursside arvu, mis on WBS-i tööpakettide jaoks nõutavad.
- Prognoosida projekti kulud.
- Määrata esialgne eelarve.
- Prognoosida rollide ja ressursside põhjal tegevuse kestust.
- Töötada välja mõned projekti haldamise kavad, mis põhinevad saadaoleval projekti teabel.

WBS-i on lisatud täiendavad valikud, et saaksite neid paremini kasutada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressursimääramised</td>
<td>Saate vaadata WBS-i tööülesannete jaoks määratud ressursse, kuupäevi, tundide arvu ja reserveeringu tüüpi.</td>
</tr>
<tr class="even">
<td>Meeskonna automaatne loomine</td>
<td>Saate automaatselt lisada plaanitud ressursse, kasutades tööülesannetega seotud rolle. Finance soovitab plaanitud ressursse automaatselt, kasutades mitme kriteeriumiga otsuste analüüsi, mis põhineb rollidel. Pärast seda, kui rollid ja mahud (tunnid) on WBS-is ülesannete jaoks määratud ning pärast struktuuri vabastamist valige <strong>Loo meeskond automaatselt</strong>. Nõutav arv planeeritud ressursse lisatakse WBS-i ja vahekaardile <strong>Projekti ja meeskonna ajastamine</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurss (ripploend)</td>
<td>Lehel <strong>Ressursi määramise käivitamine</strong> saate valida ressursid fikseeritud broneerimiseks või esialgseks broneerimiseks, olenevalt konkreetsest kestusest. Saate kohandada vaate sätteid, et näha ja määrata ressursi tegevuste kestuse. Saate ressursse valida ja määrata tööpaketi tasemel, kasutades järgmisi valikuid.
<ul>
<li><strong>Aktsepteeri</strong> – kinnitage tööülesande jaoks määratud ressursi muudatused.</li>
<li><strong>Tühista</strong> – tühistage tööülesande jaoks määratud ressursi muudatused.</li>
<li><strong>Määra automaatselt</strong> – saadaolev töötajate ressurss, millel on ühtiv roll, valitakse automaatselt ja määratakse valitud tööülesandele.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Lehel **Kõik projektid** valige projekt **XYZ värskenduse 2. etapp**.
2. Valige **Plaan** &gt; **Tegevused** &gt; **Tööjaotuse struktuur**.
3. Valige **Uus**, et lisada WBS-i järgmised esimese taseme tegevused.

    - Algatamine
    - Kavandamine
    - Täitmine
    - Jälgimine ja kontroll
    - Sule

4. Määrake kuupäevad ja mahud (tunnid), nagu järgmisel joonisel on näidatud.

    [![Kuupäevade ja pingutuse seadistamine](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Valige ülesanderida **Algatamine** ja seejärel väljal **Roll** valige suvand **Vanem-projektijuht**.
6. Valige **Avalda**.
7. Valige samal real väljal **Ressurss** suvand **Danel Kangur** ja seejärel valige nupp **Nõustun**.
8. Valige ülesanderida **Planeerimine** ja seejärel väljal **Roll** valige suvand **Ärianalüüs**.
9. Valige käsk **Avalda** ja seejärel valige käsk **Loo meeskond automaatselt**.
10. Avanevas sõnumiväljas valige **Jah**.
11. Kontrollige, et välja **Ressurss** väärtuseks oleks **Ärianalüütik 1**.
12. Ressursi **Ärianalüütuk 1** puhul avage otsing ja valige **Käivita ressursi määramidśed**. Seejärel valige ülesande jaoks töötaja.
13. Valige **Esialgne määramine** &gt; **Täisvõimsus**.

    > [!NOTE] 
    > Teile ei kuvata hoiatust, et määratud ressurss on nüüd 2, kuna ressursside arvuks jääb 1.

14. Kontrollige lehel **Tööjaotuse struktuur** ressursi määramist WBS-ile ja seejärel valige käsk **Salvesta**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressursside täitmine planeeritud ressursside jaoks
Projektijuht saab kavandada projekti jaoks nõutavaid ressursi rolle. Ressursihaldur näeb neid kavandatud ressursse taotlustena lehel **Ressursi täitmine** ja saab määrata tegelikud ressursid.

1. Lehel **Kõik projektid** valige projekt **XYZ värskenduse 2. etapp**.
2. Valige **Projekt** ja seejärel valige **Redigeeri**.
3. Vahekaardil **Projektimeeskond ja kavandamine** valige suvand **Lisa**.
4. Dialoogiboksis **Rollide lisamine** valige roll **Tarkvaraarendaja**.
5. Valige käsk **Loo** ja sulgege seejärel projekti leht.
6. Lehel **Ressursi täitmine** valige **Tarkvaraarendaja 1** projekti **XYZ värskenduse 2. etapp** jaoks.
7. Valige töötaja ja seejärel valige **Määra**.
8. Veenduge, et valiku **Tarkvaraarendaja 1** rida oleks eemaldatud projektist **XYZ värskenduse 2. etapp**.
9. Vahekaardil **Projektimeeskond ja ajastamine** kontrollige projekti **XYZ värskenduse 2. etapp** puhul seda, et töötaja, kelle eelmises etapis valisite, on lisatud kui **Tarkvaraarendaja**.

## <a name="requests-for-project-resources"></a>Projekti ressursside taotlused
Projekti ressursi ajastamise funktsioon võimaldab ressursihalduritel levitada töötajate ressursse kaasamistele või projektidele. Selle funktsiooni lubamiseks täitke järgmised tööülesanded või veenduge, et need oleks täidetud.

- Seadistage numriseeriad.
- Seadistage projektihalduse ja raamatupidamise töövood.
- Lubage ressursitaotluste töövood.

Pärast eelnevate toimingute lõpuleviimist saate vastavalt vajadusele täita järgmisi ülesandeid.

- Looge ressursi taotlus esialgselt broneeritud personali ressursilt.
- Jälgige ressursitaotlusi.
- Täitke ressursitaotlusi.
- Taotlege personali ressurssi WBS-ilt.
- Broneerige ressursid projektile ilma personaliga ressursi taotlust.

## <a name="monitor-project-teams"></a>Projektimeeskondade jälgimine
1. Lehel **Kõik projektid** valige link **Projekti ID** projekti **XYZ värskenduse 2. etapp** jaoks.
2. Kiirkaardil **Projektimeeskond ja ajastamine** veenduge, et loetletud projektiressursid oleksid õiged.
