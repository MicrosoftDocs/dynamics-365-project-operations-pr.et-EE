---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 28, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 28, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150618"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi. See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse funktsioonid ja parandused, mis on uued või muudetud rakenduse Project Service Automation V3 väljalaske 28 jaoks. See versiooni järgu number on V3.10.46.32 ja on üldiselt saadaval ise värskendamise kaudu jaanuaris 2021.

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

