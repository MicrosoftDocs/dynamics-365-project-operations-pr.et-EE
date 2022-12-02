---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 25, V3
description: Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 25, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922539"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on uued või muudetud rakenduse Project Service Automation versiooni 3 jaoks, värskenduses 25. See versiooni järgu number on V 3.10.43.76 ja on üldiselt saadaval ise värskendamise kaudu oktoobris 2020.

## <a name="update-release-25"></a>Värskenduste väljalase 25

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Järgmised probleemid on parandatud.

- Ajakirje diagramm näitas täiendavaid andmeid liiga suure toodud intervalli põhjal.

**Ressursihaldus**

Järgmised probleemid on parandatud.

- Lisatud paki juurutamise kood, et jätta teenuse Universal Resource Scheduling paiga importimine vahele, kui uuema versiooni paik on juba olemas.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Parandatud on ümardamise ja vahetuskursi lahknevusi, mis põhjustasid projekti jälgimise ruudustikus valesti planeeritud kulu.
- Vormil **Projekt** kahe või rhkema reageerimisruudustiku kuvamise võimaluse tugi.
- Esitatud valideerimine, et lahendada võime määrata ülesanne, mis on kalendri lõpukuupäevast hilisem, mis põhjustab ressursi määramise nurjumise.
- Parandatud on vea käsitlemine, et tegeleda null-viite erandiga, mis loodi järgnevast.

    - Lisandmoodul **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate**, kui projekti ülesanne on loodud ilma seostatud pojektita
    - Lisandmoodul **PreProjectTeamMemberCreate**
    - Lisandmoodul **PostProjectTeamMemberDelete**
    - Lisandmoodul **PreValidateProjectTaskDelete**

**Sales**

Lahendatud on järgmised probleemid.

- Täiustatud vigade käsitlemine, et lahendada null-viite erandid, mis on loodud suvandist **Projekti kopeerimine: prognoosib abiressursi halduse**.
- Valik **Pole arveldamiseks valmis** suvandis **Aja ja materjali arveldamise võlgnevus** ei tühjenda arveldamise olekut.
- Parandatud valesti sildistatud nupud **Hinnad** vahekaartidel **Rolli hind** ja **Kataloogi üksus**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
