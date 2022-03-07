---
title: Mis on uus detsember 2021 - Project Operations lite juurutamine
description: See teema annab teavet kvaliteedivärskenduste kohta, mis on saadaval Project Operations lite juurutamise 2021. aasta detsembri väljaandes.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942972"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Mis on uus detsember 2021 - Project Operations lite juurutamine

_Kohaldub: lihtjuurutus - tehing proforma arveldusega_

See teema kehtib järgmiste Microsofti komponentide ja versioonide Dynamics 365 Project Operations kohta.

- Project Operations Dataverse keskkonnaversioonis 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Selles väljaandes sisalduvad funktsioonid

### <a name="subcontract-management"></a>Alltöövõtu haldus 

- [Alltöövõtu projektimeeskonna](../subcontracting/subcontracting-project-team-members.md) liikmed: projektijuht saab luua nimelisi või üldisi meeskonnaliikmeid alltöövõtu ja alltöövõtuliinidega, et mõjutada personali ja hindamist.
- [Projektimeeskonna liikmete alltöövõtuvõimalused:](../subcontracting/subcon-options.md) Nimeliste või üldiste projektimeeskonna liikmete personalivalikute tegemisel saab projektijuht vaadata üle olemasolevad allhanked või luua uusi allhankeid ühele või mitmele projektimeeskonna liikmele. 
- [Allhankeressursside määramiste](../subcontracting/costing-subcon-ra.md) kuluhinnang: projekti kuluhinnangus võetakse arvesse allhankeressursside määranguid ja need lähevad neile maksma alltöövõtuga seotud ostuhinnakirjade abil. 
- [Konfigureerige ajakava juhatus, et kuvada lepingulised töötajad ja alltöövõtumaht](../subcontracting/configure-sb-subcon.md) : Projektitoimingute ajakavatahvlit saab nüüd konfigureerida otsima ja soovitama lepingulise töötaja tüüpi broneeritavaid ressursse ja alltöövõtuvõimsust koos töötajatega. Seda konfiguratsiooni saab rakendada ressursside otsimisel konkreetse projektinõude personali kontekstis või kui otsite väljaspool projekti nõuet.
- [Lepinguliste töötajate ja alltöövõtuvõimsusega projekti](../subcontracting/staffing-cw.md) personalimine: lepingulisi töötajaid saab nüüd broneerida projektidele, mis võimendavad ajakava juhatuse kogemusi.
- [Alltöövõtukomponentide projektide aja, kulude ja materjalikasutuse](../subcontracting/recording-subcon-actuals.md) salvestamine: lepingulised töötajad saavad salvestada aega ja kulusid ning projektimeeskonna liikmed saavad salvestada ka projekti allhanke abil ostetud materjalide kasutamist. Selle tulemuseks on täpsed kulud projektidele, mis kasutavad ostetud võimsust või materjale.
- [Riigi üleminekud allhankele:](../subcontracting/subcon-states.md) allhankeid saab kinnitada hankijaga läbirääkimiste lõpuleviimiseks, tarne lõpuleviimiseks sulgemiseks või tühistada, et näidata hankijaga lepingu lõpetamist enne tarne lõpetamist.

### <a name="task-planning"></a>Ülesande planeerimine
- Süsteemiadministraatorite täiustatud tõrkeotsing. Kui kasutaja ei saa projekti avada, saab administraator [projecti plaanimislogides project for the web loodud litsentsiga mittesegevaid vigu üle vaadata](../../project-management/schedule-api-logs.md).
- [Kasutage Microsoft Project for'i veebirakenduses ülesannete kontroll-loendeid](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Microsoft Project for'i veebirakenduses saate lisada ülesandele kontroll-loendi, et jälgida konkreetseid üksusi.

## <a name="quality-updates"></a>Kvaliteedi värskendused

| **Funktsiooni ala** | **Viitenumber** | **Kvaliteedi värskendus** |
| --- | --- | --- |
| Plaanimine ja jälgimine | 2392596 | Ajastada API-d võimaldavad nüüd **värskendusi väljadele Pingutus,** Lõpetatud **pingutus** ja % **Lõpetatud**. |
| Plaanimine ja jälgimine | 2478497 | Plaani **API-d Tegevuse number** ja **Ülesande ID** väljad võivad sisendil tühjad olla, kuna süsteem asustab need automatiseeritud nummerdamise abil.|
| Aeg ja kulu | 2468135 | Kordus korduste arvu vähendatakse viielt kolmele. |
| Aeg ja kulu | 2468188 | Lahendas probleemi logitekstiga, mis ületas **marginaaliolemi** noteteksti atribuudi maksimaalset **pikkust**. |
