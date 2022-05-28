---
title: Mis on uut aprillis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Selles teemas antakse teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta aprilli väljaandes ressursi-/ladustamata põhistsenaariumide jaoks.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613330"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut aprillis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See teema kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.41.0.45
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.26

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Hankekategooriaid saab kasutada projekti ostutellimustes ja ootel hankija arvetes. Lisateavet leiate teemast [Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on näidatud kahe kirjutamise kaardid, mida on project Operationsi 2022. aasta märtsi väljaandes muudetud või lisatud.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| -------------- | ------------------- | ------------|
| Project Operationsi integreerimise projekti hankija arve rea ekspordiolem msdyn\_ projectvendorinvoicelines | 1.0.0.4 | See kaart toetab hankekategooriate kasutamist ostutellimuste ja ootel hankija arvetega. |

Käivitage alati oma keskkonnas kaardi uusim versioon ja lubage project Operationsi Dataverse lahenduse ja Finance'i lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas olevat tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises Kaartide [jaotises Puudu tabeliveergude probleemi juhiseid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| ------------ | ---------------- | -------------- |
| Aeg ja kulu | 2573900 | Funktsioon **Kaasaegne kinnitamine** peab olema vaikimisi lubatud. |
| Arveldamine ja hinnakujundus | 2603313 | Parandas duplikaatkirje tõrke, mis takistas tootega hinnapakkumis- ja lepinguridade lisamist. |
| Juurutamine ja konfigureerimine | 2611368 | Kliendid peavad saama lisada lahendusele kuni viis kohandatud olemit, kasutades kaasaegset rakenduse kujundajat. |
| Aeg ja kulu | 2628285 | Lahendas probleemi, mis mõjutas võimalust määrata aja sisestamise ajal õige ressursikategooria. |
|   Müügivõimaluste haldus| 2628815 | Värskendage hinnapakkumise rea üksikasjade kirjelduse märgipiirangut, et see vastaks ülesandesubjekti märgipiirangule, nii et importimine õnnestuks ülesannete puhul, kus teema on pikem kui 100 märki. |
| Aeg ja kulu| 2629547 | Projekti **kinnituste väli Esitatud alus** peab osutama kirje esitanud kasutajale. |
| Aeg ja kulu| 2629865 | Projektide **kopeerimisel ülesannete väli Kopeeri kategooria**. |
| Aeg ja kulu| 2636463 | Kinnitage filtrid kinnitustele kaasaegsetes kinnituste vormides. |
| Projekti plaanimine ja jälgimine | 2648300 | Lahendas probleemi, mis takistab projekti omaniku muutmist. |
| Arveldamine ja hinnakujundus | 2563000 | Sisestamata müügi tööleheread, kus valuuta erineb lepinguvaluutast, ei tohi olla lubatud. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse rakendusse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
