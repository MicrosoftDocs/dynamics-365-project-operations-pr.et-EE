---
title: Ajakirje kasutajaliidese käitumine
description: Selles teemas antakse teavet kasutajaliidese käitumist ajakirjega.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961699"
---
# <a name="time-entry-ui-behavior"></a>Ajakirje kasutajaliidese käitumine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Ruudustik **Iganädalane ajakirje** on kohandatud juhtelement, millel on kaks peamist jaotist: **Dimensioonid** ja **Kestus**.

## <a name="dimensions"></a>Mõõtmed
Jaotis **Dimensioonid** kuvab neid dimensioone, mille suhtes saab aega sisestada. Valmiskujul toetatakse järgmisi dimensioone.

  - Project
  - Projekti ülesanne
  - Roll
  - Tüüp
  - Kirje olek

Jaotis **Dimensioonid** ei võimalda tekstisisest redigeerimist. Seda jaotist toetab vaade, mis võimaldab lisada kohandatud välju iganädalase ajakirje ruudustikku.

## <a name="duration"></a>Kestus
Jaotises Kestus kuvatakse nädalapäevad veerupäistena. Selles jaotises lubatakse tekstisisest redigeerimist. Pärast sobivate dimensioonidega ajakirje rea loomist saavad kasutajad kiiresti sisestada aja, mis nad nendele dimensioonidele kulutasid.

## <a name="create-a-new-time-entry"></a>Uue ajakirje loomine

1. Valige ajakirje ruudustikust **Uus**. 
2. Valige ajakirje kuupäev dialoogiaknas **Ajakirje kiirloomine**.
3. Sisestage andmed dimensioonidele **Projekt**, **Projekti tööülesanne**, **Roll** ja **Kestus**. See teave tuleb lisada minutites, tundides või päevadel, tippides koos numbriga kas **h**, **m** või **p**. 
4. Sisestage kirje kirjeldus ja mistahes kommentaarid, mida võib ajakirje kohta väliselt jagada. 

Kirje salvestamisel kuvatakse sisestatud väärtused jaotises **Dimensioonid**. Väljale **Kestus** sisestatud teave kuvatakse kuupäeval, mille jaoks ajakirje loodi.

Süsteemivaated toetavad otsinguvälju. Näiteks kui kasutaja siseneb projekti, seatakse välja **Projekti ülesanne** vaikimisi väärtuseks vaade **Koopia**. Kui soovite luua ajakirjeid selliste ülesannete jaoks, mis pole kasutajale määratud, klõpsake otsingu dialoogikastis valikut **Muuda vaadet** ja seejärel valige vaade **Kõik aktiivsed projektiülesanded**.

## <a name="edit-a-time-entry"></a>Ajakirje redigeerimine 
Mõne ajakirjete lehel oleva välja üksikasju, näiteks **kirjeldust** ja **väliseid kommentaare**, ei kuvata iganädalase ajakirje ruudustikus. Selle asemel ilmub nendesse **Kestuse** lahtritesse, millel on need täiendavad andmed olemas, väike kolmnurkne tähis. 

1. Ajakirje redigeerimiseks valige lahter, mida soovite ajakirjes värskendada.
2. Valige **Üksikasjade redigeerimine**, et värskendada paani **Ajakirje põhivorm** andmeid. 

## <a name="copy-a-time-entry-row"></a>Ajakirje rea kopeerimine
Kui rida on loodud, saate kogu rea uude ritta kopeerimiseks klõpsata valikut **Kopeeri rida**. Kui rida kopeeritakse sel viisil, kopeeritakse ka dimensioonid ja kestused. Saate klõpsata ka valikut **Redigeeri rida**, et värskendada jaotises **Kestus** tekstisiseseid dimensiooniväärtusi ja kestusi.

## <a name="open-a-time-entry-behavior"></a>Ajakirje käitumise avamine
Selleks et toetada optimaalset ja kiirsisestust kõige olulisemates väljades, kuvatakse iganädalase ajakirje ruudustikus valitud dimensioonide ning ajaliste kestuste alamhulk. Ühe ajakirje kõigi üksikasjade vaatamiseks klõpsake suvandi **Redigeeri kirjet** alt käsku **Ava**.

## <a name="submit-a-time-entry"></a>Ajakirje esitamine
Saate esitada ühe ajakirje või ajakirjete rühma, valides lahtriploki või terve ajakirje rea ning seejärel käsku **Esita**. Esitatud ajakirjed kuvatakse kirjetena, mis on kinnitajate **kinnitamise** lehel kinnitamise ootel. Kui ajakirjed on edukalt esitatud, ei saa neid enam redigeerida.

## <a name="recall-a-time-entry"></a>Ajakirje tagasivõtmine
Saate esitatud ajakirjeid tagasi võtta. Saate tagasi võtta ühe ajakirje, ajakirjete ploki või terve ajakirjete rea. Tagasikutsutud ajakirjeid saab redigeerida.

## <a name="time-entry-status"></a>Ajakirje olek

- **Mustand**: uute ajakirjete olekuks määratakse automaatselt **Mustand**. Kustutada saab ainult neid ajakirjeid, mille olek on **Mustand**.
- **Esitatud**: Kui ajakirje on esitatud, värskendatakse selle olek olekuks **Esitatud**. 
- **Kinnitatud**: Kui esitatud ajakirje on kinnitatud, värskendatakse selle olek olekuks **Kinnitatud**. 
- **Tagastatud**: Kui esitatud ajakirje on tagasi lükatud, värskendatakse selle olek olekuks **Tagastatud**, ja kirjet saab parandada ning uuesti esitada. 

## <a name="view-rejection-comments"></a>Tagasilükkamise kommentaaride vaatamine
Kui kinnitaja lükkab ajakirje tagasi, võib kinnitaja lisada kommentaarid, mis aitavad ressursil tagasilükkamise põhjust mõista. Ajakirje tagasilükkamise kommentaaride vaatamiseks klõpsake valikut **Ava kirje**. Tagasilükkamise kommentaarid kuvatakse ajaskaalal. Kasutaja saab tagasilükkamise kommentaaridele vastata enne kirje uuesti esitamist.

## <a name="copy-week"></a>Nädala kopeerimine
Pärast paari ajakirje loomist saavad kasutajad korraga luua mitu ajakirjet.

1. Valige vormil **Ajakirjed** suvand **Kopeeri nädal**, et luua hulgi täiendavaid ajakirjeid. 
2. Ajakirjete kopeerimiseks kuupäevavahemiku määratlemiseks kasutage dialoogiaknas **Kopeeri** jaotises **Perioodist** välju **Alguskuupäev** ja **Lõppkuupäev**. 
3. Määrake jaotise **Perioodi lõpp** väljal **Alguskuupäev** kuupäev, mille jaoks soovite ajakirjeid luua. 
4. Valige **Kopeeri**. Välja **Perioodini** määratud kuupäeva jaoks luuakse väljal **Perioodist** oleva vastava nädalapäeva ajakirjete koopia. Näiteks viimase nädala esmaspäeva ajakirje kopeeritakse selle nädala esmaspäeva, mis on määratud väljal **Perioodini**.

## <a name="import"></a>Import
Sama tavalist protsessi kasutatakse ka broneeringutest, määramistest ja vahetustest importimisel. Saate määrata imporditavate broneeringute kuupäevavahemiku ja seejärel eraldi valida broneeringud, mis tuleks kopeerida ajakirjete mustanditesse. 
