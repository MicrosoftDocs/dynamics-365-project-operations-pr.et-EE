---
title: Projektipõhiste müügivõimaluste kopeerimine
description: Selles teemas antakse teavet rakenduses Project Operations projektipõhiste müügivõimaluste kopeerimise kohta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074895"
---
# <a name="copy-project-based-opportunities"></a>Projektipõhiste müügivõimaluste kopeerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_


Projekti müügivõimalusi saab hõlpsasti kopeerida, et luua uusi projekti müügivõimalusi. 

1. Minge loendi lehele **Projekti müügivõimalused** ja valige loendist müügivõimalus. Või avage konkreetse müügivõimaluse üksikasjade leht. 
2. Valige lehelt **Kopeeri**. Avaneb dialoogileht, mis sisaldab järgmist välja teavet. Sõltuvalt selles dialoogis valitud väärtustest võib koopia protsess muutuda.

    | **Väli** | **Asjakohasus, eesmärk ja juhised** | **Allavoolu mõjud** |
    | --- | --- | --- |
    | Teema | Sisestage siht-müügivõimaluse vastav teema. Kui dialoog avaneb, määrab süsteem selle lähtemüügivõimaluse teemaks koos sellele lisatud suvandiga **koopia**. | Sellel väljal puudub allavoolu mõju. |
    | Ettevõte | Viide kliendi ettevõttele või konto kirjele. Kui dialoog avaneb, määrab süsteem selle lähtemüügivõimaluse kontole. | See väli on müügivõimaluse peamine klient. |
    | Lepingut sõlmiv üksus | Organisatsiooniüksus, mis vastutab selle tehinguga seotud projektide kättetoimetamise eest. Kui dialoog avaneb, määrab süsteem selle lähtemüügivõimaluse lepinguüksusele. | Lepinguüksus on ettevõtte allüksus, kes pärast tehingu sulgemist projektid teostab. Igal lepingut sõlmival üksusel on valuuta ja seda valuutat kasutatakse prognoositavate ja tegelike projekti käigus tekkinud kulude aruandluseks. |
    | Valuuta | Valuuta, milles tehing edastatakse. Kui dialoogileht avaneb, määrab süsteem selle lähtemüügivõimaluse valuutale. | Valuutat kasutatakse hinnakirja vaikimisi seadmiseks ja hinnapakkumis finantshinnangute koostamiseks. Lõpuks kasutatakse valuutat kliendile arve esitamisel lepingu võitmisel. |
    | Hinnakujunduse kopeerimine | Jah/ei väärtus, mis näitab, kas müügivõimaluse hinnakiri tuleks kopeerida lähtemüügivõimalusest. | Kui valite suvandi **Jah** , kopeeritakse hinnakirjad lähtemüügivõimalusest sihtmüügivõimalusele. Kui valite suvandi **Ei** , määratakse hinnakirjad uuesti vaikeväärtustele uusimate hinnakirjade põhjal. |

3. Valige **OK**. Süsteem loob valitud parameetrite põhjal projekti müügivõimaluse koopia ja avatakse uus projekti müügivõimalus.
