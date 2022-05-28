---
title: Meetodite lõpetamise kulu
description: Selles teemas kirjeldatakse projekti lõpetamise kulu arvutamiseks kasutatud meetodeid.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 244afa919e5fbc16be8f905acce2e2354c7da974
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601657"
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