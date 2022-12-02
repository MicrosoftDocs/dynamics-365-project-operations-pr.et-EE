---
title: Mis on uut veebruaris 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet ressursi-/mittelaopõhiste stsenaariumite jaoks mõeldud rakenduse Project Operations 2022. aasta veebruari väljalaskes saadaolevate kvaliteedi värskenduste kohta.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932981"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut veebruaris 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.28.0.120
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.24

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

- Selle versiooni seisuga saate ühte projekti lisada kuni 300 meeskonnaliiget. Varem oli meeskonnaliikmete arvu piirang 150. Lisateavet leiate jaotisest [Projekti piirangud](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Rakenduse Project Operations topeltkirjutuskaardi värskendused

Järgmises loendis kuvatakse topeltkirjutusega kaardid, mida on muudetud või lisatud Project Operationsi 2022. a veebruari väljaandes.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| --- | --- | --- |
| Project Operationsi integreerimise projekti kulude ekspordi olem (msdyn\_expenses) | 1.0.0.3 | Laiendatud projektitegevuse sünkroonimiseks teenusega Dataverse. |

Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2415109 | Vaikeväärtus väljal **Toimingute maksetingimused** peab olema projekti lepingulise kliendi kirje ja eelarvete kirje. |
| Arveldamine ja hinnakujundus | 2497369 | Materjali parandus peab järgima kuupäeva väärtust parameetrites **Parandus**. |
| Arveldamine ja hinnakujundus | 2498697 | Täiustatud turvakonfiguratsioon **Aja sisestuse tagasikutsumine** jaoks. |
| Arveldamine ja hinnakujundus | 2513824 | Ressursipõhiste stsenaariumide puhul ei tohi tehingukategooria ID rakenduses Project Operations ületada 28 tähemärki. |
| Arveldamine ja hinnakujundus | 2517455 | Toimingut **Arve rea tehingute värskendamine** ei tohi lubada sama arve puhul mitu korda samaaegselt käivitada. |
| Arveldamine ja hinnakujundus | 2517465 | Toiming **Inaktiveeri arve rea üksikasjad** on blokeeritud, kuna seda ei toetata. |
| Arveldamine ja hinnakujundus | 2556660 | Parandatud on kuupäeva tõhususe kontrolli, mida tehakse projekti parameetrite kirjele lisatud hinnakirjas. |
|   Müügivõimaluste haldus | 2369202 | Parandatud äriloogika, mis kontrollib, et samale projektilepingule saab lisada hinnakirju, mille kehtivuskuupäevad kattuvad. |
| Müügivõimaluste haldus | 2385965 | Parandasime käitumist vahekaardil **Kliendid** lehel **Projektileping**, kui valite **Salvesta ja sulge**. |
| Aeg ja kulu | 2538503 | Projektiülesanne peab olema pärast kuluaruande postitamist saadaval olemis **Projekti tegelikud näitajad**. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Hankija kreeditarvete importimisel ilmneb tõrge. Tõrketeade ütleb: „Säilitatav summa ei tohi olla suurem kui järelejäänud netosumma“. |
| Projektihaldus ja raamatupidamine | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Kui arveettepanek sisaldab nullsummaga tasulisi tehinguid, mis on arveldamata müügi tegelikud näitajad, ei saa arvet esitada. |
| Projektihaldus ja raamatupidamine | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Postitatud maksumus ei ole õige pärast ostuhinna värskendamist ja **Muudatuste haldamise aktiveerimine** on lubatud.|
| Projektihaldus ja raamatupidamine | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Fikseeritud hinnaga projekti postitamisprognoos kasutab kalkulatsioonikviitungil valet valuutat ja summat isegi siis, kui funktsioon **Projekti lepingu valuuta prognoosi arvutamiseks** on lubatud. |
| Projektihaldus ja raamatupidamine | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** ei tohiks teha kõnet muudatuste jälgimise lubamiseks ilma lubamata konfiguratsioonivõtmetega olemite erandeid püüdmata. |
| Projektihaldus ja raamatupidamine | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Partiitöö fikseeritakse, kui postitatakse mitu täpsemat ajakirjet ja ilmneb tõrge. |
| Reisimine ja kulu | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Arveldusprobleemi tõttu, mis on seotud kuluaruannete sularaha ettemaksetega, ei kaeta maksusummat sularaha ettemakse osana. |
| Reisimine ja kulu | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Käibemaksuteave ei sisaldu aruandes **Kulu - postitatud tehingud**. |
| Reisimine ja kulu | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kulupoliitika rikkumine **Vajalikud kviitungid** kuvab kuluaruannetel valet hoiatust. |
| Reisimine ja kulu | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projekti tehing ei sisalda tagastamatut müügimaksu kogu müügisummas, kui tehing tuleneb läbisõidukulust. |
| Reisimine ja kulu | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kui jaotatud real on maks, ei saa te jaotamise rea kuupäeva muuta ja ilmneb algdokumendi olekutõrge. |

## <a name="removed-and-deprecated-features"></a>Eemaldatud ja iganenud funktsioonid

Artiklis [Project Operationsis eemaldatud või aegunud funktsioonid](removed-depreciated-features-project.md) kirjeldatakse rakenduse Dynamics 365 Project Operations eemaldatud või aegunud funktsioone.

- Eemaldatud funktsioon pole enam tootes saadaval.
- Iganenud funktsiooni ei arendata aktiivselt ja võidakse tulevases värskenduses eemaldada.

Aegumisteade ilmub artiklis [Eemaldatud või aegunud funktsioonid rakenduses Project Operations](removed-depreciated-features-project.md) 12 kuud enne mis tahes funktsiooni eemaldamist tootest.

Katketavate muudatuste puhul, mis mõjutavad ainult kompileerimisaega, kuid on binaarselt ühilduvad liivakasti ja tootmiskeskkondadega, on aegumisaeg lühem kui 12 kuud. Tavaliselt on need muudatused funktsionaalsed värskendused, mis tuleb kompilaatorisse teha.
