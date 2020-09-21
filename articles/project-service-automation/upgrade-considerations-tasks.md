---
title: Tööjaotuse struktuuri täiendamise kaalutlused
description: Selles teemas kirjeldatakse, kuidas täiendada tööjaotuse struktuuri Project Service Automation versioonilt 2.x versioonile 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751001"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Tööjaotuse struktuuri täiendamise kaalutlused
Selles teemas kirjeldatakse, kuidas täiendada tööjaotuse struktuuri Project Service Automation versioonilt 2.x versioonile 3.x. Selles teemas määratletakse projekti töökorras olek Project Service Automation (PSA), mis on vajalik edukaks täienduseks. Samuti leiate sellest teemast teavet levinud blokeerimistingimuste kohta, mis põhjustavad täienduse nurjumist. Lisateavet projekti ülesannete ja nende funktsioonide määratlemise kohta projekti ajakava raames leiate jaotisest [Projekti ajakavad](project-creating.md).

## <a name="key-entities"></a>Põhiolemid
Täpse tööjaotuse struktuuri jaoks, mis on juba ressurssidega laaditud, on nõutavad järgmised olemid.

- [Projekt](../developer/entities/msdyn_project.md)
- [Projektimeeskond](../developer/entities/msdyn_projectteam.md)
- [Projekti ülesanne](../developer/entities/msdyn_projecttask.md)
- [Ressursimääramised](../developer/entities/msdyn_resourceassignment.md)
- [Projekti ülesande sõltuvus](../developer/entities/msdyn_projecttaskdependency.md)
- [Reserveeritavad ressursid](../developer/entities/bookableresource.md)

Ressursiga laaditud tööjaotuse struktuuri määratlemiseks peate läbi tegema järgmised etapid.

1. Uue projekti loomine. Lisateavet uue projekti loomise kohta leiate jaotisest [msdyn_project](../developer/entities/msdyn_project.md).
2. Ühe või mitme ülesande loomine. Lisateavet ülesande loomise kohta leiate jaotisest [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).
3. Ülesannete sõltuvuste määramine. Lisateavet leiate teemast [Projekti tööülesande sõltuvus](../developer/entities/msdyn_projecttaskdependency.md).
4. Projekti meeskonnaliikmete määramine projektile. Lisateavet leiate jaotisest [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Projekti meeskonnaliikmete määramine ülesannetele. Lisateavet leiate jaotisest [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Projekti meeskonna seosed

Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.
- Kõik projekti meeskonnaliikmed peavad olema seostatud broneeritava ressursiga.
- Kõik projekti meeskonnaliikmed peavad olema seostatud sama projektiga. 

## <a name="project-task-relationships"></a>Projekti ülesande seosed
Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.

- Kõik seostuvad ülesanded tuleb seostada sama projektiga.
- Iga rea ülesandel peab olema emaülesanne.
- Igal ülesandel peab olema emaprojekt.

### <a name="valid-conditions"></a>Sobivad tingimused

- Kõik ülesannete kestused peavad olema suuremad kui üks tund või sellega võrdsed (> =) ja väiksemad kui 1 800 000 minutit (1250 päeva).*
- Kõigi ülesannete varaseim alguskuupäev tohib olla 01.01.2000.*
- Kõigi ülesannete hiliseim alguskuupäev tohib olla 17 aastast praegusest päevast.*
- Kõigi ülesannete alguskuupäev peab olema lõppkuupäevast varasem või sellega võrdne.
- Kõigil liigituste (kulu, materjal, maks ja aeg) all olevatel kandetüüpidel peavad olema seatud väärtused väljade **Vaikeühik** ja **Ühikurühm** jaoks.
- Tähti sisaldavaid kuupäevavorminguid tuleb vältida.

### <a name="potential-mitigation-steps"></a>Potentsiaalsed lahendusetapid
- Täpsema otsingu abil saate tuvastada projekti tööülesanded, mis ei sisalda projekti ID-d.
- Täpsema otsingu abil saate tuvastada projekti tööülesanded, mille kavandatav kestus on suurem kui > 1 800 000.
- Enne andmete muutmist peaksite uurima, millised kohandused on seostatud olemiga, mis võis viia andmete halba olekusse sattumiseni. Need kohandused tuleks lahendada enne mis tahes andmetega seotud värskenduste jätkamist.
- Tuvastatud orvustunud ülesannete korral kaaluge nende tööülesannete kustutamist, kui neid pole vaja või need tuleks seostada õige peamise projektiga.
- Mis tahes toimingute korral, mille kestus on pikem kui 1 250 päeva, kaaluge vajadusel lisada mitu tööülesannet, et tähistada kogu kestust.

> [!NOTE]
> Tärniga (\*) märgitud üksustel on piirangud, sest kliendisuhete haldus (CRM) toetab ainult 7320 korduvuse laiendamist. Peate jääma sellest piirist allapoole.

## <a name="resource-assignment-relationships"></a>Ressursi määramise seosed
Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.

- Kõik tööjaotuse struktuuris olevad ressursi määramised peavad olema seotud sama projektiga.
- Kõik tööjaotuse struktuuris olevad ressursi määramised peavad olema seostatud sama projekti meeskonnaliikmetega.

### <a name="potential-mitigation-steps"></a>Potentsiaalsed lahendusetapid
- Saate tuvastada kõik tööülesanded, mis jäävad eespool kirjeldatud tingimustest välja.  
- Kõik ressursi määramised, mis enam ei kehti, peaks kustutatama.

## <a name="project-task-dependency-relationships"></a>Projekti ülesande sõltuvuse seosed
Eduka täienduse tagamiseks tuleb õigesti säilitada järgmised seosed.

- Kõik projekti ülesande sõltuvused peavad olema seotud sama projektiga.
- Ülesandel ei saa samale sõltuvusele viidata rohkem kui üks kord.
