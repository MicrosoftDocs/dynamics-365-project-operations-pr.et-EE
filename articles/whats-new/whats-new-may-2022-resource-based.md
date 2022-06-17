---
title: Mis on uut mais 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Selles artiklis antakse teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta mai väljaandes ressursi-/ladustamata stsenaariumide jaoks.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921389"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut mais 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.42.0.70
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnaversioonis 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käivitage alati oma keskkonnas kaardi uusim versioon ja lubage project Operationsi Dataverse lahenduse ja Finance'i lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastist väljas olevat tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui kaardi käivitamisel ilmneb probleem, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises Kaartide [jaotises Puudu tabeliveergude probleemi juhiseid](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused
### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Ressursihaldus | 2634019 | Täiustatud tõrketeated ettevõtte valideerimiseks üldiste meeskonnaliikmete lisamisel ressurssidena. |
| Projekti plaanimine ja jälgimine | 2648515 | Omaniku-ID **·**, **oleku** ja **oleku** piiratud värskendused plaanimisolemites. |
| Arveldamine ja hinnakujundus | 2653167 | **Hinnanguruudustiku** kümnendkoha eraldaja peab järgima isiklike suvandite **vormingusätteid**. |
| Arveldamine ja hinnakujundus| 2662251 | Väärtused väljadel **Parandatud ühik** ja **Ühik** vaikeväärtused, kui loote kirjeid materjalihinnangutes. |
| Arveldamine ja hinnakujundus| 2571408 | Sisestamata müügireaalsused tembeldatakse mustandiarve loomisel proformaarve ID-ga. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektijuhtimine ja raamatupidamine Dynamics 365 Finance

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse rakendusse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
