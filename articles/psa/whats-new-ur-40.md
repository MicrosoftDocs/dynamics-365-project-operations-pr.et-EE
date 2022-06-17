---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 40, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval versioonis Microsoft Dynamics 365 Project Service Automation Update Release 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912787"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project service automation update release 40, V3 jaoks uued või muudetud. Selle versiooni järgu number on V3.10.61.61 ja see on kõigile kättesaadav 2022. a veebruaris ise värskendamise kaudu.

## <a name="update-release-40"></a>Värskenduste väljalase 40

### <a name="features"></a>Funktsioonid
Project Service Automationilt Project Operationsile ülemineku 1. etapp - Lite ilmub 2022. aasta veebruaris kõigile klientidele. Sobivuse kontrollimiseks lugege teemat [Üleminek project service automationilt projektitoimingutele](upgrade-project-operations-non-stocked.md). Kui rakendust ei kuvata teie eksemplaris Power Platform halduskeskuses, võtke ühendust toega ja paluge lennu lubamist oma keskkondade jaoks. Teie taotlus peab sisaldama keskkonna ID-de loendit, kus lend peab olema lubatud.

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**
- Kui ajakanne lükatakse tagasi või tühistatakse, puudub märkmekirje. 

**Müük**

- Kui värskendate kulu- või müügiprognoose, kasutades kastiväliseid pistikprogramme, on teil valesti lubatud saata JSON-i kasulikke koormusi, mis ei kehti väljaspool kasutajaliidest.
- Hinnapakkumisridade värskendamisel kiirvaates on teil lubatud hinnapakkumisi aktiveerida.
