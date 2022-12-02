---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 45, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169176"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 45, V3 uued või muudetud funktsioonid ja parandused. Selle versiooni järgunumber on V3.10.76.168 ja see on üldsusele isevärskenduse kaudu kättesaadav juulis 2022.

## <a name="update-release-45"></a>Värskenduste väljalase 45

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Müük**

- Kasutajad ei saa edukalt arveid luua pärast seda, kui nad üritavad luua arvet ilma arveldamata müügita, kui nad vaatavad ka lehe sama eksemplari ega värskenda seda.

**Aeg ja kulu**

- Kui uudne kinnitamine on sisse lülitatud ja tagasikutsutud projekti kinnitamine on kinnitatud, on kirje etapp ebaõigesti värskendatud väärtusele **Tagasikutsumise taotlus kinnitatud**.
- Kui uudne kinnitamine on sisse lülitatud ja pilvevood on mitteaktiivsed, ei õnnestu kinnitamisprotsess ja kinnitamist esitavaid või kinnitavaid kasutajaid ei teavitata.
