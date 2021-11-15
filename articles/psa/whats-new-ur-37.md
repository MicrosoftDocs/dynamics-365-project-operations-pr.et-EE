---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 37, V3
description: Selles teemas loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727600"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 37, V3 uued või muudetud funktsioonid ja parandused. Versiooni järgu number on V3.10.58.120 ja see on üldiselt saadaval enesevärskenduse kaudu novembris 2021.

## <a name="update-release-37"></a>Värskenduste väljalase 37

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**
- Kasutajad ei saa lahtri tühjendamisega ajakirjet kustutada.
- Vaade **Minu nurjunud kinnitused** sisaldab ainult projekti kinnitusi olekuga **Edastatud**.

**Projektijuhtimine**
- Kasutajad saavad projekti avamisel Microsoft Desktopi lisandmoodulis tühja viite erandi tõrke, kui projektimeeskonna liikme ametikoha nimi on tühi.
- Lehel **Projekti ülesanne** pole nuppu **Salvesta**, mistõttu kasutajad ei saa ülesandekirjetesse muudatusi salvestada.
- Kasutajad ei saa kustutada projekti, mille ülesanne on seostatud hinnapakkumisega, mille olek on **Võidetud**.

**Müük**
- Lehel **Projekt** olevat välja **Valuuta** värskendatakse, et see vastaks rakendatud malli valuutale.
- Kulu arvutatakse valesti ülesannete puhul, millel on mitu valuutat.
