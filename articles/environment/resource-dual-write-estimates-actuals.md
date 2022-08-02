---
title: Projekti prognooside ja tegelike andmete integreerimine
description: See artikkel annab teavet Project Operationsi topeltkirjutusega integreerimise kohta projekti prognooside ja tegelike näitajate jaoks.
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

See artikkel annab teavet Project Operationsi topeltkirjutusega integreerimise kohta projekti prognooside ja tegelike näitajate jaoks.

## <a name="project-estimates"></a>Projekti prognoosid

Projekti tööjõu-, kulu- ja materjaliprognoosid luuakse ja säilitatakse Microsoft Dataverse ning sünkroonitakse raamatupidamise eesmärgil finants- ja toimingurakendustega. Toimingute loomist, värskendamist ja kustutamist ei toetata finance and operationsi rakenduste kaudu.

Prognooside loomiseks on projekti jaoks vaja kehtivat raamatupidamiskonfiguratsiooni. Lepinguridadega seostatud projektidel peab olema kehtiv projekti kulu- ja tuluprofiil, mis on määratletud projekti kulu- ja tuluprofiili reeglites. Lisateavet leiate teemast [Arveldatavate projektide raamatupidamisarvestuse konfigureerimine](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Tööjõu prognoosid

Tööjõu prognoosid loob projektijuht või ressursihaldur, kes määrab projekti ülesandele ka üldise või nimelise ressursi. Ressursi määramise kirjeid saab üle vaadata vahekaardil **Ressursi määramine** lehel **Projekti üksikasjad** Dataverse’is. Ressursimääramise kirjed, et Dataverse luua tunniprognoosi kirjeid finance and operationsi rakendustes, kasutades **Tunniprognooside jaoks Project Operationsi integratsiooni olemit (msdyn\_ resourceassignments)**.

   ![Tööjõu prognooside integreerimine.](./Media/DW4LaborEstimates.png)

Topeltkirjutuse abil sünkroonitakse ressursi määramise kirjed koondtabeliga (**ProjCDSEstimateHoursImport**) ja seejärel kasutatakse äriloogikat tunniprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastEmpl**).

Projekti raamatupidaja vaatab üle finance and operationsi rakendustes loodud prognoositud tunnikirjed, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaani** > **tunni prognoosid**.

## <a name="expense-estimates"></a>Kuluprognoosid

Projektijuht loob kuluprognoosid vahekaardil **Kuluprognoos** lehel **Projekti üksikasjad** Dataverse’is. Kuluprognoosi kirjed salvestatakse Dataverse’is olemisse **Prognoosirida**. Nendel prognoosikirjetel on kandeklass **Kulu** ja need sünkroonitakse kuluprognoosi kirjetega finance and operationsi rakendustes, kasutades **kuluprognooside jaoks Project Operationsi integratsiooni olemit (msdyn-i\_ prognoosiread).**

   ![Kuluprognooside integreerimine.](./Media/DW4ExpenseEstimates.png)

Topeltkirjutamine sünkroonib kuluprognoosi kirjed koondtabeliga **ProjCDSEstimateExpenseImport)** ja seejärel kasutab äriloogikat kuluprognoosi kirjete loomiseks ja värskendamiseks (**ProjForecastCost**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Finance and Operationsi rakenduste äriloogika täidab ühe kuluprognoosi kirje, kasutades koondamistabelis seda detaili.

Projekti raamatupidaja saab kuluprognoosi kirjeid finance and operationsi rakendustes üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaani** > **kuluprognoosid**.

## <a name="material-estimates"></a>Materjaliprognoosid

Materjalide prognoosid loob projektijuht vahekaardi **Materjalide prognoosid** lehel **Projekti üksikasjad** Dataverse’is. Olulised prognoosikirjed salvestatakse Dataverse’i üksuses **Prognoosirida**. Nendel hinnangukirjetel on kandeklass **Materjal** ja need sünkroonitakse kaubaprognoosi kirjetega finance and operationsi rakendustes, kasutades **projekti integratsioonitabelit materjaliprognooside jaoks (msdyn-i\_ prognoosiread).**

   ![Materjaliprognooside integreerimine.](./Media/DW4MaterialEstimates.png)

Topeltkirjutamine sünkroonib materjaliprognoosi kirjed koondtabeliga **ProjForecastSalesImpor** ja seejärel kasutab äriloogikat üksuste prognoosikirjete loomiseks ja värskendamiseks (**ForecastSales**). Prognoosiread salvestavad müügiprognoosi ja kuluprognoosi kirjed eraldi. Finance and Operationsi rakenduste äriloogika täidab koondamistabelis seda detaili kasutades ühe üksuse prognoosikirje.

Projekti raamatupidaja saab kaubaprognoosi kirjeid finance and operationsi rakendustes üle vaadata, minnes jaotisse **Projektihaldus ja raamatupidamine** > **Kõik projektid** > **Plaani** > **kauba prognoosid**.

## <a name="project-actuals"></a>Projekti tegelikud näitajad

Projekti tegelikud andmed luuakse Dataverse’is aja, kulu, materjalide ja arveldustegevuse põhjal. Selles Dataverse’i olemis hõivatakse kõik nende tehingute tegevusatribuudid, sh kogus, kuluhind, müügihind. Lisateavet vt teemast [Tegelikud näitajad](../actuals/actuals-overview.md). Tegelikud kirjed sünkroonitakse finants- ja operatsioonirakendustega, kasutades järgneva arvestuse jaoks kahekordse kirjutustabeli kaarti **Project Operations integration actuals (msdyn\_ actuals).**

   ![Tegelike näitajate integreerimine.](./Media/DW4Actuals.png)

Tabelikaart **Project Operationsi integreerimise tegelikud andmed** sünkroonib kõik kirjed Dataverse’i olemi **Tegelikud väärtused** asukohast, atribuudi **Jäta sünkroonimine vahele (ainult sisekasutuseks)** väärtuseks on määratud **Väär**. Atribuudi väärtus seatakse Dataverse’i kirje loomisel automaatselt. Näited, kus selle atribuudi väärtuseks on määratud **Tõene**, on järgmised.

  - Projekti kulude tegelikud andmed ettevõtetevaheliste tehingute puhul. Lisateavet leiate teemast [Ettevõtetevahelise kannete loomine](../project-accounting/create-intercompany-transactions.md). Need kirjed jäetakse vahele, kuna süsteem loob kontsernisisese hankija arve sisestamisel finance and operationsi rakendustes projekti tegeliku kulu uuesti.
  - Negatiivsed arveldamata müügikirjed, mis luuakse pro forma arve kinnitamisel. Need kirjed jäetakse vahele, kuna projekti alamliider finance and operationsi rakendustes ei tühista arveldamisel arveldamata müügikirjet, vaid muudab olekut täielikult arveldatuks.

Topeltkirjutatav tabelikaart sünkroonib tegelike andmete kirjed koondtabeliga **ProjCDSActualsImport**. Neid kirjeid töötleb perioodiline protsess **Impordi koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu. Lisateavet leiate teemast [integreerimise tööleht Project Operationsis](../project-accounting/project-operations-integration-journal.md).

Dataverse hõivab ka projekti tegelike kannete vahelised lingid olemis **Tehingu ühendus**. Lisateavet leiate teemast [Tegelike kirjete linkimine algsete kirjetega](../actuals/linkingactuals.md). Tegelike kannete vahelised seosed sünkroonitakse ka finants- ja toimingurakendustega, kasutades topeltkirjutustabeli kaarti, **projekti kannete seoste integratsiooniolemit (msdyn\_ transactionconnections).** Neid kirjeid kasutatakse perioodilises protsessis **Importimine koondtabelist**, kui loote Project Operationsi integreerimise töölehe ridu ja projekti arve ridu.

Project Operationsi integreerimise töölehe ja projekti arve ettepaneku sisestamine käivitab koondtabeli vastavate kirjete värskenduse **ProjCDSActualsImport**. Süsteem hõivab ja salvestab tegelike tehingute jaoks järgmised raamatupidamisatribuudid.

- Raamatupidamisvaluuta summa
- Vahetuskurss
- Kande number
- Käibemaksu summa

**Project Operationsi integreerimise tegelike andmete** tabelikaart värskendab vastavate tegelike andmetega Dataverse’i kirjeid.
