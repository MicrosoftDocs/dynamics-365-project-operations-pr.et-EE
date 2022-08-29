---
title: Allhankelepingu tooteread
description: Selles artiklis selgitatakse, kuidas salvestada toodete allhankeridu ja kasutada erinevaid välju hankijatelt tehtud tooteostude salvestamiseks.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b5852df1876eff591ae6a131b229d979eacf5aad
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262101"
---
# <a name="subcontract-lines-for-products"></a>Allhankelepingu tooteread

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Rakenduses Dynamics 365 Project Operations võib allhankelepingul olla rida toodete jaoks. Need read võimaldavad projektijuhil osta hankijatelt tooteid, mida nad saavad seejärel projekti tööülesannetes kasutada.

Läbige järgmised etapid, et luua Project Operationsis allhankelepingu tooterida.

1. Valige navigeerimislehel **Allhankelepingud** ja seejärel avage see allhankeleping, millega soovite töötada. 
2. Uue allhankelepingu rea loomiseks tehke vahekaardil **Allhankelepingute read** valik **+ Uus**.
3. Tehke lehe **Kiirloomine** väljal **Kande klass** valik **Materjal** ja sisestage või valige nõutav välja teave. 
4. Valige **Salvesta**.

Järgmine tabel sisaldab teavet lehe **Allhankelepingu rea üksikasjad** ja lehe **Kiirloomine** väljade kohta, sest need on toodete ostmisel asjakohased.

| Väli | Kirjeldus | Funktsionaalne mõju|
| ----- | ----------- | ----------- |
| Nimetus | Tuvastamisel abiks oleva allhankelepingu rea nimi. |See kuvatakse kõigis otsingutes allhankelepingu ridade põhjal esimese veeruna.
| Kirjeldus | Allhankelepingu real tellitavate toodete lühikirjeldus. | Pole |
| Rea tüüp | Selle välja vaikeväärtus on **Kogusepõhine**. |Pole |
| Arveldusmeetod | See on Project Operationsi toetatud kahte peamist lepingumudelit esindav suvandikomplekt: **Fikseeritud hind** ning **Kellaaeg ja materjal**. | Valitud arveldusmeetodil põhinedes tehakse allhankelepingu ridade jaoks kättesaadavaks vahe-eesmärkidel põhineva arve ajakava koos fikseeritud hinnaga arveldusmeetodiga. |
| Tehingu liik |Selle välja vaikeväärtus on **Kellaaeg**. Toodete ostmiseks allhankelepingu ridade loomiseks määrake välja **Kande liik** väärtuseks **Materjal**.  | See näitab, et projektides kasutatavate toodete ostu talletamiseks kasutatakse allhankelepingu rida. |
| Vali toode | Valige, kas ostetavat toodet hoitakse tootekataloogis või on see sisestatav toode. |Pole |
| Toode | Valige kataloogist aktiivne toode. See väli on saadaval ainult juhul, kui **Vali toode** on seadistatud väärtusele **Olemasolev**. |Suvandite **Toode** ja **Ühik** kombinatsiooni kasutatakse allhankelepingu rea vaikeväärtusena või arvutatud ühikuhinnana.
| Sisestatav toode | Sisestage sisestatava toote nimi. See väli on saadaval ainult juhul, kui **Vali toode** on seadistatud väärtusele **Sisestatav**.  |Sisestatavate toodete ostuhinda automaatselt ei täideta.|
| Soovitud tarnekuupäev | Sisestage toodete nõutav tarnekuupäev.| Seda kuupäeva kasutatakse ka projekti hinnakirja valimiseks allhankelepingule lisatud projekti hinnakirjade hulgast. Allhankelepingu rea toote hinna vaikeväärtus saadakse sellest hinnakirjast. |
| Lepingupõhine tarnekuupäev | Sisestage kuupäev, millal on toodete kohaletoimetamine lepingu järgi kokku lepitud.  |Pole|
| Tellitud kogus | Sisestage hankijalt ostetava toote kogus.| Seda kasutatakse hoiatuste nägemiseks, kui projektijuht saab selle kogusega võrreldes liiga palju.|
| Ühikurühm | See väärtus on vaid kataloogi toodete vaikeväärtuseks. |Kui valitud on nii **Toode** kui ka **Soovitud tarnekuupäev**, valib süsteem tarnekuupäeva põhjal kohaldatava hinnakirja. Vastava toote jaoks esitatakse seostuvate hinnakirjaüksuste päring. Ühiku- ja ühikurühma vaikeväärtused saadakse hinnakirjaüksuste kirje seadistusest. |
| Üksus | See väärtuse on vaikeväärtuseks on hinnakirjaüksuse kirjes määratud ühik. Vajadusel saate selle muuta mõneks muuks ühikuks.| Toote ja ühiku kombinatsiooni kasutatakse olemasolevate kataloogitoodete allhankelepingu real vaikimisi ühiku hinna saamiseks. |
| Ühiku hind | Ühiku hinnavälja vaikeväärtuse saamiseks kasutatakse allhankelepingu real soovitud tarnekuupäevale kohalduva projekti hinnakirjaga seotud hinnakirjaüksuste toote ja ühiku kombinatsiooni.  |Pole |
| Vahesumma | See kirjutuskaitstud väli arvutatakse valemiga kogus x ühiku hind, kui mõlemale väljale on sisestatud väärtused. Kui kas väli **Kogus**, väli **Ühiku hind** või mõlemad on tühjad, saate sisestada väärtuse käsitsi.  |Pole |
| Käibemaks | Sisestage käibemaksu väärtus. |Pole |
| Kogusumma | See arvutatud väli kuvab allhankelepingu rea kogusumma koos maksudega. Selle välja väärtus arvutatakse kui vahesumma + käibemaks. |Pole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
