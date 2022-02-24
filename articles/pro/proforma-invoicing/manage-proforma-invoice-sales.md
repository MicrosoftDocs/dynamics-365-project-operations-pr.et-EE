---
title: Näidisarve haldamine – liht
description: Selles teemas antakse teavet näidisarvetega töötamise kohta.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cd56b99c3ed455848edbd9ff4419afa58d782a3e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181537"
---
# <a name="manage-a-proforma-invoice---lite"></a>Näidisarve haldamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations luuakse näidisarved rakenduse Dynamics 365 Sales arvete laiendusena. Samas esineb arveldamise ajal rakenduste Sales ja Project Operations arveldamise toimingus palju erinevusi. Näiteks pole rakenduses Project Operations võimalik luua lehel **Arvete loend** uut arvet, kuid rakenduses Sales on see võimalik. Need erinevused ja laiendused on olemas, et toetada arveldamistoiminguid projetides, mis erinevad tavalisest müügitellimuse arvest.

> [!IMPORTANT]
> Erinevuste tõttu ärge kasutage rakenduste Sales ja Project Operations arveid vaheldumisi.

## <a name="invoice-header"></a>Arve päis

Rakenduses Project Operations on näidisarve päises saadaval järgmine teave.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Arve ID** | Vahekaart **Kokkuvõte** | Näidisarve loomisel automaatselt genereeritav ID. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja kasutatakse iga näidisarve jaoks viitena. |
| **Nimi** | Vahekaart **Kokkuvõte** | On vaikimisi määratud projektilepingu nimele. Kasutaja saab seda välja muuta. | &nbsp;  |
| **Valuuta** | Vahekaart **Kokkuvõte** | On vaikimisi määratud projektilepingu valuutale. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |&nbsp; |
| **Hinnakiri** | Vahekaart **Kokkuvõte** | On vaikimisi määratud projektilepingu hinnakirjale. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Müügivõimalus** | Vahekaart **Kokkuvõte** | Lingitud müügivõimaluse viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp;  |
| **Leping** | Vahekaart **Kokkuvõte** | Lingitud projektilepingu viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Klient** | Vahekaart **Kokkuvõte** | Lingitud projektilepingu viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |&nbsp;  |
| **Kirjeldus** | Vahekaart **Kokkuvõte** | Arvet kirjeldav tekstiväli. Kasutaja saab seda välja muuta. | &nbsp; |
| **Maksja** ja seostuvad väljad | **Kokkuvõtte vahekaart** | Vaikeväärtused määratakse projektilepingu kliendilt. Kasutaja saab seda välja muuta.  | &nbsp; |
| **Olek** | Vahekaart **Kokkuvõte** | Määrab järgmised valikud: **Aktiivne**, **Suletud**, **Makstud** ja **Tühistatud** ning kasutaja saab neid muuta. | Project Operationsi mittetoetatavad olekud on **Suletud** ja **Tühistatud**. </br> Arve loomisel seatakse olekuks **Aktiivne**. </br>Olekuks tuleks määrata **Makstud** ainult pärast arve kinnitamist. |
| **Projektiarve olek** | Vahekaart **Kokkuvõte** | Määrab järgmised valikud: **Mustand**, **Läbivaatamisel** ja **Kinnitatud** ning kasutaja saab neid muuta. | Nii olekus **Mustand** kui ka **Läbivaatusel** saab arvet muuta. Pärast kinnitamist ei saa arvet muuta. |
| **Reasumma** | Vahekaart **Kokkuvõte** | Kõikide arveridade kogusumma pärast ettemakseid ja mahaarvamisi. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja kasutatakse lõppsumma arvutamiseks. |
| **Allahindlus (%)** | Vahekaart **Kokkuvõte** | Seda välja saab allahindlusprotsendi lisamiseks muuta. Project Operationsi funktsioonid ei toeta seda välja. | See on toetuseta väli. |
| **Allahindlussumma** | Vahekaart **Kokkuvõte** | Seda välja saab allahindluse summa lisamiseks muuta. Project Operationsi funktsioonid ei toeta seda välja. | See on toetuseta väli. |
| **Veotasueelne summa** | **Kokkuvõtte vahekaart** | Arve kogusumma pärast allahindluste rakendamist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja kasutatakse lõppsumma arvutamiseks. |
| **Veotasu summa** | Vahekaart **Kokkuvõte** | Seda välja saab veotasu summa lisamiseks muuta. Project Operationsi funktsioonid ei toeta seda välja. | See on toetuseta väli. |
| **Kogumaks** | Vahekaart **Kokkuvõte** | Arve kõikide arveridade maksu kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Pole. |
| **Kogusumma** | Vahekaart **Kokkuvõte** | Kogusumma pärast allahindlusi ja makse. | See on summa, mille klient peab maksma. |
## <a name="project-based-invoice-lines"></a>Projektipõhised arveread

Rakenduses Project Operations on iga prijekti lepingurea jaoks üks arverida. Arverida luuakse ka juhul, kui tegelikke näitajaid pole. Arvereal on näidisarve päises saadaval järgmine teave.

| Väli | Asukoht | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- | --- |
| **Arve ID** | Vahekaart **Üldine** | Viide arve ID-le. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Arve ID linki saab kasutada tagasi arve päisesse liikumiseks. |
| **Nimi** | Vahekaart **Üldine** | Arverea nimi, mis on määratud vaikimisi lepingurea nimest. Kasutaja saab seda välja muuta. | &nbsp; |
| **Project** | Vahekaart **Üldine** | Projekt seotud projekti lepingureal. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Projekti linki saab kasutada projektile navigeerimiseks. |
| **Arveldusmeetod** | Vahekaart **Üldine** | Arveldusmeetod seotud projekti lepingureal. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Lepingurea summa** | Vahekaart **Üldine** | Seotud projekti arverea lepingu summa. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Arveldatud kuupäevani** | Vahekaart **Üldine** | Arve kõigi arveridade üksikasjade kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Summa** | Vahekaart **Üldine** | Arve kõigi arveldatavate arveridade üksikasjade kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja kasutatakse arve päises lõppsumma arvutamiseks. |
| **Maks** | Vahekaart **Üldine** | Arverea kõigi arveridade üksikasjade maksude kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja kasutatakse arve päises maksu lõppsumma arvutamiseks. |
| **Laiendatud summa** | Vahekaart **Üldine** | Arverea kõigi arveldatavate arveridade üksikasjade üldine kogusumma (**maks + summad**). Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja kasutatakse arve päises lõppsumma arvutamiseks. |


## <a name="invoice-line-details"></a>Arve rea üksikasjad

Iga projekti arve arverida sisaldab arverea üksikasju. Need rea üksikasjad on seotud arveldamata müügi tegelike ja vahe-eesmärkide summaga, mis on seotud arverea viidatud lepingureaga. Kõik need tehingud on märgitud kui **Arveldamiseks valmis**.

Rea **Aja ja materjali arve** jaoks on arverea üksikasjad rühmitatud valikuteks **Arveldatav**, **Mittearveldatav** ja **Tasuta** lehel **Arverida**. **Arveldatava arverea** üksikasjad lisatakse arverea kogusummale. **Tasuta** ja **mitte-arveldatavaid tegelikke näitajaid** arverea kogusummale ei lisata.

Rea **Fikseeritud hinnaga arve** jaoks luuakse arverea üksikasjad vahe-eesmärkidest, mis on seotud arvereal märgitud kui **Arveldamiseks valmis**. Pärast seda, kui arverea üksikasjad on vahe-eesmörgi põhjal loodud, uuendatakse vahe-eesmärgi arveldamine olekule **Kliendi arve loodud**.

### <a name="edit-invoice-line-details"></a>Arve rea üksikasjade redigeerimine

Arverea üksikasjades, mida toetavad arveldamata müügi tegelikud näitajad, on saadaval järgmised väljad.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| **Arverida** | **Arverea ID** viide. Kirjutuskaitstud väli, redigeerimiseks lukus. | Seda linki saab kasutada tagasi arve päisesse liikumiseks. |
| **Kirjeldus** | Arverea üksikasjade kirjeldus. Määratakse vaikimisi väljalt **Sisemised kommentaarid** suvandis **Ajakirje** ja väljalt **Kirjeldus** suvandis **Kulukirje**. Kasutaja saab välja muuta.| &nbsp; |
| **Väline kirjeldus** | Arverea üksikasjade kirjeldus. Määratakse vaikimisi väljalt **Välised kommentaarid** suvandis **Ajakirje** ja väljalt **Kirjeldus** suvandis **Kulukirje**. Kasutaja saab välja muuta. | Seda kirjeldust saab kasutada määramaks, mis peaks olema kliendile saadetaval prinditud arvel. Rakendusel Project Operations ei ole näidisarvel kõiki nõutavaid funktsioone, et konfigureerida arve printimise seadistused. |
| **Alguskuupäev** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta. |
| **Project** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Määratakse vaikimisi seotud lepingurea projektile. |
| **Tööülesanne** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Seda välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta. Ripploendis kuvatakse kõik ülesanded, mis on projekti lepingureaga seotud.  |
| **Kande kategooria** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida tegelik allikas ei toeta. |
| **Roll** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta. |
| **Broneeritav ressurss** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida tegelik allikas ei toeta. |
| **Ressursi üksus** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta. |
| **Kogus** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta. |
| **Üksuse ajakava** | Arverea aja üksikasja puhul on see alati määratud ajale ja seda ei saa muuta. Kulude puhul on see määratud vaikimisi lähtekulu tegelikule näitajale. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | On määratud vaikimisi uue arverea üksikasjade suvandile **Aeg**, mida tegelikud näitajad ei toeta. |
| **Ühik** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta |
| **Hind** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Välja saab redigeerida uue arverea üksikasjades, mida allika tegelikud näitajad ei toeta. Kui väärtust ei sisestata, määratakse see nupu **Salvesta** valimist vaikeväärtusele. |
| **Valuuta** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Määratakse vaikimisi arve päisest, kui loote uue arve üksikasja ilma tegelike näitajate toetuseta.  Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Summa** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Arvutatakse valemiga **kogus \* hind**, kui loote uue arve üksikasja ilma tegelike näitajate toetuseta. See arvutatakse pärast nupu **Salvesta** valimist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Maks** | Määratakse vaikimisi allika tegelikust näitajast. Kasutaja saab välja muuta | Kasutaja saab välja muuta, kui loob uue arverea üksikasja ilma tegeliku näitaja toeta. |
| **Laiendatud summa** | Arvutatud väli, arvutatakse valemiga **summa + maks**. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Arveldustüüp** | Määratakse vaikimisi allika tegelikust näitajast. Kasutaja saab välja muuta. | Suvandi **Arveldatav** lisab arverea kogusummale rea. **Tasuta** ja **Mitte-arveldatav** jätavad selle arverea kogusummast välja. |
| **Kandetüüp** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | On vaikimisi määratud valikule **Arveldatud müük** ja lukustatud, kui loote uue **arverea üksikasja** ilma tegeliku näitaja toeta.  |
| **Kande klass** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Määratakse vaikimisi vastavalt sellele, kas kasutaja otsustab luua arverea üksikasja **Aeg**, **Kulu** või **Tasu**, luues samal ajal ilma tegeliku näitaja toetuseta uue **arverea üksikasja**. Redigeerimiseks lukustatud. |

Arverea üksikasjades, mida toetab vahe-eesmärk, on saadaval järgmised väljad.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| **Arverida** | **Arverea ID** viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | Linki saab kasutada tagasi arve päisesse liikumiseks. |
| **Kirjeldus** | Arverea üksikasjade kirjeldus. Määratakse vaikimisi allika vahe-eesmärgi kirjeldusest. | &nbsp; |
|**Väline kirjeldus** | Arverea üksikasjade kirjeldus, mis on vaikimisi määratud allika vahe-eesmärgi kirjeldusest. | Seda välja saab kasutada määramaks, mis peaks olema kliendile saadetaval prinditud arvel. Rakenduse Project Operations näidisarvel ei ole kõiki nõutavaid funktsioone, et konfigureerida arve printimise seadistused. |
| **Alguskuupäev** | Määratakse vaikimisi allika vahe-eesmärgi kuupäevast **Vahe-eesmärk**. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Project** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Tööülesanne** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Kande kategooria** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Roll** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Broneeritav ressurss** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Ressursi üksus** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Üksuse ajakava** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Ühik** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Hind** | Määratakse vaikimisi allika vahe-eesmärgi summast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Valuuta** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |&nbsp; |
| **Summa** | Määratakse vaikimisi allika vahe-eesmärgi summast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Maks** | Määratakse vaikimisi allika vahe-eesmärgi maksusummast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Laiendatud summa** | Määratakse vaikimisi allika vahe-eesmärgi rea summast. Kasutaja saab välja muuta | &nbsp; |
| **Arveldustüüp** | Alati määratud vaikimisi valikule **Arveldatav**. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Kandetüüp** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |
| **Kande klass** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Uue arverea üksikasjade loomine

Aja- ja materjali arveridadel saate luua uusi arverea üksikasju. Need arverea üksikasjad ei ole tegelike näitajate poolt varundatud. Aja- ja materjali arvereal saate valida suvandi **Uus**, et luua lepingureale lisatavatele tehingutele uue arverea üksikasjad.

## <a name="refresh-invoice-transactions"></a>Arve tehingute värskendamine

Kui teil on tegelikke näitajaid, mis lisandusid pärast arve loomist, saate lisada need tegelikud näitajad arvele.

1. Märkige **arvelduse võlgnevuse vaates** andmed kui **Arveldamiseks valmis**.   
2. Avage näidisvormi mustand ja ribal **Toimingud** klõpsake valikutd **Värskenda arverea tehinguid**.

  See loob arveterea üksikasjad iga tegeliku näitaja jaoks, mis on möödunud kuupäevaga ja märgitud kui **Arveldamiseks valmis**, kuid mis ei ole arvesse lisatud.

## <a name="product-based-invoice-lines"></a>Tootepõhised arveread

Rakenduses Project Operations saate luua projektipõhiste arveridadega arveread toodete jaoks, mis ei kohaldu ühelegi projektile või kohalduvad kõikidele projektidele koos. Need arveread luuakse projektipõhiste lepinguridadena ja pärast nende märkimist arveldamiseks valmis, lisatakse need tootepõhiste arveridadena.

Pärast tootepühiste arveridade lisamist ei saa neid muuta. Samas saab need näidisarve mustandist kustutada.
