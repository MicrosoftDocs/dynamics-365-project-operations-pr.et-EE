---
title: Hankija arveread toodete jaoks
description: See artikkel kirjeldab, kuidas kirjendada hankija arveridu ja kasutada erinevaid välju hankijatelt toodete ostmise kirjendamiseks.
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

Rakenduse Microsoft Dynamics 365 Project Operations hankija arvel võivad olla toodete hankija arveread (mida nimetatakse ka materjalideks). Projektijuhid saavad kasutada hankija arve ridu toodete jaoks, et registreerida ostetud toodete kulu.

Hankija arveread toodete jaoks võivad viidata, kuid ei pruugi viidata materjalide osas allhankelepingureale. Kui hankija toodete arverida viitab allhankelepingule, saavad projektijuhid võrrelda ja kontrollida tooteid, millele hankija arve rida arveldab, ostetud toodete kasutamisega, mis on salvestatud ja projektijuhtide poolt kinnitatud.

Alljärgnevas tabelis on esitatud teave hankija arveridade toodete väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve rea nimi, mis aitab tuvastada. | See nimi kuvatakse esimese veeruna kõigis hankija arve ridadel põhinevates otsingutes. |
| Kirjeldus | Lühikirjeldus toodete kohta, mille kohta hankija esitab arvereale arve. | Pole |
| Allhankeleping | Allhankeleping, mille alusel tooted algselt telliti. | Kui tarnija arve jaoks on valitud allhankeleping, pärivad kõik hankija arveread selle valiku. Hankija arvel ei saa olla hankija arveridu, mis viitavad erinevatele allhankelepingutele. |
| Allhankelepingu rida | Allhankelepingu rida, mille alusel tooted algselt telliti. Valitavate allhankelepingu ridade loend piirdub valitud allhankelepingu ridadega. | Kui tarnija arve tootdete reale on valitud allhankelepingu rida, sisestatakse vaikeväärtused väljadele **Projekt**, **Ülesanne** ja **Toode** allhankelepingurea vastavatest väljadest. Kui valitud allhankelepingureal on väärtused väljadel **Projekt**, **Ülesanne** ja **Toode**, ei tohi hankija arve rea vastavate väljade väärtused nendest väärtustest erineda. |
| Tehingu kuupäev | Kuupäev, mil hankija arverea kulu tegelik näitaja kirjendatakse projektile. | Pole|
| Kande klass | Kui toodetele esitatakse arve, tuleks selle välja väärtuseks määrata **Materjal**. | Väärtus **Materjal** näitab, et hankija arve rida kasutatakse ostetud materjalide arve summa kirjendamiseks. |
| Project | Projekti nimi, mille raames kasutati arve aluseks olevaid tooteid. | See väli on kohustuslik ja seda ei saa tühjaks jätta. |
| Toiming | Projekti ülesande nimi, mille raames kasutati arve aluseks olevaid tooteid. See väli on saadaval ainult siis, kui projekt on valitud. Projekti ülesande valimine on valikuline. | Kui see väli jääb tühjaks, saab projektijuht sobitada hankija arve rea ostetud tootega, mida kasutatakse projekti mis tahes ülesande täitmisel. Kui hanikja arverida ei viita allhankelepingu reale ja see väli on tühjaks jäetud, ei seotaks hankija arverea poolt loodud kulu tegelikku näitajad ühegi arveldamata müügitehingu tegelike näitajatega. Kui ülesandepõhine arveldamine on seadistatud, ei saa sel juhul kulusid lõppkliendile arveldada. |
| Toote valimine | Valige, kas arveldatav toode on kataloogis olemasolev toode või sisestatav toode. | Vaikeväärtus sisestatakse allhankelepingu realt allhankelepingu rea valimisel. |
| Toode | Valige kataloogist toode. Kui toode on sisestatav toode, sisestage toote nimi. | Seda välja kasutatakse olemasolevate toodete vaikeostuhindade sisestamiseks. |
| Kogus | Sisestage sellele arvereale materjali kogus, mida hankija arveldab. | Pole |
| Ühikurühm | Valige ühiku ühikurühm, milles arveldatav kogus on väljendatud. | Pole |
| Üksus | Vaikeväärtus on valitud ühikurühma baasühik. Saate seda väärtust muuta, et maksta valitud ühikurühma mis tahes ühikus. | Väärtuste **Toode** ja **Ühik** kombinatsiooni kasutatakse hankija arve real välja **Ühiku hind** vaike- või arvutatud väärtusena. |
| Ühiku hind | Ühiku vaikehind kasutab **Toode** ja **Ühik** väärtuste kombinatsiooni projekti hinnakirjast, mis on rakendatav hankija arve rea tehingukuupäevale. | Pole |
| Vahesumma | See kirjutuskaitstud väli arvutatakse järgmiselt: *Kogus* &times; *Ühikuhind*, kui väärtused on sisestatud nii väljale **Kogus** kui ka väljale **Ühikuhind**. Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse sisestada. | Pole |
| Käibemaks | Sisestage käibemaksu summa. | Pole |
| Kogusumma | Hankija arverea kogusumma koos maksudega. See väli arvutatakse järgmiselt: *Vahesumma* + *Müügimaks*. | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
