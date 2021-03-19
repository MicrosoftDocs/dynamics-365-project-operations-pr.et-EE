---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 19, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 19, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280708"
---
# <a name="project-service-automation-update-release-19-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 19, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse PSA V3 värskenduse väljalaske 19 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.30.41 ja on üldiselt saadaval 2020. a mai enesevärskenduse kaudu.

## <a name="update-release-19"></a>Värskenduste väljalase 19

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid. 

- Ajakirjest importimisel tuletatud tõrked pole õigesti esile toodud.
- Ajakirje ruudustik ei toeta välja **Ainult kuupäev** käitumist.
- Projekti ressursid ei saa projektiga kulu luua.

**Projektijuhtimine**

Lahendatud on järgmised probleemid. 

-  Alamülesande alamülesanne põhjustab vale koormuse prognoosi arvutamise lõpileviimisel (EAC).

**Sales**

Lahendatud on järgmised probleemid. 

- **Ümberarvutamine** ei tööta kulude lepingurea üksikasjadega või hinnapakkumise rea üksikasjadega.
- **Uuendatud hinnad** puuduvad kulude prognoosi jaoks.
-  Kliendid ei saa valida lehelt **Projekti leping** kohandatud lepingu oleku põhjust.
- Kliendikogemuse nõrgem tulemus, kui luua hinnapakkumisest kohandatud hinnakirja.
- Kliendid kogevad vastuolu **ühiku** vaikeväärtustega lehtedel **Hinnapakkumise rea üksikasjad** ja **Lepingu rea üksikasjad**.
- Mittearveldatavate kannete kategooria üksuste lisamine arveldatavale lepingureale ei austa kande kategooria **mittearveldatavat** arveldustüüpi.
- Kliendid ei saa varem loodud lepingutes kasutada äsja lisatud rolle ja kategooriaid.
- Kliendid kogevad ebavajaliku toomise nõrgemat tulemust PreValidateProjectTeamMemberUpdate.cs korral
- Rollid luuakse kui mittearveldatavad loendis **Ressursikategooriad** tuleb lisada vahekaardile **Arveldatavad rollid** kui **Mittearveldatavad** projekti lepingureas.
- Projekti loomisel võivad kliendid halvenenud tulemusi kogeda, kuna **GetBookableResourceIdFromUser** toob esmase ID asemel kõik arvestusliku ressursi veerud.
- Olemist **TransactionType** puudub eelvalideerimise uuenduse lisandmoodul, et takistada kasutajatel sisestada **Üksusi** ja **Üksusegruppe**, mis ei kehti kandetüüpide jaoks.
- Etapp **Eemaldamine** ei tööta ajakirje impordi puhul.


[!INCLUDE[footer-include](../includes/footer-banner.md)]