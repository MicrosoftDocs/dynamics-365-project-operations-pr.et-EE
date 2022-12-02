---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 41, V3
description: Selles artiklis on loetletud funktsioonid ja parandused, mis on saadaval rakenduses Microsoft Dynamics 365 Project Service Automation värskenduse väljalase 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930543"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 41, V3 uued või muudetud funktsioonid ja parandused. Selle versiooni järgunumber on V3.10.62.162 ja see on märtsis 2022 automaatvärskendusega kõigile saadaval.

## <a name="update-release-41"></a>Värskenduste väljalase 41

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Projektijuhtimine**
- Kui püüate luua projekti mallist, mis põhineb töölaua lisandmoodulist loodud projektil, kuvatakse järgmine tõrketeade: „Ressursi määramise plaanitud töö välja valideerimine: iga ressursi määramise ajaviite lõppkuupäev ei tohi olla varasem selle alguskuupäevast“.

**Aeg ja kulu**
- Kui üritate ajakirjet kustutada, ilmub järgmine tõrketeade: „ISV-koodis ilmneb ootamatu viga“.

**Müük**
- Kui loote fikseeritud hinnaga vahekokkuvõtte jaoks arve, ei täideta välju **Kirjeldus** ja **Väline kirjeldus**. 
