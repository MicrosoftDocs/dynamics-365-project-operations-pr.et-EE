---
title: Mis on uut juunis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta juuni väljaandes ressursi-/ladustamata põhistsenaariumide jaoks.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959634"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut juunis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.43.0.77
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on näidatud kahe kirjutamise kaardid, mida on muudetud või lisatud project Operationsi 2022. aasta juuni väljaandes.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| --- | --- | --- |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.1 | Tühistas pärandvälja ja vastendas hankija arve oleku jälgimise uue väljaga. |

Käivitage alati oma keskkonnas kaardi uusim versioon ja lubage project Operationsi Dataverse lahenduse ja Finance'i lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas olevat tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises Kaartide [jaotises Puudu tabeliveergude probleemi juhiseid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Allhanked | 2708885 | Parandas tõrketeate, mis ilmneb siis, kui kasutaja loob broneeritava ressursi broneerimise päise kirje, kus ühtegi broneeritavat ressurssi pole täidetud. |
| Projekti plaanimine ja jälgimine | 2629441 | Parandas töövoo käivitamise loogikat, et vältida projektiülesannete värskendamisel lõpmatut silmust. |
| Aeg ja kulu | 2641209 | Ajasisestuse import määramistest/broneeringutest peab säilitama broneeritava ressursiviite. |
| Projekti plaanimine ja jälgimine | 2651148 | Projektidokumendi päist tuleb valvata.|
| Projekti plaanimine ja jälgimine | 2653145 | Lisatud kinnitused tagamaks, et projektikirjet ei saa luua, mille nimes on sobimatud märgid. |
| Aeg ja kulu | 2654710 | Parandas filtreerimist **lehel Kinnitused**. |
| Arveldamine ja hinnakujundus | 2667805 | Lisatud valideerimised, mis aitavad vältida arveldatud müügireaalsuste loomist, kui sisestamata müügi tegelike andmete varundamist pole olemas. |
| Arveldamine ja hinnakujundus | 2668378 | Lisatud valideerimised, mis aitavad vältida kohandatud hinnakujundusdimensiooni lisamist, välja arvatud juhul, kui on täidetud loogiline nimi ja välja nimi. |
| Allhanked | 2677485 | Värskendas hankija arveridade topeltkirjutuskaardi sihtversiooni. |
| Aeg ja kulu | 2700428 | Parandas kinnituste loogikat, et tagada projekti muude kinnituskomplektide töötlemine isegi siis, kui üks kinnituskomplektidest on süsteemitöödes kinni. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse rakendusse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
