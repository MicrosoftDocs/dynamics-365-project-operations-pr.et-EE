---
title: Mis on uut novembris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: See teema annab teavet kvaliteedivärskenduste kohta, mis on saadaval Project Operationsi 2021. aasta novembri väljaandes ressursi/ladustamata stsenaariumide jaoks.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827321"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut novembris 2021 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

*Kehtib: ressursipõhiste/mitteladustatavate stsenaariumite jaoks*

See teema kehtib järgmiste Microsoft Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Project Operations Dataverse keskkonnaversioonis 4.26.0.145, 4.26.0.148, või 4.26.0.150
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.22

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- Projekti plaanimise rakenduse programmeerimisliidesed (API-d) toetavad nüüd projektiämbrite loomise ja kustutamise võimalust.

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](/dynamics365/project-operations/environment/resource-dual-write-maps).

Project Operationsi Dataverse lahenduse ja Finance lahenduse versiooni värskendamisel käivitage alati kaardi uusim versioon ja lubage kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas oleva tabelikaardi, taotlege muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige kahe [kirja tõrkeotsingu juhendi kaartide jaotises Puuduvad tabeliveerud olevaid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) juhiseid.

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-in-dataverse"></a>Projektitoimingud Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2240080 | **Pro forma arvel ei tohi välja Maksetingimused** dubleerida. |
| Arveldamine ja hinnakujundus | 2358236 | Arve korrigeerimine peab võimaldama nullhinnaga ridadega parandusi. |
| Ressursihaldus | 2410072 | Saate lubada ülesandele projektijuhina määratud ressursi seadistamise. |
| Arveldamine ja hinnakujundus | 2430234 | Kulutõhususe arvutamise probleemi lahendamine. |
| Aeg ja kulu | 2436978 | Sisestage aeg vormingus hh:mm. |
| Arveldamine ja hinnakujundus | 2448623 | Luba hinnakirjad värskendada pärast nende seostamist organisatsiooniüksusega. |
| Aeg ja kulu | 2460396 | Saate lahtri tühjendamisega ajakirje kustutada. |
| Arveldamine ja hinnakujundus | 2467386 | Luba projekti, mille ülesanne on kustutada, isegi kui ülesanne on seotud võidetud hinnapakkumisega. |
| Aeg ja kulu | 2461744 | **Vaade Minu nurjunud kinnitus sisaldab ainult projekti** kinnitusi **etapil** Esitatud. |
| Aeg ja kulu | 2464082 | Eemaldage link projekti kinnitustest kinnitamiseks, kui sihtolek on sobitatud. |
| Aeg ja kulu | 2468108 | Töö Ajakava ei tohiks **määrata** kinnituskomplekti töötlemisolekut. |
| Aeg ja kulu | 2471503 | Kustutage seitsmepäevased kinnituskomplektid. |
| Arveldamine ja hinnakujundus | 2480687 | Hinnapakkumise rea viidet ei tohi hinnapakkumise rea verstaposti loomisel eemaldada. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Projektihaldus ja raamatupidamine | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projekti kulukannetes säilitatud hankija summasid ei kuvata kandeloendis. |
| Projektihaldus ja raamatupidamine | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kontsernisisene hankija arve on hankija arve integreerimise sisselülitamisel katki. |
| Projektihaldus ja raamatupidamine | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projektiarvete maksetingimused ei tööta ootuspäraselt. |
| Projektihaldus ja raamatupidamine | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kui hankija säilitamine on vabastatud, on kande sisestamisel lisaread, mis on valed. |
| Projektihaldus ja raamatupidamine | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operationsi integratsioonitöölehe konteerimisel nurjub see, kuna kontol puuduvad dimensioonid, mida ei konteerita. |
| Projektihaldus ja raamatupidamine | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Vahekaarti Projekt** ei saa ootel hankija arvel redigeerida, kui kaubale on määratud hankekategooria. |
| Projektihaldus ja raamatupidamine | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeerimispaan puudub, kui te pole Project Operationsi Dataverse sisse logitud. |
| Projektihaldus ja raamatupidamine | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kui konteerite projektiarve tulu rakendatud hoidu korpusesse, ilmneb probleem, kuna kande kande kanded ei tasakaalusta. |
| Projektihaldus ja raamatupidamine | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Hinnangu loomine pärast arvesoovituse konteerimist blokeerib parandusridade importimise. |
| Projektihaldus ja raamatupidamine | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Täielikult arveldatud vahe-eesmärgi kirje muutmine ei tohiks olla võimalik. |
| Reisimine ja kulu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Kõik kuluaruanded on nähtavad, kui otsite kategooriat mobiilirakenduses Kulu. |
| Reisimine ja kulu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Hankijakannete ja käibemaksukannete valed summad sisestatakse krediitkaardikandest loodud kulust. |
| Reisimine ja kulu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kuluaruande lehe värskendamisel ilmneb ebaoluline **hoiatus**. |
| Reisimine ja kulu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Vahepealse kinnitaja kustutamisel ja seejärel kuluaruande uuesti esitamisel töövoo kaudu kasutatakse valet ajutist kinnitajat. |
| Reisimine ja kulu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Esineb läbisõidu häälestusega seotud konteeringutõrge. |
