---
title: Projekti lepingu sätted
description: See artikkel kirjeldab välju, mis mõjutavad lepinguridu ja annab lepingu kohta teavet, mis summeeritakse kõigist reaüksustest.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c3317eb36a98e14074fb504cfac5ff6e25fa3a0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921573"
---
# <a name="header-details-for-project-based-contracts"></a>Projektipõhiste lepingute päise üksikasjad

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel kirjeldab välju, mis rakenduvad kogu projekti lepingule, sh kõiki lepinguridu mõjutavaid sätteid. Kaasatakse ka teave lepingu kohta, mis on võetud kokku kõigist reaüksustest, et juhtida projekti lepingu KPI-sid.

Järgmises tabelis on esitatud projektilepingu väljad, mis on rakendusele Dynamics 365 Project Operations kordumatud või mille käitumises on tehtud võrreldes rakendusega Dynamics 365 Sales olulisi muudatusi.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| Tüüp | Vahekaart **Kokkuvõte** (peidetud) | See on järgmiste suvanditega suvandikomplekti väli.</br>- **Tööpõhine** (saadaval ainult juhul, kui Project Operations on installitud)</br>- **Kaubapõhine** (saadaval ainult juhul, kui Project Operations ja Sales on installitud)</br>- **Hoolduspõhine teenindus** (saadaval juhul, kui Dynamics 365 Field Service on installitud) | Project Operationsis on selle välja väärtuseks vaikimisi **Tööpõhine** ja leping klassifitseerub projektipõhiseks lepinguks. Leping peaks olema projektipõhine, et võimaldada kõiki projektipõhiseid laiendusi ja funktsionaalsusi. |
| Omanikust ettevõte | Vahekaart **Kokkuvõte** | Juriidiline olem, mis arvestab selle projekti lepinguga seotud projektide viidatud kulude ja tuluga. Kui leping luuakse hinnapakkumisest, kopeeritakse see väli hinnapakkumise kirje vastavalt väljalt. | Omanikust ettevõte võrdub juriidilise isiku mõistega Project Operationsi moodulis **Projektide haldamine ja raamatupidamine**. Kõik sellest projektist tulenevad kulud ja tulud arvestatakse omanikust ettevõtte pearaamatus. |
| Klient | Vahekaart **Kokkuvõte** | Viide kliendi ettevõttele või konto kirjele. Kui leping luuakse hinnapakkumisest, kopeeritakse see väli hinnapakkumise kirje vastavalt väljalt. | Projekti lepingu valuuta põhineb vaikimisi kliendi valuutal. Valuutat saab aga enne lepingu salvestamist muuta. |
| Kontohaldur | Vahekaart **Kokkuvõte** | Selle tehingu kontohalduri nimi. Kui leping luuakse hinnapakkumisest, kopeeritakse see väli hinnapakkumise kirje vastavalt väljalt. | Kontohaldur vastutab kuni selle projekti lõpuleviimiseni kliendisuhete haldamise eest. Vastavalt kontohalduriga seotud broneeritud ressursi kirjele on lepingut sõlmiv üksus vaikimisi projekti lepingus. |
| Lepingut sõlmiv üksus | Vahekaart **Kokkuvõte** | Organisatsiooniüksus, mis vastutab selle lepinguga seotud projektide kättetoimetamise eest. Kui leping luuakse hinnapakkumisest, kopeeritakse see väli hinnapakkumise kirje vastavalt väljalt. | Lepinguüksus on ettevõtte allüksus, kes projektid teostab. Igal lepingut sõlmival üksusel on valuuta ja seda valuutat kasutatakse prognoositavate ja tegelike projekti käigus tekkinud kulude aruandluseks. |
| Toote hinnakiri | Vahekaart **Kokkuvõte** | Seda hinnakirja kasutatakse toodetel põhinevate lepinguridade korral vaikehindadena. Selle välja suvandite ripploendis kuvatakse hinnakirjade loendit, kus hinnakirja valuuta vastab lepingu valuutale. Kui leping luuakse hinnapakkumisest, kopeeritakse see väli hinnapakkumise kirje vastavalt väljalt. Projekti lepingul saadakse see väli vaikimisi konto kirjest, kuid seda saab muuta. | Selle välja jaoks puudub allavoolu asjakohasus. |
| Valuuta | Vahekaart **Kokkuvõte** | Valuuta, mida kasutatakse selle tehingu väärtuse aruandluseks ja valuuta, milles kliendiga arveldatakse. Kui leping luuakse hinnapakkumisest, kopeeritakse see väli hinnapakkumise kirje vastavalt väljalt. Projekti lepingul saadakse see väli vaikimisi konto kirjest, kuid seda saab muuta. | Pärast lepingu salvestamist ei saa seda välja enam redigeerida. Seda välja kasutatakse lepingul toote ja projekti hinnakirja vaikeväärtuste saamiseks. Lepingu valuutat kasutatakse hinnakirja valuuta vastendamiseks. |
| Mitteületatav limiit | Vahekaart **Kokkuvõte** | See väli näitab lõpliku väärtuse läbiräägitud ülempiiri, millega klient selle tehingu juures nõustunud on. | Seda ülempiiri hinnatakse täitmise ajal ja seda rakendatakse kõigi selle tehinguga seostatud reaüksuste ja projektide suhtes. |
| Soovitud tarnekuupäev | Vahekaart **Kokkuvõte** | Kui leping luuakse projekti hinnapakkumisest, kopeeritakse see väli projekti hinnapakkumise vastavalt väljalt. | Seda kuupäeva kasutatakse arve ajakavade loomise lõppkuupäevana. |

Järgmised KPI-d on saadaval projekti lepingu vahekaardil **Lepingu täitmine**.

| Väli | Asukoht | Kirjeldus |
| --- | --- | --- |
| Lepingu väärtus | Üldine leping | Projekti lepingu koguväärtus. |
| Arveldatud summa | Üldine leping | Selle lepingu kõigi arvete summa. |
| Tekkinud kulu | Üldine leping | Kõigi lepingule vastendatud projektidele logitud tegelike kulude summa. |
| Kogutulu | Üldine leping | Arveldatud summa - seni kantud kulu/arveldatud summa |
| Eeldatav marginaal | Üldine leping | (Lepingu väärtus – prognoositavad kulud)/lepingu väärtus Prognoositavad kulud = kõigi lepinguga vastendatud projektide prognoositud kulude summa.|
| Lepingu väärtus | Projektipõhised read | Lepingurea väärtus. |
| Arveldatud summa | Projektipõhised read | Fikseeritud hinnaga lepingurea puhul: kõigi selle lepingu jaoks loodud selle lepingurea arveldatud müügi verstapostide tegelike näitajate summa. Aja ja materjali lepingurea puhul: kõigi tasutavate arveldatud müügi summade summa vastavalt sellele lepingureale selle lepingu jaoks loodud erinevatel arvetel. |
| Tekkinud kulu | Projektipõhised read | Kõigi lepingureale vastendatud projektidele logitud tegelike kulude summa. |
| Kogutulu | Projektipõhised read | (Arveldatud summa - seni kantud kulu)/arveldatud summa |
| Eeldatav marginaal | Projektipõhised read | (Lepingurea summa põhivaluutas - lepingurea eeldatav kulu baasvaluutas)/lepingurea summa baasvaluutas |
| Tekkinud kulu | Projektipõhise rea üksikasjad | Aeg: lepingureale vastendatud projekti sellele rollile logitud tegeliku ajakulu summa. Kulud: lepingureale vastendatud projekti sellele kategooriale logitud kõigi tegelike kulude summa. |
| Logitud kogus | Projektipõhise rea üksikasjad | Aeg: sellele lepingureale vastendatud projekti rolli kogu tegeliku ajakulu summa. Kulud: lepingureale vastendatud projekti tegelike kulude kulu kategooria kõik kogused. |
| Arveldatud summa | Projektipõhise rea üksikasjad | Fikseeritud hinnaga lepingurea korral on see väli üksikasjade tasemel tühjaks jäetud ja seda kuvatakse ainult lepingurea tasemel. Aja- ja materjalikulu lepingurea puhul täidetakse arvutused üksikasjade tasemel. Üksikasjad näitavad selle lepingurea tasustatavat kõigi arveldatud tuluridade summat. |
| Arveldatud kogus | Projektipõhise rea üksikasjad | Fikseeritud hinnaga lepingurea korral on see väli üksikasjade tasemel tühjaks jäetud ja seda kuvatakse ainult lepingurea tasemel. Aja- ja materjalikulu lepingurea puhul täidetakse arvutused aja ja kulude kohta üksikasjade tasemel. Aeg: Selle rolli arveldatavate tuluridade selle lepingurea tasustatavate tundide summa . Kulud: lepingureale vastendatud projekti tegelike kulude kulu kategooria kõik kogused. |
| Lepingu väärtus | Tootepõhised read | Selle tootepõhise lepingurea lepingurea väärtus. |
| Arveldatud summa | Tootepõhised read | Kõigi nende arve ridade summade summa, mis on seotud selle lepingu jaoks loodavate erinevate arvetega. |
| Tekkinud kulu | Tootepõhised read | Kõigi tootepõhise lepingurea jaoks logitud tegelike kulude summa. |
| Kogutulu | Projektipõhised read | Arveldatud summa - seni kantud kulu/arveldatud summa |
| Eeldatav marginaal | Tootepõhised read | (Lepingurea väärtus - lepingurea prognoositavad kulud) / lepingurea väärtus |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
