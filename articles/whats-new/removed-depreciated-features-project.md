---
title: Rakenduse Dynamics 365 Project Operations eemaldatud või iganenud funktsioonid
description: See artikkel kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada rakendusest Dynamics 365 Project Operations.
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
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Rakenduse Dynamics 365 Project Operations eemaldatud või iganenud funktsioonid

_**Kehtib järgmiste puhul:** Project Operations ressursipõhiste/mittelaopõhiste stsenaariumite jaoks, lihtjuurutus – tehing näidisarveldusele ja Project Operations ressursi-/tootmispõhiste stsenaariumite jaoks_

See artikkel kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada rakendusest Dynamics 365 Project Operations.

- *Eemaldatud* funktsioon pole enam tootes saadaval.
- *Iganenud* funktsiooni ei arendata aktiivselt ja võidakse tulevases värskenduses eemaldada.

See loend on mõeldud teie abistamiseks oma planeerimises nende eemaldamiste ja iganemistega arvestamiseks.

> [!NOTE]
> Üksikasjalikku teavet finants- ja äritoimingute rakendustes olevate objektide kohta leiate jaotisest [**Tehnilised viitearuanded**](/dynamics/s-e/global/axtechrefrep_61). Saate võrrelda nende aruannete erinevaid versioone, et saada teavet objektide kohta, mida on finants- ja äritoimingute rakendustes igas versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Rakenduse Project Operations märtsi 2022 versioonis eemaldatud või aegunud funktsioonid

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektihalduse ja raamatupidamise parameeter „Loo alati tiksu kannete loomine“

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Korrigeerimistehingud on auditi jaoks vajalikud. Pärast iganemist see parameeter peidetakse. Süsteem loob alati korrigeerimistehingud, täpselt nagu praegu, kui parameetriks on seatud **Jah**. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Project Operations tootmise/lao stsenaariumite jaoks |
| **Olek** | Iganenud: 1. märtsiks 2023 peidame parameetri ja muudame süsteemi käitumist nii, et korrigeerimistehingud luuakse alati. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projektihaldus ja raamatupidamise parameeter „Kasuta kohandamiskuupäeva uue projekti kuupäevana“.

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Seda parameetrit kasutati algselt eelarveperioodi sulgemise korral korrigeerimiste võimaldamiseks. Kuid see pole enam vajalik, kuna tehingu arvestuskuupäeva saab muuta avatud perioodi esimeseks kuupäevaks, kui see on konfigureeritud. Projekti kuupäeva ei tohi muuta, kuna see tähistab tehingu toimumise kuupäeva. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Project Operations tootmise/lao stsenaariumite jaoks |
| **Olek** | Iganenud: 1. märtsiks 2023 peidame parameetri ja muudame süsteemi käitumist nii, et projekti kuupäeva kohandamisel kunagi ei muudeta. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Ressursitaotluse töövoog rakenduse Project Operations lao-/tootmispõhiste stsenaariumide jaoks

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Iganenud vähese kasutuse ja tehingumahu piirangute tõttu. |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Project Operations tootmise/lao stsenaariumite jaoks |
| **Olek** | Iganenud: 1. märtsiks 2023 keelame töövoo abil projekti jaoks ressursside taotlemise võimaluse. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projektiarve ettepaneku leht ilma päise- ja reavaadeteta

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Iganenud lehe täiustuste tõttu, mis võeti kasutusele koos funktsiooniklahviga **Projektiarve ettepaneku ja arvete töölehe vormide kasutamine koos päise ja ridade vaatega**. |
| **Kas asendatakse muu funktsiooniga?** | Ja |
| **Mõjutatud tooted** | Rakendus |
| **Juurutamise valik** | Rakenduse Project Operations tootmise/lao stsenaariumide jaoks; Rakenduse Project Operations ressursi/mittelaopõhiste stsenaariumide jaoks |
| **Olek** | Iganenud: 1. märtsiks 2023 lülitame välja varasema (pärand) lehe ja lülitame vaikimisi sisse funktsiooniklahvi **Projektiarve ettepaneku ja arvete töölehe vormide kasutamine koos päise ja ridade vaatega**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Rakenduse Project Operations detsembri 2021 versioonis eemaldatud või iganenud funktsioonid

### <a name="collaboration-workspaces"></a>Koostöö tööruumid

[Koostöö tööruumi loomine või linkimine (Projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Eemaldamise/iganemise põhjus** | Iganenud vähese kasutuse tõttu. Kliendid, kes kasutavad rakendust Project Operations ressursside/mittelaopõhiste stsenaariumide jaoks, saavad kasutada [Koostöö Office Groupsiga](../project-management/collaboration-groups.md). |
| **Kas asendatakse muu funktsiooniga?** | No |
| **Mõjutatud tooted** | Rakendus  |
| **Juurutamise valik** | Project Operations tootmise/lao stsenaariumite jaoks |
| **Olek** | Iganenud: 1. detsembriks 2022 ei plaani me enam koostöö tööruume toetada. |
