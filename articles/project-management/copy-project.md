---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007186"
---
# <a name="copy-a-project"></a>Projekti kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operationsi abil saate kiiresti uusi projekte koostada, valides **Kopeeri projekt** vormil **Projektid**. Projekti kopeerimiseks avage projekt, mida soovite kopeerida, ja seejärel valige toiming **Kopeeri projekt**. Toiminguga kopeeritakse järgnev.

- Projekti atribuudid 
- Tööjaotuse struktuur
- Projektimeeskonna liikmed
- Projekti prognoosid
- Projekti kuluprognoosid
- Projektimaterjali prognoosid

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
- Eeldatav alguskuupäev: see on kuupäev, millal projekt koopiast luuakse.
- Eeldatav lõpukuupäev: seda kuupäeva muudetakse koopiast loodud uue projekti alguskuupäeva põhjal.
- Tööpanus (tunnid)
- Eeldatav tööjõukulu
- Eeldatav kulude maksumus
- Eeldatav materjalikulu

> [!NOTE]
> Projekti kopeerimine on pikaaegne toiming. Kopeeritakse ka projektikirjed, nende vastavad atribuudid ja paljud seostuvad olemid. Toimingu pikaajalise loomuse tõttu on pärast koopia käivitamist sihtprojekti leht redigeerimiseks lukus, kuni kopeerimistoiming on lõpule jõudnud.

## <a name="work-breakdown-structure"></a>Tööjaotuse struktuur

Kui projekt on kopeeritud, siis kopeeritakse kogu ressursi laaditud tööjaotuse struktuur. Nimetatud ressursid asendatakse üldiste ressurssidega. Kui nimetatud ressurssidel ei ole üldise ressursiga sama tööaega, arvutatakse ajakava uuesti ja ülesande kestused võivad muutuda.

## <a name="project-team-members"></a>Projektimeeskonna liikmed

Kui projektimeeskond kopeeritakse lähteprojektist, kopeeritakse üldised ressursid. Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid lähteprojektis. Nimetatud ressursid teisendatakse üldisteks meeskonnaliikmeteks.

## <a name="estimates"></a>Prognoosid

Kui projekt on kopeeritud, kopeeritakse ressursi, kulu ja materjali prognoosi read lähteprojektist. 

Lisateavet programmiliselt valikule Kopeeri projekt juurdepääsemise kohta leiate teemast [Projektimallide väljatöötamine toiminguga Kopeeri projekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
