---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 29, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 29, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499666"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 29 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.45.98 ja see on kõigile kättesaadav 2021. a veebruaris ise värskendamise kaudu.

## <a name="update-release-29"></a>Värskenduste väljalase 29

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Kasutajad ei näe ajakirje ruudustikus mitte-tööpäevadel registreeritud töötunne.
- Kinnitatud kulukirjeid saab ruudustikus redigeerida.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Puuduvad valideerimisloogikad, mis tagavad, et ressursi määramise panuse tundide arv ei saa olla negatiivne.
- Kohandatud toiming **AssignResourcesForTask** värskendab kõiki välja, mitte ainult muudetud välju.
- Projekti kopeerimisel lisandmoodulite või töövoogudega keskkonda, mis on registreeritud sündmusele **CreateProject**, ei värskendatud atribuuti **msdyn_bulkgenerationstatus** kui **CopyWBSToProject** nurjub.
- Projekti kalendri laiendamisel ei sordita tööpäevi kasvavas järjekorras, põhjustades mõne projekti tööülesande värskenduste nurjumise.
- Projektijuhi muutmine olemasolevas projektis käivitab organisatsiooniüksuse vaikeloogika.

**Müük**

Lahendatud on järgmised probleemid.

- Vahekaart **Lepingu täitmine** lehel **Leping** nurjub lähtestamisel vaikselt, kui lepinguridu pole olemas.
