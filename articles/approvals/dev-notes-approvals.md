---
title: Kinnituste arendaja märkmed
description: See artikkel annab täiendavat arendaja teavet kinnitustega töötamise kohta.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924747"
---
# <a name="developer-notes-for-approvals"></a>Kinnituste arendaja märkmed

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations sisaldab valideerimise loogikat, mis tagab õige kirje liikumise läbi kinnitamise etappide. Kirjete õige üleminek tagab järgneva. 

  - Seotud tabelites luuakse kõik toetavad read (nt töölehed ja tegelikud näitajad).
  - Kinnitaja märgitakse projektis enne jätkamist kui **Projekti kinnitaja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]