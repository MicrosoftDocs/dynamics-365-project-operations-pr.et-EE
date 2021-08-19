---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 34, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 34, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009751"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 34 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V3.10.55.38 ja see on üldsusele isevärskenduse kaudu kättesaadav juulis 2021.

## <a name="update-release-34"></a>Värskenduste väljalase 34

### <a name="bug-fixes"></a>Veaparandused
Lahendatud on järgmised probleemid.

**Üldist**

- Väljaandjapõhised värskendused ei aktiveeri uut tänapäevast kinnitamise töövoogu.
- **Kinnitamiskomplekti** põhilehel on puudu atribuudid **Sihtkoha olek** **Toimingu tüüp**.

**Aeg ja kulu**

- Tänapäevase kinnitamisvoo abil ei saa tagasivõtmistaotlust kinnitada.
- Nädala ajakirjete kopeerimine ei toimi, kui kopeeritakse kirjeid, mis pole sisselogitud kasutajaga seotud.

**Projekti kavandamine**

- Ressursimääramise kontuurid on Microsoft Projecti töölaua lisandmoodulist importimisel rikutud.

**Ressursihaldus**

- Projekti avaldamisel Microsoft Projecti töölauakliendi lisandmoodulist muudetakse olemasolevate nõuete lõppkuupäeva.
- Kümnendkohaline täpsus ületab broneeringu kinnituse dialoogis kaht kümnendkohta.

**Müük**

- Projektilepingule olemasoleva tootega tootepõhise rea lisamisel kuvatakse erand **sõnastikust võtit ei leitud**.
- Müügivihjeid ei saa kvalifitseerida juhul, kui tellimuse tüüp vastendatakse müügivihjest müügivõimaluseni.
