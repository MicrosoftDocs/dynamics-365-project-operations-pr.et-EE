---
title: Eemaldatud või taunitud funktsioonid rakenduses Dynamics 365 Project Operations
description: Selles teemas kirjeldatakse funktsioone, mis on eemaldatud või mis on plaanitud rakendusest eemaldamiseks Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601565"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Eemaldatud või taunitud funktsioonid rakenduses Dynamics 365 Project Operations

_**Kehtib järgmiste puhul:** Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks, lihtjuurutus – tehing näidisarveldusele ja Project Operations ressursi-/tootmispõhiste stsenaariumite jaoks_

Selles teemas kirjeldatakse funktsioone, mis on eemaldatud või mis on plaanitud rakendusest eemaldamiseks Dynamics 365 Project Operations.

- *Eemaldatud* funktsioon pole enam tootes saadaval.
- *Iganenud* funktsiooni ei arendata aktiivselt ja võidakse tulevases värskenduses eemaldada.

See loend on mõeldud teie abistamiseks oma planeerimises nende eemaldamiste ja iganemistega arvestamiseks.

> [!NOTE]
> Üksikasjalikku teavet finance and Operationsi rakenduste objektide kohta leiate tehnilise viite aruannetest [**·**](/dynamics/s-e/global/axtechrefrep_61). Saate võrrelda nende aruannete erinevaid versioone, et saada teavet objektide kohta, mis on rakenduses Finance and Operations igas versioonis muutunud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Projektitoimingute 2022. aasta märtsi väljaandes eemaldatud või aegunud funktsioonid

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektijuhtimise ja raamatupidamise parameeter "Loo alati täpsustuskande loomine"

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Korrigeerimiskanded on vajalikud auditi eesmärgil. Pärast amortisatsiooni see parameeter peidetakse. Süsteem loob alati korrigeerimiskandeid, nagu ka praegu, kui parameetri väärtuseks **on seatud Jah**. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektitoimingud tootmise/ladustatud stsenaariumide jaoks |
| **Olek** | Aegunud: 1. märtsiks 2023 peidame parameetri ja muudame süsteemi käitumist nii, et korrigeerimiskanded luuakse alati. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektijuhtimise ja raamatupidamise parameeter "Kasuta täpsustuskuupäeva uue projektikuupäevana" parameeter

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Seda parameetrit kasutati algselt kohanduste võimaldamiseks, kui fiskaalperiood suleti. Kuid see pole enam vajalik, sest tehingu arvestuskuupäeva saab muuta avatud perioodi esimeseks kuupäevaks, kui see on konfigureeritud. Projekti kuupäeva ei tohi muuta, kuna see tähistab kande toimumise kuupäeva. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektitoimingud tootmise/ladustatud stsenaariumide jaoks |
| **Olek** | Aegunud: 1. märtsiks 2023 peidame parameetri ja muudame süsteemi käitumist nii, et projekti kuupäeva ei muudeta kunagi kohandustel. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Ressursitaotluse töövoog Project Operationsis ladustatud/tootmispõhiste stsenaariumide jaoks

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Aegunud vähese kasutuse ja kandemahu piirangute tõttu. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektitoimingud tootmise/ladustatud stsenaariumide jaoks |
| **Olek** | Aegunud: 1. märtsiks 2023 keelame töövoo abil projekti ressursside taotlemise võimaluse. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projektiarve ettepaneku leht ilma Päise ja ridade vaadeteta

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Aegunud lehe täiustuste tõttu, mis võeti kasutusele koos funktsioonivõtmega **Kasuta projekti arve ettepanekut ja arvežurnaali vorme, millel on vaate** Päis ja read. |
| **Kas asendatakse muu funktsiooniga?** | Ja |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektitoimingud tootmise/ladustatud stsenaariumide jaoks; Projektitoimingud ressursi/ ladustamata stsenaariumide jaoks |
| **Olek** | Aegunud: 1. märtsiks 2023 lülitame varasema (pärand)lehe välja ja lülitame sisse **projektisoovituse ja arvežurnaali vormide kasutamise vaikimisi vaate** päise ja ridade vaate funktsioonivõtmega. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Projektitoimingute 2021. aasta detsembri väljaandes eemaldatud või aegunud funktsioonid

### <a name="collaboration-workspaces"></a>Koostöö tööruumid

[Koostööruumi loomine või linkimine (Projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Aegunud vähese kasutuse tõttu. Kliendid, kes kasutavad Project Operationsi ressursi-/ladustamata stsenaariumide jaoks, saavad kasutada [koostööd Office'i rühmadega](../project-management/collaboration-groups.md). |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus  |
| **Juurutamise valik** | Projektitoimingud tootmise/ladustatud stsenaariumide jaoks |
| **Olek** | Aegunud: 1. detsembriks 2022 plaanime koostööruume enam mitte toetada. |
