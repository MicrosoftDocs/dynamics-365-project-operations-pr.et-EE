---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 14, V3
description: See artikkel annab teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 14, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926541"
---
# <a name="project-service-automation-update-release-14-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 14, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse PSA V3 värskenduse väljalaske 14 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.4.21 ja see on saadaval järgmise ajakava järgi.

- **Üldine saadavus (automaatvärskendus):** jaanuar 2020
- **Automaatvärskendus:** veebruar 2020

## <a name="update-release-14"></a>Värskenduste väljalase 14

### <a name="enhancements"></a>Täiustused

- Sales

     - Jaotise **Hinnapakkumise rea üksikasjad** kohandatud välja väärtused kopeeritakse jaotisse **Projektilepingu rea üksikasjad** siis, kui hinnapakkumine värskendatakse olekusse **Suletud võidetuna**.
     - Kinnitatud projekte saab **sulgeda kaotatuna**.

- Ressursihaldus

     - Broneeringute pikendamisel kuvatakse kasutajatele kinnitusega dialoogiakent, et võtta kokku broneeringu tulemused ja anda link broneeringute haldamise juurde.


### <a name="bug-fixes"></a>Veaparandused

- Aeg ja kulu

     - Parandatud: täiustatud kasutajakogemust, kui kasutaja ei ole valinud parandamiseks ühtegi kirjet.

- Ressursihaldus

     - Parandatud: ressursi mitmekordne broneerimine ujutab broneeritava ressursi üle.

- Sales

     - Parandatud: kogu müügihinda ei arvutata enne, kui kasutaja sisestab ka projekti kuluprognoosi omahinna.
     - Parandatud: hinnapakkumise sulgemine olekus **Võidetud** ebaõnnestub, kui seotud projekti leping ei ole olekus **Mustand**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
