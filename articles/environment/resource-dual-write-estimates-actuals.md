---
title: Projekti prognooside ja tegelike andmete integreerimine
description: Selles teemas antakse teavet Project Operationsi topeltkirjutamise integreerimise kohta projekti prognooside ja tegelike andmete puhul.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577185"
---
# <a name="project-estimates-and-actuals-integration"></a>Projekti prognooside ja tegelike andmete integreerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas antakse teavet Project Operationsi topeltkirjutamise integreerimise kohta projekti prognooside ja tegelike andmete puhul.

## <a name="project-estimates"></a>Projekti prognoosid

Projekti tööjõu-, kulu- ja materjalihinnangud luuakse ja säilitatakse raamatupidamise eesmärgil rakendustes Microsoft Dataverse Finance and Operations ning sünkroonitakse nendega. Finance and Operationsi rakenduste kaudu ei toetata toimingute loomist, värskendamist ja kustutamist.

Prognooside loomiseks on projekti jaoks vaja kehtivat raamatupidamiskonfiguratsiooni. Lepinguridadega seostatud projektidel peab olema kehtiv projekti kulu- ja tuluprofiil, mis on määratletud projekti kulu- ja tuluprofiili reeglites. Lisateavet leiate teemast [Arveldatavate projektide raamatupidamisarvestuse konfigureerimine](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Tööjõu prognoosid

Tööjõu prognoosid loob projektijuht või ressursihaldur, kes määrab projekti ülesandele ka üldise või nimelise ressursi. Ressursi määramise kirjeid saab üle vaadata vahekaardil **Ressursi määramine** lehel **Projekti üksikasjad** Dataverse’is. Ressursimäärangu kirjed Dataverse tunniprognoosi kirjete loomisel rakendustes Finance and Operations rakendustes, kasutades **projektioperatsioonide integreerimise olemit tunnihinnangute jaoks (msdyn\_ resourceassignments)**.

   ![Tööjõu prognooside integreerimine.](./Media/DW4LaborEstimates.png)

Topeltkirjutuse abil sünkroonitakse ressursi määramise kirjed koondtabeliga (**ProjCDSEstimateHoursImport**) ja seejärel kasutatakse äriloogikat tunniprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastEmpl**).

Projekti raamatupidaja vaatab üle rakendustes Finance and Operations loodud prognoosi tunnikirjed, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaani** > **tunni prognoosid**.

## <a name="expense-estimates"></a>Kuluprognoosid

Projektijuht loob kuluprognoosid vahekaardil **Kuluprognoos** lehel **Projekti üksikasjad** Dataverse’is. Kuluprognoosi kirjed salvestatakse Dataverse’is olemisse **Prognoosirida**. Nendel hinnangukirjetel on kandeklass Kulu **ja** need sünkroonitakse kuluprognoosi kirjetega rakendustes Finance and Operations, kasutades **kuluprognooside jaoks project Operationsi integratsiooniolemit (msdyn\_ estimatelines)**.

   ![Kuluprognooside integreerimine.](./Media/DW4ExpenseEstimates.png)

Topeltkirjutamine sünkroonib kuluprognoosi kirjed koondtabeliga **ProjCDSEstimateExpenseImport)** ja seejärel kasutab äriloogikat kuluprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastCost**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Finance and Operationsi rakenduste äriloogika asustab ühe kuluprognoosi kirje, kasutades seda detaili lavastustabelis.

Projekti raamatupidaja saab vaadata kuluprognoosi kirjeid rakendustes Finance and Operations, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaani** > **kuluprognoose**.

## <a name="material-estimates"></a>Materjaliprognoosid

Materjalide prognoosid loob projektijuht vahekaardi **Materjalide prognoosid** lehel **Projekti üksikasjad** Dataverse’is. Olulised prognoosikirjed salvestatakse Dataverse’i üksuses **Prognoosirida**. Nendel hinnangukirjetel on kandeklass Materjal **ja** need sünkroonitakse kaubaprognoosi kirjetega rakendustes Finance and Operations, kasutades **materjalihinnangute jaoks projecti integratsioonitabelit (msdyn\_ estimatelines)**.

   ![Materjaliprognooside integreerimine.](./Media/DW4MaterialEstimates.png)

Topeltkirjutamine sünkroonib materjaliprognoosi kirjed koondtabeliga **ProjForecastSalesImpor** ja seejärel kasutab äriloogikat üksuste prognoosikirjete loomiseks ja värskendamiseks (**ForecastSales**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Rakenduste Finance and Operations äriloogika asustab ühe kaubaprognoosi kirje, kasutades seda detaili lavastustabelis.

Projekti raamatupidaja saab vaadata kaubaprognoosi kirjeid rakendustes Finance and Operations, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaani** > **kaubaprognoose**.

## <a name="project-actuals"></a>Projekti tegelikud näitajad

Projekti tegelikud andmed luuakse Dataverse’is aja, kulu, materjalide ja arveldustegevuse põhjal. Selles Dataverse’i olemis hõivatakse kõik nende tehingute tegevusatribuudid, sh kogus, kuluhind, müügihind. Lisateavet vt teemast [Tegelikud näitajad](../actuals/actuals-overview.md). Tegelikud kirjed sünkroonitakse rakendustega Finance and Operations, kasutades järgmise etapi arvestuse jaoks kahe kirjutamisega tabelikaarti **Project Operations integration actuals (msdyn\_ actuals).**

   ![Tegelike näitajate integreerimine.](./Media/DW4Actuals.png)

Tabelikaart **Project Operationsi integreerimise tegelikud andmed** sünkroonib kõik kirjed Dataverse’i olemi **Tegelikud väärtused** asukohast, atribuudi **Jäta sünkroonimine vahele (ainult sisekasutuseks)** väärtuseks on määratud **Väär**. Atribuudi väärtus seatakse Dataverse’i kirje loomisel automaatselt. Näited, kus selle atribuudi väärtuseks on määratud **Tõene**, on järgmised.

  - Projekti kulude tegelikud andmed ettevõtetevaheliste tehingute puhul. Lisateavet leiate teemast [Ettevõtetevahelise kannete loomine](../project-accounting/create-intercompany-transactions.md). Need kirjed jäetakse vahele, kuna süsteem taastab kontsernisisese hankija arve konteerimisel rakenduses Finance and Operations tegeliku projekti maksumuse.
  - Negatiivsed arveldamata müügikirjed, mis luuakse pro forma arve kinnitamisel. Need kirjed jäetakse vahele, kuna projekti alamledger rakendustes Finance and Operations ei tühista arveldamata müügikirjet, vaid muudab olekuks täielikult arveldatud.

Topeltkirjutatav tabelikaart sünkroonib tegelike andmete kirjed koondtabeliga **ProjCDSActualsImport**. Neid kirjeid töötleb perioodiline protsess **Impordi koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu. Lisateavet leiate teemast [integreerimise tööleht Project Operationsis](../project-accounting/project-operations-integration-journal.md).

Dataverse hõivab ka projekti tegelike kannete vahelised lingid olemis **Tehingu ühendus**. Lisateavet leiate teemast [Tegelike kirjete linkimine algsete kirjetega](../actuals/linkingactuals.md). Tegelike kannete vahelised seosed sünkroonitakse ka rakendustega Finance and Operations, kasutades kahe kirjutamisega tabelikaarti, **projektikannete seoste integratsiooniolemit (msdyn\_ transactionconnections)**. Neid kirjeid kasutatakse perioodilises protsessis **Importimine koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu.

Project Operationsi integreerimise töölehe ja projekti arve ettepaneku sisestamine käivitab koondtabeli vastavate kirjete värskenduse **ProjCDSActualsImport**. Süsteem hõivab ja salvestab tegelike tehingute jaoks järgmised raamatupidamisatribuudid.

- Raamatupidamisvaluuta summa
- Vahetuskurss
- Kande number
- Käibemaksu summa

**Project Operationsi integreerimise tegelike andmete** tabelikaart värskendab vastavate tegelike andmetega Dataverse’i kirjeid.
