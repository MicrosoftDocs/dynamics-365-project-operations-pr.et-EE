---
title: Allhankelepingu rea ressursid
description: Selles artiklis selgitatakse, kuidas määrata spetsiaalseid ressursse, mida hankija konkreetse allhankerea jaoks aja jooksul pakub.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d440201fde26e835b407db0b8ee1de8d663311a0
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261459"
---
# <a name="subcontract-line-resources"></a>Allhankelepingu rea ressursid

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations saab hankija määratleda ressursid, mida kasutatakse aja allhankelepingu rea ostetava ressursivõimsuse varustamiseks.

## <a name="create-subcontract-line-resources"></a>Allhankelepingu rea ressursside loomine

Allhankelepingu rea ressursside loomiseks läbige järgmised etapid.

1. Valige navigeerimispaanil **Allhankelepingud** ja avage see allhankeleping, millega soovite töötada.
2. Avage see aja allhankelepingu rida, millele soovite hankija ressursse määrata.
3. Valige vahekaardi **Allhankelepingu rea ressursid** andmeruudustikus **+ Uus allhankelepingu rea ressurss**.
4. Sisestage lehel **Uus allhankelepingu rea ressurss** nõutav teave ja valige seejärel suvand **Salvesta ja sule**.

Järgmises tabelis selgitatakse allhankelepingu rea ressursil olevaid välju.

| Väli | Kirjeldus | Funktsionaalne mõju |
| ----- | ----------- | ----------------- |
| Broneeritav ressurss | Valige broneeritav ressurss tüübiga **Lepinguline töötaja**, mida soovite kasutada ressursina allhankelepingu real.| Kui te pole lepingulise töötaja jaoks broneeritavat ressurssi loonud, jätke see väli tühjaks. Broneeritav ressurss luuakse kirje salvestamisel.  |
| Kontaktandmed | Saate luua oma allhankelepingu rea ressursi olemasolevast kontaktist. Kasutage otsingut süsteemi aktiivsete kontaktide loendi vaatamiseks. Valige selle allhankelepingu hankija jaoks kontakt. Kui teie valitud kontakt ei ole allhankelepingu hankija jaoks kehtiv kontakt, allhankelepingu rea ressursikirjet ei salvestata.| Kui valitud kontakti jaoks pole broneeritavaid ressursse, loob süsteem valitud kontakti jaoks broneeritava ressursi enne allhankelepingu rea ressursi loomist. |
| Kasutaja | Saate luua allhankelepingu rea ressursi valides aktiivse kasutaja. Kasutage otsingut süsteemi aktiivsete kasutajate loendi vaatamiseks.| Kui valitud kasutaja jaoks pole broneeritavaid ressursse, loob süsteem valitud kasutaja jaoks broneeritava ressursi enne allhankelepingu rea ressursi loomist. |
| Alguskuupäev | Kuupäev, milllal allhankelepingu töötaja tööülesanne algab.| Kui see ressurss on broneeritud perioodiks, mis sellele kuupäevavahemikule eelneb, ilmneb hoiatus. |
| Lõpukuupäev | Kuupäev, milllal allhankelepingu töötaja tööülesanne lõpeb.| Kui see ressurss on broneeritud perioodiks, mis sellele kuupäevavahemikule järgneb, ilmneb hoiatus. |
| Tööpanus | Panustatavate tundide koguarv, mille lepinguline töötaja selle allhankelepingu reale kulutab.| Kui see ressurss on broneeritud rohkemaks kui antud allhankelepingu jaoks määratud panus, kuvatakse hoiatus. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
