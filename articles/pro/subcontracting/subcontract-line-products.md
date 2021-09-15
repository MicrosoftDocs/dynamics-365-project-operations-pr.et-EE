---
title: Allhankelepingu tooteread
description: Selles teemas kirjeldatakse, kuidas kirjendada allhankelepingute tooteridu ja kasutada erinevaid välju hankijatelt toodete ostmise kirjendamiseks.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323681"
---
# <a name="subcontract-lines-for-products"></a>Allhankelepingu tooteread

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations võib allhankelepingul olla rida toodete jaoks. Need read võimaldavad projektijuhil osta hankijatelt tooteid, mida nad saavad seejärel projekti tööülesannetes kasutada.

Läbige järgmised etapid, et luua Project Operationsis allhankelepingu tooterida.

1. Valige navigeerimislehel **Allhankelepingud** ja seejärel avage see allhankeleping, millega soovite töötada. 
2. Uue allhankelepingu rea loomiseks tehke vahekaardil **Allhankelepingute read** valik **+ Uus**.
3. Tehke lehe **Kiirloomine** väljal **Kande klass** valik **Materjal** ja sisestage või valige nõutav välja teave. 
4. Valige **Salvesta**.

Järgmine tabel sisaldab teavet lehe **Allhankelepingu rea üksikasjad** ja lehe **Kiirloomine** väljade kohta, sest need on toodete ostmisel asjakohased.

| Väli | Kirjeldus |
| ----- | ----------- |
| Nimetus | Allhankelepingu rea nimi. |
| Kirjeldus | Allhankelepingu real tellitavate toodete lühikirjeldus. |
| Rea tüüp | Selle välja vaikeväärtus on **Kogusepõhine**. |
| Arveldusmeetod |  Allhankelepingu rea arveldusmeetod. Fikseeritud hinnaga arveldusmeetodite jaoks on saadaval vahe-eesmärgil põhinev arve ajakava. |
| Tehingu liik | Selle välja vaikeväärtus on **Aeg**. Toodete ostmiseks allhankelepingu ridade loomiseks tehke väljal **Kande liik** valik **Materjal**. See valik näitab, et allhankelepingu rida kasutatakse projektides kasutatavate toodete ostu kirjendamiseks. |
| Vali toode | Valige, kas ostetavat toodet hoitakse tootekataloogis või on see sisestatav toode. |
| Toode | Valige kataloogist aktiivne toode. See väli on saadaval ainult juhul, kui **Vali toode** on seadistatud väärtusele **Olemasolev**. |
| Sisestatav toode | Sisestage sisestatava toote nimi. See väli on saadaval ainult juhul, kui **Vali toode** on seadistatud väärtusele **Sisestatav**.  |
| Soovitud tarnekuupäev | Valige toodete jaoks nõutav tarnekuupäev. Seda kuupäeva kasutatakse ka projekti hinnakirja valimiseks allhankelepingule lisatud projekti hinnakirjade hulgast. Allhankelepingu rea toote hinna vaikeväärtus saadakse sellest hinnakirjast. |
| Lepingupõhine tarnekuupäev | Valige kuupäev, millal tooted lepingu järgi peaksid kohale jõudma.  |
| Tellitud kogus | Sisestage hankijalt ostetava toote kogus. Kui projektijuht seda kogust ületab, kuvatakse hoiatus. |
| Ühikurühm | See väärtus on vaid kataloogi toodete vaikeväärtuseks. Kui valitud on nii **Toode** kui ka **Soovitud tarnekuupäev**, valib süsteem tarnekuupäeva põhjal kohaldatava hinnakirja. Vastava toote jaoks esitatakse seostuvate hinnakirjaüksuste päring. Ühiku- ja ühikurühma vaikeväärtused saadakse hinnakirjaüksuste kirje seadistusest. |
| Üksus | See väärtus on hinnakirjaüksuse kirje ühiku seadistamise vaikeväärtuseks. Vajadusel saate selle muuta mõneks muuks ühikuks. Toote ja ühiku kombinatsiooni kasutatakse olemasolevate kataloogitoodete allhankelepingu real vaikimisi ühiku hinna saamiseks. |
| Ühiku hind | Ühiku hinnavälja vaikeväärtuse saamiseks kasutatakse allhankelepingu real soovitud tarnekuupäevale kohalduva projekti hinnakirjaga seotud hinnakirjaüksuste toote ja ühiku kombinatsiooni.  |
| Vahesumma | See kirjutuskaitstud väli arvutatakse valemiga kogus x ühiku hind, kui mõlemale väljale on sisestatud väärtused. Kui kas väli **Kogus**, väli **Ühiku hind** või mõlemad on tühjad, saate sisestada väärtuse käsitsi.  |
| Käibemaks | Sisestage käibemaksu väärtus. |
| Kogusumma | See arvutatud väli kuvab allhankelepingu rea kogusumma koos maksudega. Selle välja väärtus arvutatakse kui vahesumma + käibemaks. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
