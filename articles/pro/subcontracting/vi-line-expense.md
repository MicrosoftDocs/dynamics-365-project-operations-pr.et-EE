---
title: Hankija arveread kulukategooriate jaoks
description: See artikkel kirjeldab, kuidas kirjendada hankija arveridu kulukategooriate jaoks.
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

Rakenduse Microsoft Dynamics 365 Project Operations hankija arvel võivad olla hankija arve read kulukategooriate kohta. Projektijuhid saavad kulukategooriatena hangitud teenuste kulude kajastamiseks kasutada kulukategooriate jaoks hankija arve ridu.

Hanikja arvete read kulukategooriate jaoks võivad, kuid ei pruugi viidata kulukategooriate allhankelepingureale. Kui kulukategooriate hankija arve rida viitab allhankelepingule, saavad projektijuhid võrrelda ja kontrollida hankija arve rea arvel olevaid kulusid nendes kulukategooriates registreeritud ja projekti projektijuhtide poolt kinnitatud kuludega.

Alljärgnevas tabelis on esitatud teave hankija arveridade kulukategooriate väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Lühikirjeldus teenuste kohta, mille kohta hankija esitab arvereale arve. | Pole |
| Allhankeleping | Allhankeleping, mille alusel teenused algselt telliti. | Kui tarnija arve jaoks on valitud allhankeleping, pärivad kõik hankija arveread selle valiku. Hankija arvel ei saa olla hankija arveridu, mis viitavad erinevatele allhankelepingutele. |
| Allhankelepingu rida | Allhankelepingu rida, mille alusel teenused algselt telliti. Valitavate allhankelepingu ridade loend piirdub valitud allhankelepingu ridadega. | Kui tarnija arve kulukategooriate reale on valitud allhankelepingu rida, sisestatakse vaikeväärtused väljadele **Projekt**, **Ülesanne** ja **Tehingukategooria** allhankelepingurea vastavatest väljadest. Kui valitud allhankelepingureal on väärtused väljadel **Projekt**, **Projekti ülesanne** ja **Tehinkukategooria**, ei tohi hankija arve rea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, mil hankija arverea kulu tegelik näitaja kirjendatakse projektile. |Pole |
| Kande klass | Valige **Kulu**, et salvestada kulukategooria jaoks hankija arve. | Väärtus **Kulu** näitab, et hankija arverida kasutatakse kulukategooriatena hangitud teenuste arve summa kirjendamiseks. |
| Project | Projekti nimi, mille raames kasutati arve aluseks olevaid teenuseid. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projekti ülesande nimi, mille raames kasutati arve aluseks olevaid teenuseid. See väli on saadaval ainult siis, kui projekt on valitud. Projekti ülesande valimine on valikuline. | Kui see väli jääb tühjaks, saab projektijuht sobitada hankija arve rea kuludega, mille allhankelepingu ressursid salvestavad projekti mis tahes ülesande puhul. Kui hanikja arverida ei viita allhankelepingu reale ja see väli on tühjaks jäetud, ei seotaks hankija arverea poolt loodud kulu tegelikku näitajad ühegi arveldamata müügitehingu tegelike näitajatega. Kui ülesandepõhine arveldamine on seadistatud, ei pruugi sel juhul kulusid lõppkliendile arveldada. |
| Kande kategooria | Tehingukategooria, misa arveldatakse. Valitud tehingukategooriale tuleb luua vastav kulukategooria. | Väärtuste **Tehingukategooria** ja **Ühik** kombinatsiooni kasutatakse hankija arve real välja **Ühiku hind** vaike- või arvutatud väärtusena. |
| Kogus | Sisestage arvereale kogus, mida hankija arveldab. |Pole|
| Ühikurühm | Vaikeväärtus sisestatakse valitud tehingukategooria ühikurühma alusel. | Pole |
| Üksus | Vaikeväärtus on valitud ühikurühma baasühik. Saate seda väärtust muuta, et osta ühikurühma mis tahes ühikus. | Väärtuste **Tehingukategooria** ja **Ühik** kombinatsiooni kasutatakse hankija arve real välja **Ühiku hind** vaike- või arvutatud väärtusena. |
| Ühiku hind | Ühiku vaikehind kasutab **Tehingukategooria** ja **Ühik** väärtuste kombinatsiooni projekti hinnakirjast, mis on rakendatav hankija arve rea tehingukuupäevale. | Kui kehtiva projekti hinnakirja hind on seadistatud ühikus, mis erineb hankija arvereal olevast ühikust, kasutab süsteem ühikuhinna arvutamiseks ühikute teisendust. |
| Vahesumma | See kirjutuskaitstud väli arvutatakse järgmiselt: *Kogus* &times; *Ühikuhind*, kui väärtused on sisestatud nii väljale **Kogus** kui ka väljale **Ühikuhind**. Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse sisestada.| Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arverea kogusumma koos maksudega. See väli arvutatakse järgmiselt: *Vahesumma* + *Müügimaks*. | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
