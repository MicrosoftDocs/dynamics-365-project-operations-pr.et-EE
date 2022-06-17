---
title: Hankija arveread toodete jaoks
description: Selles artiklis selgitatakse, kuidas salvestada hankija arveread toodetele ja kasutada erinevaid välju hankijatelt tooteostude kirjendamiseks.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931371"
---
# <a name="vendor-invoice-lines-for-products"></a>Hankija arveread toodete jaoks

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankija arvel võivad olla toodete hankija arveread (mida nimetatakse ka materjalideks). Projektijuhid saavad toodete puhul kasutada hankija arveridu projektidest ostetud toodete kulude kirjendamiseks.

Toodete hankija arveread võivad või ei pruugi viidata materjalide alltöövõtureale. Kui toodete hankija arverida viitab allhankele, saavad projektijuhid sobitada ja kontrollida tooteid, mida hankija arverida arveldab projektijuhtide poolt salvestatud ja kinnitatud ostetud toodete kasutamisega.

Järgmises tabelis on esitatud teave toodete hankija arveridade väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, et aidata ID-d. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Nende toodete lühikirjeldus, mille hankija hankija arvereal arveldab. | Pole |
| Allhankeleping | Alltöövõtt, millele tooted algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei saa olla hankija arve ridu, mis viitavad erinevatele alltöövõtulepingutele. |
| Alltöövõtu rida | Alltöövõtuliin, millele tooted telliti. Valitavate alltöövõturidade loend piirdub valitud allhankelepingute ridadega. | Kui hankija arvereal on toodete jaoks valitud alltöövõturida, sisestatakse väljade Projekt **,** Ülesanne **ja** Toode **vaikeväärtused** alltöövõturea vastavatelt väljadelt. Kui valitud allhankereal **on väärtused väljadel Projekt**, **Ülesanne** ja **Toode**, ei saa hankija arverea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektile kirjendatakse. | Pole|
| Kande klass | Toodete arveldamisel tuleks selle välja väärtuseks **seada Materjal**. | VäärtusMaterjal **näitab**, et ostetud materjalide arve summa kirjendamiseks kasutatakse hankija arve rida. |
| Project | Projekti nimi, milles arveid esitatavaid tooteid kasutati. | See väli on nõutav ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, milles arveldatavaid tooteid kasutati. See väli on saadaval ainult siis, kui projekt on valitud. Projektiülesande valimine on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arverea ostetud tootega, mida kasutatakse projekti mis tahes ülesandes. Kui hankija arve rida ei viita alltöövõtureale ja see väli jäetakse tühjaks, ei seota hankija arve rea loodud tegelikku kulu ühegi sisestamata müügiväärtusega. Sellisel juhul, kui ülesandepõhine arveldamine on seadistatud, ei saa kulusid lõpptarbijale arveldada. |
| Vali toode | Valige, kas arveldatav toode on kataloogist olemasolev toode või sissekirjutustoode. | Vaikeväärtus sisestatakse alltöövõturealt, kui valitakse alltöövõturida. |
| Toode | Valige toode kataloogist. Kui toode on sissekirjutustoode, sisestage toote nimi. | Seda välja kasutatakse olemasolevate toodete vaikeostuhindade sisestamiseks. |
| Kogus | Sisestage materjali kogus, mille hankija arve esitab sellele arvereale. | Pole |
| Ühikurühm | Valige selle ühiku ühikugrupp, milles arveldatav kogus on väljendatud. | Pole |
| Üksus | Vaikeväärtus on valitud ühikugrupi põhiühik. Seda väärtust saate muuta nii, et see maksaks valitud ühikugrupi mis tahes ühikuühikus. | Toote ja ühiku väärtuste kombinatsiooni **kasutatakse hankija arverea välja Ühiku hind** vaike- või arvutusväärtusena **.** **·** |
| Ühiku hind | Ühiku vaikehind kasutab projekti hinnakirjast pärinevate toote **-** ja **ühikuväärtuste** kombinatsiooni, mis rakendub hankija arve rea kandekuupäevale. | Pole |
| Vahesumma | See kirjutuskaitstud väli arvutatakse *koguse*&times; ühikuhinnana *·*, kui väärtused sisestatakse nii väljale Kogus **kui ka** väljale **Ühiku hind.** Kui üks või mõlemad väljad on tühjad, saate sellele väljale sisestada väärtuse. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse vahesumma *käibemaksuna.* + *·* | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
