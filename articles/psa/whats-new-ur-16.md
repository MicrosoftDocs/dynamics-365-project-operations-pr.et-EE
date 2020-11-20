---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 16, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 16, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121573"
---
# <a name="project-service-automation-update-release-16-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 16, v3

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.  See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Selles teemas loetletakse PSA V3 värskenduse väljalaske 16 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V3.10.6.34 ja see on jaanuaris 2020 automaatvärskendusega kõigile saadaval.


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

