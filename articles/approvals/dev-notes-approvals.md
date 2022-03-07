---
title: Kinnituste arendaja märkmed
description: Selles teemas antakse täiendavat arendaja teavet kinnitustega töötamise kohta.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991661"
---
# <a name="developer-notes-for-approvals"></a>Kinnituste arendaja märkmed

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide. Kirjete õige üleminek tagab järgneva. 

  - Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).
  - Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]