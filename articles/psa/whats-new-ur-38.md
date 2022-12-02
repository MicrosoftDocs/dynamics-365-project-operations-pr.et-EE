---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 38, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 38, V3.
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915180"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 38, V3 uued või muudetud funktsioonid ja parandused. Selle versiooni järgu number on V3.10.59.117 ja see on kõigile kättesaadav 2021. a detsembris ise värskendamise kaudu.

## <a name="update-release-38"></a>Värskenduste väljalase 38

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**

- Erand tekib siis, kui kinnituskomplekti logide pikkus ületab 100 000 kirjet.
- Kasutajad ei pääse **Ajakirje** ruudustikule juurde **Ajakirje** avalehelt.
- Dialoogiboksis **Ajakirje import** ei kuvata teksti, kui ükski üksus pole importimiseks sobilik.
- Kasutajad saavad luua kinnituskomplekte, kus välja **Sihtolek** väärtuseks on määratud **Tundmatu**.

**Projektijuhtimine**

- Suveaja alguses ei kuvata kontuure õigesti UTC(+09:30) ja UTC(+10:00) ressursside määramisel.
- Välja **Lisaveerg** tööde jaotusstruktuuri jaoks on mõnes piirkonnas peidetud.
- **Projekti ülesanne** ruudustiku kalendrikontrolli kuupäevavalik ei ole hiina keele jaoks korrektselt lokaliseeritud.

**Müük**

- **Lepingu jõudlus** ja **Projekti kulu tegelikud näitajad** väärtused ei ühti, kui broneeritavad ressursid, millel on erinevad lepingulised üksused ja valuutad, esitavad ajakirjeid.
- Kohandatud töövoog arvete automaatseks kinnitamiseks ebaõnnestub, kui arved imporditakse hallatava lahendusena. Kuvatakse järgmine teade: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException Teade: kehtetu arveolek“.
- Kui summeerimisvalikuks on valitud **Juur** ja projektis on prognoosid erinevatest tehinguklassidest (näiteks aja-, kulu- ja materjaliprognooside kombinatsioon), teeb süsteem tehinguklasside kokkuvõtte üheainsa tasu rida.
- Stsenaariumides, kus kulurida lisatakse enne lepingurea seostamist projektiga, ei sisestata väljale **Värskenda hinda** vaikeväärtusena õiget hinnakujundust.
- Negatiivsed müügisummad ei ole üksuste **Projekt** ja **Ülesanne** puhul lubatud.
