---
title: Kinnituste arendaja märkmed
description: Selles teemas antakse täiendavat arendaja teavet kinnitustega töötamise kohta.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996786"
---
# <a name="developer-notes-for-approvals"></a>Kinnituste arendaja märkmed

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide. Kirjete õige üleminek tagab järgneva. 

  - Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).
  - Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]