---
title: Allhankelepingu read kulukategooriate jaoks
description: Selles teemas kirjeldatakse, kuidas kirjendada kulude allhankelepingute ridu ja kasutada välju hankijatelt aja ostmise kirjendamiseks.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323816"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Allhankelepingu read kulukategooriate jaoks

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations võib allhankelepingul olla rida kulukategooriate jaoks. Kulukategooriate allhankelepingu read võimaldavad projektijuhil osta hankijatelt teenuste või toodete kategooriaid, mida projekti arvele kanda.

Rakenduses Project Operations kulukategooriatele allhankelepingu rea loomiseks tehke järgmised toimingud.

1. Valige navigeerimispaanil **Allhankelepingud** ja avage see allhankeleping, millega soovite töötada.
2. Uue rea loomiseks tehke vahekaardil **Allhankelepingute read** valik **Uus**.
3. Tehke lehe **Kiirloomine** väljal **Kande klass** valik **Kulu** ja sisestage või valige mistahes muu nõutava välja teave.

Järgmine tabel sisaldab teavet **Allhankelepingu rea** üksikasjade lehe väljade ja **Kiirloomise** lehe kohta.

| **Väli** |  **Kirjeldus** |
| ----------| ---------------- |
| Nimetus | Allhankelepingu rea nimi. |
| Kirjeldus | Allhankelepingu real ostetavate teenuse- või tootekategooriate lühikirjeldus. |
| Rea tüüp | Selle välja vaikeväärtus on **Kogusepõhine**.  |
| Arveldusmeetod | Allhankelepingu rea arveldusmeetod. Rea arveldusmeetodi põhjal on fikseeritud hinnaga arveldusmeetodi jaoks saadaval vahe-eesmärgi põhine arvegraafik.  |
| Tehingu liik | Selle välja vaikeväärtus on **Aeg**. Toodete ostmiseks allhankelepingu ridade loomiseks määrake välja **Kande liik** väärtuseks **Kulu**. See väljaväärtus näitab, et allhankelepingu rida kasutatakse projektides kasutatavate toodete või teenuste kategooria ostu kirjendamiseks. |
| Tehingu kategooria | Valige kandekategooria. |
| Soovitud algus | Kuupäev, millal ostu kategooriad peavad hankijalt saadaval olema. Soovitud algust kasutatakse projekti hinnakirja valimiseks allhankelepingule lisatud projekti hinnakirjade hulgast. Allhankelepingu rea kategooria kulu vaikeväärtus saadakse sellest hinnakirjast. |
| Soovitud lõpp | Kuupäev, millal ostu kategooriaid enam ei vajata. See kuupäev põhjustab hoiatuse, kui projektijuht seostab selle allhankelepingu rea konkreetse kuluprognoosiga selliste projektide jaoks, mille kuupäev on pärast seda kuupäeva. |
| Tellitud kogus | Hankijalt ostetava kategooria kogus. Kui projektijuht ületab ostetud kogust, kuvatakse hoiatus.  |
| Ühikurühm | Selle välja väärtuse vaikeväärtused põhinevad valitud kategooria jaoks seadistatud vaikimisi ühikurühmal. |
| Üksus | Selle välja väärtuse vaikeväärtused põhinevad valitud kategooria jaoks seadistatud vaikeühikul. Kategooria ja ühiku kombinatsiooni kasutatakse allhankelepingu real vaikimisi ühiku hinna saamiseks. |
| Ühiku hind | Ühiku hinnavälja vaikeväärtuseks on projekti hinnakirjaga seotud kategooria hindade kategooria ja ühiku kombinatsioon, mis on kohaldatav allhankelepingu rea soovitud algusele.  |
| Vahesumma | See kirjutuskaitstud väli arvutatakse koguse ühiku hinnana koguse ja ühiku hinna väärtuste sisestamisel automaatselt. Kui üks või mõlemad väljad on tühjad, saate sellele väljale väärtuse käsitsi sisestada.  |
| Käibemaks | Sisestage käibemaksu summa.  |
| Kogusumma | Allhankelepingu rea kogusumma koos maksudega. Selle välja väärtus arvutatakse kui vahesumma + käibemaks.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
