---
title: Mis on uut septembris 2022 – Project Operationsi lihtjuurutamine
description: See artikkel annab teavet rakenduse Microsoft Dynamics 365 Project Operations lihtjuurutamise 2022. a septembri väljalaskes saadaolevate kvaliteedivärskenduste kohta.
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

See artikkel kehtib rakenduse Microsoft Dynamics 365 Project Operations järgmiste komponentide ja versioonide kohta.

- Rakenduse Project Operations Dataverse keskkonna versioonis 4.46.0.60

## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

| Funktsiooni ala | Funktsiooni nimi | Lisateave |
| --- | --- | --- |
| Müügivõimaluse haldus | **Hinnapakkumiste läbivaatamine ja aktiveerimine**<br>Project Operations pakub müügiprotsessile täielikku tuge. Projekti hinnapakkumisi saab aktiveerida, et esindada olekut, kus hinnapakkumine on kirjutuskaitstud ja seda vaadatakse üle. Aktiveeritud hinnapakkumisi saab üle vaadata, et luua uusi hinnapakkumisi, millel on suurendatud revisjoni number. Aktiveeritud projekti hinnapakkumised või hinnapakkumise versioonid saab sulgeda võidetud või kaotatud kujul. | [Projekti hinnapakkumise aktiveerimine ja kontrollimine](/dynamics365/project-operations/sales/activation-and-revision) |
| Arveldamine ja hinnakujundus | **Ajavööndi agnostiline hind ei tööta**<br>Project Operations on võtnud kasutusele ajavööndi agnostilise kuupäeva kontseptsiooni kõigi projekti tegelike näitajate puhul. Uus väli **Tehingu kuupäev** on nüüd saadaval töölehele kandmistel ja tegelikel näitajatel ning seda kasutatakse tehingu toimumise kuupäeva salvestamiseks, kuid ilma seda kuupäeva koordineeritud universaalajaks teisendamata. Seda kuupäeva kasutatakse järgnevate protsesside jaoks, nagu hinna rikkumine ja arvete koostamine. | <p>[Määrake projektipõhiste prognooside ja tegelike näitajate kulumäärad](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projektipõhiste prognooside ja tegelike näitajate müügihinna määratlemine](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Arveldamine ja hinnakujundus | **Kuupäeva kehtivad hinnad alistatakse rakenduses Project Operations**<br>Kuupäeva kehtiva hinna tühistamised pakuvad võimalust hinnakirjas konkreetseid hindu tühistada või muuta. | [Kuupäeva kehtiva hinna tühistamised](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Aeg ja kulu | **Globaalne kinnitaja**<br>See funktsioon võimaldab sõltumatut tarkvara hankijat (ISV) ja tsentraliseeritud kinnitust, olenemata projekti või meeskonnaliikme staatusest projektis. | [Turve ja kinnitused](/dynamics365/project-operations/approvals/approvals-security) |
|Projekti plaanimine ja jälgimine|**Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks** </br> </br>Ressursi määramise kontuuride redigeerimise API võimaldab arendajatel programmiliselt määrata ülesande määraja jõupingutusi mis tahes toetatud kuupäevavahemikus, et ajaliselt etapiviisilisemalt planeerida.|[Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvaliteedi värskendused

| Funktsiooni ala | Viitenumber | Kvaliteedi värskendus |
| --- | --- | --- |
| Arveldamine ja hinnakujundus | 2754422 | Materjali- ja kuluprognoosid ei voola rakendusse Dynamics 365 Finance, kui projekte kopeeritakse rakendusse Dataverse. |
| Aeg ja kulu | 2787409 | Mittekehtiv kinnitaja võib kinnitada projektivälise ajakirje. |
| Müügivõimaluse haldus | 2788907 | Värskendatud tõrketeate lippe sisaldavate tellimuseridade unikaalsuse kinnitamise kohta. |
| Aeg ja kulu | 2842253 | Null-erandiga töötlemine aja kinnitamiseks. |
| Arveldamine ja hinnakujundus | 2844181 | Korrelatsiooni ID hankimise ebaõnnestumine blokeerib arve loomise. |
| Arveldamine ja hinnakujundus | 2876628 | QLD, CLD – prognoositava hinnakirja lahendus peaks kasutama hinnakirja pärandkuupäevavahemiku välju. |
| Allhankeleping | 2893222 | Kui allhankelepingurea jaoks pole rolli määratud, peaks olema võimalik seda rida meeskonnaliikmel iga rolli jaoks valida. |
