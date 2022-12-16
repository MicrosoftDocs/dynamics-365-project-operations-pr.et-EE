---
title: Turve ja kinnitused
description: See artikkel annab turbesätestuse kohta teenuses Microsoft Dynamics 365 Project Operations kinnitustega töötamiseks.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841918"
---
# <a name="security-and-approvals"></a>Turve ja kinnitused

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoft Dynamics 365 Project Operations kasutab aja-, kulu- ja materjalikirjete kinnitamiseks kahte turberolli.

- Projekti kinnitaja
- Projekti kinnitaja administraator

## <a name="project-approver"></a>Projekti kinnitaja

Projekti aja, kulude ja materjalikirjete kinnitamiseks peab teil olema **Projekti kinnitaja** turberoll. Teil peab olema juurdepääs ka asjakohastele seotud üksustele, näiteks **Projekt**. Selle juurdepääsu saab määrata keegi, kellel on **Projektijuhi** roll. Lisaks peate olema projekti meeskonnaliige ja märgitud kinnitajaks.

Projektiväliste kirjete kinnitamiseks peate olema esitaja juht.

## <a name="project-approver-admin"></a>Projekti kinnitaja administraator

> [!NOTE]
> Funktsioon [Kinnitamiskomplektid](approval-sets.md) peab olema lubatud, enne kui saate kasutada projekti kinnitaja administraatori funktsiooni.

**Projekti kinnitaja administraatori** turberoll võimaldab kasutajatel eeskirjadest mööda minna ja võimaldab kinnitada kõigi projektide kirjeid. Selle rolli määramine läheb mööda kinnitamisloogikast, mis nõuab meeskonna liikmelisust ja kinnitajaks märkimist. Teil peab olema juurdepääs asjakohastele seotud tabelitele, näiteks **Projekt**, teile määratud turberollide kaudu.

SÜSTEEMI kasutajakontekst möödub kinnitamisest samamoodi nagu projekti kinnitaja administraatori turberoll.
