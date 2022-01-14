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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901507"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse funktsioonid ja parandused, mis on project Service Automation Update Release 38, V3 jaoks uued või muudetud. Selle versiooni järgu number on V3.10.59.117 ja see on kõigile kättesaadav 2021. a detsembris ise värskendamise kaudu.

## <a name="update-release-38"></a>Värskenduste väljalase 38

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Aeg ja kulu**

- Erand ilmneb siis, kui kinnituskomplekti logide pikkus ületab 100 000 kirjet.
- Kasutajad ei pääse **ajakirje** ruudustikule juurde **ajakirje** avalehel.
- **Dialoogiboksis Ajakande importimine** ei kuvata teksti, kui ühtegi üksust pole importimiseks sobilik.
- Kasutajad saavad luua kinnituskomplekte, kus **välja Sihtolek** väärtuseks on seatud **Tundmatu**.

**Projektijuhtimine**

- Utc (+09:30) ja UTC (+10:00) ressursimäärangutes ei kuvata suveaja alguses õigesti kontuure.
- **Tööjaotusstruktuuride väli Lisaveerg** on mõnes lokas peidetud.
- Projektiülesande ruudustiku kalendri juhtelemendi kuupäevavalija **pole hiina keele jaoks õigesti** lokaliseeritud.

**Müük**

- **Lepingu jõudluse** ja projekti tegeliku kulu väärtused ei **ühti**, kui broneeritavad ressursid, millel on erinevad lepinguüksused ja valuutad, esitavad ajakandeid.
- Kohandatud töövoog arvete automaatseks kinnitamiseks nurjub, kui arved imporditakse hallatav lahendus. Kuvatakse järgmine teade: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Teade: Kehtetu arve olek."
- Kui **summeerimissuvandiks** on valitud Juur ja projektil on hinnangud kannete klasside segust (näiteks aja, kulu ja materjali hinnangute kombinatsioon), võtab süsteem tehinguklasside vahel kokku ühe tasurea.
- Stsenaariumides, kus kulurida lisatakse enne lepingurea seostamist projektiga, ei sisestata õiget hinnakujundust vaikeväärtusena **väljale** Värskendushind.
- Negatiivsed müügisummad pole **projekti** ja tööülesande **olemite** puhul lubatud.
