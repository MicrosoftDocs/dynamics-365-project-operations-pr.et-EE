---
title: Allhankelepingu ajaread
description: Selles teemas kirjeldatakse, kuidas kirjendada aja allhankelepingute ridu ja kirjendada hankijatelt aja ostmist.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547239"
---
# <a name="subcontract-lines-for-time"></a>Allhankelepingu ajaread

[!include [banner](../../includes/dataverse-preview.md)]

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
