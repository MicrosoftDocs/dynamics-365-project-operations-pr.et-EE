---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643258"
---
<a name="project-service-automation-update-release-26-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 26, v3
================================================

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 26 ver 3 uused või muudetud funktsioonid ja parandused. Selle versiooni järgu number on V3.10.44.59 ja see on kõigile kättesaadav 2020. a detsembris ise värskendamise kaudu.

<a name="update-release-26"></a>Värskenduste väljalase 26
-----------------

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

-   Kasutajad saavad muuta kinnitatud/esitatud ajakirje ülesannet.

-   Tõrge „Objekti viide pole määratud” ajakirje salvestamisel.

-   Ajakirje importimine ressursi määramistest loob ajakirjed valede DateTime väärtustega.

-   Kui intstallitud on nii rakendus Project Service Automation kui ka Field Service, kuvatakse rakenduse Field Service ajakirjete jaoks nupp **Uus** käsuribal kaks korda.

-   Lahtrite **Luba üksus** ja **Ühikurühm** töötavad nüüd ruudustikus **Kuluarvutused**.

-   Vorm **Ajakirje redigeerimise värskendus** hõlmab suvandit **Ajajoon**.

-   Mitte-projektipõhiste ajakirjete kellaaja kinnitamine blokeerib süsteemi projekti kinnitaja rolli otsimisel.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

-   Lisatud on lisandmooduli **PostProjectCreate** valideerimine, et kontrollida enne selle loomist peamist nõuet.

-   Kiirloomisvorm **Projekti meeskonnaliige** esitab nullviite erandi, kui väljad eemaldatakse vormist.

-   12-tunniste nõuete loomine üle ühe aasta nurjub.

-   Paranenud on veateate nullviite erand ressursinõude loomise ajal.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

-   Paranenud on valideerimine nullviite erandi adresseerimiseks, mis on loodud lisandmoodulis **PreProjectUpdate**.

-   Microsoft Projecti töölaua lisandmooduli poolt avaldatud projektd kustutavad määramata ülesanded.

-   Lisatud uus valideerimine, kui tööülesande projektiviide on kehtetu nullviite erandi tõttu lisandmoodulis **PreValidateProjectTaskUpdate**.

-   Meeskonnaliikmete ruudustik ei kuva meeskonnaliikme kirjes eraldi määramisi.

-   Lisatud on uus valideerimine ja tõrketeated nullviite erandi tõttu lisandmoodulis **PreProjectTaskDelete**.

**Sales**

Lahendatud on järgmised probleemid.

-   Projektipõhise rea hinnapakkumise või lepingu valimisel peaks nupp **Soovitus** olema nähtav ainult siis, kui valite projektipõhise rea, mis on seotud olemasoleva tootega.

-   Eraldage õigus **Create_Product** õigusest **Create_ProjectContract**.

-   Arverea kustutamine põhjustab nuppviite tõrget lisandmoodulis **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
