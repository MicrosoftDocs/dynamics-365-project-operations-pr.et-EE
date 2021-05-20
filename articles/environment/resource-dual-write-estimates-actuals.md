---
title: Projekti prognooside ja tegelike andmete integreerimine
description: Selles teemas antakse teavet Project Operationsi topeltkirjutamise integreerimise kohta projekti prognooside ja tegelike andmete puhul.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955736"
---
# <a name="project-estimates-and-actuals-integration"></a>Projekti prognooside ja tegelike andmete integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet Project Operationsi topeltkirjutamise integreerimise kohta projekti prognooside ja tegelike andmete puhul.

## <a name="project-estimates"></a>Projekti prognoosid

Projekti tööjõu-, kulu- ja materjaliprognoosid luuakse ning neid hallatakse rakenduses Microsoft Dataverse ja sünkroonitakse rakendusega Finance and Operations raamatupidamisarvestuse eesmärgil. Rakendustes Finance and Operations ei toetata loomise, värskendamise ja kustutamise toiminguid.

Prognooside loomiseks on projekti jaoks vaja kehtivat raamatupidamiskonfiguratsiooni. Lepinguridadega seostatud projektidel peab olema kehtiv projekti kulu- ja tuluprofiil, mis on määratletud projekti kulu- ja tuluprofiili reeglites. Lisateavet leiate teemast [Arveldatavate projektide raamatupidamisarvestuse konfigureerimine](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Tööjõu prognoosid

Tööjõu prognoosid loob projektijuht või ressursihaldur, kes määrab projekti ülesandele ka üldise või nimelise ressursi. Ressursi määramise kirjeid saab üle vaadata vahekaardil **Ressursi määramine** lehel **Projekti üksikasjad** Dataverse’is. Ressursi määramise kirjed Dataverse’is loovad tunniprognoosi kirjed rakenduses Finance and Operations, kasutades **Project Operationsi integreerimise üksust tunniprognoosideks (msdyn\_resourceassignments)**.

   ![Tööjõu prognooside integreerimine](./Media/DW4LaborEstimates.png)

Topeltkirjutuse abil sünkroonitakse ressursi määramise kirjed koondtabeliga (**ProjCDSEstimateHoursImport**) ja seejärel kasutatakse äriloogikat tunniprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastEmpl**).

Projekti raamatupidaja vaatab rakendustes Finance and Operations loodud prognoositundide kirjed üle, minnes jaotisse **Projektide haldamine ja raamatupidamine** > **Kõik projektid** > **Plaan** > **Tunniprognoos**.

## <a name="expense-estimates"></a>Kuluprognoosid

Projektijuht loob kuluprognoosid vahekaardil **Kuluprognoos** lehel **Projekti üksikasjad** Dataverse’is. Kuluprognoosi kirjed salvestatakse Dataverse’is olemisse **Prognoosirida**. Need prognoosikirjed on kannete klassiga **Kulu** ja sünkroonitakse rakendustes Finance and Operations kuluprognoosi kirjetega, kasutades **Kuluprognooside Project Operationsi integreerimise üksust (msdyn\_estimatelines)**.

   ![Kuluprognooside integreerimine](./Media/DW4ExpenseEstimates.png)

Topeltkirjutamine sünkroonib kuluprognoosi kirjed koondtabeliga **ProjCDSEstimateExpenseImport)** ja seejärel kasutab äriloogikat kuluprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastCost**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Äriloogika täidab rakenduses Finance and Operations ühe kuluprognoosi kirje, kasutades seda üksikasja koondtabelis.

Projekti raamatupidaja saab vaadata kuluprognoosi kirjeid rakenduses Finance and Operations, avades jaotise **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaan** > **Kuluprognoosid**.

## <a name="material-estimates"></a>Materjaliprognoosid

Materjalide prognoosid loob projektijuht vahekaardi **Materjalide prognoosid** lehel **Projekti üksikasjad** Dataverse’is. Olulised prognoosikirjed salvestatakse Dataverse’i üksuses **Prognoosirida**. Neil prognoosikirjetel on kandeklass **Materjal** ja need sünkroonitakse üksuste prognoosikirjetega rakendustes Finance and Operations, kus kasutatakse **Materjaliprognooside jaoks projekti integreerimise tabelit (msdyn\_estimatelines)**.

   ![Materjaliprognooside integreerimine](./Media/DW4MaterialEstimates.png)

Topeltkirjutamine sünkroonib materjaliprognoosi kirjed koondtabeliga **ProjForecastSalesImpor** ja seejärel kasutab äriloogikat üksuste prognoosikirjete loomiseks ja värskendamiseks (**ForecastSales**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Äriloogika täidab rakenduses Finance and Operations ühe üksuse prognoosikirje, kasutades seda üksikasja koondtabelis.

Projekti raamatupidaja saab vaadata üksuste prognoosikirjeid rakenduses Finance and Operations, avades jaotise **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaan** > **Üksuse prognoosid**.

## <a name="project-actuals"></a>Projekti tegelikud näitajad

Projekti tegelikud andmed luuakse Dataverse’is aja, kulu, materjalide ja arveldustegevuse põhjal. Selles Dataverse’i olemis hõivatakse kõik nende tehingute tegevusatribuudid, sh kogus, kuluhind, müügihind. Lisateavet vt teemast [Tegelikud näitajad](../actuals/actuals-overview.md). Tegelikud kirjed sünkroonitakse rakendusega Finance and Operations, kasutades edasiseks arvestuseks topeltkirjutamise tabelikaarti **Project Operationsi integreerimise tegelikud näitajad (msdyn\_actuals)**.

   ![Tegelike näitajate integreerimine](./Media/DW4Actuals.png)

Tabelikaart **Project Operationsi integreerimise tegelikud andmed** sünkroonib kõik kirjed Dataverse’i olemi **Tegelikud väärtused** asukohast, atribuudi **Jäta sünkroonimine vahele (ainult sisekasutuseks)** väärtuseks on määratud **Väär**. Atribuudi väärtus seatakse Dataverse’i kirje loomisel automaatselt. Näited, kus selle atribuudi väärtuseks on määratud **Tõene**, on järgmised.

  - Projekti kulude tegelikud andmed ettevõtetevaheliste tehingute puhul. Lisateavet leiate teemast [Ettevõtetevahelise kannete loomine](../project-accounting/create-intercompany-transactions.md). Need kirjed jäetakse vahele, kuna süsteem loob projekti tegelikud rakenduskulud rakenduses Finance and Operations, kui ettevõtetevahelise hankija arve sisestatakse.
  - Negatiivsed arveldamata müügikirjed, mis luuakse pro forma arve kinnitamisel. Need kirjed jäetakse vahele, kuna rakenduste projekti alamtüüp ei tühista arveldamisel arveldamata müügikirjet, vaid muudab selle olekuks rakenduses Finance and Operations täielikult arveldatud.

Topeltkirjutatav tabelikaart sünkroonib tegelike andmete kirjed koondtabeliga **ProjCDSActualsImport**. Neid kirjeid töötleb perioodiline protsess **Impordi koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu. Lisateavet leiate teemast [integreerimise tööleht Project Operationsis](../project-accounting/project-operations-integration-journal.md).

Dataverse hõivab ka projekti tegelike kannete vahelised lingid olemis **Tehingu ühendus**. Lisateavet leiate teemast [Tegelike kirjete linkimine algsete kirjetega](../actuals/linkingactuals.md). Samuti sünkroonitakse tegelike tehingute vahelised lingid rakendusega Finance and Operations, kasutades topeltkirjutamise tabelikaarti **Projekti tehingusuhete integreerimise olem (msdyn\_transactionconnections)**. Neid kirjeid kasutatakse perioodilises protsessis **Importimine koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu.

Project Operationsi integreerimise töölehe ja projekti arve ettepaneku sisestamine käivitab koondtabeli vastavate kirjete värskenduse **ProjCDSActualsImport**. Süsteem hõivab ja salvestab tegelike tehingute jaoks järgmised raamatupidamisatribuudid.

- Raamatupidamisvaluuta summa
- Vahetuskurss
- Kande number
- Käibemaksu summa

**Project Operationsi integreerimise tegelike andmete** tabelikaart värskendab vastavate tegelike andmetega Dataverse’i kirjeid.
