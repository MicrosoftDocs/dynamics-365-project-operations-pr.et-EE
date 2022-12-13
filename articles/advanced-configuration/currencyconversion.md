---
title: Seadistage valuuta konversioon müügihindade arvutamiseks kulumäärade alusel
description: Selles artiklis selgitatakse, kuidas konfigureerida valuuta konverteerimise käitumist, mida kasutatakse Microsoftis Dynamics 365 Project Operations , kui kulukannetest luuakse müügikanded.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816688"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Seadistage valuuta konversioon müügihindade arvutamiseks kulumäärade alusel

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Microsoftis Dynamics 365 Project Operations saab kulukategooriate müügihinnad seadistada arvväärtustena või seadistada nii, et need arvutatakse tekkinud kulu põhjal.

Kui need on seadistatud arvutama kantud kulu põhjal, on saadaval järgmised suvandid.

- Omahinnaga
- Protsendi märkimine üle kulu

Stsenaariumides, kus kulukulu tehakse valuutas, mis erineb projektilepingu müügivaluutast, on kulu põhjal müügihinna arvutamiseks vajalik valuuta konverteerimine.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Valuuta konverteerimise käitumine, mis kasutab kohalikke Dataverse vahetuskursse

Vaikimisi kasutab Project Operations valuutakursse, mis on talletatud tabelis Valuuta Dataverse. Project Operationsi konfigureerimiseks nii, et see kasutaks omavahelisi vahetuskursse müügihindade arvutamiseks kulu alusel, tehke järgmist.

1. Avage jaotis **Project Operationsi \> sätete parameetrid \>**.
1.  **Avage leht Projekti parameetri** üksikasjad.
1. Seadke **loogikaväli** Valuuta teisendamine tühjaks väärtuseks.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valuutakonversioonikäitumine, mis kasutab finance and operationsi rakenduste vahetuskursse

Valuutatabelis olevad vahetuskursid, mis on algselt saadaval Dataverse , ei ole jõustumiskuupäevaga. Seetõttu ei pruugi need alati olla skaleeritud nõuetega, mis teil on müügihindade arvutamiseks kulumäärade alusel.

Saate kasutada rahanduse ja toimingute keskkonna vahetuskursse, et arvutada müügihind müügivaluutas kuluvaluuta kulukursist. Selle valuutakonversioonikäitumise konfigureerimiseks toimige järgmiselt.

1. Lisage **lehel** Projekti parameetrid **väli Valuuta teisendamise loogika** . Seejärel salvestage ja avaldage kohandus.
1. Avage jaotis **Project Operationsi \> sätete parameetrid \>**.
1.  **Avage leht Projekti parameetri** üksikasjad. 
1. Määrake **välja Valuuta konverteerimise käitumine** väärtuseks **Laiendatud koos varuvariandiga vaikimisi**.
1. Andke **topeltkirjutamisrakenduse kasutajale**  turberoll **Üldine lugemisõigus** järgmistele tabelitele.

    - MSDYNi\_ valuutavahetuskursid
    - MSDYNi\_ valuutavahetuskursid
    - MSDYNi\_ vahetuskursi tüübid

1. Käivitage oma finance and operationsi keskkonnas järgmised kahekordse kirjutamisega kaardid koos esialgse sünkroonimisega.

    - Vahetuskursi tüüp (vahetuskursi\_ tüübid)
    - Vahetuskursi valuutapaar (msdyn\_ currencyexchangeratepairs)
    - CDS-i vahetuskursid (msdyn\_ valuutavahetuskursid)

Kui need muudatused on lõpule viidud, teeb dual-write finants- ja operatsioonikeskkonna vahetuskursid kättesaadavaks Dataverse. Project Operations kasutab seejärel neid vahetuskursse kulukursside konverteerimiseks lepingu müügivaluutasse.

> [!NOTE]
> See valuuta konverteerimise käitumine rakendub ainult müügihindade arvutamisel omahinna määrade alusel. Seda ei kasutata baasvaluuta väärtuste üldiseks arvutamiseks. Baasvaluuta väärtused kasutavad alati kohalikke Dataverse vahetuskursse, olenemata sellest, kas olete selle protseduuri lõpule viinud.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
