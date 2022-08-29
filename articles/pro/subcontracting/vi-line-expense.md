---
title: Hankija arveread kulukategooriate jaoks
description: Selles artiklis selgitatakse, kuidas hankija arve ridu kulukategooriate jaoks salvestada.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261677"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Hankija arveread kulukategooriate jaoks

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankija arvel võivad olla kulukategooriate hankija arve read. Projektijuhid saavad kasutada hankija arve ridu kulukategooriate jaoks, et salvestada kulukategooriatena hangitud teenuste kulud.

Kulukategooriate hankija arve read võivad, kuid ei pruugi viidata kulukategooriate allhankereale. Kui kulukategooriate hankija arve rida viitab allhankele, saavad projektijuhid sobitada ja kontrollida hankija arve rea poolt arveldatavaid kulusid nendes kulukategooriates registreeritud ja projektijuhtide poolt projektis kinnitatud kuludega.

Järgmine tabel annab teavet kulukategooriate hankija arve ridade väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis otsingutes, mis põhinevad hankija arve ridadel. |
| Kirjeldus | Hankija poolt hankija arve real arveldatavate teenuste lühikirjeldus. | Pole |
| Allhankeleping | Alltöövõtt, millelt teenused algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei tohi olla hankija arve ridu, mis viitavad erinevatele allhangetele. |
| Allhanke liin | Alltöövõtuliin, millelt teenuseid telliti. Valitavate allhankeliinide loend on piiratud valitud allhankelepingu ridadega. | Kui hankija arve real on kulukategooriate jaoks valitud allhanke rida, sisestatakse väljade Projekt **,** Ülesanne **ja** Kanne **kategooria vaikeväärtused** allhanke rea vastavatelt väljadelt. Kui valitud allhankereal on väärtused **väljadel Projekt**, **Projekti ülesanne** ja **Kande kategooria**, ei tohi hankija arve rea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektis salvestatakse. |Pole |
| Kande klass | Valige **Kulu,** et salvestada hankija arve kulukategooria jaoks. | Väärtus **Kulu** näitab, et hankija arve rida kasutatakse kulukategooriatena hangitud teenuste arve summa salvestamiseks. |
| Project | Projekti nimi, mille kohta arvet esitavaid teenuseid kasutati. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, mille kohta arvet esitavaid teenuseid kasutati. See väli on saadaval ainult juhul, kui projekt on valitud. Projektiülesande valik on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea kuludega, mis on salvestatud projekti mis tahes ülesandes. Kui hankija arve rida ei viita allhankereale ja see väli jäetakse tühjaks, ei lingita hankija arve rea loodud tegelikku kulu ühegi arveldamata müügi tegeliku kuluga. Sel juhul, kui ülesandepõhine arveldamine on seadistatud, ei pruugi kulude eest lõppkliendile arvet esitada. |
| Kande kategooria | Kandekategooria, mille kohta arve esitatakse. Valitud kandekategooria jaoks tuleb luua vastav kulukategooria. | Kande kategooria ja ühiku väärtuste kombinatsiooni **kasutatakse hankija arve real välja Ühiku hind** vaike- või arvutatud väärtusena **.** **·** |
| Kogus | Sisestage kogus, mille kohta hankija arve esitab arve real. |Pole|
| Ühikurühm | Vaikeväärtus sisestatakse valitud kandekategooria ühikugrupi põhjal. | Pole |
| Üksus | Vaikeväärtus on valitud ühikurühma põhiühik. Saate seda väärtust muuta, et osta ühikugrupi mis tahes ühikut. | Kande kategooria ja ühiku väärtuste kombinatsiooni **kasutatakse hankija arve real välja Ühiku hind** vaike- või arvutatud väärtusena **.** **·** |
| Ühiku hind | Vaikeühiku hind kasutab kandekategooria **ja** ühiku **väärtuste kombinatsiooni** projekti hinnakirjast, mis on rakendatav hankija arve rea kandekuupäevale. | Kui rakendatava projekti hinnakirja hind on seadistatud ühikus, mis erineb hankija arve real olevast ühikust, kasutab süsteem ühiku hinna arvutamiseks ühiku teisendust. |
| Vahesumma | See kirjutuskaitstud väli arvutatakse *koguse*&times; ühikuhinnana *·*, kui väärtused sisestatakse nii väljale Kogus **kui ka** väljale **Ühiku hind.** Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse sisestada.| Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse käibemaksu *vahesummana.* + *·* | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
