---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 26, V3
description: Selles artiklis loetletakse funktsioonid ja parandused, mis on saadaval rakenduses Project Service Automation Update Release 26, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 11f722c1f31c0e8aa08192cc955aabbe97018225
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928795"
---
# <a name="project-service-automation-update-release-26-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 26, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on project service automation update release 26, V3 jaoks uued või muudetud. Selle versiooni järgu number on V3.10.44.59 ja see on kõigile kättesaadav 2020. a detsembris ise värskendamise kaudu.

## <a name="update-release-26"></a>Värskenduste väljalase 26

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Kasutajad saavad muuta kinnitatud/esitatud ajakirje ülesannet.
- Tõrge „Objekti viide pole määratud” ajakirje salvestamisel.
- Ajakirje importimine ressursi määramistest loob ajakirjed valede DateTime väärtustega.
- Kui intstallitud on nii rakendus Project Service Automation kui ka Field Service, kuvatakse rakenduse Field Service ajakirjete jaoks nupp **Uus** käsuribal kaks korda.
- Lahtrite **Luba üksus** ja **Ühikurühm** töötavad nüüd ruudustikus **Kuluarvutused**.
- Vorm **Ajakirje redigeerimise värskendus** hõlmab suvandit **Ajajoon**.
- Mitte-projektipõhiste ajakirjete kellaaja kinnitamine blokeerib süsteemi projekti kinnitaja rolli otsimisel.

**Ressursihaldus**

Lahendatud on järgmised probleemid.

- Lisatud on lisandmooduli **PostProjectCreate** valideerimine, et kontrollida enne selle loomist peamist nõuet.
- Kiirloomisvorm **Projekti meeskonnaliige** esitab nullviite erandi, kui väljad eemaldatakse vormist.
- 12-tunniste nõuete loomine üle ühe aasta nurjub.
- Paranenud on veateate nullviite erand ressursinõude loomise ajal.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Paranenud on valideerimine nullviite erandi adresseerimiseks, mis on loodud lisandmoodulis **PreProjectUpdate**.
- Microsoft Projecti töölaua lisandmooduli poolt avaldatud projektd kustutavad määramata ülesanded.
- Lisatud uus valideerimine, kui tööülesande projektiviide on kehtetu nullviite erandi tõttu lisandmoodulis **PreValidateProjectTaskUpdate**.
- Meeskonnaliikmete ruudustik ei kuva meeskonnaliikme kirjes eraldi määramisi.
- Lisatud on uus valideerimine ja tõrketeated nullviite erandi tõttu lisandmoodulis **PreProjectTaskDelete**.

**Sales**

Lahendatud on järgmised probleemid.

- Projektipõhise rea hinnapakkumise või lepingu valimisel peaks nupp **Soovitus** olema nähtav ainult siis, kui valite projektipõhise rea, mis on seotud olemasoleva tootega.
- Eraldage õigus **Create_Product** õigusest **Create_ProjectContract**.
- Arverea kustutamine põhjustab nuppviite tõrget lisandmoodulis **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
