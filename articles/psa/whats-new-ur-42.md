---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 42, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912710"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 42, V3 uued või muudetud funktsioonid ja parandused. Selle versiooni järgu number on V3.10.73.61 ja on üldiselt saadaval 2022. a aprilli enesevärskenduse kaudu.

## <a name="update-release-42"></a>Värskenduste väljalase 42

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**

- Kui tööajatabel on tagasi lükatud, on selle tagasi lükanud kasutaja valesti identifitseeritud kui **Süsteem**.
- Ajakirjete importimisel puudub väärtus **Ressursikategooria**.
- Projekti kinnitajad saavad esitatud projekte kinnitada, kui nende õigused ei ole konkreetselt määratud **Võib kinnitada**.

**Müük**

- Kui kulude tegelikud näitajad registreeritakse muude kui juurtasandi ülesannete puhul, on kulude tegelikud näitajad valesti koondatud.
