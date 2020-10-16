---
title: Müügivõimaluse päis/kokkuvõte
description: Selles teemas antakse teavet projektipõhiste tehingute ja projektipõhiste müügivõimaluste ridade kohta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908049"
---
# <a name="opportunity-headersummary"></a>Müügivõimaluse päis/kokkuvõte

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Müügivõimaluse päis või kokkuvõte hõivab üldteavet projektipõhise tehingu kohta, mis rakendub kõigile projektipõhise müügivõimaluste ridadele.

Dynamics 365 Project Operationsi projektipõhised müügivõimalused on Dynamics 365 Salesi müügivõimaluste laiendused. Need laiendused pakuvad täiendavaid funktsioone, mis on projektipõhistele müügivõimalustele omased ja vajalikud. Need laiendused võivad sisaldada uusi välju ja linditoiminguid, mis on saadaval projektipõhistes müügivõimalustes. Võimalik, et teatud väljad, funktsioonid ja vaikeloogika, mis on saadaval Salesis, pole Project Operationsis saadaval.

Järgmises tabelis on toodud projektipõhise müügivõimaluse väljad, mis on kas Project Operationsi jaoks ainulaadsed või milles on teatud olulised käitumise muudatused võrreldes Salesi müügivõimalustega.

| **Väli** | **Asukoht** | **Asjakohasus, eesmärk ja juhised** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Tüüp | Vahekaart Üldine (peidetud) | Sellel suvandikomplekti väljal on järgmised suvandid.</br>- Tööpõhine (saadaval ainult koos Project Operationsiga)</br>- Kaubapõhine (saadaval ainult juhul, kui Project Operations ja Sales on installitud)</br>- Hoolduspõhine teenindus (saadaval juhul, kui Field Service on installitud) | Kui kasutate rakendust Project Operations, seatakse selle välja väärtuseks automaatselt **Tööpõhine**, mistõttu klassifitseerub müügivõimalus projektipõhisena. Müügivõimalus peaks olema projektipõhine, et lubada kõik projektiga seotud laiendused ja funktsioonid selle tehingu allavoolu müügiprotsesside jaoks. |
| Omanikust ettevõte | Vahekaart Üldine | See on ettevõte või juriidiline isik, kes toimetab projekti kliendile. | Selle välja teave kopeeritakse selle müügivõimaluse põhjal loodud projekti hinnapakkumise vastavale väljale. |
| Kontakt | Vahekaart Üldine | Viide kliendi esmasele kontaktile selle tehingu korral. | |
| Ettevõte | Vahekaart Üldine | Viide kliendi ettevõttele või konto kirjele. | |
| Kontohaldur | Vahekaart Üldine | Selle projektipõhise müügivõimaluse kontohalduri nimi. | Kontohaldur vastutab kuni selle projekti lõpuleviimiseni kliendisuhete haldamise eest. Vastavalt kontohalduriga seotud broneeritud ressursi kirjele on lepingut sõlmiv üksus vaikeväärtusega. |
| Lepingut sõlmiv üksus | Vahekaart Üldine | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projekti või projektide kättetoimetamise eest. | Lepingut sõlmiv üksus on ettevõtte see allüksus, kes pärast tehingu sulgemist projekti(d) teostab. Igal lepingut sõlmival üksusel on valuuta ja seda valuutat kasutatakse prognoositavate ja tegelike projekti käigus tekkinud kulude aruandluseks. |

Kõigi muude väljade ja jaotiste kohta müügivõimaluse vahekaardil **Kokkuvõte** leiate infot teemast [Müügivõimaluste loomine või muutmine (müüks ja müügikeskus)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
