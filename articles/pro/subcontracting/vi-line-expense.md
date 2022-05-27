---
title: Hankija arve read kulukategooriate jaoks
description: Selles teemas selgitatakse, kuidas salvestada hankija arveread kulukategooriate jaoks.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579531"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Hankija arve read kulukategooriate jaoks

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankija arvel võivad kulukategooriate jaoks olla hankija arveread. Projektijuhid saavad kasutada hankija arveridu kulukategooriate jaoks, et kirjendada hangitud teenuste kulud kulukategooriatena.

Kulukategooriate hankija arveread võivad või ei pruugi viidata kulukategooriate alltöövõtureale. Kui kulukategooriate hankija arverida viitab allhankele, saavad projektijuhid sobitada ja kontrollida hankija arverea arveldatavaid kulusid kuludega, mis on nendes kulukategooriates salvestatud ja projektijuhtide poolt kinnitatud kulude suhtes.

Järgmises tabelis on esitatud teave kulukategooriate hankija arveridade väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, et aidata ID-d. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Nende teenuste lühikirjeldus, mida hankija hankija hankija arvereal arveldab. | Pole |
| Allhankeleping | Alltöövõtt, millele teenused algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei saa olla hankija arve ridu, mis viitavad erinevatele alltöövõtulepingutele. |
| Alltöövõtu rida | Allhankeliin, millele teenused telliti. Valitavate alltöövõturidade loend piirdub valitud allhankelepingute ridadega. | Kui hankija arvereal valitakse kulukategooriate jaoks alltöövõturida, sisestatakse väljade Projekt, Ülesanne **ja** Kanne vaikeväärtused **alltöövõturea** vastavatelt **väljadelt.** Kui valitud alltöövõtureal on väärtused kategoorias **Projekt** **,** Projektiülesanne **ja** Kanne, ei saa hankija arverea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektile kirjendatakse. |Pole |
| Kande klass | Kulukategooria hankija arve kirjendamiseks valige **Kulu**. | Väärtus **Kulu** näitab, et hankija arve rida kasutatakse hangitud teenuste arvesumma kirjendamiseks kulukategooriatena. |
| Project | Projekti nimi, milles arveldatavaid teenuseid kasutati. | See väli on nõutav ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, milles arveldatavaid teenuseid kasutati. See väli on saadaval ainult siis, kui projekt on valitud. Projektiülesande valimine on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arverea kuludega, mis on salvestatud projekti mis tahes ülesandele. Kui hankija arve rida ei viita alltöövõtureale ja see väli jäetakse tühjaks, ei seota hankija arve rea loodud tegelikku kulu ühegi sisestamata müügiväärtusega. Sellisel juhul, kui ülesandepõhine arveldamine on seadistatud, ei pruugi kulusid olla võimalik lõpptarbijale arveldada. |
| Kande kategooria | Arveldatav kandekategooria. Valitud kandekategooria jaoks tuleb luua vastav kulukategooria. | Kandekategooria ja Ühiku väärtuste kombinatsiooni **kasutatakse hankija arve rea välja Ühiku hind** vaike- või arvutusväärtusena **.** **·** |
| Kogus | Sisestage arvereale hankija arveldatav kogus. |Pole|
| Ühikurühm | Vaikeväärtus sisestatakse valitud kandekategooria ühikugrupi põhjal. | Pole |
| Üksus | Vaikeväärtus on valitud ühikugrupi põhiühik. Seda väärtust saate muuta, et osta ühikugrupi mis tahes ühikuühikus. | Kandekategooria ja Ühiku väärtuste kombinatsiooni **kasutatakse hankija arve rea välja Ühiku hind** vaike- või arvutusväärtusena **.** **·** |
| Ühiku hind | Ühiku vaikehind kasutab hankija arverea kandekuupäevale rakendatava projekti hinnakirja kannete kategooria **ja** ühikuväärtuste **kombinatsiooni**. | Kui rakendatava projekti hinnakirja hind on seadistatud ühikus, mis erineb hankija arve real olevast ühikust, kasutab süsteem ühikupõhise hinna arvutamiseks ühikuteisendust. |
| Vahesumma | See kirjutuskaitstud väli arvutatakse *koguse*&times; ühikuhinnana *·*, kui väärtused sisestatakse nii väljale Kogus **kui ka** väljale **Ühiku hind.** Kui üks või mõlemad väljad on tühjad, saate sellele väljale sisestada väärtuse.| Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse vahesumma *käibemaksuna.* + *·* | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
