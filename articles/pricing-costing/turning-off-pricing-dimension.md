---
title: Hinnakujunduse dimensiooni väljalülitamine
description: Selles artiklis antakse teavet hinnakujundusdimensioonide väljalülitamise kohta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4a13074e20d3005873c28fb95b7443b6ffc84140
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924287"
---
# <a name="turning-off-a-pricing-dimension"></a>Hinnakujunduse dimensiooni väljalülitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Võimalik, et peate iga paari aasta tagant oma hinnakujunduse strateegia üle vaatama ja seda värskendama. Teie tehtud värskendused võivad nõuda olemasoleva hinnakujunduse dimensiooni väljalülitamist ja uue loomist. Näiteks võib juhtuda, et olete varem määranud hinna **Rolli** järgi, kuid nüüd olete otsustanud määrata hinna **Töökogemuse** järgi. Võib juhtuda, et peate selleks **Rolli** hinnakujunduse dimensioonina välja lülitama ja looma **Töökogemuse** uue hinnakujunduse dimensioonina. 

Hinnakujunduse dimensiooni saab välja lülitada (olenemata sellest, kas see on valmis või kohandatud), kui seate hinnakujunduse dimensiooni väljade **Kehtib kulu kohta** ja **Kehtib müügi kohta** väärtuseks **Ei**.

Kuid seda tehes võidakse kuvada tõrketeade, **Hinnakujunduse dimensiooni ei saa värskendada ega kustutada, kui seostuvad hinnakirjad on olemas.**

![Hinnakujunduse dimensiooni väljalülitamisel ilmneb tõenäoliselt äriprotsessi tõrge.](media/Business-Process-Error.png)

See tõrketeade näitab, et on olemas hinnakirjed, mis on väljalülitatava dimensiooni jaoks juba varem seadistatud. Enne kui dimensiooni kohaldatavust saab seada väärtusele **Ei**, tuleb kustutada kõik dimensioonile viitavad **Rolli hinna** ja **Rolli hinna hinnalisandi** kirjed. See reegel kehtib nii valmishinnakujunduse dimensioonide kui ka kõigile teie loodud kohandatud hinnakujunduse dimensioonidele. Selle valideerimise põhjuseks on asjaolu, et igal **Rolli hinna** kirjel peab olema kordumatu dimensioonide kombinatsioon. Näiteks hinnakirjas **US Cost Rates 2018** (USA 2018. aasta kulumäärad) on teil olemas järgmised **Rolli hinna** read. 

| Standardpealkiri         | Organisatsiooniüksus    |Ühik   |Hind  |Valuuta  |
| -----------------------|-------------|-------|-------|----------|
| Süsteemiinsener|Jõgi US|Hour| 100|USD|
| Süsteemi vaneminsener|Jõgi US|Hour| 150| USD|


Kui lülitate **Standardpealkirja** hinnakujunduse dimensioonina välja ja hinnakujunduse mootor otsib hinda, kasutab see ainult **Org. üksuse** väärtust sisendi kontekstist. Kui sisendi konteksti **Org. üksus** on „Jõgi US”, on tulemus mittedeterministlik, sest mõlemad read on ühesugused. Selle stsenaariumi vältimiseks kontrollib süsteem, et **Rolli hinna** kirjete loomisel oleks dimensioonide kombinatsioon kordumatu. Kui dimensioon lülitatakse pärast **Rolli hinna** kirjete loomist välja, saab seda piirangut rikkuda. Seetõttu on nõutav, et enne dimensiooni väljalülitamist kustutaksite te ära kõik need **Rolli hinna** ja **Rolli hinna hinnalisandi** read, millel on dimensiooni väärtus täidetud.


[!INCLUDE[footer-include](../includes/footer-banner.md)]