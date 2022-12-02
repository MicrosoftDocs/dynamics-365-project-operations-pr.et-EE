---
title: Projektipõhise näidisarve haldamine
description: See artikkel annab teavet projektipõhiste näidisarvete haldamise ja nendega töötamise kohta.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 31822947a4fbb60218ce1c3c9415a60491f6d8fa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932107"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Projektipõhise näidisarve haldamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Rakenduses Dynamics 365 Project Operations luuakse näidisarved rakenduse Dynamics 365 Sales arvete laiendusena. Samas esineb arveldamise ajal rakenduste Sales ja Project Operations arveldamise toimingus palju erinevusi. Näiteks pole rakenduses Project Operations võimalik luua lehel **Arvete loend** uut arvet, kuid rakenduses Sales on see võimalik. Need erinevused ja laiendused on olemas, et toetada arveldamistoiminguid projetides, mis erinevad tavalisest müügitellimuse arvest.

> [!IMPORTANT]
> Erinevuste tõttu ärge kasutage rakenduste Sales ja Project Operations arveid vaheldumisi.

## <a name="invoice-header"></a>Arve päis

Rakenduses Project Operations on näidisarve päises saadaval järgmine teave.

| Väli | Asukoht | Kirjeldus |
| --- | --- | --- | 
| **Arve ID** | Vahekaart **Kokkuvõte** | Näidisarve loomisel automaatselt genereeritav ID. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Seda välja kasutatakse iga näidisarve jaoks viitena. |
| **Nimi** | Vahekaart **Kokkuvõte** | On vaikimisi määratud projektilepingu nimele. Seda välja saab redigeerida. | 
| **Valuuta** | Vahekaart **Kokkuvõte** | On vaikimisi määratud projektilepingu valuutale. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Hinnakiri** | Vahekaart **Kokkuvõte** | On vaikimisi määratud projektilepingu hinnakirjale. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Müügivõimalus** | Vahekaart **Kokkuvõte** | Lingitud müügivõimaluse viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Leping** | Vahekaart **Kokkuvõte** | Lingitud projektilepingu viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Klient** | Vahekaart **Kokkuvõte** | Lingitud projektilepingu viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Kirjeldus** | Vahekaart **Kokkuvõte** | Arvet kirjeldav tekstiväli. Seda välja saab redigeerida. | 
| **Maksja** ja seostuvad väljad | **Kokkuvõtte vahekaart** | Vaikeväärtused määratakse projektilepingu kliendilt. Seda välja saab redigeerida.  | 
| **Olek** | Vahekaart **Kokkuvõte** | Määrab järgmised valikud: **Aktiivne**, **Suletud**, **Makstud** ja **Tühistatud** ning neid saab redigeerida. Project Operationsi mittetoetatavad olekud on **Suletud** ja **Tühistatud**. </br> Arve loomisel seatakse olekuks **Aktiivne**. </br>Olekuks tuleks määrata **Makstud** ainult pärast arve kinnitamist.  | 
| **Projektiarve olek** | Vahekaart **Kokkuvõte** | Seab järgmised valikud: **Mustand**, **Läbivaatusel** ja **Kinnitatud** ning neid saab redigeerida. Nii olekus **Mustand** kui ka **Läbivaatusel** saab arvet muuta. Pärast kinnitamist ei saa arvet muuta. | 
| **Reasumma** | Vahekaart **Kokkuvõte** | Kõikide arveridade kogusumma pärast ettemakseid ja mahaarvamisi. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud.  Seda välja kasutatakse lõppsumma arvutamiseks. | 
| **Allahindlus (%)** | Vahekaart **Kokkuvõte** | Seda välja saab allahindlusprotsendi lisamiseks muuta. Project Operationsi funktsioonid ei toeta seda välja. See on toetuseta väli.|  
| **Allahindlussumma** | Vahekaart **Kokkuvõte** | Seda välja saab allahindluse summa lisamiseks muuta. Project Operationsi funktsioonid ei toeta seda välja. See on toetuseta väli. |  
| **Veotasueelne summa** | **Kokkuvõtte vahekaart** | Arve kogusumma pärast allahindluste rakendamist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Seda välja kasutatakse lõppsumma arvutamiseks.  | 
| **Veotasu summa** | Vahekaart **Kokkuvõte** | Seda välja saab veotasu summa lisamiseks muuta. Project Operationsi funktsioonid ei toeta seda välja. See on toetuseta väli. |
| **Kogumaks** | Vahekaart **Kokkuvõte** | Arve kõikide arveridade maksu kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Kogusumma** | Vahekaart **Kokkuvõte** | Kogusumma pärast allahindlusi ja makse. See on summa, mille klient peab maksma. | 

## <a name="project-based-invoice-lines"></a>Projektipõhised arveread

Rakenduses Project Operations on iga prijekti lepingurea jaoks üks arverida. Arverida luuakse ka juhul, kui tegelikke näitajaid pole. Arvereal on näidisarve päises saadaval järgmine teave.

| Väli | Asukoht | Kirjeldus | 
| --- | --- | --- |
| **Arve ID** | Vahekaart **Üldine** | Viide arve ID-le. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Arve ID linki saab kasutada tagasi arve päisesse liikumiseks. | 
| **Nimi** | Vahekaart **Üldine** | Arverea nimi, mis on määratud vaikimisi lepingurea nimest. Seda välja saab redigeerida. |
| **Project** | Vahekaart **Üldine** | Projekt seotud projekti lepingureal. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Projekti linki saab kasutada projektile navigeerimiseks. | 
| **Arveldusmeetod** | Vahekaart **Üldine** | Arveldusmeetod seotud projekti lepingureal. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Lepingurea summa** | Vahekaart **Üldine** | Seotud projekti arverea lepingu summa. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Arveldatud kuupäevani** | Vahekaart **Üldine** | Arve kõigi arveridade üksikasjade kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Summa** | Vahekaart **Üldine** | Arve kõigi arveldatavate arveridade üksikasjade kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Seda välja kasutatakse arve päises lõppsumma arvutamiseks. | 
| **Maks** | Vahekaart **Üldine** | Arverea kõigi arveridade üksikasjade maksude kogusumma. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Seda välja kasutatakse arve päises maksu lõppsumma arvutamiseks. | 
| **Laiendatud summa** | Vahekaart **Üldine** | Arverea kõigi arveldatavate arveridade üksikasjade üldine kogusumma (**maks + summad**). Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Seda välja kasutatakse arve päises lõppsumma arvutamiseks. |

## <a name="invoice-line-details"></a>Arve rea üksikasjad

Iga projekti arve arverida sisaldab arverea üksikasju. Need rea üksikasjad on seotud arveldamata müügi tegelike ja vahe-eesmärkide summaga, mis on seotud arverea viidatud lepingureaga. Kõik need tehingud on märgitud kui **Arveldamiseks valmis**.

Real **Aja ja materjali arve** on arverea üksikasjad rühmitatud lehel **Arverida** valikuteks **Arveldatav**, **Mittearveldatav** ja **Tasuta** lehel. **Arveldatava arverea** üksikasjad lisatakse arverea kogusummale. **Tasuta** ja **mitte-arveldatavaid tegelikke näitajaid** arverea kogusummale ei lisata.

Real **Fikseeritud hinnaga arve** luuakse arverea üksikasjad vahe-etappidest, mis on seotud lepingureal märgitud kui **Arveldamiseks valmis**. Pärast seda, kui arverea üksikasjad on vahe-eesmörgi põhjal loodud, uuendatakse vahe-eesmärgi arveldamine olekule **Kliendi arve loodud**.

### <a name="edit-invoice-line-details"></a>Arve rea üksikasjade redigeerimine

Arverea üksikasjades, mida toetavad arveldamata müügi tegelikud näitajad, on saadaval järgmised väljad.

| Väli | Kirjeldus |
| --- | --- | 
| **Arverida** | **Arverea ID** viide. See väli on kirjutuskaitstud ja redigeerimiseks lukus. Seda linki saab kasutada tagasi arve päisesse liikumiseks. | 
| **Kirjeldus** | Arverea üksikasjade kirjeldus. Määratakse vaikimisi väljalt **Sisemised kommentaarid** suvandis **Ajakirje** ja väljalt **Kirjeldus** suvandis **Kulukirje**. Välja saab redigeerida.| 
| **Väline kirjeldus** | Arverea üksikasjade kirjeldus. Määratakse vaikimisi väljalt **Välised kommentaarid** suvandis **Ajakirje** ja väljalt **Kirjeldus** suvandis **Kulukirje**. Välja saab redigeerida. Seda kirjeldust saab kasutada määramaks, mis peaks olema kliendile saadetaval prinditud arvel. Rakendusel Project Operations ei ole näidisarvel kõiki nõutavaid funktsioone, et konfigureerida arve printimise seadistused. | 
| **Alguskuupäev** | See on kirjutuskaitstud väli, mis on vaikimisi allika tegelikust väärtusest määratud. |
| **Project** | See on kirjutuskaitstud väli, mis määratakse vaikimisi projektile allika tegelikust väärtusest seotud lepingureal. |  
| **Toiming** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Kande kategooria** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Roll** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |  
| **Broneeritav ressurss** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Ressursiettevõte** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Ressursi üksus** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Kogus** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |  
| **Üksuse ajakava** | Arverea aja üksikasja puhul on see alati määratud ajale ja seda ei saa muuta. Kulude puhul on see määratud vaikimisi lähtekulu tegelikule näitajale. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Üksus** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |  
| **Hind** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Valuuta** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Summa** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Maks** | Määratakse vaikimisi allika tegelikust näitajast. Välja saab redigeerida.| 
| **Rea summa** | Arvutatud väli, arvutatakse valemiga **summa + maks**. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Arveldustüüp** | Määratakse vaikimisi allika tegelikust näitajast. Välja saab redigeerida. Suvandi **Arveldatav** lisab arverea kogusummale rea. **Tasuta** ja **Mitte-arveldatav** jätavad selle arverea kogusummast välja.| 
| **Vali toode** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Toode** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Toote nimi** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |  
| **Sisestatav kirjeldus** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Kandetüüp** | See on kirjutuskaitstud väli, mis on määratud vaikimisi allika tegelikust väärtusest suvandile **Arveldatud müük**. |  
| **Tehingu klass** | Määratakse vaikimisi allika tegelikust näitajast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 

Arverea üksikasjades, mida toetab vahe-eesmärk, on saadaval järgmised väljad.

| Väli | Kirjeldus |
| --- | --- | 
| **Arverida** | **Arverea ID** viide. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. Linki saab kasutada tagasi arve päisesse liikumiseks.  | 
| **Kirjeldus** | Arverea üksikasjade kirjeldus. Määratakse vaikimisi allika vahe-eesmärgi kirjeldusest. | 
|**Väline kirjeldus** | Arverea üksikasjade kirjeldus, mis on vaikimisi määratud allika vahe-eesmärgi kirjeldusest. Seda välja saab kasutada määramaks, mis peaks olema kliendile saadetaval prinditud arvel. Rakenduse Project Operations näidisarvel ei ole kõiki nõutavaid funktsioone, et konfigureerida arve printimise seadistused. | 
| **Alguskuupäev** | Määratakse vaikimisi allika vahe-eesmärgi kuupäevast **Vahe-eesmärk**. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Project** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Tööülesanne** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Kande kategooria** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Roll** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Broneeritav ressurss** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Ressursi üksus** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Üksuse ajakava** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Ühik** | Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Hind** | Määratakse vaikimisi allika vahe-eesmärgi summast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Valuuta** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Summa** | Määratakse vaikimisi allika vahe-eesmärgi summast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Maks** | Määratakse vaikimisi allika vahe-eesmärgi maksusummast. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Laiendatud summa** | Määratakse vaikimisi allika vahe-eesmärgi rea summast. Välja saab redigeerida. | 
| **Arveldustüüp** | Alati määratud vaikimisi valikule **Arveldatav**. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. |
| **Kandetüüp** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 
| **Tehingu klass** | Määratakse vaikimisi allika vahe-eesmärgist. Kirjutuskaitstud väli, mis on redigeerimiseks lukustatud. | 

## <a name="refresh-invoice-transactions"></a>Arve tehingute värskendamine

Kui teil on tegelikke näitajaid, mis lisandusid pärast arve loomist, saate lisada need tegelikud näitajad arvele.

1. Märkige **arvelduse võlgnevuse vaates** andmed kui **Arveldamiseks valmis**.   
2. Avage näidisarve mustand ja valige lindil **Toimingud** suvand **Värskenda arverea tehingud**.

  Arverea üksikasjad luuakse mis tahes tegeliku väärtuse jaoks, mis on möödunud kuupäevaga ja märgitud kui **Arveldamiseks valmis**, kuid mis pole arvele lisatud.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
