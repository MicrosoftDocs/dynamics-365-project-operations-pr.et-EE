---
title: Mis on uut detsembris 2021 – Project Operationsi lihtjuurutamine
description: See artikkel kirjeldab kvaliteedivärskendusi, mis on saadaval Project Operationsi lihtjuurutuse 2021. aasta detsembri väljalaskes.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914075"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Mis on uut detsembris 2021 – Project Operationsi lihtjuurutamine

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

### <a name="subcontract-management"></a>Allhankelepingu haldus 

- [Projektimeeskonna alltöövõtuliikmed](../subcontracting/subcontracting-project-team-members.md): projektijuht saab luua allhankelepingute ja allhankelepinguridade nimelisi või üldisi meeskonnaliikmeid, et mõjutada personali ja hinnanguid.
- [Projektimeeskonna liikmete allhankevõimalused](../subcontracting/subcon-options.md): nimetatud või üldiste projektimeeskonna liikmete personalivalikuid tehes saab projektijuht üle vaadata olemasolevad alltöövõtjad või luua ühe või mitme projekti jaoks uusi alltöövõtjatest meeskonnaliikmeid. 
- [Alltöövõtu ressursside määramise kulude prognoos](../subcontracting/costing-subcon-ra.md): projekti kulude prognoosimisel võetakse arvesse alltöövõtu ressursside määramist ja nende maksumuse määramisel kasutatakse allhankelepingutega seotud ostuhinnakirju. 
- [Konfigureerige ajakava, et näidata lepingulisi töötajaid ja alltöövõtjate võimsust](../subcontracting/configure-sb-subcon.md): rakenduse Project Operations ajakava tahvlit saab nüüd konfigureerida nii, et see otsib ja soovitab broneeritavate ressursside lepinguliste töötajate tüüpi ja alltöövõtu mahtu koos töötajatega. Seda konfiguratsiooni saab kasutada, kui otsitakse ressursse konkreetse projektinõude personaliga seotud kontekstis või kui otsitakse väljaspool projektinõude konteksti.
- [Projekti mehitamine lepinguliste töötajate ja alltöövõtjate abil](../subcontracting/staffing-cw.md): lepingulised töötajad saab nüüd projektidele broneerida, kasutades ajakava tahvli kogemusi.
- [Aja, kulude ja materjalikasutuse registreerimine alltöövõtu komponentide projektides](../subcontracting/recording-subcon-actuals.md): lepingulised töötajad saavad registreerida aega ja kulusid ning projektimeeskonna liikmed saavad registreerida ka projekti raames allhankelepingu abil ostetud materjalide kasutamist. Selle tulemuseks on täpsete kulude kirjendamine projektide puhul, kus kasutatakse ostetud võimsust või materjale.
- [Allhankelepingu oleku üleminekud](../subcontracting/subcon-states.md): alltöövõtjad võib kinnitada, et lõpetada läbirääkimised hankijaga, sulgeda, et näidata tarne lõpuleviimist, või tühistada, et näidata lepingu lõpetamist hankijaga enne tarne lõpuleviimist.

### <a name="task-planning"></a>Ülesande planeerimine
- Parem tõrkeotsing süsteemiadministraatorite jaoks. Kui kasutaja ei saa projekti avada, saab administraator vaadata litsentsiga mitteseotud vigu, mida Project for the web genereerib [Projekti ajastamise logid](../../project-management/schedule-api-logs.md).
- [Ülesannete kontrollnimekirjade kasutamine Microsoft Project for the webis](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Microsoft Project for the Webis saate lisada ülesandele kontroll-loendi, et jälgida konkreetseid objekte.

## <a name="quality-updates"></a>Kvaliteedi värskendused

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Plaanimine ja jälgimine | 2392596 | Ajakava API-d võimaldavad nüüd värskendada välju **Järeljäänud jõupingutused**, **Lõpetatud jõupingutus** ja **% lõpule viidud**. |
| Plaanimine ja jälgimine | 2478497 | Ajakava API-de **Tegevusnumber** ja **Ülesande ID** võivad sisestamisel olla tühjad, kuna süsteem täidab need automaatse nummerdamise abil.|
| Aeg ja kulu | 2468135 | Kinnituskatsete arvu vähendatakse viielt kolmele. |
| Aeg ja kulu | 2468188 | Parandatud probleem, mille puhul logi tekst ületas maksimaalset pikkust atribuudis **märkmetekst** olemis **marginaal**. |
