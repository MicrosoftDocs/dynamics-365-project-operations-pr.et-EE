---
title: Mis on uut augustis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta augusti väljaandes ressursipõhiste/varumata stsenaariumide jaoks.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403851"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut augustis 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektitoimingud keskkonnaversioonis Dataverse 4.45.0.53
- Projektijuhtimine ja raamatupidamine Dynamics 365 Finance keskkonnas versioon 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käivitage oma keskkonnas alati kaardi uusim versioon ja lubage project operationsi Dataverse lahenduse ja finance lahenduse versiooni värskendamisel kõik seotud tabelikaardid. Mõned funktsioonid ja võimalused ei pruugi õigesti töötada, kui kaardi uusim versioon pole aktiveeritud. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud valmis tabelikaarti, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib kaardi käivitamisel probleem, järgige juhiseid, mis on toodud [tõrkeotsingu juhendi Jaotises Puuduvad tabeli veerud kaardil](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
|   Müügivõimaluste haldus | 2762089 | Vigade käsitlemine lepingu sulgemisel kadunuks, kui automaatne salvestamine on organisatsioonis keelatud.|
|Projekti plaanimine ja jälgimine | 2767841 | Telemeetria värskendab Projekti olemit Stsenaariumide loomine või värskendamine.|
|Arveldamine ja hinnakujundus | 2771072 | Nullviite erandi käsitlemine võitva hinnapakkumise ajal.|
|Arveldamine ja hinnakujundus | 2844181 |Ebaõnnestumine korrelatsiooni ID saamisel ja arve loomise blokeerimisel.|
|Arveldamine ja hinnakujundus | 2852836 | Kontsernisisesed tegelikud kulud puuduvad kontsernisisese kulu puhul, mis on loodud ja kinnitatud CE-s.|


### <a name="project-management-and-accounting-in-finance"></a>Projektijuhtimine ja raamatupidamine rahanduses

Selles värskenduses sisalduvate veaparanduste kohta teabe saamiseks logige sisse teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja vaadake [teabebaasi artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
