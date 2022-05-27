---
title: Hankija arvete päise üksikasjad
description: Selles teemas selgitatakse Microsofti hankija arve päises pakutavat funktsionaalsust Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575575"
---
# <a name="header-details-for-vendor-invoices"></a>Hankija arvete päise üksikasjad

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas selgitatakse Microsofti hankija arve päises pakutavat funktsionaalsust Dynamics 365 Project Operations.

Kuna projektijuhid planeerivad ja viivad ellu projekte, võivad nad palgata alltöövõtjaid ning osta müüjatelt tooteid ja teenuseid. Projekti täitmise ajal tekivad kulud teenustest, materjalidest ja kulukategooriatest, mis hangitakse hankijatega allhanke korras. Hankijad arveldavad need kulud projektidele, luues hankija arveid.

Järgmises tabelis on esitatud teave projektitoimingute hankija arve päiste väljade kohta.

| Väli | Kirjeldus | Funktsionaalne mõju |
| --- | --- | --- |
| Nimetus | Hankija arve nimi. | Kõigis hankija arvete ripploendites on hankija arve nimi loetletud esimeses veerus, mis aitab teil hankija arvet tuvastada. Vaikimisi, kui hankija arve luuakse allhankelepingust, **seatakse hankija arve välja nimi** väärtuseks, mis koosneb alltöövõtu nimest ja praegusest kuupäevast. |
| Kirjeldus | Hankija arvel arveldatavate teenuste ja toodete lühikirjeldus. | Pole |
| Tarnija | Toodete ja teenuste eest arveid esitava ettevõtte nimi. See ettevõte peaks olema kontokirje, mille seosetüüp **on Hankija** või **Tarnija**. | <p>Valitud hankija põhjal sisestatakse vaikeväärtused automaatselt järgmistele väljadele.</p><ul><li>Valuuta</li><li>Hinnakirjad</li><li>Maksetingimused</li><li>Makse aadress</li></ul> |
| Allhankeleping | Viide hankija arve alltöövõtule. | <p>Valitud alltöövõtu põhjal sisestatakse vaikeväärtused automaatselt järgmistele väljadele.</p><ul><li>Valuuta</li><li>Hinnakirjad</li><li>Maksetingimused</li><li>Makse aadress</li></ul><p>Hankija arve päises valitud alltöövõtt sisestatakse vaikimisi hankija arve ridadele ja seda ei saa seal muuta.</p> |
| Arve kuupäev | Hankija arve kinnitamisel loodavate kulunäitajate kuupäev. | Arve kuupäeva kasutatakse ka õige ostuhinnakirja valimiseks kas seotud hankijaga seotud hinnakirjadest või projekti parameetritest. |
| Oleku põhjus | Hankija arve olek. | <p>Olek määrab, kus hankija arve äriprotsessis on ja kas seda saab redigeerida. Siin on mõned saadaolevad väärtused:</p><ul><li>**Mustand** – hankija arvet saab redigeerida.</li><li>**Kinnitatud** – hankija arve kinnitati ja kinnitati. Selles olekus hankija arveid ei saa redigeerida ega kustutada.</li><li>**Pooleli** – hankija arve vaadatakse üle. Selles olekus hankija arveid saab redigeerida, kuid neid ei saa kustutada.</li><li>**Tühistatud** – hankija arve tühistati. Selles olekus hankija arveid ei saa redigeerida ega kustutada.</li></ul> |
| Valuuta | Valuuta, mille hankija hankija hankija arvel olevate toodete ja teenuste eest arveldab. | Alltöövõtule viitaval hankija arvel sisestatakse allhanke valuuta vaikimisi hankija arve valuutana. Hankija arvel, mis ei viita allhankele, sisestatakse vaikeväärtus hankija kontokirjest ja seda saab muuta. Pärast hankija arve salvestamist ei saa valuutat enam redigeerida. |
| Lepingut sõlmiv üksus | Teenuste ja/või toodete müüjalt vastuvõtmise eest vastutava ettevõtte jagunemine. | Pole |
| Maksetingimused | Väljastatud hankija arvete maksetingimused. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Alltöövõtu maksetingimused kopeeritakse kõigile allhankega seotud hankija arvetele. Maksetingimusi saab uuendada, kui hankija arve olek **on Mustand**. |
| Makse aadress | Hankija aadress, kellele maksed tuleb saata. Vaikeväärtus sisestatakse hankija konto kirjelt automaatselt. | Allhanke makseaadress kopeeritakse makseaadressina kõigile selle allhanke jaoks loodud hankija arvetele. Makseaadressi saab uuendada, kui hankija arve olek **on Mustand**. |
| Vahesumma | Kui hankija arvel pole ridu, sisestage enne makse arve vahesumma. Kui hankija arvel on read, loetakse seda välja ainult. Sellisel juhul on kuvatavaks summaks vahesumma hankija arve kõigilt ridadelt. | Pole |
| Kogumaks | Kui hankija arvel pole ridu, sisestage allhankelepingule maksud kokku. Kui hankija arvel on read, loetakse seda välja ainult. Sellisel juhul on kuvatavaks summaks maksusummade summa hankija arve kõigilt ridadelt. | Pole |
| Kogusumma | Sellel arvutatud väljal kuvatakse hankija arve kogusumma pärast maksude kaasamist. | Pole |

> [!NOTE]
> Hankija arve järgmisi välju ei saa pärast hankija arve salvestamist muuta: **Hankija, Alltöövõtt**, **Valuuta** **,** Lepinguühik **ja** Maksetingimused **·**. Kui hankija arvel on nendele väljadele vaja muudatusi, peate hankija arve kustutama ja looma uue hankija arve.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
