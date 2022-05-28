---
title: Projektide kulude finantsprognoosid
description: Selles teemas antakse teavet projektipõhiste kulude määratlemise või prognoosimise kohta.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589467"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Projektide kulude finantsprognoosid
_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations võimaldab projektijuhtidel määratleda iga projekti või ülesande jaoks projektipõhised kulutused. Iga kuluüksuse saab seostada konkreetse projektiülesandega. Kulud liigitatakse erinevateks kulukategooriatesse, mis on määratletud organisatsiooni tasemel. Iga kulukategooria hinnakujundus ja kuluarvestus on määratletud hinnakirjas. 

Projekti kulu vaatamiseks, lisamiseks või kustutamiseks tehke järgmist.

1. Avage **Projektid** ja valige projekt, mille kallal soovite töötada.
2. Valige vahekaart **Projekti prognoosid** ja vaadake projekti kulude loendit.
3. Valige uue kulu lisamiseks suvand **Uus kulu**. Või valige kustutamiseks kulu ja valige seejärel **Kustuta kulu**.

Järgmine tabel sisaldab teavet väljade kohta projekti real **Kuluprognoos**. 

| **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- |
| Toiming | Projekti ülesannete loend. See hõlmab kokkuvõtte- ja lehetoiminguid. | Ülesande valimine kuluprognoosi rea jaoks mõjutab ülesande prognoositavad maksumuse kulu ja eeldatava kulu müüki. Kui see väli jäetakse tühjaks, jälgitakse ja summeeritakse kuluprognoosi ainult projekti tasandil. |
| Kategooria | Kandekategooriate loend, mille kulukategooriad on rakenduses lingitud. | Kategooria valimine juhib kuluprognoosi rea hinnakujundust ja kulusid. |
| Alguskuupäev | Kulu ilmnemise prognoositav kuupäev. | Sellel väljal puudub allavoolu mõju. |
| Ühikurühm | Selle välja vaikeväärtus pärineb ühikurühmast, mis on häälestatud valitud kategooria vaikevalikuks. Saate selle välja värskendada, et valida mõne muu ühikurühma. | Sellel väljal puudub allavoolu mõju. |
| Üksus | Selle välja vaikeväärtus on vaikimisi valitud kategooria vaikeühik. Saate selle välja värskendada, et valida mõne muu ühiku. | Ühiku muutmise tulemuseks on erinev vaikimisi ühikuhind ja kulu. |
| Kogus | Esineva prognoositava kulu kogus. | Sellel väljal puudub allavoolu mõju. |
| Ühiku kulu | Valitud kategooria ja ühiku kombinatsiooni kulu, mis on häälestatud rakendatavas kuluhinnakirjas | Ühikukulu kuvatakse alati projekti kuluvaluutas. |
| Ühiku hind | Valitud kategooria ja ühiku kombinatsiooni hind, mis on häälestatud rakendatavas müügi hinnakirjas. | Ühiku hind kuvatakse alati projekti müügivaluutas. |
| Kogukulu | Kulusumma, mis arvutatakse kui kogus \* ühikukulu.| Kulusumma kuvatakse alati projekti kuluvaluutas. |
| Müük kokku | Müügisumma, mis arvutatakse kui kogus \* ühikuhind. | Müügisumma kuvatakse alati projekti müügivaluutas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
