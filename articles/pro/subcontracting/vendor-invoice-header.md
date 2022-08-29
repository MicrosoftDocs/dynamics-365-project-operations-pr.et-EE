---
title: Hankija arvete päise üksikasjad
description: Selles artiklis selgitatakse Microsofti hankijaarve päises pakutavaid funktsioone Dynamics 365 Project Operations.
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

Selles artiklis selgitatakse Microsofti hankijaarve päises pakutavaid funktsioone Dynamics 365 Project Operations.

Projektijuhtidena võivad nad projekte kavandada ja ellu viia alltöövõtjaid ning osta tooteid ja teenuseid hankijatelt. Projekti käivitamise ajal tekivad kulud teenustest, materjalidest ja kulukategooriatest, mis hangitakse hankijatega sõlmitud allhangete alusel. Hankijad arveldavad need kulud projektidega, luues hankija arved.

Järgmine tabel sisaldab teavet hankija arve päiste väljade kohta project operationsis.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve nimi. | Kõigis hankija arve ripploendites on hankija arve nimi loetletud esimeses veerus, et aidata teil hankija arvet tuvastada. Kui hankija arve luuakse allhankest, **määratakse hankija arve välja nimi** vaikimisi väärtusele, mis koosneb allhanke nimest ja praegusest kuupäevast. |
| Kirjeldus | Hankija arvel arveldatavate teenuste ja toodete lühikirjeldus. | Pole |
| Tarnija | Selle ettevõtte nimi, kes toodete ja teenuste eest arveid esitab. See ettevõte peaks olema kontokirje, mille seose tüüp **on Hankija** või **Tarnija**. | <p>Valitud hankija põhjal sisestatakse vaikeväärtused automaatselt järgmistele väljadele.</p><ul><li>Valuuta</li><li>Hinnakirjad</li><li>Maksetingimused</li><li>Makse aadress</li></ul> |
| Allhankeleping | Viide hankija arve alltöövõtule. | <p>Valitud allhanke põhjal sisestatakse vaikeväärtused automaatselt järgmistele väljadele.</p><ul><li>Valuuta</li><li>Hinnakirjad</li><li>Maksetingimused</li><li>Makse aadress</li></ul><p>Hankija arve päises valitud alltöövõtt sisestatakse vaikimisi hankija arve ridadele ja seda ei saa seal muuta.</p> |
| Arve kuupäev | Hankija arve kinnitamisel loodavate tegelike kulude kuupäev. | Arve kuupäeva kasutatakse ka õige ostuhinnastiku valimiseks kas seotud hankijale manustatud hinnakirjadest või projekti parameetritest. |
| Oleku põhjus | Hankija arve olek. | <p>Olek määrab, kus hankija arve äriprotsessis asub ja kas seda saab redigeerida. Siin on mõned saadaolevad väärtused.</p><ul><li>**Mustand** – hankija arvet saab muuta.</li><li>**Kinnitatud** – hankija arve kinnitati ja kinnitati. Selles olekus hankija arveid ei saa redigeerida ega kustutada.</li><li>**Protsessis** – hankija arve vaadatakse üle. Selles olekus hankija arveid saab redigeerida, kuid neid ei saa kustutada.</li><li>**Tühistatud** – hankija arve tühistati. Selles olekus hankija arveid ei saa redigeerida ega kustutada.</li></ul> |
| Valuuta | Valuuta, milles hankija hankija arve toodete ja teenuste eest arveldab. | Hankijaarvel, mis viitab allhankele, sisestatakse allhanke valuuta vaikimisi hankija arve valuutana. Hankija arvel, mis ei viita allhankele, sisestatakse vaikeväärtus hankija konto kirjest ja seda saab muuta. Pärast hankija arve salvestamist ei saa valuutat enam redigeerida. |
| Lepingut sõlmiv üksus | Ettevõtte jagunemine, mis vastutab müüjalt teenuste ja/või toodete saamise eest. | Pole |
| Maksetingimused | Väljastatud hankijaarvete maksetingimused. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhanke maksetingimused kopeeritakse kõigile hankija arvetele, mis on allhankega seotud. Maksetingimusi saab värskendada, kui hankija arve olek **on Mustand**. |
| Makse aadress | Hankija aadress, kellele maksed tuleb saata. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhanke makseaadress kopeeritakse makseaadressina kõigile hankija arvetele, mis selle allhanke jaoks luuakse. Makseaadressi saab värskendada, kui hankija arve olek **on Mustand**. |
| Vahesumma | Kui hankija arvel ei ole ridu, sisestage arve vahesumma enne makse. Kui hankija arvel on read, on see väli ainult kirjutuskaitstud. Sel juhul on näidatud summa hankija arve kõigi ridade vahesumma. | Pole |
| Maks kokku | Kui hankija arvel pole ridu, sisestage allhankemaksude kogusumma. Kui hankija arvel on read, on see väli ainult kirjutuskaitstud. Sel juhul on näidatud summa hankija arve kõigi ridade maksusummade summa. | Pole |
| Kogusumma | See arvutatud väli näitab hankija arve kogusummat pärast maksude kaasamist. | Pole |

> [!NOTE]
> Hankija arve järgmisi välju ei saa pärast hankija arve salvestamist muuta: **Hankija, Allhange**, **Valuuta** **,** Lepinguühik **ja** Maksetingimused **·**. Kui hankija arvel on vaja neid välju muuta, peate hankija arve kustutama ja looma uue hankijaarve.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
