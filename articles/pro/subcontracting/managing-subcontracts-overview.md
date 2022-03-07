---
title: Allhankelepingute haldus rakenduses Project Operations
description: Selles teemas antakse terviklik ülevaade allhankelepingute haldusprotsessi kohta rakenduses Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994226"
---
# <a name="subcontract-management-in-project-operations"></a>Allhankelepingute haldus rakenduses Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduse Microsoft Dynamics 365 Project Operations allhankelepingud toetavad järgmist äriprotsessi voogu.

![Allhankelepingute sõlmimisprotsessi voog](../media/SubcontractingProcessFlow.png)

Siin on allhankelepingute sõlmimisprotsessi üksikasjalik kirjeldus.

1. Projektijuht sõlmib hankijaga allhankelepingu. Vaikimisi kasutatakse allhankelepingut sõlmides hankijakirjele lisatud hinnakirju. Hankija kontol on seosetüüp **Hankija** või **Tarnija**.
2. Projektijuht saab kõik ostud täpsustada allhankelepingu reaüksustena. Allhankelepingu read võivad olla aja, kulude või toodete jaoks. Igal allhankelepingu real valitud tehinguklass määratleb, mille jaoks rida on.
3. Hankija kontohaldur ja projektijuht saavad allhankelepingut itereerida. Hinnakirju saab kohandada ostuhinnakirjades, mis on allhankelepingule manustatud.
4. Kui allhankeleping on ajapõhine, seostab hankija kontohaldur selles või hilisemas protsessi punktis kontaktid iga allhankelepingu reaga. See seos annab teavet projektijuhile, kes töötab allhankelepinguga. Kui kontakt seostatakse allhankelepingu reaga, loob süsteem kontaktist automaatselt broneeritava ressursi, kui broneeritavat ressurssi pole veel olemas.
5. Iga allhankelepingu rea arveldamisviisiks võib olla **Fikseeritud hind** või **Aeg ja materjal**. Fikseeritud hinnaga allhankelepingu ridade jaoks saate seadistada vahe-eesmärgi põhise arve ajakava.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
