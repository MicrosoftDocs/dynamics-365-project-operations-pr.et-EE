---
title: Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine
description: Selles teemas antakse teavet Project Operationsi topeltkirjutamise kaartide seadistamise ja konfigureerimise kohta.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938973"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet rakenduse Project Operations seadistamis- ja konfiguratsiooniolemite topeltkirjutamise integreerimise kohta.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektilepingud, lepinguread ja projektid

Projektilepinguid, lepinguread ja projektid luuakse rakenduses Dataverse ja sünkroonitakse rakendusega Finance and Operations, et neid täiendavalt raamatupidamist kasutada. Nende olemite kirjeid saab luua ja kustutada ainult rakenduse Dataverse kaudu. Küll aga saab nendesse kirjetesse rakenduses Finance and Operations lisada raamatupidamisatribuute, nagu müügimaksurühma vaikeatribuudid ja finantsdimensioonid.

  ![Projekti lepingu integreerimise mõisted](./media/1ProjectContract.jpg)

Müügitegevuse müügivihjeid, võimalusi ja hinnapakkumisi jälgitakse rakenduses Dataverse ning neid ei sünkroonita rakendusega Finance and Operations, kuna selle tegevusega pole seotud järelarvestust.

Projektilepingu funktsioon rakenduses Dataverse loob projektilepingu kirje rakenduses Finance and Operations, kasutades tabelikaarti **Projekti lepingu päised (müügitellimused)**. Projekti lepingu salvestamine Dataverse’is käivitab ka projekti lepingu kliendi olemikirje loomise. See kirje sünkroonitakse rakendusega Finance and Operations, kasutades tabelikaarti **Projekti rahastamisallikas (msdyn\_projectcontractssplitbillingrules)**. See kaart sünkroonib ka projekti lepingu kliendi lisamised, värskendused ja kustutamised. Projekti lepinguklientide arveldusprotsentide tükeldamine on lubatud ainult rakenduses Dataverse ja neid ei sünkroonita rakendusega Finance and Operations.

Pärast projektilepingu loomist rakenduses Dataverse, saab projekti raamatupidaja uuendada selle projektilepingu raamatupidamisatribuute rakendustes Finance and Operations, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Seadistus** > **Kuva vaikeraamatupidamine**. Raamatupidaja saab vaadata rakendusprojekti lepingu atribuute (nt nõutud tarnekuupäev ja lepingu summa), valides rakenduses Finance and Operations projektilepingu ID, mis avab seotud projektilepingu kirje Dataverse’is.

Projekti olem sünkroonitakse rakendusega Finance and Operations, kasutades tabelikaarti **Projektid V2 (msdyn\_projects)**. Projekti raamatupidaja saab teha järgmist.

  - Projekte rakenduses Finance and Operations üle vaadata, avades jaotise **Projektihaldus ja raamatupidamine** > **Kõik projektid**. 
  - Projekti raamatupidamisatribuutide värskendamiseks rakendustes Finance and Operations avage **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Seadistus** > **Kuva vaikeraamatupidamine**.  
  - Vaadake üle rakendusprojekti atribuudid (nt hinnangulised algus- ja lõppkuupäevad), valides rakenduses Finance and Operations projekti ID, mis avab seotud projektikirje rakenduses Dataverse.

Projekt seostatakse projekti lepinguga olemi **Projekti lepingurida** kaudu.

Projektilepingu read rakenduses Dataverse loovad projektilepingu arveldusreegli rakendustes Finance and Operations, kasutades tabelikaarti **Projektiread (müügitellimused)**. Arveldusmeetod määratleb projektilepingu arveldusreegli tüübi rakendustes Finance and Operations.

  - Aja ja materjali arveldusmeetodiga projektilepingu read loovad aja- ja materjalitüübi arveldusreegli.
  - Fikseeritud hinnaga arveldusmeetodiga lepinguread loovad vahekokkuvõtte arveldusreegli.

Projekti lepinguread saab läbi vaadata projekti raamatupidaja rakenduses Finance and Operations, avades jaotise **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Seadistus** > **Kuva vaikeraamatupidamine** ning vaadates üle üksikasjad vahekaardil **Lepinguread**. Raamatupidaja saab sellel vahekaardil seadistada ka fikseeritud hinnaga arveldusmeetodi lepinguridadele vaikedimensioonid.

## <a name="billing-milestones"></a>Arvelduse vahekokkuvõtted

Fikseeritud hinnaga arveldamise meetodit kasutavad projektilepingu read arveldatakse arveldamise vahekokkuvõtete kaudu. Arvelduse vahekokkuvõtted sünkroonitakse rakenduse Finance and Operations ettemaksukannetega, kasutades tabelikaarti **Projekti integreerimise lepingu rea vahekokkuvõtted (msdyn\_contractlinescheduleofvalues)**.

  ![Arvelduste vahekokkuvõtete integreerimine](./media/2Milestones.jpg)

Raamatupidaja saab üle vaadata ettemaksukanded ja kohandada nende tehingute raamatupidamisatribuute, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Haldus** > **Kontokanded** või **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Haldus** > **Kontokanded**.

Kui loote selle projektilepingu rea jaoks esmalt arvelduse vahekokkuvõtte, loob süsteem selle lepingureaga seotud projekti jaoks automaatselt fikseeritud hinnaga tulu prognoosi projekti. Fikseeritud hinnaga tulude eelarvestamise projekte saab üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Fikseeritud hinnaga tulu prognoosi projektid**.

### <a name="project-tasks"></a>Projekti ülesanded

Projekti tööülesanded sünkroonitakse rakendusega Finance and Operations, kasutades tabelikaarte **Projektiülesanded (msdyn\_projecttasks)** ainult viiteks. Toimingute loomist, värskendamist ja kustutamist ei toetata rakenduse Finance and Operations kaudu.

  ![Projektiülesandega integreerimine](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekti ressursid

Olem **Projekti ressursirollid** sünkroonitakse rakendusega Finance and Operations, tabelikaarti **projekti ressursirolle kõigi ettevõtete jaoks (broneeritavate ressursside kategooriad)** kasutatakse ainult viitamiseks. Kuna ressursirollid rakenduses Dataverse pole ettevõttekohased, loob süsteem automaatselt vastavad ettevõttekohased ressursirollide kirjed rakenduses Finance and Operations automaatselt kõigi juriidiliste isikute jaoks, kes on kaasatud topeltkirjutamisega integreerimisulatusse.

![Ressursirollide integreerimine](./media/5Resources.jpg)

Rakenduse Project Operations projektiressursse hallatakse Dataverse’is ja neid ei sünkroonita rakendusega Finance and Operations.

### <a name="transaction-categories"></a>Kandekategooriad

Kandekategooriaid hallatakse Dataverse’is ja sünkroonitakse rakendusega Finance and Operations, kasutades tabelikaarti **Projektikannete kategooriad (msdyn\_transactioncategories)**. Pärast kandekategooria kirje sünkroonimist loob süsteem automaatselt neli ühiskategooria kirjet. Iga kirje vastab rakenduses Finance and Operations olevale tehingutüübile ja seob need kandekategooria kirjega.

![Kandekategooriate integreerimine](./media/4TransactionCategories.jpg)

Prognooside ja tegelike kulude kandekategooriate kasutamiseks peab projekti ettevõte või süsteemiadministraator looma igas juriidilises isikus vastavad projektikategooriad. Lisateavet leiate teemast [Projektikategooriate konfigureerimine](../project-accounting/configure-project-categories.md).
