---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 37, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval versioonis Microsoft Dynamics 365 Project Service Automation Update Release 37, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922493"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project service automation update release 37, V3 jaoks uued või muudetud. Versiooni järgu number on V3.10.58.120 ja see on üldiselt saadaval enesevärskenduse kaudu novembris 2021.

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
