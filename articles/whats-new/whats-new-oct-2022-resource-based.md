---
title: Mis on uut oktoobris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations 2022. aasta oktoobri väljaandes ressursipõhiste/varudeta stsenaariumide jaoks.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806731"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mis on uut oktoobris 2022 – Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.57.0.176
- Projektihaldus ja raamatupidamine rakenduse Dynamics 365 Finance keskkonna versioonis 10.0.30

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Projekti plaanimine ja jälgimine | **Projekti toimingud Väline plaanimine**<br>Väline plaanimisrežiim võimaldab klientidel algupäraselt luua, värskendada ja kustutada olemeid, mis on seotud tööjaotuse struktuuridega (WBS), kasutades kohalikke Dataverse API-sid, ilma praeguste piiranguteta, mida Project for the Web jõustab. | [Väline ajastamine](/dynamics365/project-operations/project-management/external-scheduling) |
| Juurutamine ja konfiguratsioon | <p>**Luba klientidel valida juurutuse tüüp**<br>Project Operationsi tootepõhiseid värskendusi (PDU-sid) kasutatakse Project Operationsi topeltkirjutuslahenduse automaatseks installimiseks, kui keskkonda on installitud kahe kirjutusega tuum- ja orkestreerimislahendused.</p><p>See funktsioon tutvustab projekti parameetrites uut **lahenduse täiendamise käitumise** parameetrit. Kui see parameeter on seatud väärtusele **Ainult** Lite, ei installi PUD-id enam automaatselt Project Operations Dual-write lahendust, isegi kui keskkonda on installitud kahe kirjutusega tuum- ja orkestreerimislahendused. Selline käitumine on kasulik klientidele, kes kavatsevad kasutada topeltkirjutuslahendusi müügitellimuste integreerimiseks finance and operationsi rakendustesse, kuid soovivad kasutada Project Operationsi Lite-režiimis (st ilma finance and operationsi rakendustesse integreerimata).</p> | |
| Arveldamine ja hinnakujundus | <p>**Valuuta konverteerimine kulu arveldamata müügikande jaoks integreeritud keskkondades**<br>Klientide jaoks, kes kasutavad Finance and Operationsi rakendustega integreeritud Project Operationsi (st ressursi/varumata juurutuse tüübis), kasutatakse vahetuskursse tavaliselt finance and operationsi rakendustes. Kui aga kulukategooria hinnastamisel tuleks kliendi arveldamisel kasutada hinna arvutamise meetodit "omahinnas" või "omahinnas ülehinnas", kasutab müügisumma arvutamiseks kasutatav vahetuskurss valuutakursse Dataverse, mitte finance and operationsi rakenduste vahetuskursse.</p><p>See funktsioon tutvustab projekti parameetrites uut **valuutakonversioonikäitumise** parameetrit. Kui selle parameetri väärtuseks on seatud Laiendatud **varuvariandiga**, arvutatakse kulukannete arveldamata müügisummad finance and operationsi rakenduste vahetuskursside abil.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Rakenduse Project Operations topeltkirjutamise kaartide värskendused

Selles väljaandes ei ole Project Operationsi topeltkirjutuse kaartide jaoks värskendusi. Project Operationsi topeltkijrutusega kaartide praeguse loendi ja versioonide jaoks vaadake teemat [Project Operationsi topeltkirjutamise kaardi versioonid](../environment/resource-dual-write-maps.md).

Käitage oma keskkonnas alati kaardi uusimat versiooni ja lubage kõik seotud tabelikaardid oma Project Operationsi lahenduse Dataverse ja Finance versiooni värskendamisel. Kui kaardi uusim versioon pole aktiveeritud, ei pruugi mõned funktsioonid ja võimalused õigesti töötada. Kaardi aktiivset versiooni saate vaadata veerust **Versioon** lehel **Topeltkirjutamine**. Kaardi uue versiooni aktiveerimiseks valige **Tabelivastenduse versioonid**, valige uusim versioon ja seejärel salvestage valitud versioon. Kui olete kohandanud kastivälise tabelikaardi, rakendage muudatused uuesti. Lisateabe saamiseks vt [Rakenduse elutsükli haldus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Kui teil tekib probleeme kaardi käivitamisel, järgige topeltkirjutamise tõrkeotsingu juhendi jaotises [Probleem kaardilt puuduvate tabeli veergudega](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvaliteedi värskendused

### <a name="project-operations-on-dataverse"></a>Project Operations teenuses Dataverse

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2316317 | Süsteem võimaldab luua arveid, millel ei ole tasulisi kandeid. |
| Arveldamine ja hinnakujundus | 2737300 | Enne vormile juurdepääsu kontrollimist **saate kontrollida, kas kliendi** väli on saadaval. |
| Arveldamine ja hinnakujundus | 2744948 | Lisage arveldusmeetodile nullkontroll. |
| Arveldamine ja hinnakujundus | 2763515 | Nullviite veakäsitlus, kui arve müügileping puudub. |
| Arveldamine ja hinnakujundus | 2844301 | Partiiarve loomine nurjub tõrke tõttu. |
| Arveldamine ja hinnakujundus | 2845869 | Organisatsiooniteenuse vale salvestamine. |
| Arveldamine ja hinnakujundus | 2853729 | Rolli ja hinna üksikasju värskendatakse siis, kui muudetakse Arvelduse tüüpi. |
| Arveldamine ja hinnakujundus | 2940350 | Kui tegelikud hinnad on määratud, tuleb automaatselt sisestada ainult aktiivsed hinnakirjad. |
| Juurutamine ja konfiguratsioon | 3001206 | Olem msdyn\_ replaylogheader takistab Customer Orgs’i uuendamist. |
| Müügivõimaluse haldus | 2755582 | Nullviite erandid käsitlevad jagatud arveldusreegli abistajas. |
| Müügivõimaluse haldus | 2761477 | Kui kasutatakse jagatud arveldamist, jätab verstaposti (päise) kustutamine omanikuta verstapostid. |
| Müügivõimaluse haldus | 2767595 | Kui materjali kasutamise kirje avatakse põhivormil, muudetakse kirje broneeritav ressurss parajasti sisselogitud kasutajaks. |
| Projekti plaanimine ja jälgimine | 2790384 | Ootel OperationSeti ajalõpp on liiga lühike. |
| Projekti plaanimine ja jälgimine | 2957840 | Tööülesandeid ei saa salvestada ja veerge ei saa lisada **integreeritud projektitoimingute lehele Tööülesanded** . |
| Ressursihaldus | 2751560 | Ebajärjekindlad eelistatud organisatsiooniüksused ressursinõudes. |
| Allhankeleping | 2853245 | Hankija arverea tegelike näitajate vastendamine ei värskenda kinnitamise olekut, kui lepingurida on hankija arve reaga juba lingitud. |
| Allhankeleping | 2907231 | Hankija arvete protsessietappi ei saa edasi liikuda. |
| Aeg ja kulu | 2867363 | Kirjed ei kao vaatest Puudumised/Puhkused kinnitamiseks, kui need on kinnitamise järjekorras. |
| Aeg ja kulu | 2894405 | TESA: kasutamata POC-kataloog põhjustab vastavusprobleeme. |

### <a name="project-management-and-accounting-in-finance"></a>Projektihaldus ja raamatupidamine rahanduses

Lisateabe saamiseks tõrkeparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Microsoft Dynamics Lifecycle Services ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
