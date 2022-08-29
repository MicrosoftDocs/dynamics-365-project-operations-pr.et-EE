---
title: Allhankelepingu read kulukategooriate jaoks
description: Selles artiklis selgitatakse, kuidas salvestada allhanke ridu kulude jaoks ja kasutada välju hankijatelt aja ostmise salvestamiseks.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261835"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Allhankelepingu read kulukategooriate jaoks

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations võib allhankelepingul olla rida kulukategooriate jaoks. Kulukategooriate allhankelepingu read võimaldavad projektijuhil osta hankijatelt teenuste või toodete kategooriaid, mida projekti arvele kanda.

Rakenduses Project Operations kulukategooriatele allhankelepingu rea loomiseks tehke järgmised toimingud.

1. Valige navigeerimispaanil **Allhankelepingud** ja avage see allhankeleping, millega soovite töötada.
2. Uue rea loomiseks tehke vahekaardil **Allhankelepingute read** valik **Uus**.
3. Tehke lehe **Kiirloomine** väljal **Kande klass** valik **Kulu** ja sisestage või valige mistahes muu nõutava välja teave.

Järgmine tabel sisaldab teavet **Allhankelepingu rea** üksikasjade lehe väljade ja **Kiirloomise** lehe kohta.

| **Väli** | **Kirjeldus** | **Funktsionaalne mõju** |
| --- | --- | --- |
| Nimetus | Tuvastamisel abiks oleva allhankelepingu rea nimi. | See kuvatakse kõigis otsingutes allhankelepingu ridade põhjal esimese veeruna. |
| Kirjeldus | Allhankelepingu real ostetavate kulukategooriate lühikirjeldus. | Pole |
|Rea tüüp | Selle välja vaikeväärtus on **Kogusepõhine**. |Pole |
| Arveldusmeetod | See on Project Operationsi toetatud kahte peamist lepingumudelit esindav suvandikomplekt: **Fikseeritud hind** ning **Kellaaeg ja materjal**. | Kui valitud on fikseeritud hinnaga arveldusmeetod, on allhankelepingu ridade jaoks tehtud kättesaadavaks vahe-eesmärkidel põhineb arve ajakava. |
| Tehingu liik | Selle välja vaikeväärtus on **Kellaaeg**. Toodete ostmiseks allhankelepingu ridade loomiseks määrake välja **Kande liik** väärtuseks **Kulu**.  | See näitab, et projektides kasutatava kulukategooria ostu talletamiseks kasutatakse allhankelepingu rida. |
| Tehingu kategooria | Näitab süsteemi aktiivsete kannete kategooriate loendit. |Pole |
| Soovitud algus | Sisestage kuupäev, millal ostukategooriad peavad olema hankijalt saadaval. | Taotletud algust kasutatakse allhankelepingule lisatud projekti hinnakirjade loendist projekti hinnakirja valimiseks. Allhankelepingu rea kategooria kulu pärineb sellest hinnakirjast. |
| Soovitud lõpp | Sisestage kuupäev, millal ostukategooriaid enam vaja pole. | Seda kasutatakse hoiatuste kuvamiseks, kui projektijuht seostab selle allhankelepingu rea projekti konkreetse kuluprognoosiga, mis on pärast seda kuupäeva vajalik. |
| Tellitud kogus | Hankijalt ostetava kategooria kogus. | Seda kasutatakse hoiatuste nägemiseks, kui projektijuht saab selle kogusega võrreldes liiga palju.|
| Ühikurühm | Vaikeväärtus põhineb valitud kategooria jaoks määratud vaikimisi ühikurühmal. |Pole |
| Üksus | Vaikevalik põhineb valitud kategooria jaoks määratud vaikimisi ühiku.  | Suvandite **Kategooria** ja **Ühik** kombinatsiooni kasutatakse allhankelepingu rea vaikeväärtusena või arvutatud ühikuhinnana.  |
| Ühiku hind | Vaikeväärtus kasutab suvandite **Kategooria** ja **Ühik** kombinatsiooni projekti hinnakirjaga seotud kategooria hindadest, mis kehtivad allhankelepingu rea taotletud ajal. |Pole |
| Vahesumma | See on kirjutuskaitstud väli, mis arvutatakse koguse X ühikuhinnana, kui sisestatud on nii koguse- kui ka ühikuhinna väärtused. Kui mõlemad väljad on tühjad, võite sellele väljale sisestada väärtuse. |Pole |
| Käibemaks | Sisestage käibemaksu summa. |Pole |
| Kogusumma | Allhankelepingu rea kogusumma koos maksudega. Selle välja väärtus arvutatakse kui vahesumma + käibemaks. |Pole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
