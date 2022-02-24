---
title: Mida on uut või muudetud rakenduse Project Service Automation värskenduse väljaandes 17, V3
description: Selles teemas loetletakse Project Service Automationi värskenduse väljalaske 17, V3 saadaolevaid funktsioone ja parandusi.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143701"
---
# <a name="project-service-automation-update-release-17-v3"></a>Rakenduse Project Service Automation, värskenduse väljaanne 17, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Meil on hea meel teatada uusimast Dynamics 365 Project Service Automationi rakenduse värskendusest. See väljaanne sisaldab mõningaid olulisi kvaliteedi, jõudluse ja kasutatavuse täiustusi.  See väljalase ühildub Dynamics 365 9. x-iga. Sellele väljaandele värskendamiseks külastage veebis Dynamics 365 administreerimiskeskuse lahenduste lehte värskenduse installimiseks. Lisateabe saamiseks vt jaotist [Eelistatud lahenduse installimine, värskendamine või eemaldamine](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Selles teemas loetletakse PSA V3 värskenduse väljalaske 17 uusi või muudetud funktsioone ja parandusi. Selle versiooni järgunumber on V3.10.6.34 ja see on märtsis 2020 automaatvärskendusega kõigile saadaval.


## <a name="update-release-17"></a>Värskenduste väljalase 17

### <a name="bug-fixes"></a>Veaparandused

**Üldine**

- Parandatud: värskendada Project Service Automation, et rakendada rakenduse Team Member litsentsid (Projekti ressursside keskus sisaldab Team Memberi teenuse plaani metaandmeid 3.x)
 
**Aeg ja kulu**

- Parandatud: ei ole võimalik muuta kuluprognoosi nullist erinevalt hinnalt nulli (0) peale. Muudatust ignoreeritakse.

**Projektijuhtimine**

- Parandatud: meeskonnaliikme positsiooni nimele on lisatud null-väärtuste kontroll.
- Parandatud: **msdyn_userresourceid** väli olemil **msdyn_resourceassignment** on kasutuselt kõrvaldatud.
- Parandatud: värskendus versioonilt 2.x versioonile 3.x käsitleb nüüd ülesande määrangute tühje panusekontuure.

**Sales**

- Parandatud: **Arve.PreValidateInvoiceUpdate** käsitleb nüüd kirje omanike ümbermääramise stsenaariumi õigesti.
- Parandatud: kui tehingu klass on **Aeg**, on **UnitGroup** redigeerimatu kõigi olemite, sealhulgas olemite **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ja **ContractLineDetails**, korral. Siiski, **Ühik** on redigeerimatu ainult olemite **JournalLine** ja **InvoiceLineDetails** korral.


