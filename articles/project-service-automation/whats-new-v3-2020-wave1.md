---
title: Mis on uut või muudetud Project Service Automation versioonis 3.x laine 1 2020
description: Selles teemas kirjeldatakse, mis on Project Service Automationi versioonis 3 laine 1 2020 uus ja mida on muudetud.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750960"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Mis on uut või muudetud Project Service Automation versioonis 3 laine 1 2020
Teema toob esile peamised versiooniuuenduse kaalutlused, kui liigute Project Service Automationi (PSA) uusimale väljaande versioonile 3. x Wave 1 2020.

## <a name="time-entry"></a>Ajakirje
Ajakirje kogemust on pikendatud, et pakkuda võimalusi ajakirje pikendamiseks rohkemateks klientide stsenaariumiteks. See hõlmab võimalust lisada kirjetüüpe, mis juhivad nüüd konkreetset käitumist, mis põhineb välja skeemil nimega **Ajakirje sätted**, mida kuvatakse kui **Aja allikas**.

### <a name="upgrade-consideration"></a>Mida versioonitäienduse puhul arvestada
Selle funktsiooni toetamiseks värskendatakse PSA rolle, et kaasata uusi õigusi. Need õigused lubavad lugeda juurdepääsu uuele olemile, **Ajakirje sätetele**.

Kasutajatele, kes vajavad aja logimise võimalust, tuleks lisaks olemasolevatele rollidele anda kasutajaroll **Ajakirje kasutaja**. See roll hõlmab uut funktsionaalsust ja kindlustab, et ajakirje töötab edasi.

### <a name="currently-extended-time-entry-changes"></a>Praegu laiendatud ajakirje muudatused
Selleks, et vähendada mõju praegustele ajakirjete kasutajatele, on see rollimuutus ainuke põhiline nõue ajakirje kasutamise jätkamiseks. Kui olete loonud kohandatud vaated või eraldi ajakirjega kogemused, peate seadistama väljad **Ajakirje sätted** õigetele PSA väärtustele.
