---
title: Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine
description: Selles artiklis antakse teavet Project Operationsi kahe kirjutamiskaartide seadistamise ja konfigureerimise kohta.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914535"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles artiklis antakse teavet seadistus- ja konfiguratsiooniolemite Project Operationsi topeltkirjutamise integratsiooni kohta.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektilepingud, lepinguread ja projektid

Projektilepingud, lepinguread ja projektid luuakse täiendavaks raamatupidamiseks rakendustes Dataverse Finance and Operations ja sünkroonitakse nendega. Nende olemite kirjeid saab luua ja kustutada ainult rakenduse Dataverse kaudu. Siiski saab rakendustes Finance and Operations nendele kirjetele lisada raamatupidamisatribuute, nagu käibemaksugrupi vaikesätted ja finantsdimensioonid.

  ![Projekti lepingu integreerimise mõisted.](./media/1ProjectContract.jpg)

Müügitegevuse müügivihjeid, müügivõimalusi ja hinnapakkumisi jälgitakse rakenduses ja neid ei sünkroonita rakendustega Dataverse Finance and Operations, kuna selle tegevusega pole seotud järgmise etapi raamatupidamist.

Projektilepingu funktsioon rakenduses Dataverse loob projektilepingu kirje rakendustes Finance and Operations, kasutades **tabelikaarti Projekti lepingupäised (müügitellimused).** Projekti lepingu salvestamine Dataverse’is käivitab ka projekti lepingu kliendi olemikirje loomise. See kirje sünkroonitakse rakendustega Finance and Operations tabelikaardi Project funding source (msdyn **projectcontractssplitbillingrules)\_ abil**. See kaart sünkroonib ka projekti lepingu kliendi lisamised, värskendused ja kustutamised. Tükeldatud arveldusprotsendid projektilepingu klientide vahel on omandatud ainult rakenduses Dataverse ja neid ei sünkroonita rakendustega Finance and Operations.

Pärast projektilepingu loomist Dataverse rakenduses saate projekti raamatupidaja värskendada selle projektilepingu raamatupidamisatribuute finance and Operations rakendustes, minnes jaotisse **Projektihaldus- ja raamatupidamislepingud** > **Projektilepingud** > **Kuva** > **vaikearvestus**. Raamatupidaja saab üle vaadata projekti tegevuslepingu atribuudid, näiteks nõutud tarnekuupäeva ja lepingu summa, valides rakenduses Finance and Operations projektilepingu ID, mis avab seotud projektilepingu kirje Dataverse rakenduses.

Projekti olem sünkroonitakse rakendustega Finance and Operations tabelikaardi Projektid V2 (msdyn **projects)\_ abil**. Projekti raamatupidaja saab teha järgmist.

  - Vaadake projektid finance and Operationsi rakendustes üle, minnes projektijuhtimisse **ja raamatupidamisse** > **Kõik projektid**. 
  - Saate värskendada projekti raamatupidamisatribuute rakendustes Finance and Operations rakendustes, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Seadista** > **Kuva vaikearvestus**.  
  - Vaadake üle operatiivprojekti atribuudid (nt hinnangulised algus- ja lõppkuupäevad), valides rakenduses Finance and Operations projekti ID, mis avab rakenduses seotud projektikirje Dataverse.

Projekt seostatakse projekti lepinguga olemi **Projekti lepingurida** kaudu.

Projektilepingu read rakenduses Dataverse loob projektilepingu arveldusreegli rakendustes Finance and Operations, kasutades **tabelikaarti Projekti lepinguridu (salesorderdetails).** Arveldusmeetod määratleb projektilepingu arveldusreegli tüübi rakendustes Finance and Operations.

  - Aja ja materjali arveldusmeetodiga projektilepingu read loovad aja- ja materjalitüübi arveldusreegli.
  - Fikseeritud hinnaga arveldusmeetodiga lepinguread loovad vahekokkuvõtte arveldusreegli.

Projekti lepinguridu saab projekti raamatupidaja vaadata rakendustes Finance and Operations, minnes jaotisse **Projektihaldus- ja raamatupidamisprojektilepingud** > **·** > **Seadistage** > **Kuva vaikearvestus** ja vaadake üle vahekaardi Leping ridade **üksikasjad**. Raamatupidaja saab sellel vahekaardil määrata fikseeritud hinna arveldusmeetodi lepinguridade vaikedimensioonid.

## <a name="billing-milestones"></a>Arvelduse vahekokkuvõtted

Fikseeritud hinnaga arveldamise meetodit kasutavad projektilepingu read arveldatakse arveldamise vahekokkuvõtete kaudu. Arvelduse vahe-eesmärgid sünkroonitakse projekti ettemaksukannetega Finance and Operationsi rakendustes, kasutades **tabelikaarti Project Operations integration contract line milestones (msdyn\_ contractlinescheduleofvalues).**

  ![Arvelduste vahekokkuvõtete integreerimine.](./media/2Milestones.jpg)

Raamatupidaja saab üle vaadata ettemaksukanded ja kohandada nende tehingute raamatupidamisatribuute, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Haldus** > **Kontokanded** või **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Haldus** > **Kontokanded**.

Kui loote selle projektilepingu rea jaoks esmalt arvelduse vahekokkuvõtte, loob süsteem selle lepingureaga seotud projekti jaoks automaatselt fikseeritud hinnaga tulu prognoosi projekti. Fikseeritud hinnaga tulude eelarvestamise projekte saab üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Fikseeritud hinnaga tulu prognoosi projektid**.

### <a name="project-tasks"></a>Projekti ülesanded

Projektiülesanded sünkroonitakse rakendustega Finance and Operations tabelikaardi Project tasks (msdyn **projecttasks)\_ kaudu** ainult viiteeesmärkidel. Finance and Operationsi rakenduste kaudu ei toetata toimingute loomist, värskendamist ja kustutamist.

  ![Projektiülesannete integreerimine.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekti ressursid

Olem **Projekti ressursirollid** sünkroonitakse rakendustega Finance and Operations, kasutades **projekti ressursirolle kõigi ettevõtete (broneeritavate ressursside)** tabelikaardi jaoks ainult viiteeesmärkidel. Kuna ressursirollid rakenduses Dataverse ei ole ettevõttespetsiifilised, loob süsteem finance and Operationsi rakendustes automaatselt vastavad ettevõttespetsiifilised ressursirollide kirjed kõigi juriidiliste isikute jaoks, kes on kaasatud kahe kirjutamise integratsiooniulatusse.

![Ressursirollide integreerimine.](./media/5Resources.jpg)

Project Operationsi projektiressursse hoitakse rakenduses Dataverse ja neid ei sünkroonita rakendustega Finance and Operations.

### <a name="transaction-categories"></a>Kandekategooriad

Tehingukategooriaid säilitatakse ja sünkroonitakse rakendustega Dataverse Finance and Operations, kasutades **tabelikaarti Project transaction categories (msdyn\_ transactioncategories).** Pärast kandekategooria kirje sünkroonimist loob süsteem automaatselt neli ühiskategooria kirjet. Iga kirje vastab rakenduse Finance and Operations kandetüübile ja seob need kandekategooria kirjega.

![Kandekategooriate integreerimine.](./media/4TransactionCategories.jpg)

Prognooside ja tegelike kulude kandekategooriate kasutamiseks peab projekti ettevõte või süsteemiadministraator looma igas juriidilises isikus vastavad projektikategooriad. Lisateavet leiate teemast [Projektikategooriate konfigureerimine](../project-accounting/configure-project-categories.md).
