---
title: Mis on uut aprillis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta aprilli väljaandes ressursipõhiste/varudeta stsenaariumide jaoks.
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

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektitoimingud keskkonnaversioonis Dataverse 4.41.0.45
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.26

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Hankekategooriaid saab kasutada projekti ostutellimustes ja ootel hankija arvetes. Lisateavet vaadake jaotisest [Hankekategooriate kasutamine projekti ostutellimuste ja ootel hankija arvetega](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Järgmises tabelis on kuvatud topeltkirjutusega kaardid, mida on muudetud või lisatud Project Operationsi 2022. aasta märtsi väljaandes.

| Olemikaart | Värskendatud versioon | Kommentaarid |
| -------------- | ------------------- | ------------|
| Project Operations integratsioon projekti hankija arve rea ekspordi olem msdyn\_ projectvendorinvoicelines | 1.0.0.4 | See kaart toetab hankekategooriate kasutamist ostutellimuste ja ootel hankija arvetega. |

Käivitage oma keskkonnas alati kaardi uusim versioon ja lubage project operationsi Dataverse lahenduse ja finance lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud valmis tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib kaardi käivitamisel probleem, järgige juhiseid, mis on toodud [tõrkeotsingu juhendi Jaotises Puuduvad tabeli veerud kaardil](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| ------------ | ---------------- | -------------- |
| Aeg ja kulu | 2573900 | Funktsioon **Modern Approval** peab olema vaikimisi lubatud. |
| Arveldamine ja hinnakujundus | 2603313 | Parandas duplikaatkirje tõrke, mis takistas tootega hinnapakkumis- ja lepinguridade lisamist. |
| Juurutamine ja konfiguratsioon | 2611368 | Kliendid peavad saama kaasaegse rakenduse kujundaja abil lisada lahendusele kuni viis kohandatud olemit. |
| Aeg ja kulu | 2628285 | Lahendatud on probleem, mis mõjutas võimalust määrata ajakirjete importimise ajal õige ressursikategooria. |
|   Müügivõimaluste haldus| 2628815 | Värskendage juturea üksikasjade kirjelduse tähemärgipiirangut, et see vastaks ülesande teema märgipiirangule, nii et importimine õnnestuks ülesannete puhul, mille teema on pikem kui 100 tähemärki. |
| Aeg ja kulu| 2629547 | **Projekti kooskõlastuste väli Esitatud** peab osutama kirje esitanud kasutajale. |
| Aeg ja kulu| 2629865 | Väli **Kopeeri kategooria** ülesannete puhul, kui projekte kopeeritakse. |
| Aeg ja kulu| 2636463 | Kinnituste filtrid kinnitati kaasaegsetes kinnitusvormides. |
| Projekti plaanimine ja jälgimine | 2648300 | Lahendatud on probleem, mis takistab projekti omaniku muutmist. |
| Arveldamine ja hinnakujundus | 2563000 | Töölehe read arveldamata müügi puhul, kus valuuta erineb lepingu valuutast, ei tohi olla lubatud. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance. aastal

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
