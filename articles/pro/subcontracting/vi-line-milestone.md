---
title: Hankija arveread vahe-eesmärkide jaoks
description: Selles artiklis selgitatakse, kuidas luua hankija arve ridu allhanketöövõtu verstapostide jaoks.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260990"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Hankija arveread vahe-eesmärkide jaoks

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations hankija arvel võivad olla hankija arve read verstapostide jaoks, mis on määratletud allhankereal. Projektijuhid saavad kasutada hankija arve ridu verstapostide jaoks, et salvestada hangitud teenuste kulud verstapostipõhiste kuludena, mis tekivad projekti jaoks hangitud teenustele või toodetele.

Hankija arve read verstapostide jaoks peavad alati viitama allhankereale, millel on fikseeritud hinnaga arveldusmeetod. Kui hankija arve rida verstapostide jaoks viitab allhankereale, saavad projektijuhid sobitada ja kontrollida aluseks olevaid aja-, kulu- või materjalikulusid, mis viitavad sellele allhankereale, hankija poolt arveldatava verstapostiga.

Järgmine tabel annab teavet hankija arve ridade väljade kohta verstapostide jaoks.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis otsingutes, mis põhinevad hankija arve ridadel. |
| Kirjeldus | Hankija poolt hankija arve real arveldatavate teenuste lühikirjeldus. | Pole |
| Allhankeleping | Alltöövõtt, millelt teenused algselt telliti. | Kui hankija arve jaoks on valitud alltöövõtt, pärivad kõik hankija arve read selle valiku. Hankija arvel ei tohi olla hankija arve ridu, mis viitavad erinevatele allhangetele. |
| Allhanke liin | Alltöövõtuliin, millelt teenuseid telliti. Valitavate allhankeliinide loend on piiratud valitud allhankelepingu ridadega. | Kui hankija arve real on-eesmärkide jaoks valitud allhanke rida, **on väljad Rolli** ja **Kande kategooria** ning tootega seotud väljad ebaolulised ega ole saadaval. Väljad **Kogus**, **Ühik** ja **Ühikugrupp** pole asjakohased ka verstapostipõhiste hankija arve ridade puhul. |
| Tehingu kuupäev | Kuupäev, millal hankija arve rea tegelik kulu projektis salvestatakse. | Pole |
| Kande klass | Valige **Verstapost**, et salvestada hankija arve lõpetatud verstaposti eest, mis määratleti allhanke real. | Pole |
| Vahe-eesmärk | Valige verstapost, mis on määratletud seotud allhanke real, mis on märgitud arveks **valmis**. | Allhanke rea verstapostid, mille olek **on Arveks** valmis, saab valida hankija arve real. |
| Project | Projekti nimi, mille kohta arvet esitavaid teenuseid kasutati. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projektiülesande nimi, mille kohta arvet esitavaid teenuseid kasutati. See väli on saadaval ainult juhul, kui projekt on valitud. Projektiülesande valik on valikuline. | Kui see väli jäetakse tühjaks, saab projektijuht vastendada hankija arve rea seotud allhankereal olevate kannete klassiga, mis salvestatakse projekti mis tahes ülesandele. Kui hankija arve rida ei viita allhankereale ja see väli jäetakse tühjaks, ei lingita hankija arve rea loodud tegelikku kulu ühegi arveldamata müügi tegeliku kuluga. Sel juhul, kui ülesandepõhine arveldamine on seadistatud, ei pruugi kulude eest lõppkliendile arvet esitada. |
| Vahe-eesmärgi summa | Sisestage selle verstaposti väärtus, mis on määratletud arveldamiseks valmis oleval allhanke real. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arve rea kogusumma koos maksudega. See väli arvutatakse-eesmärgi *summana* + *Käibemaks*. | Pole |

> [!NOTE]
> Kui luuakse hankija arve rida, mis viitab allhanke rea verstapostile, värskendatakse allhanke verstaposti olekuks **Loodud** hankija arve. Seejärel, kui see hankija arve on kinnitatud, värskendatakse allhanke rea verstaposti olekuks **Hankija arve kinnitatud**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
