---
title: Projekti müügivõimaluste päise üksikasjad
description: See artikkel annab teavet projektipõhiste tehingute ja projektipõhiste müügivõimaluste ridade kohta.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec332e2fb97436d7ec3d31b75ee2383edcb5c7e4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824574"
---
# <a name="header-details-for-project-opportunities"></a>Projekti müügivõimaluste päise üksikasjad

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Müügivõimaluse päis hõivab üldteavet projektipõhise tehingu kohta, mis rakendub kõigile projektipõhise müügivõimaluste ridadele.

Projektipõhised müügivõimalused rakenduses Dynamics 365 Project Operations on laiendused rakenduse Dynamics 365 Sales müügivõimalustele. Need laiendused pakuvad täiendavaid funktsioone, mis on projektipõhistele müügivõimalustele omased ja vajalikud. Need laiendused võivad sisaldada uusi välju ja linditoiminguid, mis on saadaval projektipõhistes müügivõimalustes. Võimalik, et teatud väljad, funktsioonid ja vaikeloogika, mis on saadaval Salesis, pole Project Operationsis saadaval.

Järgmises tabelis on toodud projektipõhise müügivõimaluse väljad, mis on kas Project Operationsi jaoks ainulaadsed või milles on teatud olulised käitumise muudatused võrreldes Salesi müügivõimalustega.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Tüüp | Vahekaart Üldine (peidetud) | Sellel suvandikomplekti väljal on järgmised suvandid.</br>- Tööpõhine (saadaval ainult koos Project Operationsiga)</br>- Kaubapõhine (saadaval ainult juhul, kui Project Operations ja Sales on installitud)</br>- Hoolduspõhine teenindus (saadaval juhul, kui Field Service on installitud) | Kui kasutate rakendust Project Operations, seatakse selle välja väärtuseks automaatselt **Tööpõhine**, mistõttu klassifitseerub müügivõimalus projektipõhisena. Müügivõimalus peaks olema projektipõhine, et lubada kõik projektiga seotud laiendused ja funktsioonid selle tehingu allavoolu müügiprotsesside jaoks. |
| Kontakt | Vahekaart Üldine | Viide kliendi esmasele kontaktile selle tehingu korral. | |
| Ettevõte | Vahekaart Üldine | Viide kliendi ettevõttele või konto kirjele. | |
| Kontohaldur | Vahekaart Üldine | Selle projektipõhise müügivõimaluse kontohalduri nimi. | Kontohaldur vastutab kuni selle projekti lõpuleviimiseni kliendisuhete haldamise eest. Vastavalt kontohalduriga seotud broneeritud ressursi kirjele on lepingut sõlmiv üksus vaikeväärtusega. |
| Lepingut sõlmiv üksus | Vahekaart Üldine | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projekti või projektide kättetoimetamise eest. | Lepingut sõlmiv üksus on ettevõtte see allüksus, kes pärast tehingu sulgemist projekti(d) teostab. Igal lepingut sõlmival üksusel on valuuta ja seda valuutat kasutatakse prognoositavate ja tegelike projekti käigus tekkinud kulude aruandluseks. |

Kõigi muude väljade ja jaotiste kohta müügivaõimaluse vahekaardil **Kokkuvõte** leiate infot teemast [Müügivõimaluste loomine või muutmine (müüks ja müügikeskus)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
