---
title: Allhankelepingu rea ressursid
description: Selles teemas kirjeldatakse, kuidas määrata sihtotstarbelised ressursid, mille hankija on konkreetse allhankelepingu aja rea jaoks andnud.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323366"
---
# <a name="subcontract-line-resources"></a>Allhankelepingu rea ressursid

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations saab hankija määratleda ressursid, mida kasutatakse aja allhankelepingu rea ostetava ressursivõimsuse varustamiseks.

## <a name="create-subcontract-line-resources"></a>Allhankelepingu rea ressursside loomine

Allhankelepingu rea ressursside loomiseks läbige järgmised etapid.

1. Valige navigeerimispaanil **Allhankelepingud** ja avage see allhankeleping, millega soovite töötada.
2. Avage see aja allhankelepingu rida, millele soovite hankija ressursse määrata.
3. Valige vahekaardi **Allhankelepingu rea ressursid** andmeruudustikus **+ Uus allhankelepingu rea ressurss**.
4. Sisestage lehel **Uus allhankelepingu rea vahe-eesmärk** nõutav teave ja seejärel valige **Salvesta ja sule**.

Järgmises tabelis selgitatakse allhankelepingu rea ressursil olevaid välju.

| Väli |  Kirjeldus |
| ----- | ------------ |
| Broneeritav ressurss | Valige broneeritav ressurss tüübiga "Lepinguline töötaja", mida soovite kasutada ressursina allhankelepingu real. Kui te pole lepingulisele töötajale veel broneeritavat ressurssi loonud, jätke see väli tühjaks. Broneeritav ressurss luuakse kirje salvestamisel.  |
| Kontaktandmed | Kui väli **Broneeritav ressurss** on tühi, saate oma allhankelepingu rea ressursi luua olemasoleva kontakti kaudu. Kasutage otsingut süsteemi aktiivsete kontaktide loendi vaatamiseks. Valige selle allhankelepingu hankija jaoks kontakt. Valitud kontakt valideeritakse kirje salvestamisel. Kui teie valitud kontakt pole sobiv kontakt, siis teie kirjet ei salvestata. Kui valitud kontakti jaoks pole broneeritavaid ressursse, loob süsteem valitud kontakti jaoks broneeritava ressursi enne allhankelepingu rea ressursi loomist. |
| Kasutaja | Kui väli **Broneeritav ressurss** on tühi, saate oma allhankelepingu rea ressursi luua, valides aktiivse kasutaja. Kasutage otsingut süsteemi aktiivsete kasutajate loendi vaatamiseks. Kui valitud kasutaja jaoks pole broneeritavaid ressursse, loob süsteem valitud kasutaja jaoks broneeritava ressursi enne allhankelepingu rea ressursi loomist. |
| Alguskuupäev | Kuupäev, milllal allhankelepingu töötaja tööülesanne algab. Kui see ressurss on broneeritud perioodiks, mis sellele kuupäevavahemikule eelneb, ilmneb hoiatus. |
| Lõpukuupäev | Kuupäev, milllal allhankelepingu töötaja tööülesanne lõpeb. Kui see ressurss on broneeritud perioodiks, mis sellele kuupäevavahemikule järgneb, ilmneb hoiatus. |
| Tööpanus | Panuse tundide koguarv, millal allhankelepingu töötaja tegeleb selle allhankelepingu reaga. Kui see ressurss on broneeritud rohkem kui sellele allhankelepingule eraldatud panus, ilmneb hoiatus. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
