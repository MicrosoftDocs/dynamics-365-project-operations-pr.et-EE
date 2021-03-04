---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131788"
---
# <a name="copy-a-project"></a>Projekti kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations võimaldab teil kiiresti luua uusi projekte, valides vormil **Projektid** toimingu **Kopeeri projekt**. Projekti kopeerimiseks avage projekt, mida soovite kopeerida, ja seejärel valige toiming **Kopeeri projekt**. Toiming kopeerib järgneva.

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

Lisateavet programmiliselt valikule Kopeeri projekt juurdepääsemise kohta leiate teemast [Projektimallide väljatöötamine toiminguga Kopeeri projekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]