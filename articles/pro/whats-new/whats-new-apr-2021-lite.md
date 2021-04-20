---
title: Mis on uut aprillis 2021 – Project Operationsi lihtjuurutamine
description: See teema annab teavet Project Operationsi lihtjuurutamise 2021. a aprilli väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd6fbe8d75fbe9157a97d2edd38d40a97395c924
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868033"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Mis on uut aprillis 2021 – Project Operationsi lihtjuurutamine

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

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
