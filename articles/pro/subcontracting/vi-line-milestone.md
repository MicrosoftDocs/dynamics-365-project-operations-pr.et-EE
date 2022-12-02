---
title: Hankija arveread vahe-eesmärkide jaoks
description: See artikkel selgitab, kuidas luua allhankelepingu vahekokkuvõtete jaoks hankija arveridu.
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

Hankija arvel rakenduses Microsoft Dynamics 365 Project Operations võivad olla hankija arve read vahekokkuvõtete jaoks, mis on määratletud allhankelepingureal. Projektijuhid saavad kasutada vahekokkuvõtete jaoks hankija arveridu, et salvestada teenuste kulud, mis on hangitud vahekokkuvõttepõhiste kuludena, mis tekivad projekti jaoks hangitud teenuste või toodete puhul.

Vahekokkuvõtete hankija arveread peavad alati viitama allhankelepingu reale, millel on fikseeritud hinnaga arveldusmeetod. Kui hankija vahekokkuvõtete arvete rida viitab allhankelepingureale, saavad projektijuhid sobitada ja kinnitada selle aluseks olevaid aja-, kulu- või materjalikulusid, mis viitavad sellele allhankelepingureale, hankija poolt arvele pandud vahekokkuvõttega.

Alljärgnevas tabelis on esitatud teave hankija arveridade vahekokkuvõtete väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Lühikirjeldus teenuste kohta, mille kohta hankija esitab arvereale arve. | Pole |
| Allhankeleping | Allhankeleping, mille alusel teenused algselt telliti. | Kui tarnija arve jaoks on valitud allhankeleping, pärivad kõik hankija arveread selle valiku. Hankija arvel ei saa olla hankija arveridu, mis viitavad erinevatele allhankelepingutele. |
| Allhankelepingu rida | Allhankelepingu rida, mille alusel teenused algselt telliti. Valitavate allhankelepingu ridade loend piirdub valitud allhankelepingu ridadega. | Kui hankija arvereal on vahekokkuvõtete jaoks valitud allhankelepingu rida, ei ole väljad **Roll** ja **Tehingukategooria** ning tootega seotud väljad asjakohased ega saadaval. Väljad **Kogus**, **Ühik** ja **Ühikurüjm** ei ole samuti olulised vahekokkuvõttepõhiste hankija arveridade puhul. |
| Tehingu kuupäev | Kuupäev, mil hankija arverea kulu tegelik näitaja kirjendatakse projektile. | Pole |
| Kande klass | Valige **Vahekokkuvõte**, et kirjendada hankija arve lõpetatud vahekokkuvõtte kohta, mis on määratletud allhankelepingu real. | Pole |
| Vahe-eesmärk | Valige vahekokkuvõte, mis on määratletud seotud allhankelepingureal, mis on märgitud kui **Arveldamiseks valmis**. | Allhankelepingurea vahekokkuvõttes, mille olek on **Arveldamiseks valmis**, saab valida hankija arvereal. |
| Project | Projekti nimi, mille raames kasutati arve aluseks olevaid teenuseid. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projekti ülesande nimi, mille raames kasutati arve aluseks olevaid teenuseid. See väli on saadaval ainult siis, kui projekt on valitud. Projekti ülesande valimine on valikuline. | Kui see väli jääb tühjaks, saab projektijuht sobitada hankija arve rea tehingute klassiga seotud allhankelepingu real, mis on salvestatud projekti mis tahes ülesandele. Kui hanikja arverida ei viita allhankelepingu reale ja see väli on tühjaks jäetud, ei seotaks hankija arverea poolt loodud kulu tegelikku näitajad ühegi arveldamata müügitehingu tegelike näitajatega. Kui ülesandepõhine arveldamine on seadistatud, ei pruugi sel juhul kulusid lõppkliendile arveldada. |
| Vahe-eesmärgi summa | Sisestage vahekokkuvõtte väärtus, mis on määratletud allhankelepingureale, mis on arveldamiseks valmis. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arverea kogusumma koos maksudega. See väli arvutatakse järgmiselt: *Vahekokkuvõtte summa* + *Müügimaks*. | Pole |

> [!NOTE]
> Kui luuakse hankija arve rida, mis viitab allhankelepingurea vahekokkuvõttele, värskendatakse allhanke verstaposti olekuks **Hankija arve loodud**. Seejärel, kui hankija arve kinnitatakse, värskendatakse allhankelepingurea vahekokkuvõtte olekuks **Hankija arve kinnitatud**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
