---
title: Projekti prognooside ja tegelike andmete integreerimine
description: See artikkel annab teavet rakenduse Project Operations topeltkirjutuse integreerimise kohta projekti prognooside ja tegelike näitajate puhul.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029075"
---
# <a name="project-estimates-and-actuals-integration"></a>Projekti prognooside ja tegelike andmete integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

See artikkel annab teavet rakenduse Project Operations topeltkirjutuse integreerimise kohta projekti prognooside ja tegelike näitajate puhul.

## <a name="project-estimates"></a>Projekti prognoosid

Projekti tööjõu-, kulu- ja materjaliprognoosid luuakse ning neid hallatakse rakenduses Microsoft Dataverse ja sünkroonitakse finants- ja äritoimingute rakendustega raamatupidamisarvestuse eesmärgil. Finants- ja äritoimingute rakendused ei toetata loomise, värskendamise ja kustutamise toiminguid.

Prognooside loomiseks on projekti jaoks vaja kehtivat raamatupidamiskonfiguratsiooni. Lepinguridadega seostatud projektidel peab olema kehtiv projekti kulu- ja tuluprofiil, mis on määratletud projekti kulu- ja tuluprofiili reeglites. Lisateavet leiate teemast [Arveldatavate projektide raamatupidamisarvestuse konfigureerimine](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Tööjõu prognoosid

Tööjõu prognoosid loob projektijuht või ressursihaldur, kes määrab projekti ülesandele ka üldise või nimelise ressursi. Ressursi määramise kirjeid saab üle vaadata vahekaardil **Ressursi määramine** lehel **Projekti üksikasjad** Dataverse’is. Ressursi määramise kirjed teenuses Dataverse loovad tunniprognoosi kirjed finants- ja äritoimingute rakendustes, kasutades **Project Operationsi integreerimise üksust tunniprognoosideks (msdyn\_resourceassignments)**.

   ![Tööjõu prognooside integreerimine.](./Media/DW4LaborEstimates.png)

Topeltkirjutuse abil sünkroonitakse ressursi määramise kirjed koondtabeliga (**ProjCDSEstimateHoursImport**) ja seejärel kasutatakse äriloogikat tunniprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastEmpl**).

Projekti raamatupidaja vaatab finants- ja äritoimingute rakendustes loodud prognoositundide kirjed üle, minnes jaotisesse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaan** > **Tunniprognoosid**.

## <a name="expense-estimates"></a>Kuluprognoosid

Projektijuht loob kuluprognoosid vahekaardil **Kuluprognoos** lehel **Projekti üksikasjad** Dataverse’is. Kuluprognoosi kirjed salvestatakse Dataverse’is olemisse **Prognoosirida**. Need prognoosikirjed on kirjeklassiga **Kulu** ja sünkroonitakse finants- ja äritoimingute rakendused kuluprognoosi kirjetega, kasutades **Kuluprognooside rakenduse Project Operations integreerimise üksus (msdyn\_estimatelines)**.

   ![Kuluprognooside integreerimine.](./Media/DW4ExpenseEstimates.png)

Topeltkirjutamine sünkroonib kuluprognoosi kirjed koondtabeliga **ProjCDSEstimateExpenseImport)** ja seejärel kasutab äriloogikat kuluprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastCost**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Äriloogika täidab finants- ja äritoimingute rakendustes ühe kuluprognoosi kirje, kasutades seda üksikasja koondtabelis.

Projekti raamatupidaja saab vaadata kuluprognoosi kirjeid finants- ja äritoimingute rakendustes, avades jaotise **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaan** > **Kuluprognoosid**.

## <a name="material-estimates"></a>Materjaliprognoosid

Materjalide prognoosid loob projektijuht vahekaardi **Materjalide prognoosid** lehel **Projekti üksikasjad** Dataverse’is. Olulised prognoosikirjed salvestatakse Dataverse’i üksuses **Prognoosirida**. Neil prognoosikirjetel on kirjeklass **Materjal** ja need sünkroonitakse üksuste prognoosikirjetega finants- ja äritoimingute rakendustes, kus kasutatakse **Materjaliprognooside jaoks projekti integreerimise tabelit (msdyn\_estimatelines)**.

   ![Materjaliprognooside integreerimine.](./Media/DW4MaterialEstimates.png)

Topeltkirjutamine sünkroonib materjaliprognoosi kirjed koondtabeliga **ProjForecastSalesImpor** ja seejärel kasutab äriloogikat üksuste prognoosikirjete loomiseks ja värskendamiseks (**ForecastSales**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Äriloogika täidab finants- ja äritoimingute rakendustes ühe kaubaprognoosi kirje, kasutades seda üksikasja koondtabelis.

Projekti raamatupidaja saab vaadata kaubaprognoosi kirjeid finants- ja äritoimingute rakendustes, avades jaotise **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaan** > **Kaubaprognoosid**.

## <a name="project-actuals"></a>Projekti tegelikud näitajad

Projekti tegelikud andmed luuakse Dataverse’is aja, kulu, materjalide ja arveldustegevuse põhjal. Selles Dataverse’i olemis hõivatakse kõik nende tehingute tegevusatribuudid, sh kogus, kuluhind, müügihind. Lisateavet vt teemast [Tegelikud näitajad](../actuals/actuals-overview.md). Tegelikud kirjed sünkroonitakse finants- ja äritoimingute rakendustega, kasutades edasiseks arvestuseks topeltkirjutuse tabelikaarti **Project Operationsi integreerimise tegelikud näitajad (msdyn\_tegelikud näitajad)**.

   ![Tegelike näitajate integreerimine.](./Media/DW4Actuals.png)

Tabelikaart **Project Operationsi integreerimise tegelikud andmed** sünkroonib kõik kirjed Dataverse’i olemi **Tegelikud väärtused** asukohast, atribuudi **Jäta sünkroonimine vahele (ainult sisekasutuseks)** väärtuseks on määratud **Väär**. Atribuudi väärtus seatakse Dataverse’i kirje loomisel automaatselt. Näited, kus selle atribuudi väärtuseks on määratud **Tõene**, on järgmised.

  - Projekti kulude tegelikud andmed ettevõtetevaheliste tehingute puhul. Lisateavet leiate teemast [Ettevõtetevahelise kannete loomine](../project-accounting/create-intercompany-transactions.md). Need kirjed jäetakse vahele, kuna süsteem loob kontsernisisese hankija arve postitamisel finants- ja äritoimingute rakendustes uuesti projekti kulu tegelik näitaja.
  - Negatiivsed arveldamata müügikirjed, mis luuakse pro forma arve kinnitamisel. Need kirjed jäetakse vahele, kuna rakenduste projekti alamtüüp ei tühista arveldamisel arveldamata müügikirjet, vaid muudab selle olekuks finants- ja äritoimingute rakendustes täielikult arveldatud.

Topeltkirjutatav tabelikaart sünkroonib tegelike andmete kirjed koondtabeliga **ProjCDSActualsImport**. Neid kirjeid töötleb perioodiline protsess **Impordi koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu. Lisateavet leiate teemast [integreerimise tööleht Project Operationsis](../project-accounting/project-operations-integration-journal.md).

Dataverse hõivab ka projekti tegelike kannete vahelised lingid olemis **Tehingu ühendus**. Lisateavet leiate teemast [Tegelike kirjete linkimine algsete kirjetega](../actuals/linkingactuals.md). Samuti sünkroonitakse tegelike tehingute vahelised lingid finants- ja äritoimingute rakendustega, kasutades topeltkirjutuse tabelikaarti **Projekti tehingusuhete integreerimise olem (msdyn\_transactionconnections)**. Neid kirjeid kasutatakse perioodilises protsessis **Importimine koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu.

Project Operationsi integreerimise töölehe ja projekti arve ettepaneku sisestamine käivitab koondtabeli vastavate kirjete värskenduse **ProjCDSActualsImport**. Süsteem hõivab ja salvestab tegelike tehingute jaoks järgmised raamatupidamisatribuudid.

- Raamatupidamisvaluuta summa
- Vahetuskurss
- Kande number
- Käibemaksu summa

**Project Operationsi integreerimise tegelike andmete** tabelikaart värskendab vastavate tegelike andmetega Dataverse’i kirjeid.
