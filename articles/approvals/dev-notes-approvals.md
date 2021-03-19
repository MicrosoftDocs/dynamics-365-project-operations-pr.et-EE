---
title: Kinnituste arendaja märkmed
description: Selles teemas antakse täiendavat arendaja teavet kinnitustega töötamise kohta.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290264"
---
# <a name="developer-notes-for-approvals"></a>Kinnituste arendaja märkmed

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide. Kirjete õige üleminek tagab järgneva. 

  - Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).
  - Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]