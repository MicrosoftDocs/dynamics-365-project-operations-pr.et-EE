---
title: Hinnapakkumised – põhimõisted – liht
description: Selles teemas kirjeldatakse projekti hinnapakkumiste kasutamist Project Operationsis.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009436"
---
# <a name="concepts-unique-to-project-quotes"></a>Projekti hinnapakkumiste kordumatud mõisted

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Järgmised on põhimõisted, mida peate enne projekti hinnapakkumiste kasutamist rakenduses Dynamics 365 Project Operations arvesse võtma.

## <a name="contracting-unit"></a>Lepingut sõlmiv üksus

Lepingut sõlmiv üksus esindab allüksust või praktikat, millele kuulub projekti kättetoimetamine. Saate seadistada ressursi kulud iga lepingut sõlmiva üksuse jaoks. Kui määrate lepingut sõlmivas üksuse ressursile ressursi kulu, saate seadistada ka erinevaid kulumäärasid ressurssidele, millest see lepingut sõlmiv üksus laenab või teistele ettevõtte allüksustele või praktikatele. Neile viidatakse kui üleviidud hindadele, ressurssi laenamisele või hindade vahetamisele. Kui seadistate teistest allüksustest ressursside laenamise kulu, saate need kulumäärad seadistada ka laenava allüksuse valuutas.

## <a name="cost-currency"></a>Kulu valuuta

Kulu valuuta Project Operationsis on valuuta, milles kulud aruandesse lisatakse. See valuuta tuletatakse hinnapakkumise, lepingu ja projekti väljale **Lepingut sõlmiv üksus** lisatud valuutast. Kulusid saab projektis registreerida mis tahes valuutas. Siiski konverteeritakse valuuta sellest valuutast, milles kulud registreeriti, projekti kulu valuutasse.

Kuna CDS-i platvormi valuutakursid võivad olla kuupäevapõhised, võivad ekraanil kuvatavad kulude kogusummad aja jooksul muutuda, kui värskendate valuutakursse. Siiski jäävad andmebaasi salvestatud kulud muutumatuks, kuna summad salvestatakse selles valuutas, milles need tekkisid.

## <a name="sales-currency"></a>Müügi valuuta

Project Operationsi müügi valuutaks on see valuuta, milles registreeritakse ja kuvatakse prognoositud ja tegelikke müügi summasid. See on ka valuuta, mis on kliendile tehingu eest esitataval arvel. Projekti hinnapakkumises on saadakse müügi valuuta vaikimisi kliendi või konto kirjest ja seda saab hinnapakkumise loomisel muuta. Pärast hinnapakkumise salvestamist ei saa müügi valuutat muuta. Toote ja projekti hinnakirja vaikeväärtused põhinevad hinnapakkumise müügi valuutal.

Erinevalt kuludest saab müügi väärtusi kirjendada ainult müügi valuutas.

## <a name="billing-method"></a>Arveldusmeetod

Projektidel on tavaliselt fikseeritud tasul ja tarbimisel põhinevad lepingute mudelid. See on Project Operationsis esindatud kui **Arveldusmeetod** ja sellele on kaks väärtust, aeg ja materjal ning fikseeritud hind.

- **Aeg ja materjal:** see on tarbimisel põhinev lepingumudel, kus iga tekkinud kulu on tagatud vastava tuluga. Kui prognoosite või kannate rohkem kulusid, tõuseb ka vastab prognoositav ja tegeliku müük. Saate määrata mitte ületatavad piirid hinnapakkumise ridadele, millel on see arveldusmeetod. See seab tegelikule tulule piiri. Mitte ületatavad piirangud ei mõjuta prognoositavat tulu.
- **Fikseeritud hind:** see on fikseeritud tasuga lepingumudel, mis näitab, et müügi väärtus ei sõltu tekkinud kuludest. Müügiväärtus on fikseeritud ja ei muutu, kui prognoosite või kannate rohkem kulusid.

## <a name="project-price-lists"></a>Projekti hinnakirjad

Projekti hinnakirjad on hinnakirjad, mida kasutatakse aja, kulu ja muude projektiga seotud komponentide hindade vaikeväärtuste, mitte kulumäärade, määramiseks. Võib olla mitu hinnakirja ja igas hinnakirjas võivad olla iga projekti hinnapakkumise jaoks oma kehtivad kuupäevad. Project Operationsis ei toetata projekti hinnakirjadel kehtivate kuupäevade kattumist.

## <a name="product-price-lists"></a>Toote hinnakirjad

Toodete hinnakirjad on hinnakirjad, mida kasutatakse hinnapakkumise tootepõhiste ridade vaikeväärtuste, mitte kulumäärade, määramiseks. Hinnapakkumise kohta on ainult üks toodete hinnakiri.

## <a name="transaction-classes"></a>Kandeklassid

Project Operations toetab nelja tüüpi kandeklasse.

- Aeg
- Kulu
- Materjal
- Tasu

Kulu ja müügi väärtusi saab prognoosida ja kanda aja, kulu ja materjali kandeklassides. Tasu on tehingute ainult tulu klass.

## <a name="work-entities-and-billing-entities"></a>Töö olemid ja arveldamise olemid

Tööd esindavad olemid on projektid ja tööülesanded. Arveldust esindavad olemid on hinnapakkumise read ja lepinguread. Saate siduda erinevad tööolemid arveldussuvanditega, seostades need hinnapakkumise või lepingu ridadega.

## <a name="multi-customer-deals"></a>Mitme kliendiga tehingud

Mitme kliendiga seotud tehingud toimuvad juhul, kui arve esitatakse rohkem kui ühele kliendile. Selle levinud näited on järgmised.

- **OEM ettevõtted ja nende partnerid:** partnerid ja edasimüüjad müüvad lisandväärtusega teenustega toodet. See on tavaliselt stsenaarium, kui kliendiga tehtava konkreetse tehingu ajal finantseerib OEM osa projektist. 

- **Avaliku sektori projektid:** mitmed kohaliku omavalitsuse osakonnad lepivad kokku projekti rahastamises ja arveldatakse vastavalt varem kokkulepitud jagamisele. Näiteks lepivad kooli linnaosa ja linnavalitsus või kohalik omavalitsus kokku ujula ehitamise rahastamises.

## <a name="invoice-schedules"></a>Arve ajakavad

Arve ajakavad põhinevad igal hinnapakkumise real ja on ka valikulised. Arve ajakavad luuakse vastavalt teatud algus- ja lõppkuupäevadele ja arve sagedusele. Arve ajakavasid kasutatakse lepingu etapis, kus konfigureeritakse automaatne arve loomise protsessi. Hinnapakkumise etapis on ajakavad valikulised. Kui etapis **Hinnapakkumine** luuakse arve ajakavad, kopeeritakse need projekti lepingusse, mis luuakse projekti hinnapakkumise võitmisel.

## <a name="changes-from-dynamics-365-sales-quote"></a>Dynamics 365 Salesi hinnapakkumise muudatused.

Project Operationsi hinnapakkumised on ehitatud Dynamics 365 Salesi hinnapakkumistele. Siiski on funktsionaalsuse mõned olulised erinevused, mida peaksite teadma.

- Toiminguid **Muuda** ja **Aktiveeri** ei toetata.
- Project Operationsi hinnapakkumistel on kahte erinevat tüüpi ridu. Üks on projektidele ja teine on toodetele.
- Project Operationsi hinnapakkumistel on nende oma vorm ja kasutajaliidese elemendid, ärireeglid, äriloogika lisandmoodulid ja kliendipoolsed skriptid, mis muudavad need Salesi hinnapakkumistest erinevaks.

Nendel põhjustel ei soovitata kasutada Salesi hinnapakkumist ja Project Operationsi hinnapakkumist neid vahetades.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
