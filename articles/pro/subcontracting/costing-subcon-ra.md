---
title: Allhankelepinguga ressursi määramiste kuluprognoosid
description: Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 Project Operations arvutab allhanke ressursimääramiste kuluhinnangu.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 40603c1d2dfdd49909d9a4bf5085f43201e8f6bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932337"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Allhankelepinguga ressursi määramiste kuluprognoosid

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Alltöövõtuga projektimeeskonna liikmete ülesandemääramised kulutakse seotud meeskonnaliikme kirje alltöövõtuga seotud alltöövõtuga seotud ostuhinna loendi **abil**. See erineb sellest, kuidas töötaja ressursimääranguid kulutakse, kui töötaja ressursside ülesandemääramised on kulupõhised, kasutades **projekti lepinguüksusega seotud omahinnakirja**. 

Allhanke korras tellitud üldiste projektimeeskonna liikmete puhul kulutakse ülesanded allhankega seotud ostuhinnastikus rollipõhise hinnahäälestuse abil. Ostuhindu saab seadistada ka spetsiaalselt iga ressursi jaoks. Need ressursipõhised hinnad seatakse prioriteediks, kui nimeliste projektimeeskonna liikmete ülesandeülesannete määramised on lepingulised töötajad. 

Rollipõhise ostuhinna ja ressursipõhise kasutamise prioriteet sõltub hinnakujundusdimensiooni prioriteedi seadistamisest parameetrites **> summapõhise hinnakujunduse dimensioonides**.

See dünaamiliselt tuletavate hindade funktsioon, mis põhineb alltöövõtjate ostuhindade dimensioonihäälestusel, on sarnane sellele, kuidas täistööajaga töötajate kulu- ja arvemäärad tuletatakse. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Ülesandeülesannete loomine alltöövõtja ressursside kuluprognooside saamiseks

Alltöövõtjate tööülesandeid saab luua kahel viisil: 
- **Vahekaardi Tööülesanded** abil.
- **Menüü Meeskond** kasutamine.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ressursimäärangute loomine vahekaardil Tööülesanded
Kasutades loendit **Ressursid** vahekaardil **Tööülesanded** kindla ülesande jaoks, saate luua ülesandemäärangu nimega ressursile või üldisele ressursile. Kui valite ülesande rippmenüüst **Määratud ressursid** nimega ressursi ja see ressurss on lepinguline töötaja, määratakse ülesandele nimega ressurss ja luuakse vastav projektimeeskonna liikme kirje, mille töötaja tüüp on seatud väärtusele Lepingutöötaja **ja** Kehtivus **on seatud väärtusele** **Kehtetu**. Järgmise sammuna peate avama projektimeeskonna liikme kirje ning valima allhanke- ja alltöövõturea. See värskendab ülesande määramist, et viidata alltöövõtu- ja alltöövõtureale, ning värskendab ka meeskonnaliikme olekut **Kehtiv**.

Kui otsustate luua ülesande ripploendist **Määratud ressursid** üldise meeskonnaliikme, **võimaldab dialoogiboks Üldine meeskonnaliikme loomine** valida alltöövõtu- ja alltöövõturea. Kui ülesandele on määratud üldine ressurss ja luuakse vastav projektimeeskonna liikmekirje, märkate, et projektimeeskonna liikme kirje luuakse töötaja tüübiga, mille väärtuseks **on seatud Lepingutöötaja** ja **kehtivus** on seatud väärtusele **Kehtiv**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektimeeskonna liikmete loomine vahekaardil Meeskond
Projekti vahekaardi Meeskond abil saate luua üldise või nimega meeskonnaliikme. Meeskonnaliikme loomisel saate valida alltöövõtu- ja alltöövõturea. Pärast meeskonnaliikme loomist peate määrama meeskonnaliikme ülesandele, kasutades ülesande rippmenüüd **Määratud ressursid**. 

## <a name="updating-estimates"></a>Hinnangute värskendamine
Kui olete projektimeeskonna liikmed ülesannetele määranud, peate liikuma **projekti vahekaardile Hinnangud** ja valima suvandi **Uuenda hindu**, et tagada alltöövõtja ressursi määramise kulumäärade värskendamine allhankelepinguga seotud ostuhinnakirja alusel. Microsoftis Dynamics 365 Project Operations ei looda määramata ülesannete kohta hinnanguid. Selle tulemusena peate looma tööülesanded, et hinnata ja maksta oma projektis erinevaid ülesandeid. 

> [MÄRKUS!] Projektimeeskonna liikmed, kelle tüüp **töötaja on** lepinguline töötaja **, kuid kellel pole alltöövõtu viidet, märgitakse projecti meeskonnaliikmete** ruudustikus **sobimatuks** **.** Kui selle olekuga projektimeeskonna liikmeid on mõni, avage projektimeeskonna liikme kirje ja värskendage alltöövõtu- ja alltöövõturea välju käsitsi nii, et finantskulude hinnang kajastaks täpselt allhankija kulusid vahekaardil **Hinnangud**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
