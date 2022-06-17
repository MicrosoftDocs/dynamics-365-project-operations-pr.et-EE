---
title: Mis on uut märtsis 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval project Operationsi 2022. aasta märtsi väljaandes ressursi-/ladustamata stsenaariumide jaoks.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910901"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut märtsis 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.30.0.99
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.25

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Per diems on nüüd toetatud uues ja ümberkujundatud kaasaegses kuluruumis. Ettevõtted, kes kasutavad päevaraha, võimaldavad seda funktsiooni kasutajatele hõlpsalt esitada ja hüvitada nende päevaraha kulud. Lisateavet vt teemast [Per diem costs](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises loendis kuvatakse kahe kirjutamise kaardid, mida on project Operations 2022. aasta märtsi väljaandes muudetud või lisatud.

| **Olemikaart** | **Värskendatud versioon** | **Kommentaarid** |
| --- | --- | --- |
| Project Operationsi integreerimise projekti hankija arve rea ekspordiolem msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Vastendused on värskendatud, et viia see vastavusse hankija arve rea olemiga rakenduses Dataverse. <br>Ärge aktiveerige vastendusversiooni 1.0.0.4. See on valmis kasutamiseks koos Finance'i keskkonna versiooniga 10.0.26 järgmises igakuises värskenduses. |

Käivitage alati oma keskkonnas kaardi uusim versioon ja lubage project Operationsi Dataverse lahenduse ja Finance'i lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas olevat tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises Kaartide [jaotises Puudu tabeliveergude probleemi juhiseid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Aeg ja kulu | 2388011 | Saate hulgikinnituse ajal kuvada ajasisesinemise esitajatele tagasilükkamise kommentaarid. |
| Projekti plaanimine ja jälgimine | 2495294 | Projekti üksikasjad ei tohi olla redigeeritavad **lehel Tööülesande üksikasjad**. |
| Arveldamine ja hinnakujundus | 2499605 | Pakkumise vahe-eesmärkidest loodud lepingu verstapostid märgitakse valesti kirjutuskaitstuks. |
| Projekti plaanimine ja jälgimine | 2506050 | Toimingukomplekt jääb ootele üheks tunniks, kui salvestamiseks pole muudatusi. Seejärel märgitakse komplekt valesti **nurjunuks**, samas kui see tuleks kohe lõpule viia. |
| Arveldamine ja hinnakujundus | 2507401 | Vaikimisi lepingulised üksused sisestatakse projektidele valesti vale vahemällu salvestamise tõttu. |
| Arveldamine ja hinnakujundus | 2541660 | **Müügitellimuse loomise kinnitamine** topeltkirjutuses peaks olema ainult projektipõhiste tellimuste puhul. |
| Arveldamine ja hinnakujundus | 2552745 | Maksu ei jagata klientide vahel, kes on seadistanud tükeldatud arveldusreeglid. |
| Arveldamine ja hinnakujundus | 2558859 | Täiustatud tõrketeated hinnakujundusdimensioonide seadistamisel. |
| Arveldamine ja hinnakujundus | 2558933 | **Importimine projekti hinnangutest** nurjub, kui **msdyni\_ projekt** lisatakse hinnakujundusdimensioonina. |
| Arveldamine ja hinnakujundus | 2559101 | Projekti parameetrite kustutamist ei blokeerita ja see põhjustab probleeme. |
|   Müügivõimaluste haldus | 2570390 | Topeltkirjutusega pistikprogramm sunnib konto tüüpi pakkumistele, tellimustele ja võimalustele olla **klient**, isegi kui see kontotüüp pole õige. |
| Arveldamine ja hinnakujundus | 2586097 | Tükeldatud arveldatud kulu tegelikke andmeid ei tühistata, kui projekt projektilepingu realt eemaldatakse. |
| Arveldamine ja hinnakujundus | 2589619 | Sissekirjutamismaterjali maks paljundatakse sisestamata müügireaalsustele ja arvele. |
|   Müügivõimaluste haldus | 2594015 | Pakkumist ei saa sulgeda nii, nagu see on võidetud klientidele, kellel on **Net60** maksetingimused. |
| Projekti plaanimine ja jälgimine | 2595841 | Project for the Webis saavad kasutajad uue ressursitaotluse loomisel tõrketeate puuduva **msdyni\_ tegeliku alguse** kohta. |
| Aeg ja kulu | 2602511 | Ajakannete **väli Tagasilükatud** kuvab **hülgaja asemel süsteemi**, mitte nimega kasutaja. |
| Aeg ja kulu | 2602528 | Projekti kinnitaja saab kinnitada aega projektides, kus neid pole kinnitajana loetletud. |
| Arveldamine ja hinnakujundus | 2608550 | Parandusarvet saab kinnitada ka siis, kui originaalis muudatusi ei ole. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Välja Kategooria ID **lubatud pikkuses** on finance'i ja projektitoimingute vahel ebakõla. |
| Projektihaldus ja raamatupidamine | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fikseeritud hinnaga projekte ei saa kõrvaldada, kui **välja Ettemaksu arveldamine** väärtuseks **on seatud Kasum ja kahjum** ning **kasutatakse põhimõtet Lõpetatud protsent**. |
| Projektihaldus ja raamatupidamine | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Projekti seadistusest sisestatakse projekti seadistusest projekti seadistusest projekti toimingute integratsioonižurnaali kuluridadele vale käibemaksu vaikegrupp. |
| Projektihaldus ja raamatupidamine | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Projektiarve ettepaneku päise dimensioone ei saa projektitoimingutega integreeritud juurutuses redigeerida. |
| Projektihaldus ja raamatupidamine | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Kontsernisiseseid hankija arveid ei tohi rakendusega Dataverse integreerida. |
| Projektihaldus ja raamatupidamine | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Kliendi saldode valuutas ja aruandlusvaluutas on mittevastavus. |
| Projektihaldus ja raamatupidamine | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektiarve saate konteerida ka siis, kui klient on kõigi arvete puhul ootel. |
| Projektihaldus ja raamatupidamine | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Nupp **Kustuta kõik read** puudub projektiarve ettepanekutest, millel on vaated Päis **ja** **Read**. |
| Projektihaldus ja raamatupidamine | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Hankija arve konteerimisel ilmneb järgmine tõrge: "Arve arvestuskuupäev peab olema samal aruandeaastal kui seotud ostetud tellimus. Käivitage ostutellimuse aastalõpu protsess või muutke kuupäev jooksvaks aruandeaastaks." |
| Reisimine ja kulu | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Projekti pühendunud kulusid ei vabastata pärast reisitaotluse pühendunud kulude vabastamist. |
| Reisimine ja kulu | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kuluaruande esitamisel ilmneb järgmine tõrge: "Stack Trace: Ettevõtet pole olemas." |
| Reisimine ja kulu | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Projekti vaike-ID-d **ei** sisestata kuluaruannetele, **kui projektis on valitud parameeter Nõua tegevust žurnaali** jaoks. |
| Reisimine ja kulu | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Nupp **Konteeri kulusid** ei tööta projektitoimingutes ressursi-/ladustamata stsenaariumide puhul õigesti. |
| Reisimine ja kulu | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Läbisõidu kuluaruande puhul **, mis sisaldab reisijaid, on probleem kiirusega miili** kohta. |
| Reisimine ja kulu | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Töötajate kulu läbisõidumäärasid ei summeerita õigesti, kui läbisõidumäära kulukategoorias **kasutatakse** kahte erinevat sõidukitüüpi. |
| Reisimine ja kulu | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Reisitaotluse rea välja Projekt **otsing** ei tagasta õiget projektide loendit. |
| Reisimine ja kulu | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Ülevaatuse** läbisõit näitab hoiatust kuluaruannete kohta. |
| Reisimine ja kulu | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Kviitungi optilise märgituvastuse (OCR) teenus ei tööta kulu OCR-teenuse URL-i probleemi tõttu. |
| Reisimine ja kulu | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **Kui funktsioon Võime korduvaid kulusid kiiresti** loetleda on lubatud, muudavad kuluaruannete üksikasjalikel ridadel olevad summad summasid iga kord, **kui leht Itemize** avatakse. |
| Reisimine ja kulu | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Kuluaruannet ei saa kustutada, kui vaheloendis on mitu kinnitajat. |

## <a name="removed-and-deprecated-features"></a>Eemaldatud ja aegunud funktsioonid

Artiklis [Eemaldatud või aegunud funktsioonid jaotises Project Operations](removed-depreciated-features-project.md) kirjeldatakse funktsioone, mis on rakenduse jaoks Dynamics 365 Project Operations eemaldatud või aegunud.

- Eemaldatud funktsioon pole enam tootes saadaval.
- Aegunud funktsioon pole aktiivses arenduses ja võidakse tulevases värskenduses eemaldada.

Amortisatsiooniteade kuvatakse [Project Operationsi](removed-depreciated-features-project.md) artiklis Eemaldatud või aegunud funktsioonides 12 kuud enne mis tahes funktsiooni tootest eemaldamist.

Muudatuste katkestamiseks, mis mõjutavad ainult kompileerimisaega, kuid on binaarsed ühilduvad liivakasti ja tootmiskeskkondadega, on amortisatsiooniaeg vähem kui 12 kuud. Tavaliselt on need muudatused funktsionaalsed värskendused, mis tuleb kompilaatorile teha.
