---
title: Projektipõhiste hinnapakkumiste kordumatud mõisted
description: Sellest artiklist leiate teavet Microsofti projektipakkumiste kohta Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824322"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Projektipõhiste hinnapakkumiste kordumatud mõisted

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Enne kui hakkate Microsoftis Dynamics 365 Project Operations projekti hinnapakkumisi kasutama, peaksite olema teadlik järgmistest põhimõistetest.

## <a name="owning-company"></a>Omanikust ettevõte

Omav ettevõte esindab juriidilist isikut, kellele kuulub projekti elluviimine. Hinnapakkumisel olev klient peaks olema finance and operationsi rakendustes selles juriidilises isikus kehtiv klient. Omanikust ettevõtte valuuta ja projektipõhisel hinnapakkumisel valitud lepinguüksuse valuuta peavad ühtima.

## <a name="contracting-unit"></a>Lepingut sõlmiv üksus

Allhankeüksus esindab allüksust või praktikat, kellele projekti elluviimine kuulub. Saate seadistada ressursi kulud iga lepingut sõlmiva üksuse jaoks. Kui määrate allhankeüksuses olevale ressursile ressursikulud, saate seadistada erinevad kulumäärad ressurssidele, millelt allhankeüksus laenab, või muudele ettevõtte allüksustele või tavadele. Neid kulumäärasid nimetatakse siirdehindadeks, ressursilaenuks või börsihindadeks. Kui seadistate teistelt osakondadelt ressursside laenamise kulu, saate seadistada kulumäärad laenudivisjoni valuutas.

## <a name="cost-currency"></a>Kulu valuuta

Project Operationsi kuluvaluuta on valuuta, milles kulusid kajastatakse. See valuuta tuletatakse valuutast, mis on lisatud **hinnapakkumise, lepingu ja projekti väljale Lepinguüksus** . Projekti kulusid saab kirjendada mis tahes valuutas. Siiski toimub valuuta konverteerimine valuutast, milles kulud kirjendati, projekti kuluvaluutasse.

Kuna platvormi vahetuskursid Dataverse ei saa olla kuupäevaliselt tõhusad, võivad valuutakursside värskendamisel ekraanil kuvatavad kulude kogusummad aja jooksul muutuda. Andmebaasis kirjendatud kulud jäävad siiski muutumatuks, sest summad salvestatakse valuutas, milles need tekkisid.

## <a name="sales-currency"></a>Müügi valuuta

Project Operationsi müügivaluuta on valuuta, milles hinnangulised ja tegelikud müügisummad registreeritakse ja kuvatakse. See on ka valuuta, milles kliendile tehingu eest arve esitatakse. Projekti hinnapakkumise puhul määratakse kliendi või konto kirjest müügi vaikevaluuta ja seda saab hinnapakkumise loomisel muuta. Müügivaluutat ei saa aga pärast hinnapakkumise salvestamist muuta. Toote ja projekti vaikehinnakirjad määratakse hinnapakkumise müügivaluuta alusel.

Erinevalt kuludest saab müügiväärtusi kirjendada **ainult** müügivaluutas.

## <a name="billing-method"></a>Arveldusmeetod

Projektidel on tavaliselt fikseeritud tasu ja tarbimispõhised lepingumudelid. Project Operationsis esindab projekti lepingupõhist mudelit arveldusmeetod. Arveldusmeetodil on kaks väärtust: aeg ja materjal ning fikseeritud hind.

- **Aeg ja materjal** - Tarbimispõhine lepingumudel, kus iga tehtud kulu on tagatud vastava tuluga. Kui prognoosite või kannate rohkem kulusid, tõuseb ka vastab prognoositav ja tegeliku müük. Saate määrata mitte ületatavad piirid hinnapakkumise ridadele, millel on see arveldusmeetod. Sel viisil saate tegelikku tulu piirata. Hinnangulisi tulusid ei mõjuta piirangud, mida ei tohi ületada.
- **Fikseeritud hind**  – fikseeritud tasuga lepingumudel, kus müügiväärtused ei sõltu tekkivatest kuludest. Müügiväärtus on fikseeritud ja ei muutu, kui prognoosite või kannate rohkem kulusid.

## <a name="project-price-lists"></a>Projekti hinnakirjad

Projekti hinnakirjad on hinnakirjad, mida kasutatakse aja, kulu ja muude projektiga seotud komponentide vaikehindade, mitte kulumäärade sisestamiseks. Võib olla mitu hinnakirja ja igas hinnakirjas võivad olla iga projekti hinnapakkumise jaoks oma kehtivad kuupäevad. Project Operations ei toeta projekti hinnakirjade kattuvat kuupäevaefekti.

## <a name="product-price-lists"></a>Toote hinnakirjad

Toote hinnakirjad on hinnakirjad, mida kasutatakse hinnapakkumise tootepõhiste ridade vaikehindade, mitte omahindade sisestamiseks. Ühe hinnapakkumise kohta on ainult üks toote hinnakiri.

## <a name="transaction-classes"></a>Kandeklassid

Project Operations toetab nelja tüüpi kandeklasse.

- Aeg
- Kulu
- Materjal
- Tasu

Soetusmaksumust ja müügiväärtusi saab hinnata ja kanda kandeklassides **Aeg**, **Kulu** ja **Materjal** . **Tasu** on ainult tuludega tehinguklass.

## <a name="work-entities-and-billing-entities"></a>Töö olemid ja arveldamise olemid

Projektid ja ülesanded on olemid, mis esindavad tööd. Hinnapakkumise read ja Lepinguread on olemid, mis tähistavad arveldamist. Saate linkida erinevad tööüksused arveldusvalikutega, seostades need hinnapakkumise ridade või lepinguridadega.

## <a name="multi-customer-deals"></a>Mitme kliendiga tehingud

Mitme kliendi tehingud toimuvad siis, kui ühe arve kohta on rohkem kui üks klient. Siin on mõned tüüpilised näited:

- **Originaalseadmete tootja (OEM) ettevõtted ja nende partnerid- Partnerid ja edasimüüjad**  müüvad toodet, mis sisaldab lisandväärtusega teenuseid. Kliendiga tehingu ajal pakub OEM tavaliselt projekti osa rahastamiseks.
- **Avaliku sektori projektid** – Kohaliku omavalitsuse mitu osakonda lepivad kokku projekti rahastamises ja nende kohta esitatakse arved vastavalt eelnevalt kokku lepitud jaotusele. Näiteks lepivad kooli linnaosa ja linnavalitsus või kohalik omavalitsus kokku ujula ehitamise rahastamises.

## <a name="invoice-schedules"></a>Arve ajakavad

Arve graafikud on igale hinnapakkumise reale omased ja valikulised. Arve graafikud luuakse konkreetsete algus- ja lõppkuupäevade ning arve sageduse põhjal. Neid kasutatakse lepingu etapis, kui automaatne arve loomise protsess on konfigureeritud. Hinnapakkumise etapis on arvegraafikud valikulised. Kui need luuakse hinnapakkumise etapis, kopeeritakse need projektilepingusse, mis luuakse projektipakkumise võitmisel.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Erinevused Dynamics 365 Salesi hinnapakkumistest

Project Operationsi hinnapakkumised põhinevad rakenduse Dynamics 365 Sales hinnapakkumistel. Siiski on funktsionaalsuse mõned olulised erinevused, mida peaksite teadma.

- Project Operationsi hinnapakkumistel on kahte tüüpi ridu: üks projektide ja teine toodete jaoks.
- Project Operationsi hinnapakkumistel on oma lehe ja kasutajaliidese (UI) elemendid, ärireeglid, lisandmoodulite äriloogika ja kliendipoolsed skriptid, mis eristavad neid müügipakkumistest.
- Rakenduses Sales saate ühele müügipakkumisele lisada mitu tellimust. Project Operationsis saate projekti hinnapakkumisele lisada ainult ühe projektilepingu.
- Kui võidate müügipakkumise, võib seotud võimalus jääda avatuks. Pärast projekti hinnapakkumise võitmist suletakse seotud müügivõimalus.
- Müügipakkumine ei sisalda mõningaid välju ja mõisteid, mida projekti hinnapakkumine sisaldab. Väljad sisaldavad järgmisi: **Hankeüksus**, **Kontohaldur** ja **Maksja: kontakti nimi**.
- Müügi- ja projektihinnapakkumised tuvastatakse väljal suvandikomplekt-põhine **tüüp** . Müügipakkumise puhul on **selle välja väärtus Kaubapõhine**. Projekti hinnapakkumise puhul on **väärtus tööpõhine**.

Nende erinevuste tõttu ei soovita me kasutada müügipakkumisi ja Project Operationsi hinnapakkumisi vaheldumisi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
