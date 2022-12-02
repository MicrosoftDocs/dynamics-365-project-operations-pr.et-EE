---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 28, V3
description: Selles artiklis loetletakse Project Service Automationi värskenduse väljalaske 28, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930589"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](/power-platform/admin/install-remove-preferred-solution).

Selles artiklis loetletakse funktsioonid ja parandused, mis on uued või muudetud rakenduse Project Service Automation V3 väljalaske 28 jaoks. See versiooni järgu number on V3.10.46.32 ja on üldiselt saadaval enesevärskenduse kaudu jaanuaris 2021.

## <a name="update-release-28"></a>Värskenduste väljalase 28

### <a name="bug-fixes"></a>Veaparandused

**Aeg ja kulu**

Lahendatud on järgmised probleemid.

- Kasutajad saavad kinnitatud ja esitatud ajakirjete värskendamiseks kasutada funktsiooni **Hulgiredigeerimine**.

**Projektijuhtimine**

Lahendatud on järgmised probleemid.

- Juhtudel, kui toimingu GUID-d tõlgendatakse arvuna, ei saa tööülesandeid redigeerimiseks avada lehe **Tööjaotuse struktuur** riba **Tööülesande redigeerimine** abil.

**Sales**

Lahendatud on järgmised probleemid.

- Null-viite erand genereeritakse lisandmooduli **GetEstimatesForProject** käivitamisel.
- Suvand **Märgi arveldamiseks valmis** osamaksete ruudustikus värskendab atribuute ainult osaliselt, välja arvatud atribuut **InvoiceStatus**, mida värskendatakse.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
