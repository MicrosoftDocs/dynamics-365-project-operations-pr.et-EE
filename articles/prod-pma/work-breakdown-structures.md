---
title: Tööjaotuse struktuuride ülevaade
description: Tööjaotuse struktuur (WBS) on projekti jaoks tehtava töö kirjeldus. See on tööülesannete hierarhia, mis esindab projektimeeskonna arusaama töö koosseisust ning iga komponendi või tööülesande suurusest, maksumusest ja kestusest.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998816"
---
# <a name="work-breakdown-structures-overview"></a>Tööjaotuse struktuuride ülevaade

[!include [banner](../includes/banner.md)]

Tööjaotuse struktuur (WBS) on projekti jaoks tehtava töö kirjeldus. See on tööülesannete hierarhia, mis esindab projektimeeskonna arusaama töö koosseisust ning iga komponendi või tööülesande suurusest, maksumusest ja kestusest. WBS-il on kolm peamist eesmärki.

-   Kirjeldada tööülesannete töö jaotust ja kompositsiooni.
-   Projekti töö kavandamine.
-   Iga tööülesande maksumuse hindamine.

WBS üksikasjalikkuse aste sõltub hinnangute nõutavast täpsuse tasemest ja nende hinnangte suhtes kasutatava jälgimise tasemest. Projektid, millel on madal taluvus kõrvalekallete suhtes ajakavas või maksumuses, nõuavad tavaliselt üksikasjalikumat WBS-i ning töö edenemise ja kulude jälgimist WBS-is. Seda tüüpi projekt on levinud ehitus- ja tööstustehnoloogia valdkondades. 

Seevastu projektid sellistes tööstusharudes, nagu meedia ja reklaam, tarkvara ja IT-taristu, kipuvad olema ainulaadsed ning tootlikkus oleneb tööülesannet täitva üksikisiku kogemusest ja pädevusest. Seega kasutavad need majandusharud WBS-i, et saada ülevaade projekti ligikaudsest mahust, mitte projekti üksikasjaliku edenemise jälgimiseks. 

WBS loomine on intensiivne protsess, mida tehakse tavaliselt pika aja jooksul ja mis nõuab koostööd ning teavet paljudelt erinevatelt inimestelt. Selles teemas kirjeldatakse, kuidas saate kasutada WBS-i täiustusi, et rahuldada prognooside ja jälgimise nõudeid.

## <a name="prerequisites-for-creating-a-wbs"></a>WBS-i loomise eeltingimused
WBS-i loomiseks peab teil olema võimalik luua töögraafik ja prognoosida töö maksumust.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Töögraafiku loomise eeltingimused

WBS-i funktsioonide kõikide kavandamise võimaluste kasutamiseks lõpetage järgmine seadistus.

1.  Seadistage vaikekalender ja projekti kalender.
    1.  Klõpsake suvandit **Projektihaldus ja raamatupidamine** &gt; **Seadistamine** &gt; **Projektihalduse ja raamatupidamise parameetrid** &gt; **Kavandamine**. Väljal **Vaikimisi töökalender** määrake vaikekalender. See on kõigi uute loodavate projektide vaikimisi töökalender.
    2.  Saate vaikekalendrit konkreetse projekti jaoks muuta. Klõpsake projekti üksikasjade lehte ja seejärel kiirkaardil **Projektimeeskond ja kavandamine** värskendage välja **Plaanimiskalender**, valides muu kalendri.

2.  Seadistage standardsed tööpäevad ja tööaeg. Kalender, mille te määrate oma projekti jaoks töökalendriks, kasutatakse WBS-is, et määratleda järgmine teave.

-   Tööpäevad ja pühad
-   Töötundide arv päevas

Kalendris tööpäevade ja tööaja seadistamiseks või uue kalendri loomiseks klõpsake suvandit **Organisatsiooni haldus** &gt; **Levinud** &gt; **Kalendrid**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Töö maksumuse prognoosimise eeltingimused

WBS-i kogukulu prognoosimise võimaluste kasutamiseks peaksite seadistama töötajate kulud ja müügihinnad, töökategooriad, kulud ja tasud ning üksused.

-   Töö-, kulu- ja tasukategooriate kulude ja müügihinna seadistamiseks klõpsake suvandit **Projektihaldus ja raamatupidamine** &gt; **Seadistamine** &gt; **Hinnad**.
-   Üksuste maksumuse ja müügihinna seadistamiseks kasutage toote teabe halduses iga üksuse jaoks lehte **Kaubanduslepped** loendi lehel **Väljastatud tooted**.

## <a name="creating-a-wbs"></a>WBS loomine
WBS loomine hõlmab kolme tegevust.

1.  **Töö osadeks jagamine** – looge töö jaotamine hallatavateks tükkideks või ülesanneteks.
2.  **Töö kavandamine** – hinnake tööülesande lõpetamiseks vajalik aeg, määrake ülesande vastastikkused sõltuvused ja valige ülesannete algus- ja lõpukuupäevad.
3.  **Kulude hindamine** – hinnake iga ülesande kulud.

Järgmistest jaotistest leiate teavet selle kohta, kuidas saavad WBS-i võimalused iga selle tegevusega aidata.

### <a name="work-decomposition"></a>Töö osadeks jaotamine

Tööde jaotuse või töö osadeks jagamine on tavaliselt WBS-i loomisprotsessi esimene etapp. WBS-i funktsioonid toetavad töö jaotamise või osadeks jagamise järgmisi põhikonstruktsioone. 

**Projekti juurülesanne** – projekti juurülesanne on projekti ülataseme kokkuvõttev tööülesanne. Kõik muud projekti ülesanded luuakse selle alla. Juurülesande nimi on alati projekti nimele määratud. Juursõlme maht, kuupäevad ja kestus summeerivad juurülesande all olevate tööülesande väärtused. Te ei saa juursõlme atribuute muuta ega seda kustutada.

**Kokkuvõtvad ehk konteinerülesanded** – kokkuvõttev ülesanne on ülesanne, millel on alamülesanded või selle all on seotud ülesanded. Kokkuvõtval ülesandel pole oma tööpanust ega maksumust. Selle asemel on töö mahu ja kokkuvõtva ülesande kulu sellega seotud ülesannete töö mahu ja kulu summa. Seotud tööülesannete varaseimat alguskuupäeva kasutatakse kokkuvõtva ülesande alguskuupäevana ja seotud ülesande kõige hilisemat lõpukuupäeva kasutatakse lõpukuupäevana. Saate kokkuvõtva ülesande nime muuta, kuid te ei saa muuta mahu, kuupäevade ega kestuse kavandamise atribuute. Kokkuvõtva tööülesande kustutamisel kustutatakse ka kõik sellega seotud tööülesanded. 

**Lehesõlme tööülesanded** – lehesõlme ülesanded esindavad projekti kõige detailsemaid tööpakette. Lehesõlm on arvestuslik maht, plaanitud hulk ressursse, plaanitud alguskuupäev ja lõppkuupäev ning kestus. 

Saate lõpetada järgmised hierarhia tegevused, et lubada tööhierarhia loomine või projekti osadeks jaotamine. 

**Uus tööülesanne** – loodab uus ülesanne lisatakse automaatselt juursõlme alla ja ülesandele määratakse automaatselt WBS-i number. WBS-i number tähistab tööülesande taset hierarhias. Esimesel tasemel projekti juurülesandes olevate ülesannete jaoks kasutatakse numeratsiooniskeemi 1, 2, 3 ja nii edasi. Esimese taseme all olevate ülesannete jaoks kasutatakse numeratsiooniskeemi 1.1, 1.2, 1.3 ja nii edasi. Iga eelmise taseme alla lisatava taseme puhul lisatakse uus punktiirjoonega numbrite seeria. 

Hetkel te ei saa WBS-i nummerdamist kohandada. 

**Taandeülesanne** – kui te ülesande taandate, muutub see sellele eelneva ülesande suhtes alamülesandeks. Uue alamülesande WBS-i number arvutatakse vastavalt selle vanemüksuse WBS-i numbrile uuesti. Ülemülesanne on nüüd kokkuvõte või konteinerülesanne ja seega muutub sellele järgnevate ülesannete kokkuvõtteks. 

> [!NOTE] 
> Kui taandate tööülesanded ülesande alla, mis oli enne taandamise toimingut lehesõlm, siis vastloodud kokkuvõttev ülesanne kaotab oma kuupäevad, mahu ja ressursside arvu. See kasutab nüüd oma uute seotud ülesannete väärtuste kokkuvõtet. 

**Ülesande eendamine** – kui te ülesande eendate, ei ole see enam oma ülemülesandega seotud ülesanne. Selle tööülesande WBS-i number arvutatakse automaatselt ümber, et kajastada ülesande uut taset hierarhias. Eelmise peamise ülesande maht, kulu ja kuupäev arvutatakse ümber, et see ülesanne välistada. 

**Nihuta üles ja Nihuta alla** – valikuid **Nihuta üles** ja **Nihuta alla** klõpsates muudate tööülesande paigutust selle peamise ülesande hierarhia piires. Ülesande asend mõjuta ülesande mahtu, kulusid, kuupäevi ega kestust. Samas tööülesande WBS-i number arvutatakse automaatselt ümber, et kajastada ülesande uut asukohta.

### <a name="schedule-estimation"></a>Ajakava prognoosimine

Ajakava prognoosimine on tavaliselt WBS-i loomise teine etapp. Hea tavana peaksite lõpetama ajakava prognoosimise pärast ülesannete loomist. Finance’is lehel **Tööjaotuse struktuur** on kaks jaotist. Ülemine paan on mõeldud ajakava hindamiseks ja alumisel paanil on **Prognoositud kulud ja tulud**, mida saate kasutada kulude hindamiseks. 
**Tööülesande sõltuvused** – WBS-is saate luua tööülesannete vahel eelkäija seose. Kui määrate ülesandele eelkäijast ülesande, siis see ülesanne saab käivituda ainult pärast oma eelkäijast ülesande lõpetamist. Tööülesande kavandatav alguskuupäev seatakse automaatselt kõigi selle eelkäijate hiliseimale kuupäevale. 

**Tööülesande kavandamine** – lehtsõlme ülesannete kavandamise määratlevad järgmised tegurid.

-   Eelkäijad
-   Pingutus
-   Ressursside arv
-   algus- ja lõppkuupäevad;

Eelkäijateta lehesõlme ülesande alguskuupäev määratakse automaatselt projekti ajakava alguskuupäevale. Lehesõlme ülesande kestuseks arvutatakse alati algus- ja lõppkuupäeva vaheline päevade arv. 

*<strong><em>Plaanimise reeglid</em></strong>* – kui automaatne plaanimise abiline on sisse lülitatud, kehtivad lehesõlme ülesannete plaanimisele järgmised reeglid.

-   Ülesande algus- ja lõppkuupäev peavad alati olema projekti plaanimiskalendrile vastavad tööpäevad.
-   Eelkäijatega ülesande alguskuupäev on automaatselt määratud selle eelkäijate hiliseimale lõppkuupäevale.
-   Ülesande maht arvutatakse automaatselt järgmiselt:

inimeste arv × kestus × projektikalendri standardse tööpäeva tundide arv. 

Mõnikord võib olla vaja neist reeglitest erinevalt tegutseda. Saate automaatse kavandamise välja lülitada, et takistada rakendusel Finance lehesõlme ülesannete mis tahes seadistamist või parandamist. Kui sisestate teavet ülesande jaoks, mis põhjustab mis tahe plaanimise reeglite rikkumist, kuvatakse ülesande jaoks kavandamise vea ikoon. Kui te ei soovi kavandamise tõrkeid kuvada, klõpsake nuppu **Kuvatakse tõrgevead**, et tõrge välja lülitada. 

> [!NOTE] 
> Kokkuvõtte või konteinerülesande väärtuseid arvutatakse jätkuvalt seotud ülesannete väärtuste summana, olenemata sellest, kas automaatse kavandamise abi on sisse või välja lülitatud. 

**Kavandamisvigade parandamine** – kui automaatne kavandamise abi on sisse lülitatud, siis kavandamise vigu tõenäoliselt ei esine. Samas kui te lülitate automaatse kavandamise abi välja ja lülitate selle hiljem uuesti sisse, siis võivad WBS-is ilmuda kavandamise tõrkeikoonid. 

**Kavandamise vigade parandamine tööülesannete alusel** – kui te topeltklõpsate konkreetse ülesande ajakava viha, kuvatakse dialoogikast selle ülesande kavandamise vigadega. Saate otsustada, milliseid ülesande kavandamise vead tahate parandada. 

**Kõikide kavandamise vigade parandamine** – kui soovite et Finance parandaks WBS-is kõik kavandamise vead, klõpsake käsku **Paranda kõik kavandamise lahknevused**. 

> [!NOTE] 
> See funktsioon võib põhjustada WBS-is olulisi muudatusi. Vead parandatakse järgmises järjestuses.

1.  Kõigi tööülesannete eeldatavat mahtu muudetakse, et see oleks võrdne projektikalendris määratletud võimsusega.
2.  Iga tööülesande alguskuupäeva muudetakse nii, et tööülesanne käivitub pärast kõigi selle eelkäijate toimingute lõppemist.
3.  Iga tööülesande alguskuupäeva muudetakse, et eemaldada lüngad eelnevate tööülesannete alguskuupäevadega võrreldes.

### <a name="cost-estimation"></a>Kuluprognoos

Nagu me selles dokumendis varem mainisime, siis te sisestate iga lehesõlme ülesande kuluprognoosi kasutades vahekaarti **Prognoositud kulud ja tulud** lehe **Tööjaotuse struktuur** alumisel paanil. 

> [!NOTE] 
> Saate kokkuvõtte või konteinerülesande kuluprognoosi muuta. Kokkuvõtva ülesande kuluprognoos on võrdne selle lehesõlme ülesannete kuluprognooside summaga. Iga ülesande prognoositav kogukulu arvutatakse kuluprognooside summana järgmiste tehingutüüpide jaoks.

-   Töö
-   Ese või materjal
-   Kulud

Kandetüüpi **Tasu** kasutatakse tasupõhise tulu prognoosimiseks. Sellel kandetüübil ei ole kulukomponenti ja seega sellega ei arvestata kulude prognoosimisel. 

Kande tüüpi **Kontol** ei kasuta lepingulise müügiväärtuse salvestamiseks fikseeritud väärtusega tüüpi projektis. Seda tüüpi kandetüüpi ei arvestata ka juhul, kui kulusid hinnatakse. 

Kui prognoosite tööjõu- ja materjalikulu ning iga ülesande kulusid, peate määrama prognoositavatele kuludele projektikategooria. 

**Tööjõukulude prognoosimine** – te määrate iga lehesõlme ülesande jaoks töömahu tundides ja vaikekategooria. Seetõttu, kui seadistate tööülesande ajakava, lisatakse selle tööülesande tööjõukulude prognoos automaatselt töö vaikekategooriasse. See kuluprognoos kuvatakse selle tööülesande vahekaardil **Kulu- ja tuluprognoosid** ruudustikus **Rea üksikasjad**. Kui vajate rohkem tööjõukulu prognoose, saate need sellele vahekaardile lisada. Kui te suurendate või vähendate tundide hulka tööjõukulu prognoosis, siis tööülesande ajakava arvutatakse automaatselt ümber. 

**Kulude ja materjalikulu prognoosimine** – vahekaart **Kulude ja tulu prognoosid** võimaldab teil prognoosida ülesande kulu ja materjalikulusid, kui te vajate prognoose. 

Iga tööjõu või kuluprognoosi rea maksumus ja müügihind põhinevad seadistusel, mis on määratletud iga kategooria jaoks hinnatabelites suvandis **Projektihaldus ja raamatupidamine** &gt; **Häälestamine** &gt; **Hinnakujundus**. Üksused, maksumus ja müügihind lisatakse vaikimisi üksuse või kaubanduslepingutest leheloendis **Väljastatud tooted** tooteteabe halduses.

## <a name="tracking-progress-on-the-wbs"></a>Edenemise jälgimine WBS-is
Mõned majandusharud jälgivad projekti edenemist WBS-iga võrreldes väga üksikasjalikul tasemel, samas kui teised jälgivad edenemist WBS-is kõrgemal tasemel. Selles jaotises kirjeldatakse, kuidas saate kasutada WBS-i jälgimist vastavalt enda projektinõuetele. 

Rakendusel Finance on WBS-is projekti kohta kolm vaadet: kavandamise vaade, mahu jälgimise vaade ja kulude jälgimise vaade.

### <a name="planning-view"></a>Kavandamise vaade

Kavandamise vaates kuvatakse ajakava ja kulu teabe kavandatav või algne hinnang. Kui WBS-is ei ole projekti versiooni ja algväärtuse jälgimiseks funktsioone, on selle vaate väärtused mõeldud põhiversiooni esindamiseks. Selle teema ajakava prognoosi ja kuluprognoosi jaotised kirjeldavad seda vaadet ja kuidas seda WBS-i loomiseks kasutatakse.

### <a name="effort-tracking-view"></a>Panuse jälgimise vaade

Mahu jälgimise vaade kuvab WBS-is ülesannete edenemise jälgimist. See võrdleb tööülesande tegeliku mahukoormuse tunde plaanitud mahukoormuse tundidega. Järgmised valemid annavad mahu jälgimise vaates väärtuseid.

-   Edenemisprotsent = tegelik panus senini ÷ ülesandele plaanitud panus
-   Ülejäänud panus (tuntud ka kui lõpetamise prognoos \[ETC\]) = plaanitud panus – seni tehtud tegelik panus
-   Hinnang lõpetamisel (EAC) = ülejäänud panus + seni tehtud panus
-   Eeldatav panuse hälve = plaanitud panus – EAC

Koormuse jälgimise vaade kuvab ülesande eeldatava panuse hälbe, mis põhineb sellel, kas EAC on suurem või väiksem kui plaanitud panus.

-   Kui EAC on plaanitud panusest suurem, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega ja on graafikust maas.
-   Kui EAC on plaanitud panusest väiksem, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega ja on graafikust ees.

**Projektijuhi mahu ümberkavandamine** – aeg-ajalt projektijuht või mõni muu isik, kes jälgib projekti edenemist, peab vaatama üle ülesande algsed prognoosid. Ülesanne võib erinevate põhjuste tõttu algselt oodatust kiiremini või aeglasemalt liikuda. Näiteks ulatust on vähendatud või on töötajatel algselt planeeritust vähem kogemusi. Kavandamised hõlmavad projektijuhi ettekujutust prognoosidest, mis põhinevad projekti praegusel olekul. Üldiselt te ei peaks alusjoone numbreid muutma, kuna projekti alusjoon esindab hästi avaldatud dokumenti projekti ajakava ja kuluprognoosi jaoks, millega kõik projekti huvirühmad on nõustunud. 

Projektijuhid saavad ülesannete panust muuta kahel viisil.

-   Muutke ülejäänud mahtu, mis on automaatselt määratud tegeliku allesjäänud ülesande mahu värskendamine.
-   Muutke edenemisprotsenti, mis on automaatselt määratud värskendama ülesande tegelikku edenemist.

Mõlemad need lähenemised põhjustavad ülesande ETC, EAC ja edenemisprotsendi ning ülesande eeldatava panuse hälbe ümberarvutamist. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja edenemisprotsent ning nende prognoositud panuse hälve värskendatakse. 

**Kokkuvõtte ülesannete muudetud panus** – saate muuta kokkuvõtte või konteinerülesannete panust. Sõltumata sellest, kas te muudate neid väärtuseid kasutades järelejäänud panust või kokkuvõtlike ülesannete edenemisprotsenti, siis arvutused toimuvad automaatselt järgmises järjestuses.

1.  Arvutatakse ülesande EAC, ETC ja edenemisprotsent.
2.  Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui esialgne EAC kogus.
3.  Arvutatakse iga lehesõlme ülesande uus EAC.
4.  Ülejäänud panus ja edenemisprotsent arvutatakse uue EAC väärtuse põhjal uuesti kõigi mõjutatud alamülesannete jaoks. Nende ülesannete panuse hälve arvutatakse samuti uuesti.
5.  Kokkuvõtlike ülesannete EAC arvutatakse lehesõlmedest samuti uuesti.

Klõpsake panuse jälgimise vaates suvandit **Laienda tasemeni**, et määrata tase, mille juures teie WBS-i jälgida ja säilitada. WBS laiendatakse panuse jälgimise vaates automaatselt sellele tasemele iga kord, kui selle avate.

### <a name="cost-tracking-view"></a>Kulude jälgimise vaade

Kulude jälgimise vaade kuvab ülesande kulu tarbimise jälgimise. Selles vaates võrreldakse tööülesande seni kulutatud tegelikke kulusid tööülesande planeeritud kuluga. Järgmised valemid annavad kulu jälgimise vaates väärtuseid.

-   Tarbitud kulu protsent = senini kulutatud tegelik kulu ÷ ülesandele plaanitud kulu
-   Lõpetamise kulu (CTC) = plaanitud kulu – seni kulutatud tegelik kulu
-   Hinnang lõpetamisel (EAC) = CTC + seni kulutatud tegelik kulu
-   Eeldatav kuluhälve = plaanitud kulu – EAC

Kulu jälgimise vaade kuvab ülesande eeldatava kulu hälbe, mis põhineb sellel, kas EAC on suurem või väiksem kui plaanitud kulu.

-   Kui EAC on plaanitud kulust suurem, siis eeldatakse, et ülesanne kasutab algselt plaanitust rohkem raha ja on üle eelarve.
-   Kui EAC on plaanitud kulust väiksem, siis eeldatakse, et ülesanne kasutab algselt plaanitust vähem raha ja on alla eelarve.

**Projektijuhi tehtud kulude ümberkavandamine** – projektijuhid peavad kasutama CTC-d, et vaadata üle ülesande algne kuluprognoos. Projektijuht saab muuta CTC väärtuse kulule, mis on vajalik ülesande lõpule viimiseks. Kui muudate CTC väärtust, siis ülesande CTC, EAC ja tarbitava kulu protsent ning tööülesande prognoositava kulu hälve arvutatakse uuesti. Lisaks arvutatakse ümber ka kokkuvõtlike ülesannete EAC, ETC ja tarbitud kulu protsent ning nende prognoositud kulu hälve värskendatakse. 

> [!NOTE] 
> Kui redigeerite koormuse jälgimise vaates WBS-i ülesande koormust, siis ülesande CTC, EAC, tarbitud kulude protsent ja prognoositud kulu hälve arvutatakse kulu jälgimise vaates uuesti. Samas kulude läbivaatamine panuse jälgimise vaates väärtuseid ei mõjuta, kuna kulu kandetüübi (töö, materjal või kulu) või projekti kategooria järgi ei muudeta. 

**Kokkuvõtlike ülesannete kulude prognoosi läbivaatamine** – saate kokkuvõtlike ülesannete kulud üle vaadata ja arvutused kuvatakse automaatselt järgmised järjestuses.

1.  Ülesande tarbitud EAC, CTC ja kuluprotsent arvutatakse uuesti.
2.  Uus EAC jaotatakse alamülesannete vahel samas proportsioonis kui oli ülesannete esialgne EAC.
3.  Iga tööülesande uus EAC arvutatakse.
4.  Tarbitud CTC ja kulu protsent arvutatakse EAC väärtuse põhjal uuesti kõikide alamülesannete jaoks. Nende ülesannete kulu hälve arvutatakse samuti uuesti.
5.  Kõikide kokkuvõtlike ülesannete EAC arvutatakse selle muudatuse põhjal uuesti.

Klõpsake kulu jälgimise vaates suvandit **Laienda tasemeni**, et määrata tase, mille juures teie WBS-i jälgida ja säilitada. WBS laiendatakse kulu jälgimise vaates sellele tasemele iga kord, kui selle avate.

### <a name="earned-value-management"></a>Teenitud väärtuste haldus

Projekti edenemise jälgimiseks saate kasutada teenitud väärtuse meetodit (EVM). Saate teenitud väärtuse mõõdikuid vaadata projektijuhi rolli keskuses. Teenitud väärtuse diagrammi komponent näitab plaanitud väärtuse ja tegeliku kulu ajafaasi väärtusi. Praeguse kuupäeva teenitud väärtus kuvatakse punktina. Teenitud väärtuse ajafaasi andmed ei ole hetkel saadaval. 

Teenitud väärtuse diagrammi ajafaas kuvatakse nädala või kuu kaupa. Selles jaotises kirjeldatakse EVM kolme sammast: kavandatud väärtus, teenitud väärtus ja tegelik kulu. 

**Kavandatud väärtus** – EVM-i teooria ütleb, et kavandatud väärtus esindab määra, mille juures projektimeeskond plaanis projekti jaoks väärtust teenida. 

Finance kasutab plaanitud väärtuse kavandamisel 0:100 teenimise reeglit. Selle reegli kohaselt sisestatakse tööülesande väärtus tööülesandesse selle lõppkuupäeva seisuga. Väärtust ei sisestata enne, kui tööülesanne on 100 protsenti lõpetatud. 

Projektihalduses ja raamatupidamises te sisestate lehesõlmede lõpukuupäeva ja selle kavandatud kulu. Kui plaanitud väärtuse graafil kuvatakse nädala põhiselt, siis summeeritakse plaanitud väärtus nädala põhjal kõikide lehesõlme ülesannete jaoks projekti kestuse jooksul. 

**Teenitud väärtus** – EVM-i teooria ütleb, et teenitud väärtus esindab määra, mille juures projektimeeskond tegelikul projekti jaoks väärtust teenib. 

Finance kasutab teenitud väärtuse kavandamisel 0:100 teenimise reeglit. Selle reegli kohaselt sisestatakse tööülesande väärtus tööülesandesse selle lõppkuupäeva seisuga. Väärtust ei sisestata enne, kui tööülesanne on 100 protsenti lõpetatud. 

Teenitud väärtuse arvutamisel arvestatakse iga ülesande edenemise protsendiga. 0:100 teenimise reegli kohaselt arvestatakse konkreetse perioodi lõpus teenitud väärtuse arvutamisse ainult ülesanded, mis on sellel perioodil lõpetatud. Projekti teenitud väärtus arvutatakse kõigi tööde jaoks, mis on graafiku loomise ajaks lõpule viidud. 

> [!NOTE] 
> Hetkel ei oma WBS-i jälgimise süsteem iga ülesande ajaloolise edenemise protsentide talletamiseks andmestruktuure. Seega saab teenitud väärtusest teatada ainult kuubi töötlemise ajal. Töötlege kuupi regulaarselt, et värskendada rolli keskuses kuvatavaid teenitud väärtuse andmeid. 

**Tegelik kulu** – EVM-i teooria kohaselt tegeliku kulu seos esindab projektile raha kulutamise määra. 

Projektile postitatud kandeid kasutatakse tegeliku kulurea kavandamiseks. Kulud summeeritakse kuupäeva järgi. Neid andmeid kasutatakse seejärel tegelike kulude teenitud väärtuse diagrammil nädala või kuu lõikes kuvamiseks.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Planeeritud väärtuse, teenitud väärtuse ja tegeliku kulu mõistete kasutamine

**Ajakava hälve**– kavandamise ajal saate luua ajajoonel töötamiseks prognoosi. Seega on kavandatav väärtus määr, mille järgi projekti planeerijad arvasid, et töö projekti kestel lõpetatakse. Pärast projekti edenemist töö lõpetatakse ja projekt teenib väärtust. Kavandatud väärtuse teenitud väärtusega võrreldes saate vaadata, kuidas projekti töö edeneb. Selle võrdluse tulemust nimetatakse ajakava hälbeks. 

Kui perioodi planeeritud väärtus on suurem kui teenitud väärtus, siis on projektiga tehtud töö kogus väiksem kui plaanitud. Seega on projekt graafikust maas. Kuna kavandatud väärtus ja teenitud väärtus on väljendatud rahalises mõttes, antakse ka projekti maha jäämisele rahaline väärtus. 

Kui perioodi planeeritud väärtus on väiksem kui teenitud väärtus, siis on projektiga tehtud töö kogus suurem kui plaanitud. Seega on projekt graafikust ees. Sellele täitmisajale antakse samuti rahaline väärtus.

**Kuluhälve** – kuna teenitud väärtus kasutab omahinda kordistajana, näitab teenitud väärtus projekti kallal tehtud töö kulu. Projekti edenedes esitab kandelogi rahalise kirje, mis tegelikult sellele projektile kulutatakse. Teenitud väärtust tegeliku kuluga võrreldes saate vaadata rahasummat, mis kulutatakse, võrreldes selle teenitud väärtusega. Selle võrdluse tulemust nimetatakse kulu hälbeks. 

Kui perioodi jooksul kulutatud tegelik kulu on suurem kui teenitud väärtus, siis kulutati rohkem raha kui teeniti. Seega on projekt üle eelarve. 

Kui perioodi jooksul kulutatud tegelik kulu on väiksem kui teenitud väärtus, siis teeniti rohkem raha kui kulutati. Seega on projekt alla eelarve.

## <a name="wbs-templates"></a>WBS-i mallid
WBS-i mallide funktsiooni abil saate luua projektidele standardmalle. Kui teie ettevõtte pakutavad projektid hõlmavad palju korduvat tööd, peaksite kaaluma WBS-i malli loomist. 

Saate luua WBS-i malli olemasoleva projekti WBS-ist, et selle projekti planeerimise ajal kogutud teadmisi ja parimaid tavasid saaks tulevikus sarnaste projektide jaoks uuesti kasutada. Samas mõnikord ei ole mõistlik tervet WBS-i mallina salvestada. Seega saate luua ka projekti jaoks malle WBS-i osadest.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projekti WBS-i salvestamine mallina

Pärast malli loomist saate selle importida juursõlme all uue projekti WBS-i või mis tahes tööülesande all projekti WBS-is.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS-i malli importimine projekti WBS-i

Tööülesannete importimisel korrastatakse mallis olevad tööülesanded vastavalt selle tööülesande alguskuupäevale, mille all need imporditakse. Importimisel kasutatakse imporditud ülesannete alguskuupäevade arvutamiseks malli ülesannete eelkäija seoseid. Imporditud tööülesannete lõppkuupäeva arvutamiseks rakendatakse sihtkoha projekti standardset töökalendrit, et säiliksid praeguses projektikalendris määratud tööpäevad ja standardne tööaeg. 

Prognoosiridade kulu summad ja müügihinnad rakendatakse tagamaks, et projektile või projekti lepingule spetsiifilistel hindadel oleksid kehtiva kuupäevaga.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Projekti WBS-i ja WBS-i malli erinevused

-   WBS-i ülesannetel ei ole alguskuupäevi ega lõpukuupäevi.

WBS-i mallides ei ole tööpäevad ja mitte-tööpäevad määratud.

-   WBS-i mallid kasutavad alati plaanimiskalendrit, mis seadistatakse kõikide projektide jaoks vaikekalendrina.

Vaikimisi plaanimiskalendrit kasutatakse ainult standardse tööpäeva tundide välja selgitamiseks.

-   Eelkäija seoseid WBS-i malli ei kopeerita.

Kuna WBS-i mallid ei sisalda kuupäevi, pole eelkäija lõpukuupäeval põhinev alguskuupäeva loogika nõutav.

-   Tööjõukulude prognoosirida luuakse automaatselt, kui ülesanne luuakse WBS-i mallis. Müügihind ja kulu summa kopeeritakse valitud töötajalt.

Kulusid ja üksuse kulusid saab luua käsitsi, nagu ka projekti WBS-is.

-   Kuvatakse ajastamise vead, kui esineb kõrvalekaldeid järgmisest valemist.

Koormus = ressursside arv × kestus × tundide arv standardsel tööpäeval 

Saate kõik ajastamise vead samaaegselt parandada, kui klõpsate valikut **Paranda kõik ajastamise vead**. 

Teise võimalusena saate parandada ajastamise vigu individuaalselt, klõpsates iga ülesande hoiatusikooni.





[!INCLUDE[footer-include](../includes/footer-banner.md)]