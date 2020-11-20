---
title: Lepingus sihtpärase advansi loomine – liht
description: See teema sisaldab teavet vastavalt vajadusele lepingus avansi loomist.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181357"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Lepingus sihtpärase advansi loomine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsoft Dynamics 365 Project Operations toetab arveldamisstsenaariumeid, mis hõlmavad eelmakseid ja avansse. **Project Operationsis** suvandi **Avandsid** kasutamine sarnaneb **honorari** lepingutele. 

Kliendile avansi eest arve esitamiseks tehke järgmised toimingud.

1. Avage leht **Projektileping** ja valige vahekaart **Ettemaksed ja honorarid**.
2. Andmeruudustikus, mis loetleb kõik eelnevalt salvestatud avansid ja ettemaksed, valige **+ Uus projektilepingu honorar**. 

    Avaneb **kiirloomise** vorm ettemakse või avansi salvestamiseks.
    
3. Allolevas tabelis on loetletud avansi salvestamise väljad ja mida tuleks uute avansside loomisel meeles pidada.

    | Väli | Kirjeldus | Allavoolu mõjud |
    | --- | --- | --- |
    | **Projektilepingu klient** | See väli näitab, millisele lepingu kliendile selle avansi eest arve esitatakse. | Kui teil on lepingus mitu klienti ja soovite esitada igale neist konkreetse honorari või avansi summa, looge avanss iga kliendi jaoks eraldi. |
    | **Kirjeldus** | Avansi eesmärgi või ajastuse kirjeldus, et aidata avanssi tuvastada. | See kirjeldus kuvatakse selle avansi arvereal. |
    | **Summa** | Ettemakse või avansi summa. | See summa kuvatakse selle avansi arvereal. |
    | **Arve kuupäev** | Kuupäev, millal selle avansi arve kliendile esitatakse. | See on automatiseeritud arve loomisprotsessi kuupäev, et luua selle avansi arverida. |
    | **Arve olek** | See on suvandi säte, mis näitab, kas see avanss lisatakse selle kliendi arve mustandile. Võimalikud väärtused on järgmised.</br>- **Pole arveldamiseks valmis**</br>- **Arveldamiseks valmis** | Kui avanss või ettemaks on märgitud kui **Arveldamiseks valmis**, lisatakse see arve mustandile rea ajana. Järgmise arveldusperioodi projektikulude vastavusse viimiseks saab kasutada ainult täielikult arveldatud ettemakset. |

4. SelectAvansi või ettemakse salvestamiseks valige kiirloomise dialoogiboksis suvand **Salvesta ja sule**.
