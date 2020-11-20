---
title: Projekti hinnapakkumise sätted
description: Selles teemas kirjeldatakse teavet ja sätteid, mis rakenduvad projekti hinnapakkumistele ja neiud mõjutavad.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d5a49febf02310f1e6c26798fc0ba1aa3b8d1f1
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180232"
---
# <a name="project-quote-settings"></a>Projekti hinnapakkumise sätted

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Selles artiklis kirjeldatakse projekti hinnapakkumisega seotud teavet. See hõlmab kõiki hinnapakkumise ridu mõjutavaid sätteid ja hinnapakkumise teavet, mis on summeritud kõigi reaüksuste lõikes, et juhtida projekti hinnapakkumise KPI-sid.

Järgmises tabelis on toodud projekti hinnapakkumise kokkuvõtva teabe väljad, mis esinevad vaid Dynamics 365 Project Operationsi korral või mille käitumine erineb oluliselt Dynamics 365 Salesi hinnapakkumistest.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Tüüp | Vahekaart Kokkuvõte (peidetud) | Sellel suvandikomplekti väljal on järgmised suvandid.</br>- Tööpõhine (saadaval ainult juhul, kui Project Operations on installitud)</br>- Kaubapõhine (saadaval ainult juhul, kui Project Operations ja Sales on installitud)</br>- Hoolduspõhine teenindus (saadaval juhul, kui Dynamics 365 Field Service on installitud) | Kui kasutate rakendust Project Operations, seatakse selle välja väärtuseks automaatselt **Tööpõhine**. See liigitab hinnapakkumise projektipõhiseks hinnapakkumiseks. Hinnapakkumine peaks olema projektipõhine, et võimaldada kõiki projektipõhiseid laiendusi ja funkstionaalsusi. |
| Omanikust ettevõte | Kokkuvõte | Juriidiline olem, mis arvestab selle hinnapakkumisega seotud projekti või projektide viidatud kulude ja tuluga. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. | Omanikust ettevõte võrdub juriidilise isiku mõistega Project Operationsi moodulis **Projektide haldamine ja raamatupidamine**. Kõik sellest projektist tulenevad kulud ja tulud arvestatakse omanikust ettevõtte pearaamatus. |
| Potentsiaalne klient | Vahekaart Kokkuvõte | Viide kliendi ettevõttele või konto kirjele. Kehtiv klient, kellele viidatakse projekti hinnapakkumises, peab olema seadistatud kliendina hinnapakkumise omanikust ettevõttes. Omanikust ettevõte kuvab juriidiliste olemite loendit ja need on seadistatud Project Operationsi moodulis **Projektide haldamine ja raamatupidamine**. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. | Projekti hinnapakkumise valuuta põhineb vaikimisi kliendi valuutal. Seda saab aga enne hinnapakkumise salvestamist muuta. |
| Kontohaldur | Vahekaart Kokkuvõte | Selle tehingu kontohalduri nimi. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. | Kontohaldur vastutab kuni selle projekti lõpuleviimiseni kliendisuhete haldamise eest. Vastavalt kontohalduriga seotud broneeritud ressursi kirjele on lepingut sõlmiv üksus vaikimisi projekti hinnapakkumises.|
| Lepingut sõlmiv üksus | Vahekaart Kokkuvõte | Organisatsiooniüksus, mis vastutab selle hinnapakkumisega seotud projekti või projektide kättetoimetamise eest. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. | Lepingut sõlmiv üksus on ettevõtte see allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepingut sõlmival üksusel on valuuta ja seda valuutat kasutatakse prognoositavate ja tegelike projekti täitmise käigus tekkinud kulude aruandluseks. |
| Toote hinnakiri | Vahekaart Kokkuvõte | See on hinnakiri, mida kasutatakse toodetel põhinevate hinnapakkumise ridade korral vaikehindadena. Selle välja suvandite loendis kuvatakse hinnakirjade loendit, kus hinnakirja valuuta vastab hinnapakkumise valuutale. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. See müügivõimaluse väli saadakse vaikimisi kontokirjest, kuid seda saab muuta. | Kui hinnapakkumine võidetakse, kopeeritakse välja väärtus loodavasse projekti lepingusse. |
| Valuuta | Vahekaart Kokkuvõte | See näitab valuutat, mida kasutatakse selle tehingu väärtuse aruandluseks. See on ka valuuta, milles kliendile tehingu võitmisel arve esitatakse. Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. See müügivõimaluse väli saadakse vaikimisi kontokirjest, kuid kasutaja saab seda muuta.  | Pärast hinnapakkumise salvestamist ei saa seda välja enam redigeerida. Seda kasutatakse hinnapakkumisel toote ja projekti hinnakirja vaikeväärtuste saamiseks. Hinnapakkumise valuutat kasutatakse hinnakirja valuutana. |
| Mitteületatav limiit | Vahekaart Kokkuvõte | See näitab lõpliku väärtuse läbiräägitud ülempiiri, millega klient selle tehingu juures nõustub. | Seda ülempiiri hinnatakse täitmise ajal ja seda rakendatakse kõigi selle tehinguga seostatud reaüksuste ja projektide suhtes. |
| Nõutud kättetoimetamiskuupäev | Vahekaart Kokkuvõte | Müügivõimaluse põhjal loodud hinnapakkumises kopeeritakse see väli müügivõimaluse vastavalt väljalt. | Seda kuupäeva kasutatakse arve ajakavade loomise lõppkuupäevana. |

Allpool on toodud projekti hinnapakkumises saadaolevad vahekaardid ja KPI-d, mis on Project Operationsi jaoks kordumatud või millel on olulised erinevused Salesi hinnapakkumiste käitumisest.

| **Väli** | **Asukoht** | **Kirjeldus** |
| --- | --- | --- |
| Kasumlikkuse analüüs | Hinnapakkumise vahekaart | Vahekaart kuvab järgmisi mõõdikud.</br>- Arveldatav kulu kokku</br></br>- Mittearveldatav kulu kokku</br>- Kogutulu</br>- Kogutulu (alus)</br>- Kogutulu</br>- Korrigeeritud kogutulu|
| Võrdlus kliendi ootustega | Hinnapakkumise vahekaart | See vahekaart kuvab järgmisi mõõdikud.</br>- Eeldatav lõpetamine</br>- Nõutav lõpetamine</br>- Kliendi eelarve</br>- Hinnapakkumise väärtus |
| Hinnapakkumise analüüs | Hinnapakkumise vahekaart | See vahekaart võtab kokku järgmised projekti hinnapakkumise KPI-d</br>- Võrdlus kliendi ootustega eelarve ja ajakava suhtes</br>- Kogutulu</br>- Korrigeeritud kogutulu |
