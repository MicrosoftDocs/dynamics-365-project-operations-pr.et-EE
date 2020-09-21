---
title: Mida on uut rakenduse Project Service Automation värskenduse väljaandes 14, v3
description: Selles teemas antakse teavet selle kohta, mida on uut rakenduse Project Service Automation värskenduse väljaandes 14, v3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750963"
---
# <a name="project-service-automation-v3-update-release-14"></a>Rakenduse Project Service Automation V3, värskenduse väljaanne 14
Meil on hea meel teatada uusimast rakenduse Dynamics 365 Project Service Automation (PSA) värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskust ja avage värskenduse installimiseks lahenduste leht. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse PSA V3 värskenduse väljalaske 14 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgu number on V3.10.4.21 ja see on saadaval järgmise ajakava järgi.

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

