---
title: Mis on uut novembris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet kvaliteedivärskenduste kohta, mis on saadaval 2021. aasta novembri väljaandes Project Operations ressursi-/mittelaopõhiste stsenaariumide jaoks.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932889"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut novembris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakendus Project Operations Dataverse’i keskkonna versioonis 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.22

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- Projekti ajastamise rakendusliidesed (API-d) toetavad nüüd võimalust luua ja kustutada projektisalved.

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](/dynamics365/project-operations/environment/resource-dual-write-maps).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-in-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2240080 | Välja **Maksetingimused** ei tohi näidisarvel dubleerida. |
| Arveldamine ja hinnakujundus | 2358236 | Arve parandus peab võimaldama parandusi, millel on nullhinna read. |
| Ressursihaldus | 2410072 | Lubage seadistada ressurss, mis on projektijuhina ülesandele määratud. |
| Arveldamine ja hinnakujundus | 2430234 | Kuluarvestuse probleemi parandamine. |
| Aeg ja kulu | 2436978 | Võimaldab sisestada kellaaja tt:mm formaadis. |
| Arveldamine ja hinnakujundus | 2448623 | Võimaldab hinnakirjade värskendamist pärast nende seostamist organisatsiooniüksusega. |
| Aeg ja kulu | 2460396 | Võimaldab ajakirje kustutada, kustutades lahtri. |
| Arveldamine ja hinnakujundus | 2467386 | Lubage projekti, millel on ülesanne, kustutada, isegi kui ülesanne on seotud võidetud hinnapakkumisega. |
| Aeg ja kulu | 2461744 | Vaade **Minu ebaõnnestunud kinnitus** sisaldab ainult projektikinnitusi, mis on etapis **Esitatud**. |
| Aeg ja kulu | 2464082 | Eemaldage projekti kinnituste link kinnituskomplekti, kui sihtoleku olek on vastavuses. |
| Aeg ja kulu | 2468108 | Töö ajastamine ei tohiks kinnitamiskomplektile määrata olekuks **Töötlemine**. |
| Aeg ja kulu | 2471503 | Kustutage seitse päeva vanad kinnituskomplektid. |
| Arveldamine ja hinnakujundus | 2480687 | Hinnapakkumise rea vahekokkuvõtte loomisel ei tohi hinnapakkumisrea viidet eemaldada. |

### <a name="project-management-and-accounting-in-finance"></a>Projektihaldus ja raamatupidamine rahanduses

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projekti kulutehingutes säilitatud hankija summasid tehinguloendis ei kuvata. |
| Projektihaldus ja raamatupidamine | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kui hankija arvete integreerimine on sisse lülitatud, on kontsernisisese hankija arve katki. |
| Projektihaldus ja raamatupidamine | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektiarvete maksetingimused ei toimi ootuspäraselt. |
| Projektihaldus ja raamatupidamine | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kui hankija säilitamine vabastatakse, on kande postitamisel täiendavad read, mis on valed. |
| Projektihaldus ja raamatupidamine | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kui rakenduse Project Operations integratsiooni tööleht on postitatud, ebaõnnestub see konto dimensioonide puudumise tõttu, millele ei postitata. |
| Projektihaldus ja raamatupidamine | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Vahekaarti **Projekt** ei saa muuta ootel hankija arvel, kui kaubale on määratud hankekategooria. |
| Projektihaldus ja raamatupidamine | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeerimispaan puudub, kui te pole rakendusse Project Operations Dataverse sisse logitud. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kui postitate projektiarvest saadud tulu rakendatud säilitamisjuhtumi puhul, ilmneb probleem, kuna kandel olevad tehingud ei ole tasakaalus. |
| Projektihaldus ja raamatupidamine | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Prognoosi koostamine pärast arve ettepaneku postitamist blokeerib parandusridade importimise. |
| Projektihaldus ja raamatupidamine | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Täielikult arveldatud vahekokkuvõtte kirje muutmine ei tohiks olla võimalik. |
| Reisimine ja kulu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kõik kuluaruanded on nähtavad, kui otsite kulu mobiilirakenduses kategooriat. |
| Reisimine ja kulu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Hankija tehingute ja maksu tehingute valed summad on postitatud kulust, mis luuakse krediitkaarditehingust. |
| Reisimine ja kulu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Lehe **Kuluaruanne** värskendamisel kuvatakse asjakohatu hoiatus. |
| Reisimine ja kulu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Ajutise kinnitaja kustutamisel ja seejärel töövoo kaudu uuesti esitamisel kasutatakse vale ajutist kinnitajat. |
| Reisimine ja kulu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ilmub postitamistõrge, mis on seotud läbisõidu seadistamisega. |
