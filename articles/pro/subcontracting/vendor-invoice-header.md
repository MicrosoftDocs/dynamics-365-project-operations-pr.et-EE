---
title: Hankija arvete päise üksikasjad
description: See artikkel selgitab rakenduse Microsoft Dynamics 365 Project Operations hankija arve päises pakutavaid funktsioone.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261648"
---
# <a name="header-details-for-vendor-invoices"></a>Hankija arvete päise üksikasjad

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

See artikkel selgitab rakenduse Microsoft Dynamics 365 Project Operations hankija arve päises pakutavaid funktsioone.

Kuna projektijuhid kavandavad ja teostavad projekte, võivad nad palgata allhanketöötajaid ning osta tooteid ja teenuseid hankijatelt. Projekti teostamise käigus tekivad kulud teenustelt, materjalidelt ja kulukategooriatelt, mis hangitakse hankijatega sõlmitud allhankelepingute alusel. Hankijad esitavad nende kulude eest projektidele arve, luues hankija arveid.

Järgmine tabel sisaldab teavet hankija arve päiste väljade kohta rakenduses Project Operations.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve nimi. | Kõigis hankija arve ripploendites on hankija arve nimi loetletud esimeses veerus, et aidata allhankelepingut tuvastada. Kui allhankelepingust hankija arve luuakse, määratakse hankija arve väljale **Nimi** vaikimisi väärtus, mis koosneb allhankelepingu nimest ja praegusest kuupäevast. |
| Kirjeldus | Hankija arvel arveldatavate teenuste ja toodete lühikirjeldus. | Pole |
| Hankija | Toote ja teenuste eest arveldava ettevõtte nimi. See ettevõte peaks olema kontokirje, mille suhte tüüp on **Hankija** või **Tarnija**. | <p>Vastavalt valitud hankijale sisestatakse vaikeväärtused automaatselt järgmistes väljades:</p><ul><li>Valuuta</li><li>Hinnakirjad</li><li>Maksetingimused</li><li>Makseaadress</li></ul> |
| Allhankeleping | Viide hankija arve allhankelepingule. | <p>Vastavalt valitud allhankelepingule sisestatakse vaikeväärtused automaatselt järgmistes väljades:</p><ul><li>Valuuta</li><li>Hinnakirjad</li><li>Maksetingimused</li><li>Makseaadress</li></ul><p>Hankija arve päises valitud allhankeleping sisestatakse vaikimisi hankija arve ridadele ja seda ei saa seal muuta.</p> |
| Arve kuupäev | Kuluarvestuse tegelike näitajate kuupäev, mis luuakse hankija arve kinnitamisel. | Arve kuupäeva kasutatakse ka õige ostu hinnakirja valimiseks kas seotud hankijatele lisatud hinnakirjadest või projekti parameetritest. |
| Oleku põhjus | Hankija arve olek. | <p>Olek määratleb, kus hankija arve ettevõtte tegevuses paikneb ning kas seda saab redigeerida. Siin on mõned saadaolevad väärtused.</p><ul><li>**Mustand** – Hankija arvet saab redigeerida.</li><li>**Kinnitatud** – Hankija arvet kontrolliti ja kinnitati. Hankija arveid selles olekus ei saa redigeerida ega kustutada.</li><li>**Protsessis** – Hankija arve on läbi vaadatud. Selles olekus hankija arveid saab muuta, kuid neid ei saa kustutada.</li><li>**Tühistatud** – Hankija arve tühistati. Hankija arveid selles olekus ei saa redigeerida ega kustutada.</li></ul> |
| Valuuta | Valuuta, milles hankija arveldab hankija arvel olevate toodete ja teenuste eest. | Hankija arvel, mis viitab allhankelepingule, sisestatakse vaikimisi hankija arve valuutaks allhankelepingu valuuta. Hankija arvel, mis ei viita allhankele, sisestatakse vaikeväärtus hankija konto kirjest ja seda saab muuta. Pärast hankija arve salvestamist ei saa valuutat enam muuta. |
| Lepingut sõlmiv üksus | Ettevõtte osakond, mis vastutab hankijalt teenuste ja/või toodete vastuvõtmise eest. | Pole |
| Maksetingimused | Väljastatud hankija arvete maksetingimused. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhankelepingu maksetingimused kopeeritakse selle allhankelepinguga seotud hankija arvetele. Maksetingimusi saab uuendada, kui hankija arve on olekus **Mustand**. |
| Makseaadress | Hankija aadress, kellele maksed tuleb saata. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhankelepingu makseaadress kopeeritakse makseaadressina kõigile selle allhankelepingu jaoks loodud hankija arvetele. Makseaadressi saab uuendada, kui hankija arve on olekus **Mustand**. |
| Vahesumma | Kui hankija arvel pole ridu, sisestage arve vahesumma enne makse. Kui hankija arvel on ridu, on see väli kirjutuskaitstud. Sellisel juhul on näidatav summa hankija arve kõikide ridade vahesumma. | Pole |
| Kogumaks | Kui hankija arvel pole ridu, sisestage allhankelepingu maksud kokku. Kui hankija arvel on ridu, on see väli kirjutuskaitstud. Sel juhul on kuvatav summa hankija arve kõigilt ridadelt saadud maksusummade summa. | Pole |
| Kogusumma | See arvutatud väli kuvab hankija arve kogusummat koos maksudega. | Pole |

> [!NOTE]
> Järgmisi hankija arve välju ei saa pärast hankija arve salvestamist muuta: **Hankija**, **Allhankeleping**, **Valuuta**, **Lepinguüksus** ja **Maksetingimused**. Kui hankija arvel on vaja neid väljasid muuta, peate hankija arve kustutama ja looma uue hankija arve.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
