---
title: Allhankelepinguga ressursi määramiste kuluprognoosid
description: Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 Project Operations arvutab allhanke ressursimäärangute kuluprognoosi.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262054"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Allhankelepinguga ressursi määramiste kuluprognoosid

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Allhankeprojekti meeskonna liikmete ülesandemäärangute maksumus arvutatakse, kasutades **seotud meeskonnaliikme kirjel alltöövõtule lisatud ostu** hinnakirja. See erineb sellest, kuidas töötaja ressursimääranguid kuluarvestusse pannakse, kui töötaja ressursside ülesandemäärangud tehakse kuluarvestuseks, kasutades **projekti** tellijaüksusele lisatud hinnakirja. 

Üldiste projektimeeskonna liikmete puhul, kellele on alltöövõtt, määratakse määrangute kulu, kasutades rollipõhist hinna seadistust allhankele lisatud ostu hinnakirjas. Ostuhindu saab seadistada ka spetsiaalselt iga ressursi jaoks. Neid ressursipõhiseid hindu eelistatakse, kui projektimeeskonna liikmetest koosnevate ülesannete kuluarvestus on lepingulised töötajad. 

Rollipõhise ostuhinna ja ressursipõhise ostuhinna kasutamise prioriteet on ajendatud hinnadimensiooni prioriteedi seadistamisest parameetrites **> kogusepõhised hinnakujunduse dimensioonid**.

See dünaamiliselt tuletatavate hindade funktsioon, mis põhineb alltöövõtjate ostuhindade dimensiooni seadistusel, on sarnane sellega, kuidas täistööajaga töötajate puhul kulu- ja arvemäärad tuletatakse. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Ülesandeülesannete loomine alltöövõtja ressursside kuluprognooside saamiseks

Alltöövõtjate tööülesandeid saab luua kahel viisil: 
- Vahekaardi Tööülesanded **kasutamine**.
- **Vahekaardi Meeskond** kasutamine.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ressursimäärangute loomine menüü Tööülesanded abil
**Kasutades konkreetse ülesande menüü Tööülesanded** loendit **Ressursid**, saate luua ülesandeülesande nimega ressursi või üldise ressursi jaoks. Kui valite ülesande ripploendist **Määratud ressursid** nimega ressursi ja see ressurss on lepinguline töötaja, määratakse ülesandele nimega ressurss ja luuakse vastav projektimeeskonna liikme kirje, mille töötaja tüübiks **on seatud Lepingutöötaja** ja **Kehtivus** väärtuseks **Kehtetu**. Järgmise juhisena peate avama projektimeeskonna liikme kirje ning valima allhanke- ja allhankeliini. See värskendab ülesandeülesannet, et sellel oleks viide alltöövõtu ja allhanke reale, ning värskendatakse ka meeskonnaliikme olekuks **Kehtiv**.

Kui otsustate ülesande ripploendist **Määratud ressursid** luua üldise meeskonnaliikme, **võimaldab dialoogis Üldine meeskonnaliikme loomine** valida allhanke- ja allhankerea. Kui ülesandele on määratud üldine ressurss ja luuakse vastav projektimeeskonna liikme kirje, märkate, et projektimeeskonna liikme kirje luuakse nii, et töötaja tüübiks **on seatud Lepingutöötaja** ja **Kehtivuse** väärtuseks **On määratud Kehtivus**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektimeeskonna liikmete loomine vahekaardi Meeskond abil
Projekti vahekaardi Meeskond abil saate luua üldise või nimega meeskonnaliikme. Meeskonnaliikme loomisel saate valida allhanke ja allhanke rea. Pärast meeskonnaliikme loomist peate tööülesandele määrama meeskonnaliikme, kasutades ülesande rippmenüüd **Määratud ressursid**. 

## <a name="updating-estimates"></a>Prognooside ajakohastamine
Pärast seda, kui olete projektimeeskonna liikmed ülesannetele määranud, peate navigeerima **projekti vahekaardile Prognoosid** ja valima Värskenda **hindu**, et tagada allhankija ressursiülesannete kulumäärade värskendamine allhankelepingule lisatud ostuhinnaloendi põhjal. Hinnanguid ei looda Microsofti Dynamics 365 Project Operations määramata ülesannete jaoks. Selle tulemusena peate looma ülesandeülesanded, et hinnata ja maksta oma projektis erinevaid ülesandeid. 

> [MÄRKUS!] Projektimeeskonna liikmed, kelle tüüp **Töötaja on** Lepinguline töötaja **, kuid kellel pole alltöövõtuviidet, märgistatakse projektimeeskonna liikmete** ruudustikus **sobimatuks** **.** Kui selle olekuga projektimeeskonna liikmeid on, avage projektimeeskonna liikme kirje ja värskendage käsitsi allhanke ja allhanke rea välju, et finantskulu prognoos kajastaks täpselt alltöövõtja kulusid **vahekaardil Prognoosid**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
