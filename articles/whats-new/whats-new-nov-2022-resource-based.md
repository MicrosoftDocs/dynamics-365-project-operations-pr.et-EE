---
title: Mis on uut novembris 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta novembri väljaandes ressursipõhiste/varudeta stsenaariumide jaoks.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831125"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut novembris 2022 – Project Operations ressursi-/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.58.0.119
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2781818 | Võti ei leidnud viga materjali kasutamise logi vaikehinna määramisel. |
| Arveldamine ja hinnakujundus | 2922373 | Hinnapakkumise rida ei saa linkida projektiga, mis on kadunud tsitaadina suletud. |
| Arveldamine ja hinnakujundus | 2943206 | **Lepingurea** väli projektiüksuses peaks olema valikuline. |
| Arveldamine ja hinnakujundus | 2953182 | Parandage parandusarvete veateadet.|
| Arveldamine ja hinnakujundus | 2959500 | Hinnapakkumise rida ei saa linkida projektiülesandega, mis on juba seostatud kaotsiläinud tsitaadiga.|
| Arveldamine ja hinnakujundus | 2959560 | "See klient on juba projektilepingus" teade, mis saadi hinnapakkumise sulgemisel, kuna see on teatud lokaatides võidetud. |
| Arveldamine ja hinnakujundus | 3031727 | Ressursimäärangud nurjuvad, kui nõutav väli "msdyn_Company" puudub. |
| Arveldamine ja hinnakujundus | 3036905 | Omavat ettevõtet ei initsialiseerita kunagi ProjectTeamMemberil. |
| Müügivõimaluse haldus | 2763519 | Nullviite viga rakenduses EnsureProjectContractAllowsUpdates. |
| Müügivõimaluse haldus | 2783798 | Projekti prognooside importimisel hinnapakkumise reale puuduvad kulu- ja materjaliprognooside ülesandekirjeldused.|
| Müügivõimaluse haldus | 2988635 | Parandage tõrke msg kirjeldust kliendi hinnapakkumisel kustutamisel. |
| Müügivõimaluse haldus | 3001191 | Müügivõimalusest ei saa hinnapakkumist luua, kui arveldusmeetod on määratud nulliks. |
| Versioonitäiendus | 3012324 | Projekti teisendamine nurjus projektis, mille nimes olid juhtmärgid nagu Tab. || Projekti plaanimine ja jälgimine | 2790384 | Ootel OperationSeti ajalõpp on liiga lühike. |
| Projekti plaanimine ja jälgimine | 3044275 | Puudub lokaliseerimine: missingProjectSchedulerErrorMessage. |
| Projekti plaanimine ja jälgimine | 3044277 | Project Reconi ruudustikku ei laadita, kui planeerija on seadistamata.|
| Ressursihaldus | 2943153 | Värskenda vahekaarti Jälgimine, et kuvada kestuse puhul kaks kohta pärast koma.|
| Allhankeleping | 2932774 | Hankija arve rida Loe ainult viskamisviga valesti. |
| Allhankeleping | 2939556 | Hankija arve päise olekuks ei tohiks olla määratud Mustandi veebipõhine kustutamine, kui see pole aktiivne. |
| Aeg ja kulu | 2939998 | Võtke kasutusele uus TESA versioon ProjOpsis. |


### <a name="project-management-and-accounting-in-finance"></a>Projektihaldus ja raamatupidamine rahanduses

Lisateabe saamiseks tõrkeparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Microsoft Dynamics Lifecycle Services ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
