---
title: Ajakava abi ülevaade
description: Selles teemas antakse teavet ajakava abimehega töötamise kohta ressursside broneerimisel.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908046"
---
# <a name="schedule-assistant-overview"></a>Ajakava abi ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Ajakava abimeest kasutatakse selleks, et broneerida ressursse, lähtudes projektijuhi määratud nõuetest. Ajakava abimees toetub ressursi leidmiseks ressursinõudes esitatud parameetritele. Ajakava abimees soovitab ressursse, mis vastavad asjakohastele nõuetele, nagu vajalikud ajavahemikud või oskused.

Pärast sobivate ressursside tuvastamist saab ressursihaldur või projektijuht ressursi tööle broneerida.

## <a name="prerequisites"></a>Eeltingimused

Ajakava abimees on lahenduse Universal Resource Scheduling osa. See lahendus on kaasatud ja installitud rakendustes Dynamics 365 Project Operations, Dynamics 365 Field Service ja Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Nõuete ja ressursside ühitamine

Genereeritud ressursinõue põhineb järgmistel üksikasjadel.

-   Tunnused
-   Rollid
-   Äriüksused
-   Ressursieelistused
-   Tööpanuse kontuurid
-   Ajavöönd

Ajakava abimees kasutab neid üksikasju ressursside filtreerimiseks.

## <a name="launch-the-schedule-assistant"></a>Ajakava abimehe käivitamine

Ajakava abimehe käivitamiseks on kaks võimalust. Kui kasutate hübriidrežiimi, saate meeskonnaliikmete ruudustikus valida mis tahes meeskonnaliikme, kellel on täitmata ressursinõue, ja seejärel valige **Broneeri**. Kui kasutate keskset režiimi, leiab ja valib ressursi ressursihaldur.

## <a name="schedule-assistant-filters"></a>Ajakavaabilise filtrid

Pärast ajakava abimehe käitamist kuvatakse ressursinõude üksikasjad filtreeritud väärtustena vasakpoolsel paanil. Ressursihaldur või projektijuht saavad tulemusi viimistleda, kohandades filtreid, et need vastaksid kavandamise vajadustele.

Filtripaan kuvab järgmisi tööga seotud suvandeid.

-   Töö algus ja lõpp
-   Tunnused
-   Rollid
-   Organisatsiooniüksused
-   Ressursiettevõte
-   Ressursi tüübid
-   Eelistatud ressursid
