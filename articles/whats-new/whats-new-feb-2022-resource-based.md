---
title: Mis on uut veebruaris 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval Project Operationsi 2022. aasta veebruari väljaandes ressursi-/ladustamata stsenaariumide jaoks.
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

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.28.0.120
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.24

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

- Alates sellest väljaandest saate ühte projekti lisada kuni 300 meeskonnaliiget. Varem oli meeskonnaliikmete arvu piirang 150. Lisateavet leiate teemast [Projekti limiidid](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operationsi topeltkirjutamise kaardi värskendused

Järgmises loendis kuvatakse kahe kirjutamise kaardid, mida on projektitoimingute 2022. aasta veebruari väljaandes muudetud või lisatud.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| --- | --- | --- |
| Project Operationsi integreerimise projekti kulude ekspordi üksus (msdyni\_ kulud) | 1.0.0.3 | Projektitegevuse sünkroonimise laiendatud väärtusele Dataverse. |

Project Operationsi kahekirjutamise kaartide praeguse loendi ja versioonide kohta leiate teemast [Project Operationsi kahe kirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käivitage alati oma keskkonnas kaardi uusim versioon ja lubage project Operationsi Dataverse lahenduse ja Finance'i lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas olevat tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises Kaartide [jaotises Puudu tabeliveergude probleemi juhiseid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2415109 | Välja Operations maksetingimused **vaikeväärtuseks** peavad olema projektilepingu kliendikirje ja proforma arve kirje. |
| Arveldamine ja hinnakujundus | 2497369 | Materjali korrigeerimine peab järgima kuupäevaväärtust parameetrites **Parandus**. |
| Arveldamine ja hinnakujundus | 2498697 | Parandas ajasisestuse tagasikutsumise **turbekonfiguratsiooni**. |
| Arveldamine ja hinnakujundus | 2513824 | Ressursipõhiste stsenaariumide puhul ei tohi kandekategooria ID projektitoimingutes ületada 28 märki. |
| Arveldamine ja hinnakujundus | 2517455 | Toimingut **Arvereakannete** värskendamine ei tohi sama arve puhul lubada käivitada mitu samaaegset korda. |
| Arveldamine ja hinnakujundus | 2517465 | Arverea **üksikasjade** desaktiveerimise toiming on blokeeritud, kuna seda ei toetata. |
| Arveldamine ja hinnakujundus | 2556660 | Fikseeris kuupäevaefektiivsuse kontrolli, mis tehakse projekti parameetrite kirjega seotud hinnakirjas. |
|   Müügivõimaluste haldus | 2369202 | Parandas äriloogikat, mis kinnitab, et kattuvate efektiivsuskuupäevadega hinnakirju saab lisada samale projektilepingule. |
|   Müügivõimaluste haldus | 2385965 | Parandas käitumist lehe Projekti leping vahekaardil **Kliendid** **, kui valite suvandi** Salvesta ja sule **.** |
| Aeg ja kulu | 2538503 | Projektiülesanne peab olema saadaval **olemis Projekti tegelikud** andmed pärast kuluaruande konteerimist. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Hankija kreeditarvete importimisel ilmneb tõrge. Tõrketeates on kirjas: "Säilitamissumma ei saa olla suurem kui järelejäänud netosumma." |
| Projektihaldus ja raamatupidamine | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Kui arvesoovitus sisaldab nullsumma tasu kandeid, mis on sisestamata müügi tegelikud, ei saa arveldamine toimuda. |
| Projektihaldus ja raamatupidamine | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Sisestatud kulu pole õige pärast ostuhinna värskendamist ja **muudatuste halduse aktiveerimine** on lubatud.|
| Projektihaldus ja raamatupidamine | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Fikseeritud hinnaga projekti konteeringuhinnang kasutab hinnangukandes valet valuutat ja summat isegi siis, kui **hinnangu arvutamise** funktsiooni projektilepingu valuuta lubamine on lubatud. |
| Projektihaldus ja raamatupidamine | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Extension** ei tohiks teha üleskutset muudatuste jälgimise lubamiseks, püüdmata erandeid olemitele, millel on konfiguratsioonivõtmed, mis pole lubatud. |
| Projektihaldus ja raamatupidamine | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Pakett-töö on fikseeritud, kui konteeritakse mitu täpsemat žurnaali ja ilmneb tõrge. |
| Reisimine ja kulu | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Arvelduse probleemi tõttu, mis on seotud kuluaruannete avanssiga, ei katata maksusummat avansimakse osana. |
| Reisimine ja kulu | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Käibemaksuteavet ei kaasata aruandesse **Kulu - Konteeritud kanded**. |
| Reisimine ja kulu | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Nõutava kulupoliitika **rikkumisel kuvatakse** kuluaruannete hoiatus valesti. |
| Reisimine ja kulu | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projektikanne ei sisalda tagastamatut käibemaksu kogu müügisummas, kui kanne on läbisõidukulu tulemus. |
| Reisimine ja kulu | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kui üksikasjalikul real on maks, ei saa te üksikasjalike ridade kuupäeva muuta ja ilmneb lähtedokumendi oleku tõrge. |

## <a name="removed-and-deprecated-features"></a>Eemaldatud ja aegunud funktsioonid

Artiklis [Eemaldatud või aegunud funktsioonid jaotises Project Operations](removed-depreciated-features-project.md) kirjeldatakse funktsioone, mis on rakenduse jaoks Dynamics 365 Project Operations eemaldatud või aegunud.

- Eemaldatud funktsioon pole enam tootes saadaval.
- Aegunud funktsioon pole aktiivses arenduses ja võidakse tulevases värskenduses eemaldada.

Amortisatsiooniteade kuvatakse [Project Operationsi](removed-depreciated-features-project.md) artiklis Eemaldatud või aegunud funktsioonides 12 kuud enne mis tahes funktsiooni tootest eemaldamist.

Muudatuste katkestamiseks, mis mõjutavad ainult kompileerimisaega, kuid on binaarsed ühilduvad liivakasti ja tootmiskeskkondadega, on amortisatsiooniaeg vähem kui 12 kuud. Tavaliselt on need muudatused funktsionaalsed värskendused, mis tuleb kompilaatorile teha.
