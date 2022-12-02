---
title: Kulude üksikasjalik loetelu
description: See artikkel selgitab, kuidas kulusid jaotada, kasutades ümberkujundatud Kulude tööruumi.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920929"
---
# <a name="expense-itemization"></a>Kulude üksikasjalik loetelu

[!include [banner](../includes/banner.md)]

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Organisatsioonid nõuavad sageli töötajatelt reisil tekkinud kulude üksikasjalikku liigendust. Näiteks võib hotelli leht sisaldada mitut üksikasjalikku rida toahindade, maksude, parkimise ja muude iga päev viibimise kestel tehtud kulutuste kohta. Või võib söögikulu nõuda hommiku-, lõuna- või õhtusöögi täpsema liigenduse esitamist. Olenemata organisatsiooni vajadustest saab iga kulukategooria seadistada nii, et see kajastaks kulu moodustavaid alamkategooriaid või ridu. Kuigi jaotises **Kuluhaldus** on alati jaotamine toetatud, võimaldab tööruum **Uuesti kujundatud kulud** tõhusamat jaotamist, kui funktsioon **Korduvate kulude kiire jaotamine** on lubatud.  

## <a name="enable-quick-itemization"></a>Kiirjaotamise lubamine 

Saate kasutada funktsiooni **Korduvate kulude kiire jaotamine**, et kiiresti korduvad kulud üksikasjalikult kirjeldada, vältides vajadust iga kord päevaste kulude sisestamist kogu viibimise ajal. Kiirjaotamise lubamiseks tehke järgmised toimingud.

1. Minge tööruuumi **Funktsioonihaldus** ja otsige funktsioonide loendist üles ja valige **Ümberkujundatud kuluaruanded**. 
2. Valige **Luba kohe**. 
3. Funktsioonide loendis leidke ja valige **Korduvate kulude kiirjaotamine**.
4. Valige **Luba kohe**. 

## <a name="itemization-grid"></a>Jaotuseruudustik 

Kui kulukategoorial on alamkategooriad või erinevad komponendid, mis moodustavad selle kulu, siis saab selle jaotada. Kulu jaotamiseks valige kuluaruandes kulurida ja paanil **Kulu üksikasjad** valige **Toimingud** > **Jaota**. Liugur **Jaotamine** kuvab väljadega ruudustiku. Järgmises tabelis on näide igast ruudustiku väljast ja sellest, kuidas väli kuluaruandes renderdatakse. 

|     Väli          |     Kirjeldus                                                                                  |     Näide              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alamkategooria    |     Kulukategooria tüübi **Hotell** all konfigureeritud alamkategooriate loend.              |     Ruumi päevahind      |
|     Alguskuupäev     |     Kuupäev, millal kuluüksus esimest korda tekkis.                                           |     13/09/2021           |
|     Päevahind     |     Kuluüksusega eest kantud summa.                                                    |     200                  |
|     Kogus       |     Kordade arv, mille jooksul tasu kordub pideva ajavahemiku jooksul.                       |     3                    |

![Kulu jaotamine.](media/Itemization%20screen%201.png)

Kui salvestate jaotuse, näete jaotuse ruudustikus määratud koguse kohta individuaalset jaotuse rida. Iga rida algab ruudustikus määratud kuupäeval.

![Jaotatud aruanne.](media/Itemization%20screen%202.png)

