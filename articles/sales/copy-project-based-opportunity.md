---
title: Projektipõhiste müügivõimaluste kopeerimine
description: Selles artiklis antakse teavet projektipõhiste võimaluste kopeerimise kohta Project Operationsis.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926127"
---
# <a name="copy-project-based-opportunities"></a>Projektipõhiste müügivõimaluste kopeerimine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Projekti müügivõimalusi saab hõlpsasti kopeerida, et luua uusi projekti müügivõimalusi. 

1. Minge loendi lehele **Projekti müügivõimalused** ja valige loendist müügivõimalus. Või avage konkreetse müügivõimaluse üksikasjade leht. 
2. Valige lehelt **Kopeeri**. Avaneb dialoogileht, mis sisaldab järgmist välja teavet. Sõltuvalt selles dialoogis valitud väärtustest võib koopia protsess muutuda.

    | **Väli** | **Kirjeldus** | **Allavoolu mõjud** |
    | --- | --- | --- |
    | Teema | Sisestage siht-müügivõimaluse vastav teema. Kui dialoog avaneb, määrab süsteem selle lähtemüügivõimaluse teemaks koos sellele lisatud suvandiga **koopia**. | Sellel väljal puudub allavoolu mõju. |
    | Ettevõte | Viide kliendi ettevõttele või konto kirjele. Kui dialoog avaneb, määrab süsteem selle lähtemüügivõimaluse kontole. | See väli on müügivõimaluse peamine klient. |
    | Lepingut sõlmiv üksus | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projektide kättetoimetamise eest. Kui dialoog avaneb, määrab süsteem selle lähtemüügivõimaluse lepinguüksusele. | Lepinguüksus on ettevõtte allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepingut sõlmival üksusel on valuuta ja seda valuutat kasutatakse prognoositavate ja tegelike projekti käigus tekkinud kulude aruandluseks. |
    | Valuuta | Valuuta, milles tehing edastatakse. Kui dialoogileht avaneb, määrab süsteem selle lähtemüügivõimaluse valuutale. | Valuutat kasutatakse hinnakirja vaikimisi seadmiseks ja hinnapakkumis finantshinnangute koostamiseks. Lõpuks kasutatakse valuutat kliendile arve esitamisel lepingu võitmisel. |
    | Hinnakujunduse kopeerimine | Jah/ei väärtus, mis näitab, kas müügivõimaluse hinnakiri tuleks kopeerida lähtemüügivõimalusest. | Kui valite suvandi **Jah**, kopeeritakse hinnakirjad lähtemüügivõimalusest sihtmüügivõimalusele. Kui valite suvandi **Ei**, määratakse hinnakirjad uuesti vaikeväärtustele uusimate hinnakirjade põhjal. |

3. Valige **OK**. Süsteem loob valitud parameetrite põhjal projekti müügivõimaluse koopia ja avatakse uus projekti müügivõimalus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]