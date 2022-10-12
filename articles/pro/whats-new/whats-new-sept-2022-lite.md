---
title: Mis on uut septembris 2022 – Project Operationsi lihtjuurutamine
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsoft Dynamics 365 Project Operations lite’i juurutuse 2022. aasta septembri väljaandes.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621325"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Mis on uut septembris 2022 – Project Operationsi lihtjuurutamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

See artikkel kehtib microsofti järgmiste komponentide ja versioonide kohta Dynamics 365 Project Operations:

- Projektitoimingud keskkonnaversioonis Dataverse 4.46.0.60

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Müügivõimaluse haldus | **Tsitaatide läbivaatamine ja aktiveerimine**<br>Project Operations toob müügiprotsessi täieliku toe. Projekti hinnapakkumisi saab aktiveerida, et esindada olekut, kus hinnapakkumine on kirjutuskaitstud ja seda vaadatakse üle. Aktiveeritud hinnapakkumisi saab muuta, et luua uusi hinnapakkumisi, millel on astmeline parandusnumber. Aktiveeritud projekti hinnapakkumisi või hinnapakkumisi saab sulgeda kui võidetud või kaotatud. | [Projekti hinnapakkumise aktiveerimine ja kontrollimine](/dynamics365/project-operations/sales/activation-and-revision) |
| Arveldamine ja hinnakujundus | **Ajavööndi agnostiline hind on vaikimisi**<br>Project Operations on võtnud kasutusele ajavööndi agnostilise kuupäeva kontseptsiooni kõigil projekti tegelikel osadel. Uus väli **Kande kuupäev** on nüüd saadaval töölehe ridadel ja tegelikel andmetel ning seda kasutatakse kande toimumise kuupäeva salvestamiseks, kuid ilma seda kuupäeva koordineeritud maailmaajaks teisendamata. Seda kuupäeva kasutatakse järgmise etapi protsesside jaoks, nagu hinna vaikeväärtuse määramine ja arve loomine. | <p>[Projektipõhiste prognooside ja tegelike kulude määra määramine](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projektipõhiste prognooside ja tegelike hindade müügihindade määramine](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Arveldamine ja hinnakujundus | **Jõustumiskuupäeva hinna alistamised Project Operationsis**<br>Jõustumiskuupäevaga hinna alistamised võimaldavad hinnakirjas konkreetseid hindu alistada või muuta. | [Jõustumiskuupäevaga hinna alistamised](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Aeg ja kulu | **Globaalne kinnitaja**<br>See funktsioon võimaldab sõltumatut tarkvaratarnijat (ISV) ja tsentraliseeritud kinnitamist, olenemata projekti või meeskonnaliikme staatusest projektis. | [Turve ja kinnitused](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2754422 | Materjali- ja kuluprognoosid ei liigu projektide kopeerimisel Dataverse Dynamics 365 Finance. |
| Aeg ja kulu | 2787409 | Mittekehtiv kinnitaja saab kinnitada projektivälise ajakirje. |
| Müügivõimaluse haldus | 2788907 | Värskendatud tõrketeade kordumatuse valideerimise kohta tellimusridade puhul, mis sisaldavad lippe. |
| Aeg ja kulu | 2842253 | Null erandi käsitlemine aja kinnitamiseks. |
| Arveldamine ja hinnakujundus | 2844181 | Korrelatsiooni ID mittesaamine blokeerib arve loomise. |
| Arveldamine ja hinnakujundus | 2876628 | QLD, CLD – hinnanguline hinnakirja lahendus peaks kasutama hinnakirja varasema kuupäevavahemiku välju. |
| Allhanked | 2893222 | Kui allhankeliinile ei ole rolli määratud, peaks olema võimalik valida see rida meeskonnaliikmel mis tahes rolli jaoks. |
