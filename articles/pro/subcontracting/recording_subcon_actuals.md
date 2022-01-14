---
title: Alltöövõtu komponentide aja, kulude ja materjalikasutuse salvestamine
description: Selles teemas selgitatakse, kuidas Microsoft jälgib alltöövõtukomponentide projektidele salvestatud aega, kulu ja materjalikasutust Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903010"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Alltöövõtukomponentide projektide aja, kulude ja materjalikasutuse registreerimine

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas selgitatakse, kuidas Microsoft jälgib alltöövõtukomponentide projektidele salvestatud aega, kulu ja materjalikasutust Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Alltöövõtja aja kulumine projektidele
Project Operationsis saavad lepingulised töötajad projektidele aega salvestada sarnaselt töötajatega. Projektidele ja/või projektiülesannetele aja sisestamisel saab lepinguline töötaja valida konkreetse allhanke- ja alltöövõturea.

Kui lepinguliste töötajate esitatud aeg kinnitatakse, kirjendatakse projekti maksumus selle lepingulise töötaja ressursi jaoks seadistatud ühiku omahinna alusel **alltöövõtu** ostuhinnakirja jaotises Rollihinnad.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projektide alltöövõtukulude kuluarvestus
Projektidega seotud kulude sisestamisel saate valida kulukandel allhanke- ja alltöövõturea. 

Kui see kulukanne esitatakse ja kinnitatakse, kirjendatakse kulukulu projektile selle kandekategooria jaoks seadistatud ühiku omahinna alusel **alltöövõtu** ostuhinnakirja jaotises Kategooria hinnad.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projektide allhankematerjalide kuluarvestus
Projektide materjalikasutuse sisestamisel saate materjalikasutuse logis valida allhanke- ja alltöövõturea. Materjali kasutuslogi esitamisel ja kinnitamisel kirjendatakse materjalikulu projektile **alltöövõtu hinnakirja jaotises Hinnakirja kaupade jaoks seadistatud ühiku omahinna** alusel.

Materjalikasutust saab salvestada ka projektidesse kirjutamistoodete jaoks. Seda tüüpi materjalikasutust saab linkida ka allhanke- ja alltöövõtuliiniga. Sissekirjutustoodete materjalikasutuse salvestamisel peate sisestama sissekirjutustoote ühikuhinna. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
