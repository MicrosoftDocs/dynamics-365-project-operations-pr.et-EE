---
title: Sihtpärase ettemaksu loomine lepingus
description: See teema sisaldab teavet vastavalt vajadusele lepingus avansi loomist.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 51e3b0ac8e111be70fe6ad0f9c162dfaec3339ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003491"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Sihtpärase ettemaksu loomine lepingus

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoft Dynamics 365 Project Operations toetab arveldamisstsenaariumeid, mis hõlmavad ettemakseid ja avansse. **Project Operationsis** suvandi **Avandsid** kasutamine sarnaneb **honorari** lepingutele. 

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]