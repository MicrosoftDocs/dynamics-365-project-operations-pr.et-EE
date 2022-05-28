---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 38, V3
description: Selles teemas loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598713"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse funktsioonid ja parandused, mis on project service automation update release 38, V3 jaoks uued või muudetud. Selle versiooni järgu number on V3.10.59.117 ja see on kõigile kättesaadav 2021. a detsembris ise värskendamise kaudu.

## <a name="update-release-38"></a>Värskenduste väljalase 38

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**

- Erandiks on see, kui kinnituskomplekti logide pikkus ületab 100 000 kirjet.
- Kasutajad ei pääse ajasisestuse avalehelt **ajasisestuse** **ruudustikule juurde**.
- Dialoogiboksis **Ajasisestuse importimine** ei kuvata teksti, kui ükski üksus pole importimiseks sobilik.
- Kasutajad saavad luua kinnituskomplektid, **kus välja Sihtolek** väärtuseks **on seatud Teadmata**.

**Projektijuhtimine**

- Suveaja alguses ei kuvata kontuure õigesti UTC (+09:30) ja UTC (+10:00) ressursimääramistes.
- Tööjaotusstruktuuride **väli Täiendav veerg** on mõnes lokaadis peidetud.
- Projektiülesande **ruudustiku kalendri juhtelemendi** kuupäevavalija pole hiina keeles õigesti lokaliseeritud.

**Müük**

- **Lepingu täitmise** ja **projekti tegeliku kulu** väärtused ei ühti, kui broneeritavad ressursid, millel on erinevad lepinguühikud ja valuutad, esitavad ajakandeid.
- Arvete automaatseks kinnitamiseks kohandatud töövoog nurjub, kui arved imporditakse hallatav lahendus. Kuvatakse järgmine teade: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Invalid invoice olek."
- Kui **root** on valitud summeerimissuvandiks ja projektil on hinnangud tehingute klasside segust (nt aja-, kulu- ja materjaliprognooside kombinatsioon), võtab süsteem tehinguklasside lõikes kokku ühe tasureana.
- Stsenaariumides, kus kulurida lisatakse enne lepingurea seostamist projektiga, ei sisestata õiget hinnakujundust vaikeväärtusena väljale **Värskendushind**.
- Negatiivsed müügisummad pole projekti **- ja** tööülesandeolemites **lubatud**.
