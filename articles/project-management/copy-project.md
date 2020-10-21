---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908055"
---
# <a name="copy-a-project"></a>Projekti kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations võimaldab teil kiiresti luua uusi projekte, kasutades vormil **Projekt** toimingut **Kopeeri projekt**. Projekti kopeerimiseks valige projekt ja seejärel valige käsk **Kopeeri**. Toiming kopeerib järgneva.

- Projekti atribuudid
- Tööjaotuse struktuur
- Projektimeeskonna liikmed
- Projekti prognoosid
- Projekti kuluprognoosid

## <a name="project-properties"></a>Projekti atribuudid

Kui projekt on kopeeritud, kopeeritakse väärtused järgmistel väljadel.

- Nimetus
- Kirjeldus
- Klient
- Kalendri mall
- Valuuta
- Lepingut sõlmiv üksus
- Projektijuht
- Olek
- Üldine projekti olek
- Kommentaarid
- Prognoosid
- Eeldatav alguskuupäev
- Lõppkuupäev
- Tööpanus (tunnid)
- Eeldatav tööjõukulu
- Eeldatav kulude maksumus

## <a name="work-breakdown-structure"></a>Tööjaotuse struktuur

Kui projekt on kopeeritud, siis kopeeritakse kogu ressursi laaditud tööjaotuse struktuur. Nimetatud ressursid asendatakse üldiste ressurssidega. Kui nimetatud ressurssidel ei ole üldise ressursiga sama tööaega, arvutatakse ajakava uuesti ja ülesande kestused võivad muutuda.

## <a name="project-team-members"></a>Projektimeeskonna liikmed

Kui projektimeeskond kopeeritakse lähteprojektist, kopeeritakse üldised ressursid. Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid lähteprojektis. Nimetatud ressursid teisendatakse üldisteks meeskonnaliikmeteks.

## <a name="estimates"></a>Prognoosid

Kui projekt on kopeeritud, kopeeritakse lähteprojektist nii ressursi kui ka kulu prognoosiread.