---
title: Hankija arveread toodete jaoks
description: Selles artiklis selgitatakse, kuidas salvestada toodete hankija arve ridu ja kasutada erinevaid välju hankijatelt tehtud tooteostude salvestamiseks.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261553"
---
# <a name="vendor-invoice-lines-for-products"></a>Hankija arveread toodete jaoks

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankijaarvel võivad olla toodete hankija arve read (nimetatakse ka materjalideks). Projektijuhid saavad kasutada toodete hankija arve ridu projektidest ostetud toodete kulude salvestamiseks.

Toodete hankija arve read võivad, kuid ei pruugi viidata materjalide allhankereale. Kui toodete hankija arve rida viitab allhankele, saavad projektijuhid võrrelda ja kontrollida hankija arve rea poolt arveldatavaid tooteid projektijuhtide poolt registreeritud ja kinnitatud ostetud toodete kasutamisega.

Järgmine tabel annab teavet toodete hankija arve ridade väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis otsingutes, mis põhinevad hankija arve ridadel. |
| Kirjeldus | Nende toodete lühikirjeldus, mille kohta hankija esitab arve hankija arve real. | Pole |
| Allhankeleping | Alltöövõtt, millelt tooted algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei tohi olla hankija arve ridu, mis viitavad erinevatele allhangetele. |
| Allhanke liin | Allhankeliin, millelt tooted telliti. Valitavate allhankeliinide loend on piiratud valitud allhankelepingu ridadega. | Kui toodete hankija arve real on valitud allhanke rida, sisestatakse väljade Projekt **,** Ülesanne **ja** Toode **vaikeväärtused** allhanke rea vastavatelt väljadelt. Kui valitud allhankereal on väärtused **väljadel Projekt**, **Ülesanne** ja **Toode**, ei tohi hankija arve rea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektis salvestatakse. | Pole|
| Kande klass | Kui toodete eest esitatakse arve, tuleb selle välja väärtuseks **määrata Materjal**. | Väärtus **Materjal** näitab, et hankija arve rida kasutatakse ostetud materjalide arve summa registreerimiseks. |
| Project | Projekti nimi, mille kohta arvet esitavaid tooteid kasutati. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, milles arvet esitavaid tooteid kasutati. See väli on saadaval ainult juhul, kui projekt on valitud. Projektiülesande valik on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arve rea ostetud tootega, mida kasutatakse projekti mis tahes ülesandes. Kui hankija arve rida ei viita allhankereale ja see väli jäetakse tühjaks, ei lingita hankija arve rea loodud tegelikku kulu ühegi arveldamata müügi tegeliku kuluga. Sel juhul, kui ülesandepõhine arveldamine on seadistatud, ei saa kulude eest lõppkliendile arvet esitada. |
| Toote valimine | Valige, kas arveldatav toode on kataloogi olemasolev toode või sissekirjutustoode. | Vaikeväärtus sisestatakse allhankerealt, kui allhankerida on valitud. |
| Toode | Valige kataloogist toode. Kui toode on sissekirjutustoode, sisestage toote nimi. | Seda välja kasutatakse olemasolevate toodete vaikeostuhindade sisestamiseks. |
| Kogus | Sisestage sellel arvereal materjali kogus, mille kohta hankija arve esitab. | Pole |
| Ühikurühm | Valige selle ühiku ühikurühm, milles arveldatavat kogust väljendatakse. | Pole |
| Üksus | Vaikeväärtus on valitud ühikurühma põhiühik. Saate seda väärtust muuta, et maksta valitud ühikugrupi mis tahes ühikus. | Toote ja ühiku väärtuste kombinatsiooni **kasutatakse hankija arve real välja Ühiku hind** vaike- või arvutatud väärtusena **.** **·** |
| Ühiku hind | Vaikeühiku hind kasutab toote **ja** ühiku **väärtuste kombinatsiooni** projekti hinnakirjast, mis on rakendatav hankija arve rea kandekuupäevale. | Pole |
| Vahesumma | See kirjutuskaitstud väli arvutatakse *koguse*&times; ühikuhinnana *·*, kui väärtused sisestatakse nii väljale Kogus **kui ka** väljale **Ühiku hind.** Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse sisestada. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse käibemaksu *vahesummana.* + *·* | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
