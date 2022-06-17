---
title: Allhankelepinguga komponentide aja, kulude ja materjalikasutuse kirjendamine
description: Selles artiklis selgitatakse, kuidas Microsoft jälgib allhankekomponentide projektidele salvestatud aega, kulusid ja materjalikasutust Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927645"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Allhankekomponentide projektide aja, kulude ja materjalikasutuse registreerimine

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles artiklis selgitatakse, kuidas Microsoft jälgib allhankekomponentide projektidele salvestatud aega, kulusid ja materjalikasutust Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Alltöövõtja aja kulu projektidele
Projektitoimingutes saavad lepingulised töötajad projektidele aega salvestada sarnaselt töötajatega. Projektidele ja/või projektiülesannetele aja sisestamisel saab lepinguline töötaja valida kindla alltöövõtu- ja alltöövõturea.

Kui lepinguliste töötajate esitatud aeg kinnitatakse, kirjendatakse projekti maksumus selle lepingutöötaja ressursi **jaoks seadistatud ühiku omahinna määra abil allhanke ostuhinna loendi jaotises Rollihinnad**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projektide allhankekulude maksumus
Projektidega seotud kulude sisestamisel saate kulukandel valida alltöövõtu- ja alltöövõturea. 

Kui see kulukanne esitatakse ja kinnitatakse, kirjendatakse kulukulu projektile, mis põhineb ühiku omahinnal, mis on seadistatud selle kandekategooria **jaoks allhanke ostuhinnastiku jaotises Kategooria hinnad**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projektide allhankematerjalide maksumus
Projektide materjalikasutuse sisestamisel saate materjali kasutuslogist valida alltöövõtu- ja alltöövõturea. Materjali kasutuslogi esitamisel ja kinnitamisel kirjendatakse materjalikulu projektile vastavalt ühiku omahinnale, mis on selle toote **jaoks seadistatud allhanke hinnakirja hinnakirja hinnakirja jaotises**.

Materjalikasutust saab salvestada ka projektidesse kirjutamiseks. Seda tüüpi materjalikasutust saab linkida ka alltöövõtu- ja alltöövõtuliiniga. Sissekirjutustoodete materjalikasutuse salvestamisel peate sisestama sissekirjutustoote ühiku omahinna. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
