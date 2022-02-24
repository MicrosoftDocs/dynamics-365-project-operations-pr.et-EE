---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 25, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 25, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143734"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse funktsioonid ja parandused, mis on uued või muudetud rakenduse Project Service Automation versiooni 3 jaoks, värskenduses 25. See versiooni järgu number on V 3.10.43.76 ja on üldiselt saadaval ise värskendamise kaudu oktoobris 2020.

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
