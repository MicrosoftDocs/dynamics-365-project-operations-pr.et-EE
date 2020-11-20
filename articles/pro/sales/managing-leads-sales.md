---
title: Hinnapakkumiste haldamine – liht
description: Selles teemas antakse teavet projektipõhiste müügivihjete halduse kohta (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 00fc16b0e723d4df88ceae961d9772e26dd1451e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180502"
---
# <a name="manage-leads---lite"></a>Hinnapakkumiste haldamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Projektil põhinevaid müügivihjeid saab hallata ja kvalifitseerida Project Operationsis. Müügivihjete haldamise protsess hõlmab tööpõhiste müügivihjete loomist ja nende müügivihjete kvalifitseerimist. 

## <a name="list-of-project-sales-leads"></a>Projekti müügivihjete loend

Avage jaotises **Müük** vasakpoolsel navigeerimispaanil **Müügivihjete** loendi leht, et kuvada kõigi süsteemi müügivihjete kirjete loendit. Kuvatud müügivihjete loend on tööpõhine ja sisaldab ka muud tüüpi müügivihjeid, mida saab luua, kui teil on ka rakendused Dynamics 365 Sales või Dynamics 365 Field Service.

Saate luua filtreeritud vaate, et näha ainult projektipõhiseid müügivihjeid, luues filtri väärtusele **Tüüp**. Näiteks saate valida, et kuvada ainult tööpõhised müügivihjed.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Projektipõhise tehingu jaoks uue müügivihje loomine

Kui projektipõhine müügivihje on kvalifitseeritud, luuakse müügivõimalus ja konto. Projektipõhine müügivõimalus on müügvõimaluse etapis müügi püüdmise tegevuste alguspunktiks. Projektipõhistel müügivõimalustel on ainulaadsed võimalused, mis on projektitöö müümiseks nõutavad. Nende võimaluste hulka kuuluvad järgmised.

- Aeg ja materjal ja fikseeritud hinnaga arveldusmeetodid
- Mitu kuupäeva kehtivad hinnakirjad projektiga seotud inimressursside, kulude ja materjali jaoks.

Kvalifitseeruva müügivihje poolt müügivõimaluse automaatseks loomiseks määrake müügivihjet luues atribuut **Tüüp** valikule **Tööl põhinev**. Kui valite mõne muu tüübi, ei loo müügivihje kvalifitseerimisel projektipõhist müügivõimalust. Kui projektipõhist müügivõimalust ei looda, ei ole projektipõhised võimalused allavoolu müügiprotsessides saadaval.

Järgmine tabel sisaldab müügivihje jaoks olulist väljateavet ja nende väljade allavoolu minevat mõju.

| **Väli** | **Asukoht** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- | --- |
| Teema | Vahekaart Üldine | See tekstiväli peaks sisaldama tehingu lühikirjeldust. | Müügivihje teema kuvatakse vaikimisi müügivõimaluse teemana ning hinnapakkumise ja projektilepingu nimena. |
| Tüüp | Vahekaart Üldine | Sellel suvandikomplekti väljal on järgmised suvandid.</br>- Tööpõhine (saadaval ainult juhul, kui Project Operations on installitud)</br>- Kaubapõhine (saadaval ainult juhul, kui Project Operations ja Sales on installitud)</br>- Hoolduspõhine teenindus (saadaval juhul, kui Field Service on installitud) | Kui müügivihjel on selle välja väärtuseks on seatud **Tööpõhine**, on müügivihje kvalifitseeritud projektipõhist müügivõimalust looma. Projektipõhine müügivõimalus on vajalik, et lubada kõik projektiga seotud laiendused ja funktsioonid selle tehingu allavoolu müügiprotsesside jaoks. |
| Eesnimi | Vahekaart Üldine | Potentsiaalse kliendi kontaktisiku eesnimi | Kui müügivihje on kvalifitseeritud, luuakse konto, kontaktisik ja müügivõimalus. Kontakti eesnimi on siin määratud väärtus. |
| Perekonnanimi | Vahekaart Üldine | Potentsiaalse kliendi kontaktisiku perekonnanimi | Kui müügivihje on kvalifitseeritud, luuakse konto, kontaktisik ja müügivõimalus. Kontakti perekonnanimi on siin määratud väärtus. |
| Ettevõte | Vahekaart Üldine | Potentsiaalse kliendi ettevõtte nimi | Kui müügivihje on kvalifitseeritud, luuakse konto, kontaktisik ja müügivõimalus. Loodud konto nimi on siin määratud väärtus. |
| Valuuta | Vahekaart Üksikasjad | Potentsiaalse kliendi valuuta | Kui müügivihje on kvalifitseeritud, luuakse konto, kontaktisik ja müügivõimalus. Loodud konto valuuta on siin määratud väärtus. |

## <a name="qualify-a-new-project-based-lead"></a>Uue projektipõhise müügivihje kvalifitseerimine

Müügivihjeid, mille väärtus **Tüüp** on seadistatud olekusse **Tööpõhine**, nimetatakse projektipõhisteks müügivihjeteks. Projektipõhise müügivihje kvalifitseerimisel luuakse järgnev.

- Konto, mis kasutab müügivihje välja **Ettevõte**.
- Kontoga seotud kontaktikirjet, mis põhineb müügivihje väljade **Eesnimi** ja **Perekonnanimi** väärtustel.
- Projektipõhine müügivõimalus, mille välja **Tüüp** väärtuseks on määratud **Tööpõhine**.

Täpsemat teavet müügivihjete kvalifitseerimise kohta leiate teemast [Müügivihjete kvalifitseerimine või teisendamine](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Projektipõhiste tehingute äriprotsessi voog

Project Operationsi projektipõhistes tehingutes toetatakse järgmisi äriprotsessi voogusid.

- Müügivihjest müügivõimaluseni äriprotsess
- Müügivõimaluse müügiprotsess

Müügivihjest müügivõimaluseni äriprotsess toetab järgmisi etappe.

| Etapi nimi | Vastendatud olem | Funktsionaalsus |
| --- | --- | --- |
| Sobivaks kinnitamine | Müügivihje | Konto, kontakti ja müügivõimaluse loomiseks müügivihje kvalifitseerimine. |
| Arendage | Müügivõimalus | Müügivõimaluse arendamine, et lisada lisateavet seotud töö, peamiste sidusrühmade ja konkurentide kohta. |
| Soovita | Müügivõimalus | Ettepaneku väljaarendamine ja sisemise läbivaatuse meeskonnalt heakskiidu saamine. |
| Saate dialoogiakna sulgeda | Müügivõimalus | Tehingu sulgemiseks müügivõimaluse võitmine. |
