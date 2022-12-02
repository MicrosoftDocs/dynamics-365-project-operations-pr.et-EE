---
title: Arveldusprotsessi ülevaade
description: See artikkel annab arveldustoimingute ülevaate rakenduses Project Operations ressursipõhiste/mittelaopõhiste stsenaariumide korral.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923091"
---
# <a name="invoicing-process-overview"></a>Arveldusprotsessi ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Project Operations ressursipõhistele/mittelaopõhistele stsenaariumidele pakub terviklikke võimalusi, mis on kohandatud nii projektijuhi kui ka müügireskontro administraatori/projekti raamatupidaja vajadustele vastavaks. Arveldusprotsessi jaoks haldab projektijuht projekti arvelduse mahajäämust ja müügireskontro administraator/projekti raamatupidaja loob ühilduva ja täpse kliendile suunatud arvedokumendi.

![Arveldusvoo diagramm.](./media/invoicing-flow.png)

Projekti lepingurida määratleb seostatud projektitehingute arveldusmeetodi. Kui projektijuht kiidab aja- ja kulutehingud heaks, salvestab süsteem tehingud olemis **Projekti tegelikud näitajad** ja saadab andmed Dynamics 365 Finance’i moodulisse **Projektijuhtimine ja raamatupidamine**. Seejärel vaatab projekti raamatupidaja kirjed üle ja postitab need [Project Operationsi integreerimise töölehe](../project-accounting/project-operations-integration-journal.md) abil. See tööleht sisaldab projekti tegelike näitajate jaoks olulisi raamatupidamise üksikasju, nagu arveldamine, käibemaksu rühm, arveldusüksuse käibemaksu rühm ja finantsdimensioonid.

Projektijuht arveldamata müügitehingud üle vaadata, kasutades aja- ja materjali arveldusmeetodit jaotises [Aja ja materjali arveldamise võlgnevused](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) ja fikseeritud hinnaga arveldamist jaotises [Fikseeritud hinnaga osamaksed](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Need vaated võimaldavad teil filtreerida ja valida tehinguid, mis tuleb kaasata järgmisesse arveldustsüklisse, ja märkida need siis olekusse **Arveldamiseks valmis**.

Saate [luua käsitsi proforma arve](../proforma-invoicing/create-manual-proforma-invoice.md) või kasutada [perioodilist protsessi](../proforma-invoicing/configure-automated-invoice-creation.md). Projektijuht saab vajadusel [reguleerida ja koostada proforma arve mustandi](../proforma-invoicing/manage-proforma-invoice.md) ja selle siis kinnitada.

Kinnitatud proforma arve saadetakse Finance'i **Projektihalduse ja raamatupidamise** moodulisse. Projekti raamatupidaja vormindab ja värskendab projekti arve ettepanekut ja seejärel sisestab ning prindib dokumendi. Sisestatud projekti arved kirjendatakse pearaamatus ja ka kliendi- ja projekti registrites.


[!INCLUDE[footer-include](../includes/footer-banner.md)]