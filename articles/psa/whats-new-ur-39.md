---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 39, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval versioonis Microsoft Dynamics 365 Project Service Automation Update Release 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922447"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project service automation update release 39, V3 jaoks uued või muudetud. Selle versiooni järgunumber on V3.10.60.170 ja see on jaanuaris 2022 automaatvärskendusega kõigile saadaval.

## <a name="update-release-39"></a>Värskenduste väljalase 39

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Üldist**

- Araabiakeelse tõlke saidikaardile on tehtud mitmeid parandusi.

**Projektijuhtimine**

- Tõrge ilmneb siis, kui muudate projektijuhi projektijuhi kasutajaks, kes on juba projekti meeskonnaliige.

**Müük**

- Projekti lepingu hinnakirja **omanik** eksib, kui hinnakiri luuakse automaatselt. 
- Hinnakirja kuupäevaefektiivsust ei austata, kui hinnakirja rakendatakse projekti parameetrile.
- Lepinguüksusel ei pruugi kahe eraldi hinnapakkumise redigeerimisel olla õiget vaikeväärtust.