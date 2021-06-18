---
title: Arveldusprotsessi ülevaade
description: Selles teemas antakse arveldustoimingute ülevaade Project Operationsis ressursipõhiste/mittelaopõhiste stsenaariumide korral.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 13f16d42ffdc0a9a6f369c311dfd9e15ad3f7aff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001511"
---
# <a name="invoicing-process-overview"></a>Arveldusprotsessi ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Project Operations ressursipõhistele/mittelaopõhistele stsenaariumidele pakub terviklikke võimalusi, mis on kohandatud nii projektijuhi kui ka müügireskontro administraatori/projekti raamatupidaja vajadustele vastavaks. Arveldusprotsessi jaoks haldab projektijuht projekti arvelduse mahajäämust ja müügireskontro administraator/projekti raamatupidaja loob ühilduva ja täpse kliendile suunatud arvedokumendi.

![Arveldusvoo diagramm](./media/invoicing-flow.png)

Projekti lepingurida määratleb seostatud projektitehingute arveldusmeetodi. Kui projektijuht kiidab aja- ja kulutehingud heaks, salvestab süsteem tehingud olemis **Projekti tegelikud näitajad** ja saadab andmed Dynamics 365 Finance'i moodulisse **Projektijuhtimine ja raamatupidamine**. Seejärel vaatab projekti raamatupidaja kirjed üle ja postitab need [Project Operationsi integreerimise töölehe](../project-accounting/project-operations-integration-journal.md) abil. See tööleht sisaldab projekti tegelike näitajate jaoks olulisi raamatupidamise üksikasju, nagu arveldamine, käibemaksugrupp, arveldusüksuse käibemaksugrupp ja finantsdimensioonid.

Projektijuht arveldamata müügitehingud üle vaadata, kasutades aja- ja materjali arveldusmeetodit jaotises [Aja ja materjali arveldamise võlgnevused](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) ja fikseeritud hinnaga arveldamist jaotises [Fikseeritud hinnaga osamaksed](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Need vaated võimaldavad teil filtreerida ja valida tehinguid, mis tuleb kaasata järgmisesse arveldustsüklisse, ja märkida need siis olekusse **Arveldamiseks valmis**.

Saate [luua käsitsi proforma arve](../proforma-invoicing/create-manual-proforma-invoice.md) või kasutada [perioodilist protsessi](../proforma-invoicing/configure-automated-invoice-creation.md). Projektijuht saab vajadusel [reguleerida ja koostada proforma arve mustandi](../proforma-invoicing/manage-proforma-invoice.md) ja selle siis kinnitada.

Kinnitatud proforma arve saadetakse Finance'i **Projektihalduse ja raamatupidamise** moodulisse. Projekti raamatupidaja vormindab ja värskendab projekti arve ettepanekut ja seejärel sisestab ning prindib dokumendi. Sisestatud projekti arved kirjendatakse pearaamatus ja ka kliendi- ja projekti registrites.


[!INCLUDE[footer-include](../includes/footer-banner.md)]