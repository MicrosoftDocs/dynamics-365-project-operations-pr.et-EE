---
title: Allhankelepingu ajaread
description: Selles teemas kirjeldatakse, kuidas kirjendada aja allhankelepingute ridu ja kirjendada hankijatelt aja ostmist.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323861"
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

| **Väli** | **Kirjeldus** |
| --- | --- |
| Nimetus | Allhankelepingu rea nimi. |
| Kirjeldus | Allhankelepingu real ostetavate teenuste lühikirjeldus. | 
| Rea tüüp | See väli on vaikeväärtus.  |
| Arveldusmeetod | Valige arveldusmeetod. Viidatud allhankelepingu rea arveldusmeetodi põhjal tehakse fikseeritud hinnaga arveldusmeetodi jaoks kättesaadavaks vahe-eesmärgi põhine arvegraafik. |
| Tehingu liik | See väli on vaikeväärtus, mis näitab, kas allhankelepingu rida kasutatakse alltöövõtja aja ostmise kirjendamiseks. |
| Roll | Selle allhankelepingu ressursi roll, kelle aega ostetakse. Allhankelepingu ressursile määratud roll määrab ostu maksumuse. |
| Soovitud algus | Kuupäev, millal allhankelepingu ressursid peavad tööd alustama. Soovitud algust kasutatakse projekti hinnakirja valimiseks allhankelepingule lisatud projekti hinnakirjade hulgast. Allhankelepingu rea rolli hinna vaikeväärtus saadakse sellest hinnakirjast. |
| Soovitud lõpp | Kuupäev, millal alltöövõtja ressursside määramine lõpeb. Seda kuupäeva kasutatakse hoiatuste kuvamiseks, kui projektijuht kasutab seda mahtu pärast seda kuupäeva toimuvate ressursinõuete jaoks. |
| Tellitud kogus | Hankijalt ostetavate rolli tundide arv. Seda väärtust kasutatakse hoiatuste kuvamiseks, kui projektijuht ületab ressursinõude jaoks seda mahtu. |
| Ühikurühm | Selle välja vaikeväärtuseks on ühikurühm Aeg ja seda ei saa muuta.  |
| Üksus | Selle välja vaikeväärtuseks on tundide baasühik ühikurühmast Aeg. Seda väärtust saate muuta, et osta mistahes ühikurühma Aeg ühik, näiteks päev või nädal. Rolli ja ühiku kombinatsiooni kasutatakse allhankelepingu real ühiku hinna arvutamiseks. |
| Ühiku hind | Ühiku hinnavälja vaikeväärtuseks on projekti hinnakirja hindade rolli ja ühiku kombinatsioon, mis on kohaldatav allhankelepingu rea soovitud alguskuupäevale. Kui rakendatavas projekti hinnakirjas on hind seadistatud muus ühikus kui allhankelepingu rea ühik, kasutab süsteem ühikuhinna arvutamiseks ühiku teisendamist. |
| Vahesumma | See on kirjutuskaitstud väli, mis arvutatakse valemiga **kogus x ühiku hind**, kui nii koguse kui ka ühiku hinna väärtused on sisestatud. Kui kas kogus, ühikuhind või mõlemad on tühjad, võite sisestada väärtuse väljale. |
| Käibemaks |  Sisestage käibemaksu summa. |
| Kogusumma | Allhankelepingu rea kogusumma koos maksudega. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
