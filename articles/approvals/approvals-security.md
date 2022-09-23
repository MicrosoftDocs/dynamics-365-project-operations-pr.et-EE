---
title: Turvalisus ja kinnitused
description: Sellest artiklist leiate teavet Microsofti kinnitustega töötamise turbehäälestuse kohta Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525402"
---
# <a name="security-and-approvals"></a>Turvalisus ja kinnitused

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoft Dynamics 365 Project Operations kasutab aja-, kulu- ja materjalikirjete kinnitamiseks kahte turberolli.

- Projekti kinnitaja
- Projekti kinnitaja administraator

## <a name="project-approver"></a>Projekti kinnitaja

Teil peab olema **projekti kinnitaja** turberoll, et kinnitada projekti aeg, kulu ja materjalikirjed. Samuti peab teil olema juurdepääs asjakohastele seotud olemitele,nt **Projectile**. Selle juurdepääsu saab määrata keegi, kellel on **projektijuhi** roll. Lisaks peate olema projekti meeskonnaliige ja märgitud kinnitajaks.

Projektiväliste kirjete kinnitamiseks peate olema esitaja juht.

## <a name="project-approver-admin"></a>Projekti kinnitaja administraator

> [!NOTE]
> Kinnitamisekomplektide [funktsioon](approval-sets.md) peab olema lubatud, enne kui saate kasutada Project Approver Admin funktsiooni.

Projekti **kinnitaja administraatori** turberoll võimaldab kasutajatel poliitikatest mööda hiilida ja võimaldab kõigi projektide kirjeid kinnitada. Selle rolli määramine läheb mööda valideerimisloogikast, mis nõuab meeskonna liikmelisust ja kinnitajaks märkimist. Teil peab olema juurdepääs asjakohastele seotud olemitele,nt **Projectile**. Selle juurdepääsu saab määrata keegi, kellel on **projektijuhi** roll.

SÜSTEEMI kasutaja kontekst möödub valideerimistest samamoodi nagu projekti kinnitaja administraator turberoll.
