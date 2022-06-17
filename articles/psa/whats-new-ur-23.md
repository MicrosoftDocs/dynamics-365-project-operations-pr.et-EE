---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 23, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval project service automation update release 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913024"
---
# <a name="project-service-automation-update-release-23-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 23, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project Service Automation V3, Update Release 23 jaoks uued või muudetud. Selle versiooni järgunumber on V 3.10.34.30 ja see on augustis 2020 automaatvärskendusega kõigile saadaval.

## <a name="update-release-23"></a>Värskenduste väljalase 23

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.
- Servajuhtumi käsitlemine suvandis **Projektimeeskonnaliikme kustutamine**, et pakkuda mõttekat erandit.
- Ülesande importimise tulemuseks on tühi eemaldamise ekraan.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- **Ressursikasutuse ruudustiku ressursi kaardil** kuvatakse valed andmed, kui ajaskaala on pikem kui viis päeva.
- Kui kliendid loovad broneeritava ressursi, siis lisandmoodulil aeg-ajalt ei õnnestu lisada ressurssi automaatselt Microsoft Office 365 rühma.
- Vaade **Vastavusseviimine** kuvab vaates **Nädal** või **Kuu** käsitsi kontuurid valesti.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Liiga suur hulk olemeid **RetrieveMultiple suvandi usersettings jaoks** põhjustab projektide kinnitamiste ja teiste toimingute jõudluse halvenemist.
- Ruudustiku **Ülesande planeerimise** ressursi otsing on piiratud ainult kuni viie projektimeeskonna meeskonnaliikmeni. 
- Ruudustiku **Ülesande planeerimine** ressursiotsing ei filtreeri passiivseid ressursse.
- Käsitsi režiim ei tööta projekti planeerimise tööjaotuse struktuuris ootuspäraselt.
- Ruudustik **Ülesande planeerimine** kuvab **Passiivsed tehingukategooriad**.
- Kui ülesandel on mitu määramist, ümardab ruudustik **Ressursi määramine** valesti.
- Ühe ülesande planeeritud kulu ja tegeliku kulu ümardamise väärtused on erinevad.

**Sales**

Lahendatud on järgmised probleemid.

- Suvandi **Too kõik tehingukategooriad** topeltklõpsamine loob mitu rida.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
