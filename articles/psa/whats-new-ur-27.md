---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 27, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 27, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146658"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi V3 värskenduse väljalaske 27 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V3.10.45.98 ja see on jaanuaris 2021 automaatvärskendusega kõigile saadaval.

## <a name="update-release-27"></a>Värskenduste väljalase 27

### <a name="bug-fixes"></a>Veaparandused

**Üldine**

Lahendatud on järgmised probleemid.

- Project Service Automationis lisandmoodulite loodud logid ei ole määratud automaatsele kustutamisele.
- Automaatne värskendamine nurjub, sest lahendus Project Service Automation sisaldab pärand null NavBarArea ja pealkirja elemente.

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Ruudustik **Ajakirje** kuvab **ajavööndist sõltumatu** kuupäeva käitumise kohta valesid andmeid.
- Ruudustik **Ajakirje** loob **ajavööndist sõltumatu** kuupäeva käitumise kohta vale aja.
- Ülesande otsing ei ole piiratud valitud projektiga lehel **Ajakirje redigeerimine**.
- Mitte-projektipõhiste ajakirjete kellaaja kinnitamine on blokeeritud, sest süsteem otsib projekti kinnitajat.
- Õiged tegelike andmete kirjed kuvavad vale tõrketeadet.
- Kui tööülesanne sisaldab tegeliku kulu nullväärtust ja projekti kogusummasid värskendatakse, ilmneb järgmine tõrge: "Antud võtit pole sõnastikus".
- Kindlatel juhtudel ei kuva filtrid **Rühmitusalus** vahekaardil **Projekti prognoos** kuluprognoose.
- **Suveaja** intervall ei ole ajakirjete jaoks õige.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Vahemälu täiustused, mis võimendavad lehe **Projekt** laadimisega seotud jõudlust.
- Aegunud ärireegel ei lase projekti ülesandeid lõpetada.
- Microsoft Projecti lisandmooduli kontuurid ei pea kinni lisandmoodulite kalendrist, mille tulemuseks on valed ressursinõuded.
- Projektide loomine mallidest seab määramise kuupäevad valesti ja takistab ressursinõuete genereerimist.
- Kasutajad ei pääse klaviatuuri abil ligi suvanditele **Kategooria**, **Kirjeldus**, **Olek**.
- Projekti tegelikud müügiväärtused ei sisalda tasusid ja materjalide müügiväärtusi.
- Tegeliku müügi ja tegeliku kulu koondamine toimub erinevate vahetuskurssidega valesti.
- Jaotise **Töötunni vaikemall** kirjeldus on eksitav.
- Toimingu alandamine ei eemalda kasutajaliidesest **Kategooriat** enne, kui seda värskendatakse.
- Ei lubata kinnituse puudumist, et tagad projekti liikumine lõpukuupäevast edasi.

**Sales**

Lahendatud on järgmised probleemid.

- Projekti hinnapakkumise real luuakse nullviite erand, kuna **Impordi projektiprognoosist** on nähtav, kui projekti pole valitud.
- Järgmine tõrge "Objektiviide pole seatud objekti eksemplarile" ilmneb siis, kui hinnapakkumine on suletud olekus **Võidetud**.
- Projekti lepingurea seose tühistamise ajal ei määrata muudatuse olekut tegeliku tagasipööramise ajal.
- Kui Dynamics 365 Field Service ja Project Service Automation on mõlemad installitud, ei kuvata suvandeid **Lukusta hinnakujundus** ja **Kasuta praegust hinnakujundust** samaaegselt lehel **Arve**.
- Jaapani keele puhul pole tõlge muude kalendripõhiste lehtedega kooskõlas.
- **Aktiveeri** ja **Deaktiveeri** on Project Service Automationis olemitest **Hinnakirja sidumine** eemaldatud.


[!INCLUDE[footer-include](../includes/footer-banner.md)]