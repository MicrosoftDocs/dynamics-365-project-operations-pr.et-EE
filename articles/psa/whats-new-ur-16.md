---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 16, V3
description: Selles artiklis on loetletud funktsioonid ja parandused, mis on saadaval project service automation update release 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926495"
---
# <a name="project-service-automation-update-release-16-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 16, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.  See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine](/dynamics365/project-service/upgrade-psa-home-page).
Selles artiklis loetletakse funktsioonid ja parandused, mis on PSA V3, Update Release 16 jaoks uued või muudetud. Selle versiooni järgunumber on V3.10.6.34 ja see on jaanuaris 2020 automaatvärskendusega kõigile saadaval.


## <a name="update-release-16"></a>Värskenduste väljalase 16

### <a name="bug-fixes"></a>Veaparandused

-   Aeg ja kulu

    -   Parandatud: kasutajad, kes püüavad kinnitamiseks esitada kustutatud aja- ja kulukirjeid, ei saa nüüd asjakohaseid tõrketeateid.

-   Projektijuhtimine

    -   Parandatud: meeskonnaliikmetele mallides määratud ressursiüksuseid rakendatakse uuele projektile.

    -   Parandatud: kirje omandiõiguste ümbermääramise käsitlemise täiustamine.

    -   Parandatud: kopeeritavaid projekte ei lubata kopeerida enne, kui kõik kopeerimistoimingud on lõpetatud.

-   Ressursihaldus

    -   Parandatud: broneeringute pikendamine toimib nüüd lühikeste kestustega õigesti ja ei loo enam pikendatud broneeringutele null-tunde.

    -   Parandatud: nüüd renderdatakse vastavusseviimise vaade, kui projekti ajavöönd on + 5:30 GMT ja kasutaja ajavöönd on erinev.

-   Sales

    -   Parandatud: kui lepingureale vastendatud projekt eemaldatakse ja uus projekt vastendatakse, siis uue projekti tegelikke kirjeid ei hinnatud uut projekti ümber lepingureal määratletud arvelduse ja hinnakujunduse põhjal. See on selles väljalaskes parandatud. Äsja vastendatud projekti hinnastamine ja tegelikud kirjed pööratakse tagasi ja luuakse uuesti õigesti, vastavalt lepingurea hinnastamis- ja arveldusreeglitele. Vastendamata projekti tegelikud kirjed hinnatakse samuti ümber ja luuakse selle tulemusel uuesti.

    -   Parandatud: täiendav valideerimine on lisatud prognoosi rea väljale **Summa**, et tagada null-väärtuste säilimine.

    -   Parandatud: kui projekti tegelikud näitajad on värskendatud, on projekti põhivormile lisatud värskendamise nupp, et võimaldata kasutajatele tegelike näitajate uuesti sünkroonimine.

    -   Parandatud: kui kasutajad värskendavad versioonilt 2. X versioonile 3. X, lubatakse NULL väärtusega projektinimega projektid.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
