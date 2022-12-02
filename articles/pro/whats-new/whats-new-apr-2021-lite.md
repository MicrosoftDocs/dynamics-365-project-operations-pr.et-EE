---
title: Mis on uut aprillis 2021 – Project Operationsi lihtjuurutamine
description: See artikkel annab teavet rakenduse Project Operations lihtjuurutamise 2021. a aprilli väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 987eeaf2e57659a6facae6b0a3688f15992e8bb9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931234"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Mis on uut aprillis 2021 – Project Operationsi lihtjuurutamine

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See artikkel kehtib rakenduse Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

  - Project Operations Dataverse’i keskkonna versioonis 4.9.0.221 

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- Projektide mittelaopõhised materjalid. Peamised võimalused on järgmised.
  - Mittelaopõhiste materjalide projekti müügitsükli ajal prognoosimine ja hinnakujundus. Lisateavet vaadake teemast [Kataloogitoodete oma- ja müügihindade seadistamine – liht](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Mittelaopõhiste materjalide jälgimine projekti kohaletoimetamisel. Lisateavet vaadake teemast [Projektides ja projektiülesannetes materjali kasutuse kirjendamine](../../material/material-usage-log.md).
  - Kasutatud mittelaopõhiste materjalide kulude arveldamine. Lisateavet vaadake teemast [Arvete võlgnevuste haldamine – liht](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Dynamics 365 Dataverse’i uued API-d võimaldavad luua, värskendada ja kustutada toiminguid suvandiga **Olemite ajastamine**. Lisateavet vaadake teemast [Ajakava API-de kasutamine kavandamise olemitega toimingute tegemiseks](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvaliteedi värskendused

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2224568 | Lisatud on loogika, et lubada kohandused, mis hõlmavad arve kinnitamise lisandmooduli käivitamist. |
| Arveldamine ja hinnakujundus | 2101098 | Näidisarve vaikeväljade loogikat on parandatud: **Maksja aadress**, **Maksja nimi** ja **Maksetingimused** pärinevad nüüd vaikimisi vastavatest projektilepingu kliendikirjetest. |
| Arveldamine ja hinnakujundus | 2021413 | Väljasid **Tegeliku kulu** ja **Müük** uuendati olemis **Ülesanne**, et kaasata ülesande arveldamata ja arveldatud kulude müügiväärtus. |
| Arveldamine ja hinnakujundus | 2182110 | Projektilepingu kopeerimisel luuakse lepingurea ID sihtprojekti lepingus, et tagada selle kordumatus. |
| Müügivõimaluse haldus | 2186741 | Lisatud valideerimised tagamaks, et olemasoleva hinnapakkumise rea üksikasjades ei saaks välja **Päritolu** ja **Tehingu tüüp** värskendada. |
| Müügivõimaluse haldus | 2191353 | Vahe-eesmärke ei tohi aja ja materjali lepingureal luua. |
| Müügivõimaluse haldus | 2216956 | Lahendati probleem suvandiga **Värskenda hindu**. |
| Plaanimine ja jälgimine | 2182979 | Projekti kopeerimise funktsiooni on täiustatud, et tagada kuluprognoosi ridade kopeerimine algsest projektist. |
| Plaanimine ja jälgimine | 2184144 | Projekti kopeerimise funktsiooni on täiustatud, et tagada ressursi positsiooni nime kopeerimine algsest projektist. |
| Plaanimine ja jälgimine | 2184799 | Projekti koopia: tihendati kontrolli tagamaks, et hinnangulist alguskuupäeva ei saaks poolelioleva kopeerimise ajal muuta. |
| Plaanimine ja jälgimine | 2185134 | Projekti koopia: sihtprojekti eeldatavaks alguskuupäevaks seatakse tänane kuupäev. |
| Plaanimine ja jälgimine | 2196373 | Projekti koopia: veenduge, et projektijuhi ja meeskonnaliikme kirjeid ei dubleeritaks projektimeeskonnas. |
| Plaanimine ja jälgimine | 2211833 | Projekti koopia: ressursi määramised kopeeritakse lähteprojekti tööülesandest sihtprojekti. |
| Plaanimine ja jälgimine | 2186541 | Parandati probleem ressursside rühmitamise ajal ruudustikus **Prognoosid**. |
| Plaanimine ja jälgimine | 2166906 | Ülesande tehingu kategooria tuleb kopeerida olemisse **Ressursi määramine**. |
| Ressursihaldus | 2125362 | Lahendati probleemid üldise meeskonnaliikme loomisega tunnipõhist jaotamismeetodit kasutades. |
| Aeg ja kulu | 2113603 | Parandati kohandamisega seotud probleem koos atribuutide eemaldamisega lehelt **Ajakirje**. Süsteem kontrollib nüüd enne atribuudile skripti abil juurde pääsemist, kas atribuut on lehel olemas. |
| Aeg ja kulu | 2204377 | Kopeeritud ajatabelid peavad olema automaatselt kuvatud, kui valite aja kirjendamise ajal suvandi **Kopeeri nädal**. |
| Aeg ja kulu | 2209059 | Välja **Olek** saab ajakirjete Dynamics 365 Field Service jaoks muuta. |
