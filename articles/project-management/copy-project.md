---
title: Projekti kopeerimine
description: Selles teemas antakse teavet rakenduses Dynamics 365 Project Operations projektide kopeerimise kohta.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574425"
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
- Projekti kontroll-loendid
- Projekti ämbrid

## <a name="project-properties"></a>Projekti atribuudid

Projekti kopeerimisel kopeeritakse järgmiste väljade väärtused.

| Väli | Projektitoimingud Ladustamata materjalid | Projekti toimingute Lite | Veebiprojekt |
|-------|------------------------------------------|-------------------------|---------------------|
| Nimetus | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Kirjeldus | :heavy_check_mark: | :heavy_check_mark: | |
| klient | :heavy_check_mark: | :heavy_check_mark: | |
| Kalendri mall | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuuta | :heavy_check_mark: | :heavy_check_mark: | |
| Lepingut sõlmiv üksus | :heavy_check_mark: | :heavy_check_mark: | |
| Omanikust ettevõte | :heavy_check_mark: | | |
| Projektijuht | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Olek | :heavy_check_mark: | :heavy_check_mark: | |
| Üldine projekti olek | :heavy_check_mark: | :heavy_check_mark: | |
| Kommentaarid | :heavy_check_mark: | :heavy_check_mark: | |
| Prognoosid | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Eeldatav alguskuupäev</p><p><strong>Märkus.:</strong> See väli määrab kuupäeva, millal projekt koopiast luuakse. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Eeldatav lõpetamiskuupäev</p><p><strong>Märkus.:</strong> Selle välja kuupäeva korrigeeritakse koopiast tehtud uue projekti alguskuupäeva alusel.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Tööpanus (tunnid) | :heavy_check_mark: | :heavy_check_mark: | |
| Eeldatav tööjõukulu | :heavy_check_mark: | :heavy_check_mark: | |
| Eeldatav kulude maksumus | :heavy_check_mark: | :heavy_check_mark: | |
| Eeldatav materjalikulu | | :heavy_check_mark: | |

> [!NOTE]
> Projekti kopeerimine on pikaaegne toiming. Kopeeritakse ka projektikirjed, nende vastavad atribuudid ja paljud seostuvad olemid. Toimingu pikaajalise loomuse tõttu on pärast koopia käivitamist sihtprojekti leht redigeerimiseks lukus, kuni kopeerimistoiming on lõpule jõudnud.

## <a name="work-breakdown-structure"></a>Tööjaotuse struktuur

Kui projekt on kopeeritud, siis kopeeritakse kogu ressursi laaditud tööjaotuse struktuur. Nimetatud ressursid asendatakse üldiste ressurssidega. Kui nimetatud ressurssidel pole üldise ressursiga samu töötunde, arvutatakse ajakava ümber ja ülesande kestused võivad muutuda.

## <a name="project-team-members"></a>Projektimeeskonna liikmed

Kui projektimeeskond kopeeritakse lähteprojektist, kopeeritakse üldised ressursid. Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid lähteprojektis. Nimetatud ressursid teisendatakse üldisteks meeskonnaliikmeteks.

> [!NOTE]
> Meeskonnaliikmeid ja ülesandeid ei kopeerita Project for the Webis.

## <a name="estimates"></a>Prognoosid

Kui projekt on kopeeritud, kopeeritakse ressursi, kulu ja materjali prognoosi read lähteprojektist. 

Lisateavet programmiliselt valikule Kopeeri projekt juurdepääsemise kohta leiate teemast [Projektimallide väljatöötamine toiminguga Kopeeri projekt](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Hinnapakkumised ja lepingud

Hinnapakkumised ja lepingud pole sihtprojektiga lingitud.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
