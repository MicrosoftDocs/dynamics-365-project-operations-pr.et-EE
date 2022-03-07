---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 31, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 31, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999126"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 31 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.52.77 ja on üldiselt saadaval 2021. a mai enesevärskenduse kaudu.

## <a name="update-release-31"></a>Värskenduste väljalase 31

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Aja sisestamise juhtelemendi käsunupud lehel **Broneeritav ressurss** olid kõlbmatud.
- Ajasisestuse kinnitamisel loodi väljal **Project.SetTrackingFields** nullviite erand.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- **Meeskonna liikme** loomisel ei kuvata broneeringu seadistamise metaandmete sätet **Vaikimisi broneeritud oleku jaoks** õigesti.
- Kui täiendate versioonilt PSA 1.X versioonile 3.X, nurjub versiooniuuendus **UpgradeResourceRequirements**.


**Müük**

Lahendatud on järgmised probleemid.

- Tegelik tulu teisendab summad jälgimisruudustikus projekti valuutasse.
- Valuuta vaikeväärtus on ebaselge, kui loote töölehe read, hinnapakkumise read ja lepinguread stsenaariumides, kus organisatsiooni baasvaluuta erineb projekti valuutast.
- **Töölehe ootel paranduse valideerimise** päring ei filtreeri projekti alusel.
- Ülejäänud müügid arvutatakse projektis valesti.
- Kontaktil põhinevad hinnapakkumised nurjuvad, kui need luuakse ilma hinnakirjata.
- Kui valite suvandi **Kinnita arve**, ei kuvata töötlemisnäidikut.
- Kui valite suvandi **Loo arve**, ei kuvata töötlemisnäidikut.
- Kaotatud hinnapakkumise sulgemisel broneeringuid ei tühistata.







