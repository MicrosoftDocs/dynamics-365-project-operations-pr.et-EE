---
title: Mis on uut aprillis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: See artikkel annab teavet rakenduse Microsoft Dynamics 365 Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks 2022. a aprilli väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110879"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut aprillis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.41.0.45
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.26

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Hankekategooriaid saab kasutada projekti ostutellimustes ja menetluses olevates hankija arvetes. Lisateabe saamiseks, vt [Hankekategooriate kasutamine koos projekti ostutellimuste ja pooleliolevate tarnijate arvetega](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on esitatud topeltkirjutuskaardid, mida on muudetud või lisatud rakendusele Project Operations 2022. aasta märtsi versioonis.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| -------------- | ------------------- | ------------|
| Project Operationsi integratsiooni projekti hankija arve ekspordirea olem msdyn\_projectvendorinvoicelines | 1.0.0.4 | See kaart toetab hankekategooriate kasutamist koos ostutellimuste ja pooleliolevate hankija arvetega. |

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| ------------ | ---------------- | -------------- |
| Aeg ja kulu | 2573900 | Funktsioon **Uudne kinnitus** peab olema vaikimisi lubatud. |
| Arveldamine ja hinnakujundus | 2603313 | Parandatud dubleeriva kirje viga, mis takistas hinnapakkumise ja lepingu ridade lisamist, millel on toode. |
| Juurutamine ja konfiguratsioon | 2611368 | Kliendid peavad olema võimelised lisama lahendusele kuni viis kohandatud üksust, kasutades selleks uudset rakenduse kujundajat. |
| Aeg ja kulu | 2628285 | Parandatud probleem, mis mõjutas õiget ressursikategooriat ajakirje importimisel. |
|   Müügivõimaluste haldus| 2628815 | Värskendage hinnapakkumise rea üksikasjade kirjelduse tähemärkide piirangut, et see vastaks ülesande teema tähemärkide piirangule, nii et importimine õnnestuks ülesannete puhul, mille teema on pikem kui 100 tähemärki. |
| Aeg ja kulu| 2629547 | Projekti kinnituste väli **Esitatud** peab osutama kasutajale, kes on kirje esitanud. |
| Aeg ja kulu| 2629865 | Välja **Kopeeri kategooria** ülesannete puhul, kui projekte kopeeritakse. |
| Aeg ja kulu| 2636463 | Parandatud uudsete kinnitusvormide filtrid. |
| Projekti plaanimine ja jälgimine | 2648300 | Parandatud probleem, mis takistas projekti omaniku muutmist. |
| Arveldamine ja hinnakujundus | 2563000 | Ei tohi lubada töölehele kandmist, mis on seotud arveldamata müügiga, mille valuuta erineb lepingu valuutast. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektihaldus ja raamatupidamine rakenduses Dynamics 365 Finance

Lisateabe saamiseks tõrkeparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
