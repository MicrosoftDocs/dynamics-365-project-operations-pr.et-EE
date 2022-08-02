---
title: Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine
description: Sellest artiklist leiate teavet Project Operationsi topeltkirjutuskaartide häälestamise ja konfigureerimise kohta.
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

Sellest artiklist leiate teavet installi- ja konfiguratsiooniolemite Project Operationsi topeltkirjutusega integreerimise kohta.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektilepingud, lepinguread ja projektid

Projektilepingud, lepinguread ja projektid luuakse Dataverse ja sünkroonitakse finance and operationsi rakendustega täiendava raamatupidamise jaoks. Nende olemite kirjeid saab luua ja kustutada ainult rakenduse Dataverse kaudu. Raamatupidamisatribuute, nagu käibemaksugrupi vaikeväärtused ja finantsdimensioonid, saab aga nendele kirjetele lisada finance and operationsi rakendustes.

  ![Projekti lepingu integreerimise mõisted.](./media/1ProjectContract.jpg)

Müügitegevuse müügivihjeid, müügivõimalusi ja hinnapakkumisi jälgitakse ja neid ei sünkroonita Dataverse finants- ja toimingurakendustega, kuna selle tegevusega pole seotud järgmise etapi raamatupidamisarvestust.

Projektilepingu funktsioon loob rakenduses Dataverse Finance and Operations projektilepingu kirje, kasutades **tabelikaarti Project contract headers (salesorders).** Projekti lepingu salvestamine Dataverse’is käivitab ka projekti lepingu kliendi olemikirje loomise. See kirje sünkroonitakse finants- ja toimingurakendustega, kasutades **tabelit Project funding source (msdyn\_ projectcontractssplitbillingrules).** See kaart sünkroonib ka projekti lepingu kliendi lisamised, värskendused ja kustutamised. Arveldusprotsentide jagamine projektilepingu klientide vahel omandatakse ainult finance and operationsi rakendustes Dataverse ja neid ei sünkroonita nendega.

Pärast projektilepingu loomist Dataverse rakenduses saab projekti raamatupidaja värskendada selle projektilepingu raamatupidamisatribuute finance and operationsi rakendustes, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projektilepingute** > **seadistamine** > **Kuva vaikearvestus**. Raamatupidaja saab üle vaadata operatiivse projekti lepingu atribuudid, nagu taotletud tarnekuupäev ja lepingu summa, valides finance and operationsi rakendustes projekti lepingu ID, mis avab seotud projektilepingu kirje rakenduses Dataverse.

Projekti olem sünkroonitakse finants- ja toimingurakendustega, kasutades **tabelikaarti Projects V2 (msdyn\_ projects).** Projekti raamatupidaja saab teha järgmist.

  - Vaadake projekte finance and operationsi rakendustes üle, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid**. 
  - Värskendage projekti raamatupidamisatribuute finance and operationsi rakendustes, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Seadistatud** > **Kuva vaikearvestus**.  
  - Vaadake üle projekti tööatribuudid, nagu hinnangulised algus- ja lõppkuupäevad, valides finance and operationsi rakendustes projekti ID, mis avab seotud projektikirje rakenduses Dataverse.

Projekt seostatakse projekti lepinguga olemi **Projekti lepingurida** kaudu.

Projekti lepinguread loob Dataverse rakenduses Finance and Operations projektilepingu arveldusreegli, kasutades **tabelit Project contract lines (salesorderdetails)** kaart. Arveldusmeetod määratleb finance and operationsi rakendustes projektilepingu arveldusreegli tüübi.

  - Aja ja materjali arveldusmeetodiga projektilepingu read loovad aja- ja materjalitüübi arveldusreegli.
  - Fikseeritud hinnaga arveldusmeetodiga lepinguread loovad vahekokkuvõtte arveldusreegli.

Projekti lepinguread saab projekti raamatupidaja finance and operationsi rakendustes üle vaadata, **minnes lehele Projektihaldus ja raamatupidamine** > **Projektilepingud** > **Seadistage** > **vaikearvestus** ja vaadake üle vahekaardil Lepingu read **olevad** üksikasjad. Raamatupidaja saab sellel vahekaardil määrata ka fikseeritud hinnaga arveldusmeetodi lepingu ridadele vaikefinantsdimensioonid.

## <a name="billing-milestones"></a>Arvelduse vahekokkuvõtted

Fikseeritud hinnaga arveldamise meetodit kasutavad projektilepingu read arveldatakse arveldamise vahekokkuvõtete kaudu. Arvelduse verstapostid sünkroonitakse projekti ettemaksukannetega finance and operationsi rakendustes, kasutades **Project Operationsi integratsiooni lepingurea verstapostide (msdyn\_ contractlinescheduleofvalues)** tabelikaarti.

  ![Arvelduste vahekokkuvõtete integreerimine.](./media/2Milestones.jpg)

Raamatupidaja saab üle vaadata ettemaksukanded ja kohandada nende tehingute raamatupidamisatribuute, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Projekti lepingud** > **Haldus** > **Kontokanded** või **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Haldus** > **Kontokanded**.

Kui loote selle projektilepingu rea jaoks esmalt arvelduse vahekokkuvõtte, loob süsteem selle lepingureaga seotud projekti jaoks automaatselt fikseeritud hinnaga tulu prognoosi projekti. Fikseeritud hinnaga tulude eelarvestamise projekte saab üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Fikseeritud hinnaga tulu prognoosi projektid**.

### <a name="project-tasks"></a>Projekti ülesanded

Projektiülesanded sünkroonitakse finance and operationsi rakendustega Project tasks (msdyn **projecttasks)\_ tabelikaardi kaudu** ainult viitamise eesmärgil. Toimingute loomist, värskendamist ja kustutamist ei toetata finance and operationsi rakenduste kaudu.

  ![Projektiülesannete integreerimine.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projekti ressursid

Olem **Projekti ressursirollid** sünkroonitakse finance and operationsi rakendustega, kasutades **tabelit Project resource roles for all companies (bookableres resourcescecategories) (Projekti ressursirollid)** ainult viitamise eesmärgil. Kuna ressursirollid Dataverse ei ole ettevõttepõhised, loob süsteem vastavad ettevõttepõhised ressursirollide kirjed finants- ja operatsioonirakendustes automaatselt kõigile juriidilistele isikutele, kes on kaasatud topeltkirjutusega integratsiooni ulatusse.

![Ressursirollide integreerimine.](./media/5Resources.jpg)

Project Operationsi projektiressursse hoitakse rakenduses Dataverse Finance and Operations ja neid ei sünkroonita rakendustega Finance and Operations.

### <a name="transaction-categories"></a>Kandekategooriad

Kandekategooriaid hoitakse finants- ja toimingurakendustes Dataverse ning sünkroonitakse nendega, kasutades **tabelit Projekti kandekategooriad (msdyn\_ transactioncategories).** Pärast kandekategooria kirje sünkroonimist loob süsteem automaatselt neli ühiskategooria kirjet. Iga kirje vastab finants- ja toimingurakendustes tehingutüübile ja seob need kandekategooria kirjega.

![Kandekategooriate integreerimine.](./media/4TransactionCategories.jpg)

Prognooside ja tegelike kulude kandekategooriate kasutamiseks peab projekti ettevõte või süsteemiadministraator looma igas juriidilises isikus vastavad projektikategooriad. Lisateavet leiate teemast [Projektikategooriate konfigureerimine](../project-accounting/configure-project-categories.md).
