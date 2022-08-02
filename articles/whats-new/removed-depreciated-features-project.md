---
title: Eemaldatud või aegunud funktsioonid Dynamics 365 Project Operations
description: Selles artiklis kirjeldatakse funktsioone, mis on eemaldatud või mis on plaanitud eemaldada Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028324"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Eemaldatud või aegunud funktsioonid Dynamics 365 Project Operations

_**Kehtib järgmiste puhul:** Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks, lihtjuurutus – tehing näidisarveldusele ja Project Operations ressursi-/tootmispõhiste stsenaariumite jaoks_

Selles artiklis kirjeldatakse funktsioone, mis on eemaldatud või mis on plaanitud eemaldada Dynamics 365 Project Operations.

- *Eemaldatud* funktsioon pole enam tootes saadaval.
- *Iganenud* funktsiooni ei arendata aktiivselt ja võidakse tulevases värskenduses eemaldada.

See loend on mõeldud teie abistamiseks oma planeerimises nende eemaldamiste ja iganemistega arvestamiseks.

> [!NOTE]
> Üksikasjalikku teavet finance and operationsi rakenduste objektide kohta leiate tehnilise viite aruannetest [**·**](/dynamics/s-e/global/axtechrefrep_61). Saate võrrelda nende aruannete erinevaid versioone, et saada teavet objektide kohta, mida on finance and operationsi rakenduste igas versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Project Operationsi 2022. aasta märtsi väljaandes eemaldatud või aegunud funktsioonid

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektijuhtimise ja raamatupidamise parameeter "Loo alati korrigeerimiskanne"

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Korrigeerimiskanded on vajalikud auditi eesmärgil. Pärast aegumist on see parameeter peidetud. Süsteem loob alati korrigeerimiskanded, täpselt nagu praegu, kui parameetri väärtuseks **on seatud Jah**. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektioperatsioonid tootmise/ ladustatud stsenaariumide jaoks |
| **Olek** | Kasutuselt kõrvaldatud: 1. märtsiks 2023 peidame parameetri ja muudame süsteemi käitumist nii, et korrigeerimiskanded oleksid alati loodud. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektijuhtimise ja raamatupidamise parameeter "Kasuta korrigeerimiskuupäeva uue projektikuupäevana"

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Seda parameetrit kasutati algselt reguleerimiseks, kui fiskaalperiood suleti. Kuid see pole enam vajalik, kuna kande arvestuskuupäeva saab muuta avatud perioodi esimeseks kuupäevaks, kui see on konfigureeritud. Projekti kuupäeva ei tohi muuta, kuna see tähistab kande toimumise kuupäeva. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektioperatsioonid tootmise/ ladustatud stsenaariumide jaoks |
| **Olek** | Kasutuselt kõrvaldatud: 1. märtsiks 2023 peidame parameetri ja muudame süsteemi käitumist nii, et projekti kuupäeva kohandamisel kunagi ei muudetaks. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Ressursitaotluse töövoog rakenduses Project Operations lao-/tootmispõhiste stsenaariumide jaoks

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Kasutuselt kõrvaldatud vähese kasutuse ja kandemahu piirangute tõttu. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projektioperatsioonid tootmise/ ladustatud stsenaariumide jaoks |
| **Olek** | Kasutuselt kõrvaldatud: 1. märtsiks 2023 keelame töövoo abil võimaluse projekti jaoks ressursse taotleda. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projektiarve ettepaneku leht ilma päise- ja ridade vaadeteta

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Kasutuselt kõrvaldatud lehe täiustuste tõttu, mis võeti kasutusele koos vormidega **Kasuta projekti arvesoovitust ja arve töölehelehte koos vaate päise ja ridade vaate** funktsioonivõtmega. |
| **Kas asendatakse muu funktsiooniga?** | Ja |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Projekti toimingud tootmise / ladustatud stsenaariumide jaoks; Projekti toimingud ressursside / varudeta stsenaariumide jaoks |
| **Olek** | Kasutuselt kõrvaldatud: 1. märtsiks 2023 lülitame välja varasema (pärand)lehe ja lülitame sisse **vormid Kasuta projekti arvesoovitust ja arve töölehed, kus on vaikimisi funktsiooniklahv Päis ja Read**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funktsioonid, mis on rakenduse Project Operations 2021. aasta detsembri väljaandes eemaldatud või aegunud

### <a name="collaboration-workspaces"></a>Koostöö tööruumid

[Koostöö tööruumi loomine või linkimine (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Kasutuselt kõrvaldatud vähese kasutamise tõttu. Kliendid, kes kasutavad ressursi-/varumata stsenaariumide jaoks project operationsit, saavad kasutada [koostööd office'i rühmadega](../project-management/collaboration-groups.md). |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus  |
| **Juurutamise valik** | Projektioperatsioonid tootmise/ ladustatud stsenaariumide jaoks |
| **Olek** | Kasutuselt kõrvaldatud: 1. detsembriks 2022 ei kavatse me enam koostöö tööruume toetada. |
