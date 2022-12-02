---
title: Hankija arveread aja jaoks
description: See artikkel selgitab, kuidas salvestada hankija arve ridu allhanke kulutatud ajakulude jaoks.
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

Rakenduse Microsoft Dynamics 365 Project Operations hankija arvel võivad olla hankija arve read aja kohta. Projektijuhid saavad kasutada hankija arve ridu aja jaoks, et registreerida projektide allhanke ajakulu.

Hankija arve ajaread võivad viidata, kuid ei pruugi viidata aja osas allhankelepingureale. Kui hankija arve rida viitab allhankelepingule, saavad projektijuhid võrrelda ja kontrollida hankija arveldatava aja ja allhanke poolt registreeritud ja projekti projektijuhtide poolt kinnitatud aega.

Alljärgnevas tabelis on esitatud teave hankija arveridade aja väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Lühikirjeldus teenuste kohta, mille kohta hankija esitab arvereale arve. | Pole |
| Allhankeleping | Allhankeleping, mille alusel teenused algselt telliti. | Kui tarnija arve jaoks on valitud allhankeleping, pärivad kõik hankija arveread selle valiku. Hankija arvel ei saa olla hankija arveridu, mis viitavad erinevatele allhankelepingutele. |
| Allhankelepingu rida | Allhankelepingu rida, mille alusel teenused algselt telliti. Valitavate allhankelepingu ridade loend piirdub valitud allhankelepingu ridadega. | Kui hankija arve real valitakse aja jaoks allhankelepingu rida, sisestatakse väljadele **Projekt**, **Roll**, ja **Broneeritav ressurss** allhankelepingurea vastavatest väljadest. Kui valitud allhankelepingureal on väärtused väljadel **Projekt**, **Roll** ja **Broneeritav**, ei tohi hankija arve rea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, mil hankija arverea kulu tegelik näitaja kirjendatakse projektile. | Pole |
| Tehingu klass | Vaikeväärtus on **Aeg**. | Väärtus **Aeg** näitab, et hankija arverida kasutatakse allhanke tööaja arve summa kirjendamiseks. |
| Project | Projekti nimi, mille raames kasutati arve aluseks olevaid teenuseid. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projekti ülesande nimi, mille raames kasutati arve aluseks olevaid teenuseid. See väli on saadaval ainult siis, kui projekt on valitud. Projekti ülesande valimine on valikuline. | Kui see väli jääb tühjaks, saab projektijuht sobitada hankija arve rea ajaga, mille allhankelepingu ressursid salvestavad projekti mis tahes ülesande puhul. Kui hanikja arverida ei viita allhankelepingu reale ja see väli on tühjaks jäetud, ei seotaks hankija arverea poolt loodud kulu tegelikku näitajad ühegi arveldamata müügitehingu tegelike näitajatega. Kui ülesandepõhine arveldamine on seadistatud, ei pruugi sel juhul kulusid lõppkliendile arveldada. |
| Roll | Allhankelepingu ressursside roll, mille aja kohta arveldatakse. | See väli määrab rolli, mida täidavad allhankeressursid, mille aeg on hankija arvel arveldatud. |
| Broneeritav ressurss | Allhanke nimi, kelle aja eest arveldatakse. Broneeritava ressursi valimine on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea ajaga, mille salvestab hankija arve real hankijale kuuluv mis tahes ressurss. |
| Kogus | Sisestage arve reale tundide arv, mille jooksul hankija arvet esitab. |Pole |
| Ühikurühm | Vaikeväärtus on **Ajaühiku rühm** ja mida ei saa muuta. | Pole |
| Üksus | Vaikeväärtus on ajaühikute rühma tundide baasühik. Seda väärtust saate muuta, et osta sisse mistahes ühikurühma Aeg ühik, näiteks päev või nädal. | Väärtuste **Roll** ja **Ühik** kombinatsiooni kasutatakse hankija arve real välja **Ühiku hind** vaike- või arvutatud väärtusena. |
| Ühiku hind | Ühiku vaikehind kasutab **Roll** ja **Ühik** väärtuste kombinatsiooni projekti hinnakirjast, mis on rakendatav hankija arve rea tehingukuupäevale. | Kui kehtiva projekti hinnakirja hind on seadistatud ühikus, mis erineb hankija arvereal olevast ühikust, kasutab süsteem ühikuhinna arvutamiseks ühikute teisendust. |
| Vahesumma | See kirjutuskaitstud väli arvutatakse järgmiselt: *Kogus* &times; *Ühikuhind*, kui väärtused on sisestatud nii väljale **Kogus** kui ka väljale **Ühikuhind**. Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse sisestada. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arverea kogusumma koos maksudega. See väli arvutatakse järgmiselt: *Vahesumma* + *Müügimaks*. | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
