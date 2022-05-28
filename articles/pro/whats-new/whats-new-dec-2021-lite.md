---
title: Mis on uut detsember 2021 - Project Operations lite juurutus
description: Selles teemas antakse teavet kvaliteedivärskenduste kohta, mis on saadaval Project Operations lite juurutuse 2021. aasta detsembri väljaandes.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585373"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Mis on uut detsember 2021 - Project Operations lite juurutus

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See teema kehtib järgmiste Microsofti Dynamics 365 Project Operations komponentide ja versioonide kohta.

- Projektitoimingud keskkonnaversioonis Dataverse 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

### <a name="subcontract-management"></a>Alltöövõtu haldamine 

- [Alltöövõtuprojekti meeskonnaliikmed](../subcontracting/subcontracting-project-team-members.md): projektijuht saab luua nimelisi või üldisi meeskonnaliikmeid alltöövõtu- ja alltöövõtuliinidega, et mõjutada personali ja hindamist.
- [Alltöövõtuvõimalused projektimeeskonna liikmetele](../subcontracting/subcon-options.md): nimeliste või üldiste projektimeeskonna liikmete personalivalikute tegemisel saab projektijuht üle vaadata olemasolevad allhanked või luua uusi allhankeid ühele või mitmele projektimeeskonna liikmele. 
- [Allhankeressursside määramise](../subcontracting/costing-subcon-ra.md) kuluhinnang: projekti kulude hindamisel võetakse arvesse allhankepõhiseid ressursimääramisi ja see läheb neile maksma alltöövõtulepingutega seotud ostuhinnakirjade abil. 
- [Plaanimistahvli konfigureerimine lepinguliste töötajate ja allhanke võimsuse](../subcontracting/configure-sb-subcon.md) kuvamiseks: Project Operationsi plaanimistahvlit saab nüüd konfigureerida koos töötajatega otsima ja soovitama lepingulise töötaja tüüpi broneeritavaid ressursse ja allhankemahtu. Seda konfiguratsiooni saab rakendada ressursside otsimisel konkreetse projektinõude personali kontekstis või kui otsite väljaspool projekti nõude konteksti.
- [Projekti komplekteerimine lepinguliste töötajate ja allhankevõimsusega](../subcontracting/staffing-cw.md): lepingulisi töötajaid saab nüüd broneerida projektidele, mis võimendavad ajakava juhatuse kogemusi.
- [Allhankekomponentide](../subcontracting/recording-subcon-actuals.md) projektide aja, kulude ja materjalikasutuse registreerimine: lepingulised töötajad saavad salvestada aega ja kulusid ning projektimeeskonna liikmed saavad salvestada ka projekti allhanke korras ostetud materjalide kasutamise. Selle tulemuseks on täpsete kulude registreerimine projektidele, mis kasutavad ostetud võimsust või materjale.
- [Riigi üleminekud allhankelepingule](../subcontracting/subcon-states.md): allhankelepinguid saab kinnitada hankijaga läbirääkimiste lõpuleviimiseks, sulgeda tarne lõpuleviimiseks või tühistada, et näidata hankijaga lepingu lõpetamist enne tarne lõpuleviimist.

### <a name="task-planning"></a>Ülesande plaanimine
- Süsteemiadministraatorite täiustatud tõrkeotsing. Kui kasutaja ei saa projekti avada, saab administraator projecti plaanimislogides üle vaadata Project for the Webist [loodud litsentsiga mitteseotud tõrked](../../project-management/schedule-api-logs.md).
- [Ülesannete kontroll-loendite kasutamine Microsoft Project for the Webis](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Rakenduses Microsoft Project for the web saate lisada ülesandele kontroll-loendi, et jälgida konkreetseid üksusi.

## <a name="quality-updates"></a>Kvaliteedi värskendused

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Plaanimine ja jälgimine | 2392596 | Ajakava API-d võimaldavad nüüd värskendusi väljadele **Allesjäänud jõupingutused**, **Pingutus lõpetatud** ja **% Täielik**. |
| Plaanimine ja jälgimine | 2478497 | Ajakava API-d **Tegevuse number** ja **Ülesande ID** väljad võivad olla sisendis tühjad, kuna süsteem asustab need automatiseeritud nummerdamise abil.|
| Aeg ja kulu | 2468135 | Heakskiidu korduskatsete arvu vähendatakse viielt kolmele. |
| Aeg ja kulu | 2468188 | Lahendas probleemi logitekstiga, mis ületab annotatsiooniolemi **märkmeteksti** atribuudi **maksimaalset pikkust**. |
