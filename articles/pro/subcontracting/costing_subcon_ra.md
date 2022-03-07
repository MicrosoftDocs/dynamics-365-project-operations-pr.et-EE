---
title: Alltöövõturessursside määramiste kuluhinnang
description: Selles teemas selgitatakse, kuidas Microsoft Dynamics 365 Project Operations arvutab alltöövõturessursside määramiste kuluhinnangut.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903009"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Alltöövõturessursside määramiste kuluhinnang

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Alltöövõtuprojekti meeskonna liikmete ülesandemääramised lähevad omahinnale, kasutades **seotud** meeskonnaliikme kirje allhankega seotud ostuhinnakirja. See erineb sellest, kuidas töötaja ressursimääranguid omahinnatakse, kui töötaja ressursside ülesandemäärangud lähevad **omahinnaindeksi** alusel, mis on seotud projekti tellijaüksusega. 

Alltöövõtuga üldiste projektimeeskonna liikmete puhul lähevad ülesanded omahinnale, kasutades alltöövõtuga seotud ostuhinnakirjas rollipõhist hinnahäälestust. Ostuhindu saab seadistada ka spetsiaalselt iga ressursi jaoks. Need ressursipõhised hinnad on prioriteetsed, kui nimetatud projektimeeskonna liikmete ülesannete määramine on lepinguline töötaja. 

Rollipõhise ostuhinna ja ressursipõhise kasutamise prioriteet on tingitud hinnakujundusdimensiooni prioriteedi seadistamisest **parameetrites > summapõhise hinnakujunduse dimensioonides**.

See funktsioon dünaamiliselt tuletades hinnad põhineb dimensiooni setup ostuhinnad alltöövõtjad on sarnane, kuidas kulud ja arve määrad tuletatakse täistööajaga töötajatele. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Ülesandeülesannete loomine alltöövõtja ressursside kuluprognooside saamiseks

Alltöövõtjate ülesandemääramisi saab luua kahel viisil. 
- Vahekaardi **Tööülesanded** abil.
- Kasutage **vahekaarti** Meeskond.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ressursside määramise loomine vahekaardi Tööülesanded abil
Kasutades **konkreetse** ülesande **vahekaardil Tööülesanded loendit** Ressursid, saate luua nimega ressursi või üldise ressursi ülesandeülesande. Kui valite ülesande ripploendist Määratud ressursid nimega ressursi **ja see ressurss on** lepinguline töötaja, määratakse ülesandele nimetatud ressurss ja luuakse vastav projektimeeskonna liikmekirje, mille töötaja tüübiks on seatud **Lepingutöötaja ja Kehtivus on seatud** **kehtetuks** **·**. Järgmise sammuna peate avama projektimeeskonna liikme kirje ning valima allhanke- ja alltöövõturea. See värskendab ülesande määramist, et saada viide allhanke- ja alltöövõtureale, ning värskendab meeskonnaliikme oleku ka **olekuks Kehtiv**.

Kui otsustate **luua ülesande rippmenüüst Määratud ressursid üldise** meeskonnaliikme, võimaldab **dialoogiboks Üldine meeskonnaliikme loomine** valida allhanke- ja alltöövõturea. Kui ülesandele on määratud üldine ressurss ja luuakse vastav projektimeeskonna liikmekirje, märkate, et projektimeeskonna liikmekirje luuakse töötaja tüübiga, mille põhjuseks on **lepinguline töötaja** ja kehtivus on **seatud** **olekusse Kehtiv**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektimeeskonna liikmete loomine vahekaardi Meeskond abil
Projekti vahekaardi Meeskond abil saate luua üldise või nimega meeskonnaliikme. Meeskonnaliikme loomisel on teil võimalus valida allhanke- ja alltöövõtuliin. Pärast meeskonnaliikme loomist peate meeskonnaliikme ülesandele määrama, kasutades ülesande **rippmenüüd** Määratud ressursid. 

## <a name="updating-estimates"></a>Hinnangute uuendamine
Pärast projektimeeskonna liikmete määramist ülesannetele peate navigeerima **projekti vahekaardile Hinnangud** ja valima **suvandi Uuenda** hindu, et tagada alltöövõtja ressursimääramiste omahindade värskendamine allhankega seotud ostuhinnakirja alusel. Pange tähele, et Hinnanguid ei looda Microsofti määramata toimingute kohta Dynamics 365 Project Operations. Selle tulemusena peate looma ülesandeülesanded, et hinnata ja maksta oma projekti erinevaid ülesandeid. 

> [MÄRKUS!] Projektimeeskonna liikmed, mille töötaja tüüp **on** **lepinguline** töötaja, kuid kellel pole alltöövõtu viidet, märgitakse **projekti** **meeskonnaliikmete** ruudustikus kehtetuks. Kui selle olekuga projektimeeskonna liikmeid on, avage projektimeeskonna liikmekirje ning värskendage alltöövõtu- ja alltöövõturea välju käsitsi nii, et finantskulude hinnang kajastaks täpselt allhankija kulu **vahekaardil** Hinnangud. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
