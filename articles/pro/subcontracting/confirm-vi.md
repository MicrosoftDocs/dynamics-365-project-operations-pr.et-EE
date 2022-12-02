---
title: Projekti hankija arve kinnitamine
description: See artikkel selgitab, kuidas kinnitada projekti hankija arvet teenuses Microsoft Dynamics 365 Project Operations ja projekti hankija arve kinnitamise finantsmõju.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261506"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekti hankija arve kinnitamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Kui olete teenuses Microsoft Dynamics 365 Project Operations hankija arvel kõik read kontrollinud, saate hankija arve kinnitamiseks kasutada toimingut Kinnita.

Kui valite hankija arvel valiku **Kinnita**, ilmneb järgmine käitumine.

1. Hankija arve olekuks värskendatakse **Kinnitatud**.
2. Kinnitatud hankija arve ja sellega seotud kirjed muutuvad kirjutuskaitstuks ning neid ei saa muuta ega kustutada.
3. Kui mis tahes kulu tegelikud näitajad viitavad võrdlusprotsessi osana hankija arve reale, pööratakse kõik viidatud hankija arve reaga seotud kulu tegelikud näitajad ümber.
4. Uued kulu tegelikud näitajad luuakse hankija arve real olevat teavet kasutades.
5. Pärast hankija arve kinnitamist ei saa enam luua paranduspäevikuid, töödelda aja sissekande tagasikutsumist ega tühistada algse aja-, kulu- või materjali tegelike näitajate kinnitamist, mis olid ümberpööratud.

> [!NOTE]
> Kui hankija arve mõnel real on kinnitusolek muu kui **Täielik**, ei saa hankija arvet kinnitada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
