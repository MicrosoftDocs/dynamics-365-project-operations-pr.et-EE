---
title: Mis on uut või muudetud Project Service Automation versioonis 3.x laine 1 2020
description: Selles artiklis antakse teavet selle kohta, mis on uut ja mida on muudetud Project Service Automationi versioonis 3 wave 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: c762f2e7931046d32464cfa8486ef8405aa7d836
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928611"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Mis on uut või muudetud Project Service Automation versioonis 3 laine 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Artiklis tõstetakse esile peamised versiooniuuenduse kaalutlused, kui minna üle Project Service Automation (PSA) versiooni 3.x wave 1 2020 viimasele versioonile.

## <a name="time-entry"></a>Ajakirje
Ajakirje kogemust on pikendatud, et pakkuda võimalusi ajakirje pikendamiseks rohkemateks klientide stsenaariumiteks. See hõlmab võimalust lisada kirjetüüpe, mis juhivad nüüd konkreetset käitumist, mis põhineb välja skeemil nimega **Ajakirje sätted**, mida kuvatakse kui **Aja allikas**. Selle funktsiooni toetamiseks on lisatud uus lahendus, mida nimetatakse Time, Expense, Statusing, and Approvals (aeg, kulu, olek ja kinnitused) (TESA).

### <a name="upgrade-consideration"></a>Mida versioonitäienduse puhul arvestada
Selle funktsiooni toetamiseks värskendatakse PSA rolle, et kaasata uusi õigusi. Need õigused lubavad lugeda juurdepääsu uuele olemile, **Ajakirje sätetele**.

Kasutajatele, kes vajavad aja logimise võimalust, tuleks lisaks olemasolevatele rollidele anda kasutajaroll **Ajakirje kasutaja**. See roll hõlmab uut funktsionaalsust ja kindlustab, et ajakirje töötab edasi.

Lisaks, kui teil on mis tahes kohandatud rakenduste moodulid, mis sisaldavad ka ajakirje olemi kõiki vorme, on teil vaja eemaldada moodulist **TESA time Entry Quick Create Form**.

### <a name="currently-extended-time-entry-changes"></a>Praegu laiendatud ajakirje muudatused
Selleks, et vähendada mõju praegustele ajakirjete kasutajatele, on see rollimuutus ainuke põhiline nõue ajakirje kasutamise jätkamiseks. Kui olete loonud kohandatud vaated või eraldi ajakirjega kogemused, peate seadistama väljad **Ajakirje sätted** õigetele PSA väärtustele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
