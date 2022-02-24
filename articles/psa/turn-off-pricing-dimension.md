---
title: Hinnakujunduse dimensiooni väljalülitamine
description: Selles teemas kirjeldatakse, kuidas Project Service’i lahenduses seadistada hinnakujunduse dimensioone.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147288"
---
# <a name="turn-off-a-pricing-dimension"></a>Hinnakujunduse dimensiooni väljalülitamine

[!include [banner](../includes/psa-now-project-operations.md)]

Võimalik, et peate iga paari aasta tagant oma hinnakujunduse strateegia üle vaatama ja seda värskendama. Teie tehtud värskendused võivad nõuda olemasoleva hinnakujunduse dimensiooni väljalülitamist ja uue loomist. Näiteks võib juhtuda, et olete varem määranud hinna **Rolli** järgi, kuid nüüd olete otsustanud määrata hinna **Töökogemuse** järgi. Võib juhtuda, et peate selleks **Rolli** hinnakujunduse dimensioonina välja lülitama ja looma **Töökogemuse** uue hinnakujunduse dimensioonina. 

Hinnakujunduse dimensiooni saab välja lülitada (olenemata sellest, kas see on valmis või kohandatud), kui seate hinnakujunduse dimensiooni väljade **Kehtib kulu kohta** ja **Kehtib müügi kohta** väärtuseks **Ei**.

Seda tehes võidakse teile aga kuvada järgmine tõrketeade.

![Äriprotsessi tõrge tõenäoliselt hinnakujunduse dimensiooni väljalülitamisest](media/Business-Process-Error.png)


See tõrketeade näitab, et on olemas hinnakirjed, mis on väljalülitatava dimensiooni jaoks juba varem seadistatud. Enne kui dimensiooni kohaldatavust saab seada väärtusele **Ei**, tuleb kustutada kõik dimensioonile viitavad **Rolli hinna** ja **Rolli hinna hinnalisandi** kirjed. See reegel kehtib nii valmishinnakujunduse dimensioonide kui ka kõigile teie loodud kohandatud hinnakujunduse dimensioonidele. Selle valideerimise põhjuseks on asjaolu, et Project Service’il on piirang, mille järgi iga **Rolli hinna** kirjel peab olema kordumatu dimensioonide kombinatsioon. Näiteks hinnakirjas **US Cost Rates 2018** (USA 2018. aasta kulumäärad) on teil olemas järgmised **Rolli hinna** read. 

| Standardpealkiri         | Organisatsiooniüksus    |Ühik   |Hind  |Valuuta  |
| -----------------------|-------------|-------|-------|----------|
| Süsteemiinsener|Jõgi US|Hour| 100|USD|
| Süsteemi vaneminsener|Jõgi US|Hour| 150| USD|


Kui lülitate **Standardpealkirja** hinnakujunduse dimensioonina välja ja Project Service’i mootor otsib hinda, kasutab see ainult **Org. üksuse** väärtust sisendi kontekstist. Kui sisendi konteksti **Org. üksus** on „Jõgi US”, on tulemus mittedeterministlik, sest mõlemad read on ühesugused. Selle stsenaariumi vältimiseks kontrollib Project Service, et **Rolli hinna** kirjete loomisel oleks dimensioonide kombinatsioon kordumatu. Kui dimensioon lülitatakse pärast **Rolli hinna** kirjete loomist välja, saab seda piirangut rikkuda. Seetõttu on nõutav, et enne dimensiooni väljalülitamist kustutaksite te ära kõik need **Rolli hinna** ja **Rolli hinna hinnalisandi** read, millel on dimensiooni väärtus täidetud.

