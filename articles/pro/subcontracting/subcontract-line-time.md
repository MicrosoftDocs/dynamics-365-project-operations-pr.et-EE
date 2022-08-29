---
title: Allhankelepingu ajaread
description: Selles artiklis selgitatakse, kuidas salvestada allhanke ridu aja jooksul ja salvestada hankijatelt aja ostmist.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8e9619dc713fde3127f552234e4a7427d99be683
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261977"
---
# <a name="subcontract-lines-for-time"></a>Allhankelepingu ajaread

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations võib allhankelepingul olla rida aja jaoks. Allhankelepingu ajaread võimaldavad projektijuhil osta hankija ressursi aega projekti tööülesannete ja ressursi nõuete katmiseks.

Rakenduses Project Operations allhankelepingu ajarea loomiseks tehke järgmised toimingud.

1. Valige navigeerimispaanil **Allhankelepingud** ja avage üks allhankeleping.
2. Uue allhankelepingu rea loomiseks tehke vahekaardil **Allhankelepingute read** valik **Uus**.
3. Tehke lehe **Kiirloomine** väljal **Tehinguklass** valik **Aeg**.
4. Sisestage ülejäänud väljateave ja seejärel valige **Salvesta**.

  Järgmine tabel sisaldab teavet **Allhankelepingu rea** lehe väljade ja **Kiirloomise** lehe kohta.

| **Väli** | **Kirjeldus** | **Funktsionaalne mõju** |
| --- | --- | --- |
| Nimetus | Tuvastamisel abiks oleva allhankelepingu rea nimi. | See kuvatakse kõigis otsingutes allhankelepingu ridade põhjal esimese veeruna. |
| Kirjeldus | Allhankelepingu real ostetavate teenuste lühikirjeldus. |Pole |
| Rea tüüp |   Selle välja vaikeväärtus on **Kogusepõhine**.| Pole |
| Arveldusmeetod | See on Project Operationsi toetatud kahte peamist lepingumudelit esindav suvandikomplekt: **Fikseeritud hind** ning **Kellaaeg ja materjal**. | Valitud arveldusmeetodil põhinedes tehakse allhankelepingu ridade jaoks kättesaadavaks vahe-eesmärkidel põhineva arve ajakava koos fikseeritud hinnaga arveldusmeetodiga. |
| Tehingu liik | Vaikeväärtus on **Aeg**. | See näitab, et allhankelepingu rida kasutatakse alltöövõtja aja ostmise talletamiseks. |
| Roll | Valige allhankelepingu ressursside rull, kelle aega ostetakse. | Allhankelepingu ressursi täidetav roll määrab ostu kulu. |
| Soovitud algus | Sisestage kuupäev, millal alltöövõtja ressursid peavad tööga alustama. | Seda kasutatakse allhankelepingule lisatud projekti hinnakirjade loendist projekti hinnakirja valimiseks. Allhankelepingu rea rolli kulu pärineb sellest hinnakirjast. |
| Soovitud lõpp | Sisestage kuupäev, millal alltöövõtja ressursi ülesanne lõpeb. | Seda kasutatakse hoiatuste näitamiseks, kui projektijuht kasutab ressursi nõude jaoks mahtu pärast seda kuupäeva. |
| Tellitud kogus | Sisestage hankijalt ostetud rolli tundide arv. | Seda kasutatakse hoiatuste näitamiseks, kui projektijuht kasutab ressursi nõude jaoks seda mahtu liigselt. |
| Ühikurühm | Vaikeväärtus on **Ajaühiku rühm**, mida ei saa muuta. | Pole|
| Üksus | Selle välja vaikeväärtus on tundide baasühik suvandist **Ajaühiku rühm**. Seda väärtust saate muuta, et osta mistahes ühikut suvandist **Ajaühiku rühm**, näiteks päev või nädal. | Suvandite **Roll** ja **Ühik** kombinatsiooni kasutatakse allhankelepingu rea vaikeväärtusena või arvutatud ühikuhinnana. |
| Ühiku hind | Ühiku vaikehind kasutab suvandite **Roll** ja **Ühik** kombinatsiooni projekti hinnakirjast, mis kehtivad allhankelepingu rea kuupäeval **Taotletud algusaeg**. | Kui rakendatavas projekti hinnakirjas on hind seadistatud muus ühikus kui allhankelepingu rea ühik, kasutab süsteem ühikuhinna arvutamiseks ühiku teisendamist. |
| Vahesumma |    See on kirjutuskaitstud väli, mis arvutatakse koguse × ühikuhinnana, kui sisestatud on nii koguse- kui ka ühikuhinna väärtused. Kui kas kogus, ühikuhind või mõlemad on tühjad, võite sisestada väärtuse väljale. | Pole|
| Käibemaks |   Sisestage käibemaksu summa. |Pole |
| Kogusumma | Allhankelepingu rea kogusumma koos maksudega. Selle välja väärtus arvutatakse kui vahesumma + käibemaks.|Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
