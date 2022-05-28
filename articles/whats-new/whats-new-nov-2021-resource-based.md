---
title: Mis on uut novembris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: Selles teemas antakse teavet kvaliteedivärskenduste kohta, mis on saadaval project Operationsi 2021. aasta novembri väljaandes ressursi-/ladustamata stsenaariumide jaoks.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 730f9f051c62f44734f2d7915517baf439b1a0b8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584867"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut novembris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See teema kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.22

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- Project Scheduling rakenduse programmeerimisliidesed (API-d) toetavad nüüd projektiämbrite loomise ja kustutamise võimalust.

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](/dynamics365/project-operations/environment/resource-dual-write-maps).

Käivitage alati oma keskkonnas kaardi uusim versioon ja lubage project Operationsi Dataverse lahenduse ja Finance'i lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas olevat tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises Kaartide [jaotises Puudu tabeliveergude probleemi juhiseid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-in-dataverse"></a>Projektitoimingud rakenduses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2240080 | Välja **Maksetingimused** ei tohi pro forma arvel dubleerida. |
| Arveldamine ja hinnakujundus | 2358236 | Arve parandamine peab lubama parandused, millel on nullhinnaga read. |
| Ressursihaldus | 2410072 | Lubage ülesandele projektijuhina määratud ressursi häälestus. |
| Arveldamine ja hinnakujundus | 2430234 | Kulujõudluse arvutamise probleemi lahendamine. |
| Aeg ja kulu | 2436978 | Andke aega sisestada hh:mm formaadis. |
| Arveldamine ja hinnakujundus | 2448623 | Saate lubada hinnakirjade värskendamist pärast nende seostamist organisatsiooniüksusega. |
| Aeg ja kulu | 2460396 | Lubage lahtri tühjendamisega ajasisestus kustutada. |
| Arveldamine ja hinnakujundus | 2467386 | Lubage kustutada projekt, millel on ülesanne, isegi kui ülesanne on seostatud võidetud hinnapakkumisega. |
| Aeg ja kulu | 2461744 | Vaade **Minu nurjunud kinnitamine** sisaldab ainult projekti kinnitusi **etapis Esitatud**. |
| Aeg ja kulu | 2464082 | Kui sihtolek on sobitatud, eemaldage link projekti kinnituste komplektist kinnituskomplekti. |
| Aeg ja kulu | 2468108 | Töö Ajakava ei tohiks määrata **kinnituskomplektile töötlemise** olekut. |
| Aeg ja kulu | 2471503 | Kustutage seitsmepäevased kinnituskomplektid. |
| Arveldamine ja hinnakujundus | 2480687 | Hinnapakkumisrea viidet ei tohi hinnapakkumisrea vahe-eesmärgi loomisel eemaldada. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projekti kulukannetes säilitatud hankija summasid ei kuvata kandeloendis. |
| Projektihaldus ja raamatupidamine | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kontsernisisene hankija arve katkeb hankija arve integreerimise sisselülitamisel. |
| Projektihaldus ja raamatupidamine | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektiarvete maksetingimused ei tööta ootuspäraselt. |
| Projektihaldus ja raamatupidamine | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Hankija kinnipidamise vabastamisel on kande konteerimisel täiendavaid ridu, mis on valed. |
| Projektihaldus ja raamatupidamine | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Projektitoimingute integratsioonitöölehe konteerimisel nurjub see puuduvate dimensioonide tõttu kontol, kuhu pole konteeritud. |
| Projektihaldus ja raamatupidamine | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Vahekaarti **Projekt** ei saa redigeerida ootel hankija arvel, kui hankekategooria on kaubale määratud. |
| Projektihaldus ja raamatupidamine | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeerimispaan puudub, kui te pole Project Operationsi Dataverse sisse logitud. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kui konteerite projektiarvelt tulu rakendatud säilitaja teenindusjuhtumis, ilmneb probleem, kuna kande kanded ei saldot. |
| Projektihaldus ja raamatupidamine | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Hinnangu loomine pärast arvesoovituse konteerimist blokeerib impordi parandusread. |
| Projektihaldus ja raamatupidamine | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Täielikult arveldatud vahe-eesmärgi kirje muutmine ei tohiks olla võimalik. |
| Reisimine ja kulu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kõik kuluaruanded on nähtavad, kui otsite kategooriat mobiilirakendusest Kulu. |
| Reisimine ja kulu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Hankijakannete ja käibemaksukannete valed summad sisestatakse krediitkaardikandest loodud kulust. |
| Reisimine ja kulu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kuluaruande **lehe värskendamisel** kuvatakse ebaoluline hoiatus. |
| Reisimine ja kulu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Vahekinnitaja kustutamisel ja seejärel kuluaruande uuesti esitamisel töövoo kaudu kasutatakse valet vahekinnitajat. |
| Reisimine ja kulu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ilmneb läbisõidu häälestusega seotud sisestustõrge. |
