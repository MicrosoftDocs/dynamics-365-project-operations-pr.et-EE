---
title: Meetodite lõpetamise kulu
description: Selles teemas kirjeldatakse projekti lõpetamise kulu arvutamiseks kasutatud meetodeid.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279043"
---
# <a name="cost-to-complete-methods"></a>Meetodite lõpetamise kulu

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Selles teemas kirjeldatakse projekti lõpetamise kulu arvutamiseks kasutatud meetodeid. Projekti lõpetamise kulu arvutamiseks saate kasutada mitut viisi. 

Kui loote projekti jaoks prognoosi lehe **Loo prognoos** väljal **Meetodi lõpetamise kulu**, saate valida ühe järgmistest kuludest, et meetodid lõpetada.

| Meetodi lõpetamise kulu    | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kogukulu – tegelik            | Sisestage hinnangulised kulud käsitsi väljadel **Kogukulu** või **Kogus kokku**, kasutades selleks nuppu **Kuluprognoos** **prognoosi lehel**. Süsteem lahutab tegelikud kulud teie sisestatud kogusummast. Kogusumma on projekti lõpetamise kulu. See meetod ei kasuta Microsoft Dataverse’i lahendusse Project Operations sisse ehitatud kuluprognoose ja ressursside määramisi. Kogukulu või kogu kogust saab vajaduse korral käsitsi uuendada.  |
| Kogukulu prognoos – tegelik        | Ressursi määramisi ja kuluprognoose kasutatakse projekti kogukulu prognoosi määramiseks. Tegelikke kulusid võrreldakse selle prognoosiga, et arvutada lõpetamise kulu.                                                                                                                                                                                                                                                                          |
| Nagu eelmine prognoos         | Siin kasutatakse samu prognoosimeetodeid, mida kasutati eelmise perioodi jooksul. Selle meetodi jaoks on vaja eelarvemudelit, kui eelmine periood vajas eelarvemudelit.                                                                                                                                                                                                                                                                                                                           |
| Kulu seadmine nulli jäämiseks | Tavaliselt kasutatakse seda enne prognoositava projekti likvideerimist, see meetod vastendab prognooside kogusummad konteeritud tegelike kannetega ja kustutab veeru **Lõpetamise kulu**. Kui see on lõpetatud, on tulemuseks alati 100 protsenti. Iga loodava kulurea puhul on märkeruut **Prognoositav** tühjendatud ja kogu prognoos kopeeritakse eelmisest kuluprognoosist. Prognoositava perioodi tegelik tarbimine arvatakse projekti lõpuleviimiseks kulust maha.              |
| Kulumallist           | Meetodi lõpetamise kulu, mis on seadistatud valitud prognoosi projektiga seostatud kulumallis.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]