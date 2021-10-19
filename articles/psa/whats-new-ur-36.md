---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 36, V3
description: Selles teemas loetletakse funktsioonid ja parandused, mis on saadaval rakenduse Microsoft Dynamics 365 Project Service Automation värskenduse väljaandes 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606746"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada rakenduse Microsoft Dynamics 365 Project Service Automation uusimast värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See ühildub rakendusega Dynamics 365 9.x. Sellele väljaandele värskendamiseks külastage Dynamics 365 veebilahenduste halduskeskust ja installige värskendus. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 36 ver 3 uued või muudetud funktsioonid ja parandused. Selle versiooni järgunumber on V3.10.57.152 ja see on oktoobris 2021 automaatvärskendusega kõigile saadaval.

## <a name="update-release-36"></a>Värskenduste väljalase 36

### <a name="bug-fixes"></a>Veaparandused

Lahendatud on järgmised probleemid.

**Üldist**
- Välja **Vaikimisi töötundide mall** nimi on lehel **Projekti parameetrid** valesti tõlgitud.
- Asünkroonsed lisandmoodulid ei tule toime eranditega, mis on seotud atribuudiga **SharedVariableService**.

**Aeg ja kulu**
- Kui töölehe read puuduvad või kasutajal ei ole töölehe ridade lugemiseks õigeid lubasid, ilmub vale tõrge, kui projekti kinnitamised tühistatakse.
- Kasutajad ei saa kinnitust tühistada, kui kulu- või ajakirjel on rohkem kui üks seostatud projektikinnitus.
- Suvandid **Puudumine** ja **Puhkus** on hiina keeles kiirloomislehe **Ajakirje** otsingus valesti tõlgitud.

**Ressursihaldus**
- Kasutaja ei saa **ajakavaabimehes** ressursse otsida, kui vaaterežiimiks on määratud **Päev**, **Nädal** või **Kuu**.
- Üldistel ressurssidel lubatakse valesti tühjade asukohanimede kasutamist. 
- Kaotatud lepingu sulgemine ei tühista tulevasi broneeringuid.

**Müük**
- Kui keskkonnas on suur hulk tooteid, jõudluse ruudustikus **Materjalide prognoos** väheneb.
- Projekti mallist loomisel projekti valuuta ei tule vaikimisi vastava projektihalduri lepinguüksuset.
- Tegelikud summad ei vasta alati projekti tähtajal kajastatule või summad muutuvad konkreetsetes stsenaariumides negatiivseks.
- Tõrge ilmneb, kui seostate projektimallist loodud projekti lepingureaga.
- Kasutajad saavad kustutada lepingurea, millel on vahe-eesmärgid, **Arveldamiseks valmis** ja **Loodud arve**. See ei tohiks olla lubatud.
- Kui prognoosid imporditakse projektist, määratakse hinnapakkumise rea arveldatavus valesti, kui ülesandepõhine arveldamine on hinnapakkumise rea jaoks lubatud.
- Fikseeritud hinnaga arveldamise vahe-eesmärgi lisamisel ei kajastu vahe-eesmärk selle ruudustikus enne lehe värskendamist.
- Projektilepingu loomisel tühja hinnapakkumise nimega luuakse tühja viite erand.
- Käsitsi režiimis ülesanded, mille puhul projekti valuuta erineb ressursi valuutast, toob kaasa vale hinnaprognoosi.
- Kasutajad ei saa kutsuda tagasi tehingut, mille korrigeeriv arve on edukalt korrigeerinud.
- Desaktiveeritud kannete kategooriad kuvatakse ruudustikus **Kuluprognoosid**.



