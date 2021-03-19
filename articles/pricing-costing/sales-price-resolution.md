---
title: Prognooside ja tegelike näitajate müügihindade lahendamine
description: Selles teemas antakse teavet prognooside ja tegelike näitajate müügihindade lahendamise kohta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e89e23189fa65057d7b955897924057c440ccd8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274948"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Prognooside ja tegelike näitajate müügihindade lahendamine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Kui hinnangulised ja tegelikud müügihinnad lahendatakse rakenduses Dynamics 365 Project Operations, kasutab süsteem esmalt seotud projekti hinnapakkumise või lepingu kuupäeva ja valuutat. Pärast müügi hinnakirja lahendamist lahendab süsteem müügi või arvelduskulu.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Aja tegelike ja prognoositavate ridade kulumäärade lahendamine

Project Operationsis kasutatakse aja prognoositud ridu hinnapakkumise rea ja lepingurea üksikasjade näitamiseks projekti aja- ja ressursi määramiste jaoks.

Pärast müügi hinnakirja lahendamist täidab süsteem järgmised etapid vaikimisi arveldusmäära saamiseks.

1. Süsteem kasutab aja prognoosi real välju **Roll**, **Ressursiettevõte** ja **Ressursi üksus**, lahendatud hinnakirjas rolli hinna ridadega vastendamiseks. See vastendamine eeldab, et kasutate arveldusmäärade jaoks valmiskujul hinnakujunduse dimensioone. Kui olete hinna konfigureerinud selle asemel mistahes muu välja põhjal, või lisaks väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik**, kasutatakse vastava rolli hinna rea toomiseks seda kombinatsiooni.
2. Kui süsteem leiab rolli hinna rea, millel on väljade **Roll**, **Ressursiettevõte** ja **Ressursi ühik** kombinatsiooni arvelduskulu, kasutatakse vaikimisi seda arvelduskulu.
3. Kui rakendus ei saa vastendada väljade **Roll**, **Ressursiettevõte** ja **Ressursi ühik** väärtusi, toob see välja rolli hinna read, millel on vastav roll, kuid välja **Ressursi ühik** väärtus on tühi. Pärast seda, kui süsteem leiab vastava rolli hinna kirje, määratakse arveldusmäära vaikeväärtus sellest kirjest. See vastendus eeldab valmiskujul konfiguratsiooni **Rolli** vs **Ressursiühiku** suhtelise prioriteedi jaoks müügi hinnakujunduse dimensioonina.

> [!NOTE]
> Kui konfigureerite väljadele **Roll**, **Ressursiettevõte** ja **Ressursi ühik** erineva tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub käitumine vastavalt. Süsteem toob rollihinna kirjed väärtustega, mis vastavad igale hinnadimensiooni väärtusele tähtsuse järjekorras ridadega, mille dimensioonide jaoks on viimasena tühiväärtused.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Kulu tegelike ja prognoositavate ridade müügihindade lahendamine

Project Operationsis kasutatakse kulu prognoositud ridu hinnapakkumise rea ja lepingurea üksikasjade näitamiseks projekti kulude ja kuluprognoosi ridade jaoks.

Pärast müügi hinnakirja lahendamist täidab süsteem järgmised etapid vaikimisi ühiku müügihinna saamiseks.

1. Süsteem kasutab prognoositaval real väljade **Kategooria** ja **Üksus** kombinatsiooni, et kulu vastaks lahendatud hinnakirjas kategooria hinna ridadele.
2. Kui süsteem leiab kategooria hinna rea, millel on väljade **Kategooria** ja **Ühik** müügihinna kombinatsioon, on müügihind vaikeväärtuseks.
3. Kui süsteem leiab vastava kategooria hinna rea, võidakse müügihinna vaikeväärtusena kasutada seda hinnakujundusmeetodit. Järgmises tabelis on kuvatud kulu hinna vaikeväärtuse käitumine Project Operationsis.

    | Kontekst | Hinnakujundusmeetod | Vaikehind |
    | --- | --- | --- |
    | Hinnang | Ühiku hind | Vastavalt kategooria hinnareale |
    | &nbsp; | Omahinnaga | 0.00 |
    | &nbsp; | Juurdehindlus üle omahinna | 0.00 |
    | Tegelik | Ühiku hind | Vastavalt kategooria hinnareale |
    | &nbsp; | Omahinnaga | Vastavalt seotud tegelikule kulule |
    | &nbsp; | Juurdehindlus üle omahinna | Rakendades seotud tegeliku kulu ühiku kulumäärale kategooria hinnarea määratud hinnalisandi |

4. Kui süsteem ei suuda vastendada väljade **Kategooria** ja **Ühik** väärtusi, on müügihinna vaikeväärtuseks null (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]