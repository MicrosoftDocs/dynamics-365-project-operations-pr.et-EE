---
title: Projekti hankija arve kinnitamine
description: Selles artiklis selgitatakse, kuidas kinnitada projekti hankija arve Microsoftis Dynamics 365 Project Operations ja projekti hankija arve kinnitamise finantsmõju.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932429"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekti hankija arve kinnitamine

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Kui olete microsoftis Dynamics 365 Project Operations hankija arve kõik read kinnitanud, saate hankija arve kinnitamiseks kasutada toimingut Kinnita.

Kui valite hankija arvel suvandi **Kinnita**, ilmneb järgmine käitumine.

1. Hankija arve olek värskendatakse olekusse **Kinnitatud**.
2. Kinnitatud hankija arve ja sellega seotud kirjed muutuvad kirjutuskaitstuks ning neid ei saa redigeerida ega kustutada.
3. Kui mis tahes kulu tegelikud viited hankija arve reale sobitamisprotsessi osana, tühistatakse kõik viidatud hankija arvereaga seotud kulu tegelikud summad.
4. Uued kulu tegelikud andmed luuakse hankija arve real oleva teabe abil.
5. Pärast hankija arve kinnitamist ei saa te enam luua parandusželeid, töödelda ajakande tagasikutsumist ega tühistada tühistatud algse aja, kulu või materjali tegeliku kinnitamise kinnitamist.

> [!NOTE]
> Kui hankija arve mõnel real on kinnitamisolek, **mis ei ole täielik**, ei saa hankija arvet kinnitada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
