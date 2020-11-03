---
title: Peamised mõisted – projektilepingud
description: Selles teemas antakse teavet projektilepingute peamiste mõistete kohta Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4ab43a9de6b27f0f0e9b8cbe6ea8b613ce81e08d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074892"
---
# <a name="key-concepts---project-contracts"></a>Peamised mõisted – projektilepingud

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet põhimõistete kohta, millele enne Dynamics 365 Project Operationsis projekti lepingu kasutamist tähelepanu pöörata.

## <a name="owning-company"></a>Omanikust ettevõte

Omanikust ettevõte on juriidiline olem rakenduse Dynamics 365 Finance Project Operationsi moodulis **Projektide haldamine ja raamatupidamine**. Omanikust ettevõte esindab juriidilist olemit, mis arvestab tehinguga seotud kulu ja tulu.

## <a name="contracting-unit"></a>Lepingut sõlmiv üksus

Lepingut sõlmiv üksus esindab allüksust või praktikat, millele kuulub projekti kättetoimetamine. Saate seadistada ressursi kulud iga lepingut sõlmiva üksuse jaoks. Kui määrate ressursi jaoks ressursi kulu, saate ressursside jaoks seadistada ka erinevaid kulumäärasid. See lepinguosaline laenab need ressursid ettevõtte muudest allüksustest või tavadest. Ressursside kulumääradele viidatakse kui üleviidud hindadele, ressurssi laenamisele või hindade vahetamisele. Kui seadistate teistest allüksustest ressursside laenamise kulumäärad, kasutage laenava allüksuse valuutat.

## <a name="cost-currency"></a>Kulu valuuta

Kulu valuuta on valuuta, milles kulud ekraanil aruandesse lisatakse. See valuuta tuletatakse lepingu ja projekti väljale **Lepingut sõlmiv üksus** lisatud valuutast. Kulusid saab projektis registreerida mis tahes valuutas. Siiski konverteeritakse valuuta sellest valuutast, milles kulud registreeriti, projekti kulu valuutasse, kui seda ekraanil kuvatakse.

Kuna rakenduse Common Data Service (CDS) platvormi valuutakursid võivad olla kuupäevapõhised, võivad ekraanil kuvatavad kulude kogusummad aja jooksul muutuda, kui värskendate valuutakursse. Siiski jäävad andmebaasi salvestatud kulud muutumatuks, kuna summad salvestatakse selles valuutas, milles need tekkisid.

## <a name="sales-currency"></a>Müügi valuuta

Project Operationsi müügi valuutaks on see valuuta, milles registreeritakse ja kuvatakse prognoositud ja tegelikke müügi summasid. Müügi valuuta on ka valuuta, mis on kliendile tehingu eest esitataval arvel. Projekti lepingus saadakse müügi valuuta vaikimisi kliendi või konto kirjest ja seda saab lepingu loomisel muuta. Kui leping on loodud, sulgedes hinnapakkumise võidetud kujul, määratakse lepingu valuuta vaikimisi hinnapakkumise valuutast.

Kui loote projekti lepingu nullist, ei saa välja **Müügi valuuta** redigeerida. Toote ja projekti hinnakirja vaikeväärtused põhinevad lepingu valuutal.

Erinevalt kuludest saab müügi väärtusi kirjendada ainult müügi valuutas.

## <a name="billing-method"></a>Arveldusmeetod

Projektidel on tavaliselt kahte tüüpi lepingumudeleid, fikseeritud tasul ja tarbimisel põhinevad. Need mudelid on olemas rakenduses Project Operations kui kahe võimaliku väärtusega arveldusmeetodid.

- Aeg ja materjal: tarbimisel põhinev lepingumudel, kus iga tekkinud kulu on tagatud vastava tuluga. Kui prognoosite või kannate rohkem kulusid, tõuseb ka vastab prognoositav ja tegeliku müük. Määrake piirangud, mida ei tohi ületada, lepinguridadele, millel on see arveldusmeetod, mis piirab tegelikku tulu. Mitte ületatavad piirangud ei mõjuta prognoositavat tulu.
- Fikseeritud hind: fikseeritud tasuga lepingumudel, mis näitab, et müügi väärtus ei sõltu tekkinud kuludest. Müügiväärtus on fikseeritud ja ei muutu, kui prognoosite või kannate rohkem kulusid.

## <a name="project-price-lists"></a>Projekti hinnakirjad

Projekti hinnakirjasid kasutatakse aja, kulu ja muude projektiga seotud komponentide hindade vaikeväärtuste, mitte kulumäärade, määramiseks. Võib olla mitu hinnakirja. Igal hinnakirjal on iga projekti lepingu jaoks oma kehtiv kuupäev. Project Operationsis ei toetata projekti hinnakirjadel kehtivate kuupäevade kattumist.

Kui projekti leping luuakse projekti hinnapakkumise võitmise teel, kopeeritakse projekti hinnakirjad koos lepingu nime ja kuupäevaga. Selle teabe kopeerimine kujutab projekti komponentide kohandatud hinnakujundust selle projekti lepingule.

## <a name="transaction-classes"></a>Tehingu klassid

Project Operations toetab nelja tüüpi kandeklasse.

- Aeg
- Kulu
- Materjal
- Tasu

Kulu ja müügi väärtusi saab prognoosida ja kanda aja, kulu ja materjali kandeklassides. Tasu on tehingute ainult tulu klass.

## <a name="work-entities-and-billing-entities"></a>Töö olemid ja arveldamise olemid

Tööd esindavad olemid on projektid ja tööülesanded. Arveldamise aspekte esindavad olemid on lepinguread. Saate siduda erinevad tööolemid arveldussuvanditega, sidudes need lepinguridadega.

## <a name="multi-customer-deals"></a>Mitme kliendiga tehingud

Mitme kliendiga seotud tehingute puhul esitatakse arve rohkem kui ühele kliendile. Selle levinud näited on järgmised.

- OEM ettevõtted ja nende partnerid: partnerid ja edasimüüjad müüvad toodet mõne lisandväärtusega teenusega, mis tavaliselt hõlmavad teatud tehingut kliendiga. OEM pakub osa projekti rahastamiseks. 

- Avaliku sektori projektid: mitmed kohaliku omavalitsuse osakonnad lepivad kokku projekti rahastamises ja arveldatakse vastavalt varem kokkulepitud jagamisele. Näiteks lepivad kooli linnaosa ja kohalik omavalitsus kokku ujula ehitamise rahastamises.

## <a name="invoice-schedules"></a>Arve ajakavad

Arve ajakavad on iga lepingurea jaoks konkreetsed ja need on vajalikud automaatse arveldamise toimimiseks. Arve ajakavad luuakse vastavalt teatud algus- ja lõppkuupäevadele ja arve sagedusele. Ajakavasid kasutatakse lepingu etapis, kus konfigureeritakse automaatne arve loomise protsessi. Kui projekti leping luuakse hinnapakkumisest, kopeeritakse arve ajakava projekti lepingusse hinnapakkumisest.

## <a name="changes-from-dynamics-365-sales-orders"></a>Dynamics 365 Salesi tellimuste muudatused

Project Operationsi lepingud on koostatud Dynamics 365 Salesi tellimustele. Siiski on funktsionaalsuses olulisi kõrvalekaldeid ja erinevusi. Lepingutel on nende oma vorm ja kasutajaliidese elemendid, ärireeglid, äriloogika lisandmoodulid ja kliendipoolsed skriptid, mis muudavad need tellimustest erinevaks. Neil põhjustel ärge kasutage müügitellimust ja Project Operationsi lepingut vaheldumisi.