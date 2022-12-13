---
title: Mis on uut oktoobris 2022 – Project Operationsi lihtjuurutamine
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations lite-juurutuse 2022. aasta oktoobri väljaandes.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806732"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Mis on uut oktoobris 2022 – Project Operationsi lihtjuurutamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.57.0.176

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Projekti plaanimine ja jälgimine | **Projekti toimingud Väline plaanimine**<br>Väline plaanimisrežiim võimaldab klientidel algupäraselt luua, värskendada ja kustutada olemeid, mis on seotud tööjaotuse struktuuridega (WBS), kasutades kohalikke Dataverse API-sid, ilma praeguste piiranguteta, mida Project for the Web jõustab. | [Väline ajastamine](/dynamics365/project-operations/project-management/external-scheduling) |
| Juurutamine ja konfiguratsioon | <p>**Luba klientidel valida juurutuse tüüp**<br>Project Operationsi tootepõhiseid värskendusi (PDU-sid) kasutatakse Project Operationsi topeltkirjutuslahenduse automaatseks installimiseks, kui keskkonda on installitud kahe kirjutusega tuum- ja orkestreerimislahendused.</p><p>See funktsioon tutvustab projekti parameetrites uut **lahenduse täiendamise käitumise** parameetrit. Kui see parameeter on seatud väärtusele **Ainult** Lite, ei installi PUD-id enam automaatselt Project Operations Dual-write lahendust, isegi kui keskkonda on installitud kahe kirjutusega tuum- ja orkestreerimislahendused. Selline käitumine on kasulik klientidele, kes kavatsevad kasutada topeltkirjutuslahendusi müügitellimuste integreerimiseks finance and operationsi rakendustesse, kuid soovivad kasutada Project Operationsi Lite-režiimis (st ilma finance and operationsi rakendustesse integreerimata).</p> | |

## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2316317 | Süsteem võimaldab luua arveid, millel ei ole tasulisi kandeid. |
| Arveldamine ja hinnakujundus | 2737300 | Enne vormile juurdepääsu kontrollimist saate kontrollida, kas kliendi väli on saadaval. |
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
| Ressursihaldus | 2751560 | Ebajärjekindlad eelistatud organisatsiooniüksused ressursinõudes. |
| Allhankeleping | 2907231 | Hankija arvete protsessietappi ei saa edasi liikuda. |
| Aeg ja kulu | 2867363 | Kirjed ei kao vaatest Puudumised/Puhkused kinnitamiseks, kui need on kinnitamise järjekorras. |
| Aeg ja kulu | 2894405 | TESA: kasutamata POC-kataloog põhjustab vastavusprobleeme. |
