---
title: Hankija arveread aja jaoks
description: Selles artiklis selgitatakse, kuidas salvestada hankija arve ridu ajakulude jaoks, mille alltöövõtjad sisestavad.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262007"
---
# <a name="vendor-invoice-lines-for-time"></a>Hankija arveread aja jaoks

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankijaarvel võivad olla hankija arve read aja jooksul. Projektijuhid saavad kasutada hankija arve ridu, et salvestada projektides alltöövõtja aja kulud.

Hankija arve read aja kohta võivad, kuid ei pruugi viidata allhankereale aja kohta. Kui hankija arve rida aja kohta viitab allhankele, saavad projektijuhid sobitada ja kontrollida hankija arve rea poolt arveldatavat aega allhankijate poolt registreeritud ja projektijuhtide poolt projektis kinnitatud ajaga.

Järgmine tabel annab teavet hankija arve ridade väljade kohta aja jooksul.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis otsingutes, mis põhinevad hankija arve ridadel. |
| Kirjeldus | Hankija poolt hankija arve real arveldatavate teenuste lühikirjeldus. | Pole |
| Allhankeleping | Alltöövõtt, millelt teenused algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei tohi olla hankija arve ridu, mis viitavad erinevatele allhangetele. |
| Allhanke liin | Alltöövõtuliin, millelt teenuseid telliti. Valitavate allhankeliinide loend on piiratud valitud allhankelepingu ridadega. | Kui hankija arve real on valitud aeg allhanke rida, sisestatakse väljade Projekt, Roll **ja** Broneeritav ressurss **vaikeväärtused** allhanke rea vastavatelt **väljadelt.** Kui valitud allhankereal on väärtused **väljadel Projekt**, **Roll** ja **Broneeritav**, ei tohi hankija arve rea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektis salvestatakse. | Pole |
| Kande klass | Vaikeväärtus on **Aeg**. | Väärtus **Time** näitab, et hankija arve rida kasutatakse allhankija aja arve summa salvestamiseks. |
| Project | Projekti nimi, mille kohta arvet esitavaid teenuseid kasutati. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, mille kohta arvet esitavaid teenuseid kasutati. See väli on saadaval ainult juhul, kui projekt on valitud. Projektiülesande valik on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea ajaga, mille alltöövõtja ressursid salvestavad projekti mis tahes ülesandes. Kui hankija arve rida ei viita allhankereale ja see väli jäetakse tühjaks, ei lingita hankija arve rea loodud tegelikku kulu ühegi arveldamata müügi tegeliku kuluga. Sel juhul, kui ülesandepõhine arveldamine on seadistatud, ei pruugi kulude eest lõppkliendile arvet esitada. |
| Roll | Alltöövõturessursside roll, mille eest arve esitatakse. | See väli määrab rolli, mida täidavad allhankeressursid, mille aja eest hankija arvel arveldatakse. |
| Broneeritav ressurss | Alltöövõtja nimi, kelle kohta arve esitatakse. Broneeritava ressursi valik on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea ajaga, mille salvestab mis tahes hankijale kuuluv ressurss hankija arve real. |
| Kogus | Sisestage arve reale aeg, mille jooksul hankija arveldab. |Pole |
| Ühikurühm | Vaikeväärtus on **Ajaühiku rühm** ja seda ei saa muuta. | Pole |
| Üksus | Vaikeväärtus on ajaühikurühma tundide põhiühik. Saate seda väärtust muuta, et osta ajaühikurühma mis tahes ühikus, näiteks päeval või nädalal. | Rolli ja ühiku väärtuste kombinatsiooni **kasutatakse hankija arve real välja Ühiku hind** vaike- **või arvutatud väärtusena.** **·** |
| Ühiku hind | Vaikeühiku hind kasutab rolli **ja** ühiku **väärtuste kombinatsiooni** projekti hinnakirjast, mis rakendub hankija arve rea kandekuupäevale. | Kui rakendatava projekti hinnakirja hind on seadistatud ühikus, mis erineb hankija arve real olevast ühikust, kasutab süsteem ühiku hinna arvutamiseks ühiku teisendust. |
| Vahesumma | See kirjutuskaitstud väli arvutatakse *koguse*&times; ühikuhinnana *·*, kui väärtused sisestatakse nii väljale Kogus **kui ka** väljale **Ühiku hind.** Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse sisestada. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse käibemaksu *vahesummana.* + *·* | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
