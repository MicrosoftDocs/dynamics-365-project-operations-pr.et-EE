---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 23, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 23, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074903"
---
# <a name="project-service-automation-update-release-23-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 23, v3

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 23 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V 3.10.34.30 ja see on augustis 2020 automaatvärskendusega kõigile saadaval.

## <a name="update-release-23"></a>Värskenduste väljalase 23

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.
- Servajuhtumi käsitlemine suvandis **Projektimeeskonnaliikme kustutamine** , et pakkuda mõttekat erandit.
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
