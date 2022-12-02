---
title: Mis on uut märtsis 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet kvaliteedivärskenduste kohta, mis on saadaval 2022. aasta märtsikuu rakenduse Project Operationsi väljaandes ressursi-/mittelaopõhiste stsenaariumide jaoks.
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

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.30.0.99
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.25

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Uues ja ümberkujundatud kaasaegses kulutööruumis toetatakse nüüd päevarahasid. Ettevõtted, kes kasutavad päevaraha, saavad selle funktsiooni lubada, et kasutajad saaksid hõlpsasti päevaraha esitada ja nende eest hüvitust. Lisateavet leiate teemast [Päevaraha kulud](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises loendis kuvatakse topeltkirjutusega kaardid, mida on muudetud või lisatud Project Operationsi 2022. a märtsi väljaandes.

| **Olemikaart** | **Värskendatud versioon** | **Kommentaarid** |
| --- | --- | --- |
| Project Operationsi integratsiooni projekti hankija arve ekspordirea olem msdyn\_projectvendorinvoicelines | 1.0.0.3 | Vastendusi värskendati, et viia need vastavusse teenuses Dataverse hankija arve rea olemiga. <br>Ärge aktiveerige vastendusversiooni 1.0.0.4. See on järgmise igakuise värskendusega valmis kasutamiseks koos rahanduse keskkonna versiooniga 10.0.26. |

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Aeg ja kulu | 2388011 | Kuva tagasilükkamise kommentaarid, et ajastada kirje esitajad hulgikinnituse ajal. |
| Projekti plaanimine ja jälgimine | 2495294 | Projekti üksikasju ei tohi lehel **Ülesande üksikasjad** muuta. |
| Arveldamine ja hinnakujundus | 2499605 | Hinnapakkumise vahekokkuvõtetest loodud lepingu vahekokkuvõttes on valesti märgitud kirjutuskaitstuks. |
| Projekti plaanimine ja jälgimine | 2506050 | Toimingukomplekt jääb ootele üheks tunniks, kui salvestamiseks ei tehta muudatusi. Seejärel märgitakse komplekt ekslikult kui **Ebaõnnestunud**, kuigi see tuleks kohe lõpule viia. |
| Arveldamine ja hinnakujundus | 2507401 | Lepingu vaikeühikud sisestatakse projektidesse valesti vale vahemällusalvestuse tõttu. |
| Arveldamine ja hinnakujundus | 2541660 | **Müügitellimuse loomise valideerimine** peaks topeltkirjutuses olema ainult projektipõhiste tellimuste jaoks. |
| Arveldamine ja hinnakujundus | 2552745 | Maksu ei jaotata klientide vahel, kes on seadistanud jagatud arveldusreeglid. |
| Arveldamine ja hinnakujundus | 2558859 | Täiustatud tõrketeated hinnakujunduse dimensioonide seadistamisel. |
| Arveldamine ja hinnakujundus | 2558933 | **Projekti prognooside importimine** ebaõnnestub, kui hinnadimensiooniks lisatakse **msdyn\_project**. |
| Arveldamine ja hinnakujundus | 2559101 | Projekti parameetrite kustutamine ei ole blokeeritud ja põhjustab probleeme. |
|   Müügivõimaluste haldus | 2570390 | Topeltkirjutuse pistikprogramm sunnib pakkumiste, tellimuste ja võimaluste konto tüübiks olema **Klient**, isegi kui see kontotüüp pole õige. |
| Arveldamine ja hinnakujundus | 2586097 | Jaotatud arveldatud kulude tegelikke näitajaid ei pöörata tagasi, kui projekt eemaldatakse projekti lepingurealt. |
| Arveldamine ja hinnakujundus | 2589619 | Sisestatava materjali maks kantakse arveldamata müügi tegelikele näitajatele ja arvele. |
|   Müügivõimaluste haldus | 2594015 | Hinnapakkumist ei saa võidetuna sulgeda klientidele, kellel on **Net60** maksetingimused. |
| Projekti plaanimine ja jälgimine | 2595841 | Rakenduses Project for the Web saavad kasutajad uue ressursitaotluse loomisel tõrketeate puuduva **msdyn\_actualstart** kohta. |
| Aeg ja kulu | 2602511 | Ajakirjete väljal **Tagasilükkaja** kuvatakse tagasilükkajana nimega kasutaja asemel **Süsteem**. |
| Aeg ja kulu | 2602528 | Projekti kinnitaja saab kinnitada aega projektide puhul, kui ta pole kinnitatud kinnitajate loendis. |
| Arveldamine ja hinnakujundus | 2608550 | Parandusarve saab kinnitada ka siis, kui originaalis pole muudatusi. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Välja **Kategooria ID** lubatud pikkuses on rakenduses Finance and Project Operationsi vaheline mittevastavus. |
| Projektihaldus ja raamatupidamine | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fikseeritud hinnaga projekte ei saa kõrvaldada, kui väli **Arvelduskonto** on seatud väärtusele **Kasum ja kahjum** ja kasutatakse põhimõtet **Valmisprotsent**. |
| Projektihaldus ja raamatupidamine | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Vale käibemaksu vaikerühm sisestatakse projekti seadistustest rakenduse Project Operations integreerimise töölehe kuluridadele. |
| Projektihaldus ja raamatupidamine | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Te ei saa projekti arve ettepaneku päise dimensioone muuta rakenduse Project Operations integreeritud juurutuses. |
| Projektihaldus ja raamatupidamine | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Kontsernisiseseid hankijate arveid ei tohi integreerida teenusega Dataverse. |
| Projektihaldus ja raamatupidamine | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Kliendisaldode valuuta ja aruandlusvaluuta ei ühti. |
| Projektihaldus ja raamatupidamine | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektiarve saate postitada ka siis, kui klient on kõigi arvete jaoks ootel. |
| Projektihaldus ja raamatupidamine | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Nupp **Kustuta kõik read** puudub projekti arve ettepanekutest, millel on vaated **Päis** ja **Read**. |
| Projektihaldus ja raamatupidamine | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Hankija arve postitamisel ilmneb järgmine tõrge: „Arve arvestuskuupäev peab olema seotud ostutellimusega samal aruandeaastal. Käivitage ostutellimuse aastalõpuprotsess või muutke kuupäev jooksvaks aruandeaastaks“. |
| Reisimine ja kulu | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Projekti seotud kulu ei vabastata pärast reisitaotluse kulukohustuste vabastamist. |
| Reisimine ja kulu | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kuluaruande esitamisel ilmneb järgmine tõrge: „Virna jälg: Ettevõtet ei ole olemas“. |
| Reisimine ja kulu | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Vaikeväärtust **Projekti ID** ei sisestata kuluaruannetesse, kui projektis on valitud parameeter **Tegevuse nõudmine ajakirje jaoks**. |
| Reisimine ja kulu | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Nupp **Postituskulud** ei tööta rakenduse Project Operations ressursside/mittelaopõhiste stsenaariumide puhul õigesti. |
| Reisimine ja kulu | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Reisijaid hõlmava läbisõidukuluaruande puhul on probleem **Miilitariifiga**. |
| Reisimine ja kulu | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Kui kulukategoorias **Läbisõidumäära tase** kasutatakse kahte erinevat sõidukitüüpi, ei ole töötajate läbisõidukulumäärasid õigesti summeeritud. |
| Reisimine ja kulu | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Välja **Projekt** otsing reisitaotluse real ei anna õiget projektide loendit. |
| Reisimine ja kulu | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Läbisõit läbivaatamisel** kuvab kuluaruannetes hoiatuse. |
| Reisimine ja kulu | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Kviitungi optilise märgituvastuse (OCR) teenus ei tööta kulu OCR-teenuse URL-iga seotud probleemi tõttu. |
| Reisimine ja kulu | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Kui funktsioon **Korduvate kulude kiire kirjendamin** on lubatud, muutuvad kuluaruannete kirjendamise ridadel olevad summad iga kord, kui leht **Jaota** avatakse. |
| Reisimine ja kulu | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Kuluaruannet ei saa kustutada, kui vahepealsel loendil on rohkem kui üks kinnitaja. |

## <a name="removed-and-deprecated-features"></a>Eemaldatud ja iganenud funktsioonid

Artiklis [Project Operationsis eemaldatud või aegunud funktsioonid](removed-depreciated-features-project.md) kirjeldatakse rakenduse Dynamics 365 Project Operations eemaldatud või aegunud funktsioone.

- Eemaldatud funktsioon pole enam tootes saadaval.
- Iganenud funktsiooni ei arendata aktiivselt ja võidakse tulevases värskenduses eemaldada.

Aegumisteade ilmub artiklis [Eemaldatud või aegunud funktsioonid rakenduses Project Operations](removed-depreciated-features-project.md) 12 kuud enne mis tahes funktsiooni eemaldamist tootest.

Katketavate muudatuste puhul, mis mõjutavad ainult kompileerimisaega, kuid on binaarselt ühilduvad liivakasti ja tootmiskeskkondadega, on aegumisaeg lühem kui 12 kuud. Tavaliselt on need muudatused funktsionaalsed värskendused, mis tuleb kompilaatorisse teha.
