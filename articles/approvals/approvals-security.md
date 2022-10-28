---
title: Turve ja kinnitused
description: Sellest artiklist leiate teavet Microsofti kinnitustega töötamise turbehäälestuse kohta Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709392"
---
# <a name="security-and-approvals"></a>Turve ja kinnitused

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoft Dynamics 365 Project Operations kasutab aja-, kulu- ja materjalikirjete kinnitamiseks kahte turberolli.

- Projekti kinnitaja
- Projekti kinnitaja administraator

## <a name="project-approver"></a>Projekti kinnitaja

Projekti aja-, kulu- ja materjalikirjete kinnitamiseks peab teil olema **projekti kinnitaja** turberoll. Samuti peab teil olema juurdepääs asjakohastele seotud olemitele (nt **Project)**. Selle juurdepääsu saab määrata keegi, kellel on **projektijuhi** roll. Lisaks peate olema projekti meeskonnaliige ja märgitud kinnitajaks.

Mitteprojektikirjete kinnitamiseks peate olema esitaja haldur.

## <a name="project-approver-admin"></a>Projekti kinnitaja administraator

> [!NOTE]
> Kinnituskomplektide [funktsioon](approval-sets.md) peab olema lubatud, enne kui saate kasutada Project Approveri administraatori funktsiooni.

**Projekti kinnitaja administraatori** turberoll võimaldab kasutajatel poliitikatest mööda hiilida ja lubab kinnitada kirjeid kõigis projektides. Selle rolli määramine läheb mööda valideerimisloogikast, mis nõuab meeskonna liikmelisust ja kinnitajaks märkimist. Teil peab olema juurdepääs asjakohastele seotud tabelitele (nt **Project**) teile määratud turberollide kaudu.

SÜSTEEMI kasutaja kontekst läheb valideerimistest mööda samamoodi nagu Project Approveri administraatori turberoll.
