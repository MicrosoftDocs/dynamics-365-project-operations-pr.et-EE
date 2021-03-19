---
title: Projektipõhiste müügivõimaluste kopeerimine
description: Selles teemas antakse teavet rakenduses Project Operations projektipõhiste müügivõimaluste kopeerimise kohta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1808469a34e05eb926f13c62ec634e8273b0e33c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278548"
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