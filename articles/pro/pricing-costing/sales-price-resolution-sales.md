---
title: Projekti prognooside ja tegelike näitajate müügihinna lahendamine
description: Selles artiklis antakse teavet projekti hinnangute ja tegelike müügihindade lahendamise kohta.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9a6a19a866ab3218f2a0fa297b5f6a00ed809d2f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917479"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Projekti prognooside ja tegelike näitajate müügihinna lahendamine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Kui hinnangulised ja tegelikud müügihinnad lahendatakse rakenduses Dynamics 365 Project Operations, kasutab süsteem esmalt seotud projekti hinnapakkumise või lepingu kuupäeva ja valuutat. Pärast müügi hinnakirja lahendamist lahendab süsteem müügi või arvelduskulu.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Aja tegelike ja prognoositavate ridade kulumäärade lahendamine

Project Operationsis kasutatakse aja prognoositud ridu hinnapakkumise rea ja lepingurea üksikasjade näitamiseks projekti aja- ja ressursi määramiste jaoks.

Pärast müügi hinnakirja lahendamist täidab süsteem järgmised etapid vaikimisi arveldusmäära saamiseks.

1. Süsteem kasutab aja prognoosi real välju **Roll** ja **Ressursi üksus** lahendatud hinnakirjas rolli hinna ridadega vastendamiseks. See vastendamine eeldab, et kasutate arveldusmäärade jaoks valmiskujul hinnakujunduse dimensioone. Kui olete hinna konfigureerinud selle asemel mistahes muu välja põhjal, või lisaks väljadele **Roll** ja **Ressursi ühik**, kasutatakse vastava rolli hinna rea toomiseks seda kombinatsiooni.
2. Kui süsteem leiab rolli hinna rea, millel on väljade **Roll** ja **Ressursi ühik** kombinatsiooni arvelduskulu, kasutatakse vaikimisi seda arvelduskulu.
3. Kui rakendus ei saa vastendada väljade **Roll** ja **Ressursi ühik** väärtusi, toob see välja rolli hinna read, millel on vastav roll, kuid välja **Ressursi ühik** väärtus on tühi. Pärast seda, kui süsteem leiab vastava rolli hinna kirje, määratakse arveldusmäära vaikeväärtus sellest kirjest. See vastendus eeldab valmiskujul konfiguratsiooni **Rolli** vs **Ressursiühiku** suhtelise prioriteedi jaoks müügi hinnakujunduse dimensioonina.

> [!NOTE]
> Kui konfigureerite väljadele **Roll** ja **Ressursi ühik** erineva tähtsuse või kui teil on muid kõrgema prioriteediga dimensioone, muutub käitumine vastavalt. Süsteem toob rollihinna kirjed väärtustega, mis vastavad igale hinnadimensiooni väärtusele tähtsuse järjekorras ridadega, mille dimensioonide jaoks on viimasena tühiväärtused.

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
    | &nbsp; | Juurdehindlus üle omahinna | Rakendage seotud tegeliku kulu ühiku kulumäärale kategooria hinnarea määratud hinnalisand |

4. Kui süsteem ei suuda vastendada väljade **Kategooria** ja **Ühik** väärtusi, on müügihinna vaikeväärtuseks null (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Materjali tegelike ja prognoosiridade müügihindade lahendamine

Rakenduses Project Operations kasutatakse materjalide prognoosiridu, et märkida projekti materjalide ja materjalide prognoosiridade hinnapakkumise rea ja lepingurea üksikasju.

Pärast müügi hinnakirja lahendamist täidab süsteem järgmised etapid vaikimisi ühiku müügihinna saamiseks.

1. Süsteem kasutab prognoosireal materjali väljade **Toode** ja **Ühik** kombinatsiooni, et vastendada need lahendatud hinnakirja hinnakirjaüksuse ridadega.
2. Kui süsteem leiab hinnakirjaüksuse rea, mille väljade **Toode** ja **Ühik** kombinatsiooni jaoks on müügihind ning hinnakujundusmeetodiks on **Valuuta summa**, kasutatakse hinnakirjareal määratud müügihinna.
3. Kui väljade **Toode** ja **Ühik** väärtused ei ühti, on müügimäära väärtuseks null.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
