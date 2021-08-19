---
title: Mis on uut mais 2021 – Project Operationsi lihtjuurutamine
description: See teema annab teavet Project Operationsi lihtjuurutamise 2021. a mai väljalaskes saadaolevate kvaliteedivärskenduste kohta.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 14ff7f1f7374ffe885c511fd693cda5b7023c5beb53adb45042ddda1e932c93d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005971"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Mis on uut mais 2021 – Project Operationsi lihtjuurutamine

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See teema kehtib rakenduse Dynamics 365 Project Operations järgmistele komponentide ja versioonide kohta.

   - Project Operations Dataverse’i keskkonna versioonis 4.10.0.186.

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

Selles väljaandes sisalduvad järgmised funktsioonid.

- [Ajastamisrežiimid](../../project-management/scheduling-modes.md): projektijuhid saavad nüüd määratleda, kas projekti tuleks hallata fikseeritud kestuse, fikseeritud töö või fikseeritud ühikute ajastamisrežiimis.

## <a name="quality-updates"></a>Kvaliteedi värskendused

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2224568 | Lisatud on loogika, et lubada kohandused, mis hõlmavad arve kinnitamise lisandmooduli käivitamist. |
| Arveldamine ja hinnakujundus | 2101098 | Täiustatud on näidisarvete vaikeväljade loogikat. Nende väljade hulka kuuluvad **Maksja aadress**, **Maksja nimi** ja **Maksetingimused**. Väljade väärtused tulevad nüüd vaikimisi vastava projekti lepingu kliendikirjest. |
| Arveldamine ja hinnakujundus | 2021413 | Väljasid **Tegeliku kulu** ja **Müük** uuendati olemis **Ülesanne**, et kaasata ülesande arveldamata ja arveldatud kulude müügiväärtus. |
| Arveldamine ja hinnakujundus | 2182110 | Projektilepingu kopeerimisel luuakse lepingurea ID sihtprojekti lepingus, et tagada selle kordumatus. |
| Müügivõimaluse haldus | 2186741 | Lisatud valideerimised tagamaks, et olemasoleva hinnapakkumise rea üksikasjades ei saaks välja **Päritolu** ega tehingu tüüpi värskendada. |
| Müügivõimaluse haldus | 2191353 | Vahe-eesmärgi loomist ei tohi aja ja materjali lepingureal lubada. |
| Müügivõimaluse haldus | 2216956 | Lahendati probleem suvandiga **Värskenda hindu**. |
| Plaanimine ja jälgimine | 2182979 | Projekti kopeerimise funktsiooni on täiustatud, et tagada kuluprognoosi ridade kopeerimine algsest projektist. |
| Plaanimine ja jälgimine | 2184144 | Projekti kopeerimise funktsiooni on täiustatud, et tagada ressursi positsiooni nime kopeerimine algsest projektist. |
| Plaanimine ja jälgimine | 2184799 | Tihendati kontrolli projekti kopeerimisel tagamaks, et hinnangulist alguskuupäeva ei saaks poolelioleva kopeerimise ajal muuta. |
| Plaanimine ja jälgimine | 2185134 | Projekti kopeerimise ajal on sihtprojekti eeldatavaks alguskuupäevaks seatud tänane kuupäev. |
| Plaanimine ja jälgimine | 2196373 | Veenduge, et projektijuhi ja meeskonnaliikme kirjeid ei oleks projekti kopeerimisel projektimeeskonnas dubleeritud. |
| Plaanimine ja jälgimine | 2211833 | Ressursi määramised kopeeritakse lähteprojekti tööülesandest sihtprojekti. |
| Plaanimine ja jälgimine | 2186541 | Parandati probleem suvandi **Ressurss** rühmitamise ajal ruudustikus **Prognoosid**. |
| Plaanimine ja jälgimine | 2166906 | Ülesande tehingu kategooria tuleb kopeerida olemisse **Ressursi määramine**. |
| Ressursihaldus | 2125362 | Lahendati probleemid üldise meeskonnaliikme loomisega tunnipõhist jaotamismeetodit kasutades. |
| Aeg ja kulu | 2113603 | Parandati kohandamisega seotud probleem koos atribuutide eemaldamisega lehelt **Ajakirje**. Süsteem kontrollib enne atribuudile skripti abil juurde pääsemist, kas atribuut on lehel olemas. |
| Aeg ja kulu | 2204377 | Kopeeritud ajatabelid peavad olema automaatselt kuvatud, kui valite suvandi **Kopeeri nädal**. |
| Aeg ja kulu | 2209059 | Väli **Olek** on rakenduse Dynamics 365 Field Service ajakirjete jaoks muudetav. |
