---
title: Allhankelepinguga ressursi määramiste kuluprognoosid
description: See artikkel selgitab, kuidas Microsoft Dynamics 365 Project Operations arvutab alltöövõtu ressursside määramise kulude hinnangut.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522649"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Allhankelepinguga ressursi määramiste kuluprognoosid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Alltöövõtuga projektimeeskonna liikmete tööülesannete maksumus arvestatakse alltöövõtja lisatud **Ostu** hinnakirja alusel, mis on seotud meeskonnaliikme kirjega. See erineb töötajate ressursside kuluarvestusest, kui töötajate ressursside ülesannete kulu arvestatakse projekti lepinguosalisele lisatud **Kulu** hinnakirja abil. 

Üldise projektimeeskonna liikmete puhul, kes on sõlminud alltöövõtulepingu, arvutatakse ülesannete maksumus, kasutades alltöövõtulepingule lisatud ostuhinnakirjas rollipõhist hinnaseadistust. Ostuhinnad saab seadistada ka iga ressursi jaoks eraldi. Need ressursispetsiifilised hinnad on prioriteetsed, kui nimetatud projektimeeskonna liikmete kuluülesanded on tähtajalise lepinguga töötajad. 

Rollipõhise ostuhinna ja ressursispetsiifilise ostuhinna kasutamise prioriteetsuse määrab hinnadimensiooni prioriteedi seadistus jaotises **Parameetrid > Summapõhised hinnadimensioonid**.

See alltöövõtja ostuhindade dimensioonide seadistusel põhinevate hindade dünaamilise tuletamise funktsioon sarnaneb täistööajaga töötajate kulu- ja arvemäärade tuletamisega. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tööülesannete koostamine alltöövõtja ressursside kuluprognooside saamiseks

Alltöövõtjatele saab tööülesandeid koostada kahel viisil: 
- Vahekaardi **Ülesanded** kasutamine.
- Vahekaardi **Meeskond** kasutamine.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ressursiülesannete loomine vahekaardi Ülesanded abil
Kasutades konkreetse ülesande jaoks olevat loendit **Ressursid** vahekaardil **Ülesanded**, saate luua tööülesande määramise nimelisele ressursile või üldisele ressursile. Kui valite ülesande rippmenüüs **Määratud ressursid** nimega ressursi ja see ressurss on tähtajalise lepinguga töötaja, määratakse nimega ressurss ülesandele ja luuakse vastav projektimeeskonna liikme kirje koos töötaja tüübiga **Tähtajalise lepinguga töötaja** ja **Kehtivus** on seatud väärtusele **Kehtetu**. Järgmise sammuna peate avama projektimeeskonna liikme kirje ja valima alltöövõtu ja alltöövõtu rea. See värskendab ülesande määramist, et see sisaldaks viidet alltöövõtule ja alltöövõtu reale, ning värskendab ka meeskonnaliikme olekuks **Kehtiv**.

Kui otsustate luua ülesande rippmenüüst **Määratud ressursid** üldise meeskonnaliikme, võimaldab dialoog **Üldise meeskonnaliikme loomine** valida alltöövõtu ja alltöövõtu rea. Kui ülesandele on määratud üldine ressurss ja vastav projektimeeskonna liikme kirje luuakse, märkate, et projektimeeskonna liikme kirje luuakse töötaja tüübiga **Tähtajalise lepingu töötaja** ja **Kehtivus** seatud väärtusele **Kehtiv**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projektimeeskonna liikmete loomine vahekaardil Meeskond
Kasutades projekti vahekaarti Meeskond, saate luua üldise või nimelise meeskonnaliikme. Meeskonnaliikme loomisel saate valida alltöövõtu ja alltöövõtu rea. Pärast meeskonnaliikme loomist peate määrama meeskonnaliikme ülesandele, kasutades ülesande **Määratud ressursid** rippmenüüd. 

## <a name="updating-estimates"></a>Prognooside värskendamine
Kui olete projektimeeskonna liikmed ülesannetele määranud, peate navigeerima projekti vahekaardile **Prognoosid** ja valima **Värskenda hindu** tagamaks, et alltöövõtjate ressursside määramise kulumäärasid värskendatakse alltöövõtule lisatud ostuhinnakirjas. Rakenduses Microsoft Dynamics 365 Project Operations ei genereerita prognoose määramata ülesannetele. Selle tulemusena peate oma projekti erinevate ülesannete hindamiseks ja maksumuse määramiseks looma tööülesandeid. 

> [MÄRKUS!] Projektimeeskonna liikmed, kelle **Töötaja tüüp** on **Tähtajalise lepinguga töötaja**, kuid kellel puudub alltöövõtu viide, märgistatakse väärtusele **Kehtetu** ruudustikus **Projektimeeskonna liikmed**. Kui projektimeeskonnal on selles olekus mõni projektimeeskonna liige, avage projektimeeskonna liikme kirje ja värskendage käsitsi alltöövõtu ja alltöövõtu rea välju, nii et finantskulude prognoos kajastaks täpselt alltöövõtja kulusid vahekaardil **Prognoosid**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
