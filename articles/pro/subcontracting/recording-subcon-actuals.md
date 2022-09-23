---
title: Allhankelepinguga komponentide aja, kulude ja materjalikasutuse kirjendamine
description: Selles artiklis selgitatakse, kuidas Microsoft jälgib allhankekomponentidest projektidesse salvestatud aega, kulusid ja materjalikasutust Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522508"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Allhankekomponentide projektide aja, kulude ja materjalikasutuse registreerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Selles artiklis selgitatakse, kuidas Microsoft jälgib allhankekomponentidest projektidesse salvestatud aega, kulusid ja materjalikasutust Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Alltöövõtja aja kulu arvestamine projektidele
Rakenduses Project Operations saavad lepingulised töötajad salvestada projektide aega sarnaselt töötajatega. Projektide ja/või projektiülesannete aja sisestamisel saab lepinguline töötaja valida konkreetse allhanke- ja allhankerea.

Kui lepinguliste töötajate esitatud aeg on kinnitatud, salvestatakse projekti kulu ühiku kulumäära abil, mis on seadistatud sellele lepingulise töötaja ressursile **allhankelepingu ostuhinnaloendi jaotises Rollihinnad**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projektide alltöövõtukulude kuluarvestus
Projektidega seotud kulude sisestamisel saate kulukirjel valida allhanke ja allhanke rea. 

Kui see kulukirje on esitatud ja kinnitatud, registreeritakse kulukulu projektis **ühikukulu alusel, mis on selle kandekategooria jaoks seadistatud allhanke allhankelepingu ostuhinnaloendi jaotises Kategooria hinnad**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projektide allhangete materjalide maksumuse arvestamine
Projektide materjalikasutuse sisestamisel saate materjalikasutuse logis valida allhanke ja allhanke rea. Kui materjali kasutamise logi on esitatud ja kinnitatud, salvestatakse materjalikulu projektis **ühikuhinna alusel, mis on seadistatud sellele tootele allhanke hinnakirja jaotises Hinnakirjaüksused**.

Materjalikasutust saab salvestada ka projektide toodete sissekirjutamiseks. Seda tüüpi materjalikasutust saab siduda ka allhanke- ja allhankeliiniga. Sissekirjutustoodete materjalikasutuse registreerimisel peate sisestama sissekirjutatava toote ühikuhinna. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
