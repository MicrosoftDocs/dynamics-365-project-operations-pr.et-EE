---
title: Mis on uut juunis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta juuni väljaandes ressursipõhiste/varudeta stsenaariumide jaoks.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031326"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut juunis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektitoimingud keskkonnaversioonis Dataverse 4.43.0.77 või 4.43.0.119
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on kuvatud topeltkirjutusega kaardid, mida on muudetud või lisatud project operations juuni 2022 väljalaskesse.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| --- | --- | --- |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.1 | Aegunud on pärandväli ja vastendatud hankija arve oleku jälgimise uue väljaga. |

Käivitage oma keskkonnas alati kaardi uusim versioon ja lubage project operationsi Dataverse lahenduse ja finance lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud valmis tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib kaardi käivitamisel probleem, järgige juhiseid, mis on toodud [tõrkeotsingu juhendi Jaotises Puuduvad tabeli veerud kaardil](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Allhanked | 2708885 | Parandatud on tõrketeade, mis kuvatakse, kui kasutaja loob broneeritava ressursi broneerimise päisekirje, kus pole ühtegi broneeritavat ressurssi täidetud. |
| Projekti plaanimine ja jälgimine | 2629441 | Parandas töövoo käivitamise loogikat, et vältida lõputut silmust projektiülesannete värskendamisel. |
| Aeg ja kulu | 2641209 | Ajakirjete import ülesannetest/broneeringutest peab säilitama broneeritava ressursiviite. |
| Projekti plaanimine ja jälgimine | 2651148 | Projekti dokumendi päis peab olema valvatud.|
| Projekti plaanimine ja jälgimine | 2653145 | Lisatud valideerimised tagamaks, et ei saa luua projektikirjet, mille nimes on sobimatud märgid. |
| Aeg ja kulu | 2654710 | Parandatud filtreerimine **lehel Kinnitused**. |
| Arveldamine ja hinnakujundus | 2667805 | Lisatud valideerimised, mis aitavad vältida arveldatud müügi tegelike summade loomist, kui tasakaalustamata müügi tegelikke andmeid pole olemas. |
| Arveldamine ja hinnakujundus | 2668378 | Lisatud on valideerimised, mis aitavad vältida kohandatud hinnakujunduse dimensiooni lisamist, kui pole täidetud loogilist nime ja välja nime. |
| Allhanked | 2677485 | Värskendatud on hankija arve ridade sihtversiooni kahekordse kirjutamise kaardil. |
| Aeg ja kulu | 2700428 | Täiustatud on kinnituste loogikat, et tagada projekti muude kinnituskomplektide töötlemine isegi siis, kui üks kinnituskomplektidest on süsteemitöödes kinni. |

### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
