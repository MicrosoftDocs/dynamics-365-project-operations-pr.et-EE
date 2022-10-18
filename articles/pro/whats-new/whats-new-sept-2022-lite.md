---
title: Mis on uut septembris 2022 – Project Operationsi lihtjuurutamine
description: Sellest artiklist leiate teavet kvaliteedivärskenduste kohta, mis on saadaval Microsofti Dynamics 365 Project Operations lite-juurutuse 2022. aasta septembri väljaandes.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634847"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Mis on uut septembris 2022 – Project Operationsi lihtjuurutamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

See artikkel kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projekti toimingud keskkonnaversioonis Dataverse 4.46.0.60

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Müügivõimaluse haldus | **Hinnapakkumiste läbivaatamine ja aktiveerimine**<br>Project Operations pakub müügiprotsessile täielikku tuge. Projekti hinnapakkumisi saab aktiveerida, et need esindaksid olekut, kus hinnapakkumine on kirjutuskaitstud ja seda vaadatakse üle. Aktiveeritud hinnapakkumisi saab muuta, et luua uusi hinnapakkumisi, millel on suurendatud paranduste arv. Aktiveeritud projekti hinnapakkumisi või hinnapakkumiste parandusi saab sulgeda võidetuna või kaotatuna. | [Projekti hinnapakkumise aktiveerimine ja kontrollimine](/dynamics365/project-operations/sales/activation-and-revision) |
| Arveldamine ja hinnakujundus | **Ajavööndi agnostiline hinna vaikimisi jätmine**<br>Project Operations on kasutusele võtnud ajavööndi agnostilise kuupäeva kontseptsiooni kõigil projekti tegelikel andmetel. Uus väli Kande **kuupäev** on nüüd saadaval töölehe ridadel ja tegelikes väärtustes ning seda kasutatakse kande toimumise kuupäeva salvestamiseks, kuid ilma seda kuupäeva kooskõlastatud maailmaajaks teisendamata. Seda kuupäeva kasutatakse järgmiste protsesside jaoks, nagu hinna vaikimisi jätmine ja arve loomine. | <p>[Projektipõhiste hinnangute ja tegelike kulude määrade määramine](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projektipõhiste hinnangute ja tegelike näitajate müügihindade määramine](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Arveldamine ja hinnakujundus | **Kuupäevaga kehtivad hinnaalistamised Project Operationsis**<br>Kuupäeval kehtivad hinna alistamised annavad võimaluse hinnakirjas teatud hindu alistada või muuta. | [Kuupäeval kehtivad hinna alistamised](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Aeg ja kulu | **Globaalne kinnitaja**<br>See funktsioon võimaldab sõltumatut tarkvaratarnijat (ISV) ja tsentraliseeritud kinnitust, olenemata projekti või meeskonnaliikme olekust projektis. | [Turve ja kinnitused](/dynamics365/project-operations/approvals/approvals-security) |
|Projekti plaanimine ja jälgimine|**Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks** </br> </br>Ressursi määramise kontuuri redigeerimise API võimaldab arendajatel programmiliselt määrata ülesande määraja panuse mis tahes toetatud kuupäevavahemikus, et tagada üksikasjalikum ajaline jõupingutuste plaanimine.|[Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2754422 | Materjali- ja kuluprognoosid ei liigu Dynamics 365 Finance, kui projektid kopeeritakse Dataverse. |
| Aeg ja kulu | 2787409 | Mittekehtiv kinnitaja saab kinnitada mitteprojekti ajakirje. |
| Müügivõimaluse haldus | 2788907 | Värskendatud on tõrketeade lippe sisaldavate tellimuseridade kordumatuse valideerimise kohta. |
| Aeg ja kulu | 2842253 | Nullerandi käsitlemine aja kinnitamiseks. |
| Arveldamine ja hinnakujundus | 2844181 | Korrelatsiooni ID mittesaamine blokeerib arve loomise. |
| Arveldamine ja hinnakujundus | 2876628 | QLD, CLD - hinnanguline hinnakirja eraldusvõime peaks kasutama hinnakirja pärandkuupäevavahemiku välju. |
| Allhanked | 2893222 | Kui allhankereale ei ole rolli määratud, peaks olema võimalik valida see rida meeskonnaliikmel mis tahes rolli jaoks. |
