---
title: Mis on uut juunis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet kvaliteedivärskenduste kohta, mis on saadaval Microsoft Dynamics 365 Project Operations 2022. aasta juuni väljalaskes ressursi-/mittelaopõhiste stsenaariumide jaoks.
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

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Project Operations Dataverse’i keskkonna versioonis 4.43.0.77 või 4.43.0.119
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis kuvatakse topeltkirjutusega kaardid, mida on muudetud või lisatud Project Operationsi 2022. a juuni väljaandes.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| --- | --- | --- |
| Project Operationsi integreerimise projekti tarnija arve ekspordist (msdyn_projectvendorinvoices) | 1.0.0.1 | Pärandväli katkestati ja vastendati hankija arve oleku jälgimiseks uue väljaga. |

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Allhankeleping | 2708885 | Parandatud on tõrketeade, mis kuvatakse, kui kasutaja loob broneeritava ressursi broneerimispäise kirje, kus broneeritavat ressurssi ei täideta. |
| Projekti plaanimine ja jälgimine | 2629441 | Parandatud töövoo käivitamise loogika, mis aitab vältida projektiülesannete värskendamisel lõpmatut tsüklit. |
| Aeg ja kulu | 2641209 | Ülesannetest/broneeringutest pärit ajakirje import peab säilitama broneeritava ressursi viite. |
| Projekti plaanimine ja jälgimine | 2651148 | Projektdokumendi päis peab olema valve all.|
| Projekti plaanimine ja jälgimine | 2653145 | Lisatud kinnitused tagamaks, et ei saaks luua projektikirjet, mille nimes on kehtetuid tähemärke. |
| Aeg ja kulu | 2654710 | Lehel **Kinnitused** on filtreerimine parandatud. |
| Arveldamine ja hinnakujundus | 2667805 | Lisatud kinnitused, mis aitavad vältida arveldatud müügi tegelike näitajate loomist, kui arveldamata müügi tegelikke näitajaid ei ole. |
| Arveldamine ja hinnakujundus | 2668378 | Lisatud kinnitused, mis aitavad vältida kohandatud hinnadimensiooni lisamist, kui pole täidetud loogilist nime ja välja nime. |
| Allhankeleping | 2677485 | Värskendatud hankija arve ridade topeltkirjutuskaardi sihtversiooni. |
| Aeg ja kulu | 2700428 | Täiustatud kinnituste loogikat tagamaks, et projekti teisi kinnituskomplekte saab töödelda isegi siis, kui üks kinnituskomplektidest on süsteemitöödesse kinni jäänud. |

### <a name="project-management-and-accounting-in-finance"></a>Projektihaldus ja raamatupidamine rahanduses

Lisateabe saamiseks tõrkeparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
