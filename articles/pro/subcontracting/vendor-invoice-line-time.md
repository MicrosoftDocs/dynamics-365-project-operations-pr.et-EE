---
title: Hankija arveread aja jaoks
description: Selles artiklis selgitatakse, kuidas salvestada hankija arveridu alltöövõtjate sisestatud ajakulude eest.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927537"
---
# <a name="vendor-invoice-lines-for-time"></a>Hankija arveread aja jaoks

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankija arvel võib olla aja jooksul hankija arveread. Projektijuhid saavad kasutada hankija arve ridu aja jooksul, et salvestada projektidele alltöövõtja aja kulud.

Hankija arve read aja kohta võivad või ei pruugi viidata alltöövõtureale aja jooksul. Kui hankija arve rida viitab aja kohta alltöövõtule, saavad projektijuhid sobitada ja kontrollida hankija arverea arveldatud aega ajaga, mille alltöövõtjad salvestavad ja projekti projektis projektis heaks kiidavad.

Järgmises tabelis on esitatud teave hankija arve ridade väljade kohta aja jooksul.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, et aidata ID-d. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Nende teenuste lühikirjeldus, mida hankija hankija hankija arvereal arveldab. | Pole |
| Allhankeleping | Alltöövõtt, millele teenused algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei saa olla hankija arve ridu, mis viitavad erinevatele alltöövõtulepingutele. |
| Alltöövõtu rida | Allhankeliin, millele teenused telliti. Valitavate alltöövõturidade loend piirdub valitud allhankelepingute ridadega. | Kui hankija arvereal valitakse aja jooksul alltöövõturida, sisestatakse väljade **Projekt**, **Roll** ja **Broneeritav ressurss** vaikeväärtused alltöövõturea vastavatelt väljadelt. Kui valitud alltöövõtureal **on väärtused väljadel Projekt**, **Roll** ja **Broneeritav**, ei saa hankija arverea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektile kirjendatakse. | Pole |
| Kande klass | Vaikeväärtus on **Aeg**. | Väärtus **Aeg** näitab, et hankija arve rida kasutatakse hankija aja arve summa kirjendamiseks. |
| Project | Projekti nimi, milles arveldatavaid teenuseid kasutati. | See väli on nõutav ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, milles arveldatavaid teenuseid kasutati. See väli on saadaval ainult siis, kui projekt on valitud. Projektiülesande valimine on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea ajaga, mille alltöövõtja ressursid salvestavad projekti mis tahes ülesandele. Kui hankija arve rida ei viita alltöövõtureale ja see väli jäetakse tühjaks, ei seota hankija arve rea loodud tegelikku kulu ühegi sisestamata müügiväärtusega. Sellisel juhul, kui ülesandepõhine arveldamine on seadistatud, ei pruugi kulusid olla võimalik lõpptarbijale arveldada. |
| Roll | Nende alltöövõturessursside roll, mille aja eest arve esitatakse. | See väli määrab rolli, mida täidavad allhankeressursid, mille aeg hankija arvel arveldatakse. |
| Broneeritav ressurss | Selle alltöövõtja nimi, kelle aega arveldatakse. Broneeritava ressursi valimine on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea ajaga, mille salvestab hankija arve real hankija arve real hankijale kuuluv ressurss. |
| Kogus | Sisestage arvereal hankija arveldatavate tundide arv. |Pole |
| Ühikurühm | Vaikeväärtus on **ajaühiku grupp** ja seda ei saa muuta. | Pole |
| Üksus | Vaikeväärtus on ajaühikute rühma tundide baasühik. Seda väärtust saate muuta, et osta ajaühikute rühma mis tahes ühikus (nt päeval või nädalal). | Rolli- ja ühikuväärtuste **kombinatsiooni kasutatakse hankija arverea välja Ühiku hind** vaike- või arvutusväärtusena **.** **·** |
| Ühiku hind | Ühiku vaikehind kasutab projekti hinnakirja rolli- **ja** **ühikuväärtuste** kombinatsiooni, mis on rakendatav hankija arve rea kandekuupäevale. | Kui rakendatava projekti hinnakirja hind on seadistatud ühikus, mis erineb hankija arve real olevast ühikust, kasutab süsteem ühikupõhise hinna arvutamiseks ühikuteisendust. |
| Vahesumma | See kirjutuskaitstud väli arvutatakse *koguse*&times; ühikuhinnana *·*, kui väärtused sisestatakse nii väljale Kogus **kui ka** väljale **Ühiku hind.** Kui üks või mõlemad väljad on tühjad, saate sellele väljale sisestada väärtuse. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse vahesumma *käibemaksuna.* + *·* | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
