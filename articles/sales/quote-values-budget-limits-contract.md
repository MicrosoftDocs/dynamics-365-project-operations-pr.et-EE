---
title: Projektipõhiste hinnapakkumiste päise üksikasjad
description: See artikkel kirjeldab teavet ja sätteid, mis rakenduvad projekti hinnapakkumistele ja neid mõjutavad.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7e2b625476508d781b9f3f2440cde1f7374372c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825215"
---
# <a name="header-details-for-project-based-quotes"></a>Projektipõhiste hinnapakkumiste päise üksikasjad

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Selles artiklis kirjeldatakse projekti hinnapakkumisega seotud teavet. See hõlmab kõiki hinnapakkumise ridu mõjutavaid sätteid ja hinnapakkumise teavet, mis on summeritud kõigi reaüksuste lõikes, et juhtida projekti hinnapakkumise KPI-sid.

Järgmises tabelis on esitatud projekti hinnapakkumise kokkuvõtte teabe väljad, mis on rakendusele Dynamics 365 Project Operations kordumatud või mille käitumises on tehtud võrreldes rakendusega Dynamics 365 Sales olulisi muudatusi.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
