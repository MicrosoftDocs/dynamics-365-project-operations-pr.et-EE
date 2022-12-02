---
title: Allhankelepinguga komponentide aja, kulude ja materjalikasutuse kirjendamine
description: See artikkel selgitab, kuidas rakendus Microsoft Dynamics 365 Project Operations jälgib allhankelepingu alusel sõlmitud komponentide projektides salvestatud aega, kulusid ja materjalikasutust.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522508"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Aja, kulude ja materjalikasutuse registreerimine allhankelepingu alusel sõlmitud komponentide projektides

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

See artikkel selgitab, kuidas rakendus Microsoft Dynamics 365 Project Operations jälgib allhankelepingu alusel sõlmitud komponentide projektides salvestatud aega, kulusid ja materjalikasutust.

## <a name="costing-for-subcontractor-time-on-projects"></a>Projektide allhanke ajakulu
Rakenduses Project Operations saavad lepingulised töötajad projektidele aega salvestada sarnaselt töötajatega. Aja sisestamisel saab lepinguline töötaja valida kindla allhankelepingu ja allhankelepingu rea.

Kui lepinguliste töötajate esitatud aeg on kinnitatud, kirjendatakse projekti maksumus ühikukulu määra alusel, mis on selle lepingulise töötaja ressursi jaoks seadistatud allhankelepingu ostuhinnakirja jaotises **Rollihinnad**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projektide allhankekulude maksumus
Projektidele tehtud kulutuste sisestamisel saab kulukirjel valida allhankelepingu ja allhankelepingu rea. 

Selle kulukirje esitamisel ja kinnitamisel kajastatakse kuluprojektis ühikumaksumuse alusel, mis on selle tehingukategooria jaoks seadistatud allhankelepingu ostuhinnakirja jaotises **Kategooriahinnad**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projektide allhankematerjalide maksumus
Projektide materjalikasutuse sisestamisel saab materjalikasutuse logis valida allhankelepingu ja allhankelepingu rea. Materjalikasutuse logi esitamisel ja kinnitamisel kajastatakse materjalikulu projektis ühikuhinna alusel, mis on selle toote jaoks seadistatud allhankehinnakirja jaotises **Hinnakirja ühikud**.

Materjali kasutust saab registreerida ka projektide sisestavate toodete jaoks. Seda tüüpi materjalikasutust saab siduda ka allhankelepingu ja allhankelepingu reaga. Sisestavate toodete materjalikasutuse registreerimisel tuleb sisestada sisestava toote ühikukulu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
