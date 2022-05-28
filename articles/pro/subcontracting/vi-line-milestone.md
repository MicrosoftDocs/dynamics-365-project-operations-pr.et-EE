---
title: Hankija arve read vahe-eesmärkide jaoks
description: Selles teemas selgitatakse, kuidas luua hankija arveridu alltöövõtu vahe-eesmärkide jaoks.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590617"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Hankija arve read vahe-eesmärkide jaoks

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankija arvel võivad olla alltöövõtureal määratletud vahe-postide hankija arveread. Projektijuhid saavad vahe-eesmärkide jaoks kasutada hankija arveridu, et kirjendada hangitud teenuste kulud verstapostipõhiste kuludena, mis tekivad projekti jaoks hangitud teenuste või toodetega.

Hankija arve read vahe-eesmärkide jaoks peavad alati viitama alltöövõtureale, millel on fikseeritud hinna arveldamise meetod. Kui hankija arve rida vahe-eesmärkide jaoks viitab alltöövõtureale, saavad projektijuhid sobitada ja kontrollida aja, kulude või materjalide aluseks olevaid ajakulusid, kulusid või materjale, mis viitavad sellele allhankereale hankija arveldatava verstapostiga.

Järgmises tabelis on esitatud teave hankija arveridade väljade kohta vahe-eesmärkide puhul.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, et aidata ID-d. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Nende teenuste lühikirjeldus, mille hankija hankija hankija arvereal arveldab. | Pole |
| Allhankeleping | Alltöövõtt, millele teenused algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei saa olla hankija arve ridu, mis viitavad erinevatele alltöövõtulepingutele. |
| Alltöövõtu rida | Allhankeliin, millele teenused telliti. Valitavate alltöövõturidade loend piirdub valitud allhankelepingute ridadega. | Kui hankija arvereal valitakse vahe-eesmärkide jaoks alltöövõturida, **on kategooria Rolli** ja **Kande kategooria** väljad ning tootega seotud väljad ebaolulised ja pole saadaval. Väljad **Kogus**, **Ühik** ja **Ühikugrupp** pole olulised ka verstapostipõhiste hankijaarve ridade puhul. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektile kirjendatakse. | Pole |
| Kande klass | Valige **Verstapost** hankija arve salvestamiseks lõpule viidud vahesposti jaoks, mis määratleti alltöövõtureal. | Pole |
| Vahe-eesmärk | Valige seotud alltöövõtureal määratletud verstapost, mis on märgitud arvele **valmis olekuks**. | Alltöövõturea vahe-eesmärgid, mille olek **on Arveldamiseks** valmis, saab valida hankija arvereal. |
| Project | Projekti nimi, milles arveldatavaid teenuseid kasutati. | See väli on nõutav ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, milles arveldatavaid teenuseid kasutati. See väli on saadaval ainult siis, kui projekt on valitud. Projektiülesande valimine on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht sobitada hankija arverea seotud alltöövõturea kannete klassiga, mis salvestatakse projekti mis tahes ülesandele. Kui hankija arve rida ei viita alltöövõtureale ja see väli jäetakse tühjaks, ei seota hankija arve rea loodud tegelikku kulu ühegi sisestamata müügiväärtusega. Sellisel juhul, kui ülesandepõhine arveldamine on seadistatud, ei pruugi kulusid olla võimalik lõpptarbijale arveldada. |
| Vahe-eesmärgi summa | Sisestage arveldamiseks valmis allhankereale määratletud verstaposti väärtus. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse vahe-eesmärgi *summana* + *Käibemaks*. | Pole |

> [!NOTE]
> Kui luuakse hankija arve rida, mis viitab alltöövõturea vahestapostile, uuendatakse alltöövõtu vahesposti olek loodud **hankija arvele**. Seejärel, kui see hankija arve kinnitatakse, uuendatakse alltöövõturea vahesposti olek kinnitatud **hankija arvele**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
