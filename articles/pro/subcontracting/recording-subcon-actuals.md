---
title: Allhankelepinguga komponentide aja, kulude ja materjalikasutuse kirjendamine
description: Selles teemas selgitatakse, kuidas Microsoft jälgib allhankekomponentide projektidele salvestatud aega, kulusid ja materjalikasutust Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599219"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Allhankekomponentide projektide aja, kulude ja materjalikasutuse registreerimine

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas selgitatakse, kuidas Microsoft jälgib allhankekomponentide projektidele salvestatud aega, kulusid ja materjalikasutust Dynamics 365 Project Operations.

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
