---
title: Projektilepingute kopeerimine – liht
description: Selles artiklis antakse teavet projektilepingute kopeerimise kohta Project Operationsis.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a1846af677f7cea3ec22fdba4408f2bbd7db8a3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932613"
---
# <a name="copy-project-contracts---lite"></a>Projektilepingute kopeerimine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Saate hõlpsasti luua uusi projekti lepinguid, tehes olemasolevatest lepingutest koopiad ühel järgmisest kahest viisist. 

  - Valige loendi lehel **Projekti lepingud** projekti leping ja seejärel valige **Kopeeri**.
  - Valige üksikasjade lehel **Projekti lepingu** suvand **Kopeeri**.

Avaneb dialoogileht, kus saate valida kopeeritud lepingu parameetrid. Dialoogis on järgmised väljad. Sõltuvalt selles dialoogis valitud väärtustest võib koopia protsess muutuda.

| **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
| --- | --- | --- |
| Teema | Sisestage eesmärklepingu teema. Kui dialoogileht avaneb, määrab süsteem selle välja algse lepingu nimeks koos sellele lisatud **koopiaga**. | Sellel väljal puudub allavoolu mõju. |
| Klient | Viide kliendi ettevõttele või konto kirjele. Kui dialoog avaneb, määrab süsteem selle välja algse lepingu kontole. | See väli on lepingu peamine klient. |
| Lepingut sõlmiv üksus | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projekti(de) kättetoimetamise eest. Kui dialoogileht avaneb, määrab süsteem selle algse lepingu lepinguüksusele. | Lepingut sõlmiv üksus on ettevõtte see allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepinguüksusel on valuuta. Seda valuutat kasutatakse prognoositavate ja tegelike projekti täitmise käigus tekkinud kulude aruandluseks. |
| Valuuta | Valuuta, milles tehing edastatakse. Kui dialoogileht avaneb, määrab süsteem selle välja algse lepingu valuutale. Valuutat saab muuta. Kui seda tehakse, siis on väli **Hinnakujunduse kopeerimine** alati seatud väärtusele **Ei**, kuna algse lepingu hinnakirjad pole enam asjakohased. | Valuutat kasutatakse hinnakirjade vaikeväärtuseks, et koostada lepingu kohta finantskalkulatsioone ning arveldada kliendiga, kui tehing on võidetud. |
| Soovitud tarnekuupäev | Kliendi soovitud tarnekuupäev. | Seda kuupäeva kasutatakse konkreetse sagedusega arvelduse kuupäevadega koos lõpukuupäevana. |
| Hinnakujunduse kopeerimine | Näitab, kas lepingu hind tuleks algsest lepingust kopeerida. | Kui välja väärtuseks on seatud **Jah**, kopeeritakse projekti ja toote hinnakirja viiteid algsest lepingust eesmärklepingusse. Kui valisite **Ei**, määratakse hinnakirjad vaikeväärtustele uusimate hinnakirjade põhjal, mis on konto või projekti parameetrites. |

Kui valite dialoogilehel **OK**, loob süsteem valitud parameetrite põhjal lepingu koopia. Avaneb uus leping.

Väärtusest **Algne leping** ei kopeerita väärtusesse **Eesmärkleping** järgmist teavet.

  - Arve ajakavad
  - Lepingu ja lepingurea kliendid
  - Projektiviide projektipõhistel lepinguridadel
  - Kliendi eelarve teave

Kuna see teave on iga lepingu jaoks spetsiifiline, siis neid välju ja kirjeid ei kopeerita. Lepingu tasemel kopeeritakse projektide ja toodete lepinguread, lepingurea üksikasjade prognoosid ja mitte ületatavad väärtused. Hindade ja kulumäära vaikeväärtused sõltuvad valikust väljal **Hinnakujunduse kopeerimine**, mis on valikud dialoogilehel **Parameetrite kopeerimine**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]