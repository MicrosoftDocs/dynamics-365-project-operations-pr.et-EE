---
title: Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine
description: See artikkel annab teavet rakenduse Project Operations topeltkirjutuse kaartide seadistamise ja konfigureerimise kohta.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029147"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel annab teavet rakenduse Project Operations seadistamis- ja konfiguratsiooniolemite topeltkirjutuse integreerimise kohta.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektilepingud, lepinguread ja projektid

Projektilepinguid, lepinguread ja projektid luuakse rakenduses Dataverse ja sünkroonitakse finants- ja äritoimingute rakendustega, et neid täiendavalt raamatupidamist kasutada. Nende olemite kirjeid saab luua ja kustutada ainult rakenduse Dataverse kaudu. Küll aga saab nendesse kirjetesse finants- ja äritoimingute rakendustes lisada raamatupidamisatribuute, nagu müügimaksurühma vaikeatribuudid ja finantsdimensioonid.

  ![Projekti lepingu integreerimise mõisted.](./media/1ProjectContract.jpg)

Müügitegevuse müügivihjeid, võimalusi ja hinnapakkumisi jälgitakse rakenduses Dataverse ning neid ei sünkroonita finants- ja äritoimingute rakendustega, kuna selle tegevusega pole seotud järelarvestust.

Projektilepingu funktsioon rakenduses Dataverse loob projektilepingu kirje finants- ja äritoimingute rakendustes, kasutades tabelikaarti **Projekti lepingu päised (müügitellimused)**. Projekti lepingu salvestamine Dataverse’is käivitab ka projekti lepingu kliendi olemikirje loomise. See kirje sünkroonitakse finants- ja äritoimingute rakendustega, kasutades tabelikaarti **Projekti rahastamisallikas (msdyn\_projectcontractssplitbillingrules)**. See kaart sünkroonib ka projekti lepingu kliendi lisamised, värskendused ja kustutamised. Projekti lepinguklientide arveldusprotsentide tükeldamine on lubatud ainult rakenduses Dataverse ja neid ei sünkroonita finants- ja äritoimingute rakendustega.

Pärast projektilepingu loomist rakenduses Dataverse, saab projekti raamatupidaja uuendada selle projektilepingu raamatupidamisatribuute finants- ja äritoimingute rakendustes, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Seadistus** > **Vaikeraamatupidamise kuvamine**. Raamatupidaja saab vaadata rakendusprojekti lepingu atribuute (nt nõutud tarnekuupäev ja lepingu summa), valides finants- ja äritoimingute rakendustes projektilepingu ID, mis avab seotud projektilepingu kirje rakenduses Dataverse.

Projekti olem sünkroonitakse finants- ja äritoimingute rakendustega, kasutades tabelikaarti **Projektid V2 (msdyn\_projektid)**. Projekti raamatupidaja saab teha järgmist.

  - Projektide finants- ja äritoimingute rakenduste ülevaatamine, avades jaotise **Projektihaldus ja raamatupidamine** > **Kõik projektid**. 
  - Projekti raamatupidamisatribuutide värskendamiseks finants- ja äritoimingute rakendustes, avage **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Seadistus** > **Vaikeraamatupidamise kuvamine**.  
  - Vaadake üle rakendusprojekti atribuudid (nt hinnangulised algus- ja lõppkuupäevad), valides finants- ja äritoimingute rakendustes projekti ID, mis avab seotud projektikirje rakenduses Dataverse.

Projekt seostatakse projekti lepinguga olemi **Projekti lepingurida** kaudu.

Projektilepingu read rakenduses Dataverse loovad projektilepingu arveldusreegli finants- ja äritoimingute rakendustes, kasutades tabelikaarti **Projektiread (müügitellimused)**. Arveldusmeetod määratleb projektilepingu arveldusreegli tüübi finants- ja äritoimingute rakendustes.

  - Aja ja materjali arveldusmeetodiga projektilepingu read loovad aja- ja materjalitüübi arveldusreegli.
  - Fikseeritud hinnaga arveldusmeetodiga lepinguread loovad vahekokkuvõtte arveldusreegli.

Projekti lepinguread saab läbi vaadata projekti raamatupidaja finants- ja äritoimingute rakendustes, avades jaotise **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Seadistus** > **Vaikeraamatupidamise kuvamine** ning vaadates üle üksikasjad vahekaardil **Lepinguread**. Raamatupidaja saab sellel vahekaardil seadistada ka fikseeritud hinnaga arveldusmeetodi lepinguridadele vaikefinantsdimensioonid.

## <a name="billing-milestones"></a>Arvelduse vahekokkuvõtted

Fikseeritud hinnaga arveldamise meetodit kasutavad projektilepingu read arveldatakse arveldamise vahekokkuvõtete kaudu. Arvelduse vahekokkuvõtted sünkroonitakse finants- ja äritoimingute rakenduste ettemaksukannetega, kasutades tabelikaarti **Project Operationsi integreerimise lepingurea vahekokkuvõtted (msdyn\_contractlinescheduleofvalues)**.

  ![Arvelduste vahekokkuvõtete integreerimine.](./media/2Milestones.jpg)

Raamatupidaja saab üle vaadata ettemaksukanded ja kohandada nende tehingute raamatupidamisatribuute, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Haldus** > **Kontokanded** või **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Haldus** > **Kontokanded**.

Kui loote selle projektilepingu rea jaoks esmalt arvelduse vahekokkuvõtte, loob süsteem selle lepingureaga seotud projekti jaoks automaatselt fikseeritud hinnaga tulu prognoosi projekti. Fikseeritud hinnaga tulude eelarvestamise projekte saab üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Fikseeritud hinnaga tulu prognoosi projektid**.

### <a name="project-tasks"></a>Projekti ülesanded

Projekti tööülesanded sünkroonitakse finants- ja äritoimingute rakendustega, kasutades tabelikaarte **Projektiülesanded (msdyn\_projecttasks)** ainult viiteks. Toimingute loomist, värskendamist ja kustutamist ei toetata finants- ja äritoimingute rakenduste kaudu.

  ![Projektiülesannete integreerimine.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekti ressursid

Olem **Projekti ressursirollid** sünkroonitakse finants- ja äritoimingute rakendustega, tabelikaarti **Projekti ressursirolle kõigi ettevõtete jaoks (bookableresourcecategories)** kasutatakse ainult viitamiseks. Kuna ressursirollid rakenduses Dataverse pole ettevõttekohased, loob süsteem automaatselt vastavad ettevõttekohased ressursirollide kirjed finants- ja äritoimingute rakendustes automaatselt kõigi juriidiliste isikute jaoks, kes on kaasatud topeltkirjutusega integreerimisulatusse.

![Ressursirollide integreerimine.](./media/5Resources.jpg)

Rakenduse Project Operations projektiressursse hallatakse rakenduses Dataverse ja neid ei sünkroonita finants- ja äritoimingute rakendustega.

### <a name="transaction-categories"></a>Kandekategooriad

Tehingukategooriaid hallatakse rakenduses Dataverse ja sünkroonitakse finants- ja äritoimingute rakendustega, kasutades tabelikaarti **Projektitehingu kategooriad (msdyn\_transactioncategories)**. Pärast kandekategooria kirje sünkroonimist loob süsteem automaatselt neli ühiskategooria kirjet. Iga kirje vastab finants- ja äritoimingute rakendustes olevale tehingutüübile ja seob need tehingukategooria kirjega.

![Kandekategooriate integreerimine.](./media/4TransactionCategories.jpg)

Prognooside ja tegelike kulude kandekategooriate kasutamiseks peab projekti ettevõte või süsteemiadministraator looma igas juriidilises isikus vastavad projektikategooriad. Lisateavet leiate teemast [Projektikategooriate konfigureerimine](../project-accounting/configure-project-categories.md).
