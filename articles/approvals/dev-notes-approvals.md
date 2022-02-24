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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483943"
---
# <a name="developer-notes-for-approvals"></a>Kinnituste arendaja märkmed

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide. Kirjete õige üleminek tagab järgneva. 

  - Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).
  - Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.
