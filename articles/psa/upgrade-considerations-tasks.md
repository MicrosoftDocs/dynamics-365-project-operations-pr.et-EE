---
title: Tööjaotuse struktuuri täiendamise kaalutlused
description: Selles teemas kirjeldatakse, kuidas täiendada tööjaotuse struktuuri Project Service Automation versioonilt 2.x versioonile 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075038"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Tööjaotuse struktuuri täiendamise kaalutlused
Selles teemas kirjeldatakse, kuidas täiendada tööjaotuse struktuuri Project Service Automation versioonilt 2.x versioonile 3.x. Selles teemas määratletakse projekti töökorras olek Project Service Automation (PSA), mis on vajalik edukaks täienduseks. Samuti leiate sellest teemast teavet levinud blokeerimistingimuste kohta, mis põhjustavad täienduse nurjumist. Lisateavet projekti ülesannete ja nende funktsioonide määratlemise kohta projekti ajakava raames leiate jaotisest [Projekti ajakavad](project-creating.md).

## <a name="key-entities"></a>Põhiolemid
Täpse tööjaotuse struktuuri jaoks, mis on juba ressurssidega laaditud, on nõutavad järgmised olemid.

- [Projekt](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektimeeskond](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projekti ülesanne](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Ressursimääramised](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projekti ülesande sõltuvus](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Reserveeritavad ressursid](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Ressursiga laaditud tööjaotuse struktuuri määratlemiseks peate läbi tegema järgmised etapid.

1. Uue projekti loomine. Lisateavet uue projekti loomise kohta leiate jaotisest [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Ühe või mitme ülesande loomine. Lisateavet ülesande loomise kohta leiate jaotisest [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Ülesannete sõltuvuste määramine. Lisateavet leiate teemast [Projekti tööülesande sõltuvus](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Projekti meeskonnaliikmete määramine projektile. Lisateavet leiate jaotisest [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Projekti meeskonnaliikmete määramine ülesannetele. Lisateavet leiate jaotisest [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

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