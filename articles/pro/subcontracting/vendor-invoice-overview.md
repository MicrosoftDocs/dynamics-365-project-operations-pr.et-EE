---
title: Hankija arveldamine – mõiste ja loomine
description: See artikkel kirjeldab tarnija arvete, kasutusstsenaariumide ja tarnija arvete loomise stsenaariumeid rakenduses Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261929"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Hankija arveldamine – mõiste ja loomine

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Hankija arveldust rakenduses Microsoft Dynamics 365 Project Operations saab kasutada hankijate projekti teenuste ja/või materjalide tarnimise kulude registreerimiseks.

Kui teenuste ja/või materjalide allhankelepingud sõlmitakse hankijaga, kujutab allhankeleping selle hankijaga sõlmitud lepingut. Kui hankija osutab teenuseid või kui materjalid võetakse vastu ja kasutatakse projektiülesannete täitmiseks, kirjendatakse kulud projektis. Hankija saadab perioodiliselt arveid, mis on kontrollitud ja vastavusse viidud projektis registreeritud kuludega. Pärast kontrolliprotsessi lõppu kinnitatakse hankija arve ja see vabastatakse tasumiseks.

## <a name="scenarios-for-use"></a>Kasutamise stsenaariumid

Rakenduse Project Operations hankija arveid saab kasutada kahe erineva stsenaariumi toetamiseks.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kliendid kasutavad kõiki allhankekogemusi

Hankija arvekogemused võimaldavad kontrollida ja sobitada ajakirjeid, materjalikasutuse ja kulukirjeid, mis viitavad allhankelepingute sõlmitud komponentidele hankija arve ridadega. Seda protsessi saab kasutada hankija arve ridade täpsuse kontrollimiseks. Pärast kinnitamisprotsessi lõpetamist ja hankija arve kinnitamist tühistab rakendus kinnitatud aja-, kulu- ja materjalikasutuse logides registreeritud tegelikud näitajad ning loob hankija arve ridu kasutades uusi kuluarvete tegelikke näitajaid.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kliendid ei kasuta kõiki allhankekogemusi, kuid soovivad rakenduse Project Operations projektide kuludest ühtset ülevaadet

Kui jälgite allhankeprotsessi kolmanda osapoole süsteemis, saate registreerida selle kolmanda osapoole süsteemi kulud rakendusele Project Operations, luues hankija arveid, mis ei viita allhankelepingutele. Nii saavad teie projektijuhid omada ühte ja ühtset ülevaadet antud projekti kõigist kuludest.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Hankija arvete loomine rakenduses Project Operations

Hankija arvete loomiseks on kaks võimalust:

- Hankija arvete loendi lehelt või üksiku hankija arve üksikasjade lehelt
- Allhankelepingute loendi lehelt või üksiku allhankelepingu üksikasjade lehelt

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Loomine hankija arvete loendi lehelt või üksikasjade lehelt

1. Minge jaotisesse **Ostmine** \> **Hankija arved**.
2. Hankija arvete loendilehel või üksiku hankija arve üksikasjade lehel valige uue hankija arve loomiseks **Uus**.

Sel viisil koostatud hankija arved võivad viidata ka allhankelepingule.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Loomine allhankelepingute loendi lehelt või üksikasjade lehelt

1. Minge jaotisesse **Ostmine** \> **Allhanked**.
2. Valige üks või mitu allhankelepingut.
3. Hankija allhankelepingu loendilehel või üksiku allhankelepingu üksikasjade lehel valige loomiseks **Hankija arve loomine**.

Iga valitud allhankelepingu jaoks luuakse uus hankija arve olekuga **Mustand**.

Sel viisil loodud hankija arved viitavad hankija arve päises alati allhankelepingule. Iga allhankelepingu rida, millel on aja ja materjali arveldusmeetod, loob hankija arvele rea. Iga allhankelepingu rida, millel on fikseeritud hinnaga arveldusmeetod, loob hankija arvel rea iga allhankelepingurea vahekokkuvõtte jaoks, mille olek on **Arveldamiseks valmis**.

Järgmised väljad ja seotud kirjed kopeeritakse allhankelepingust hankija arve päisesse.

- Hankija.
- Seotud hinnakirjad kopeeritakse hinnakirjadena hankija arvele.
- Valuuta:
- Lepingut sõlmiv üksus.
- Maksetingimused.

Aja ja materjali allhankelepingu ridade puhul kopeeritakse allhankelepingurea hankija arve reale järgmised väljad ja seotud kirjed:

- Allhankeleping ja allhankelepingu viited
- Tehingu klass
- Roll
- Kande kategooria
- Tooteväljad
- Project
- Toiming
- Broneeritav ressurss

Fikseeritud hinnaga allhankelepingu ridade puhul kopeeritakse allhankelepingu realt ja allhankelepingurea vahekokkuvõttest hankija arve reale järgmised väljad.

- Allhankeleping ja allhankelepingu viited.
- Tehingu klass. Vaikimisi on väärtuseks **Vahekokkuvõte**.
- Vahekokkuvõtte nimi ja summa kopeeritakse seotud allhankelepingurea vahekokkuvõttest.
- Kasutaja saab hankija arve real valida projekti ja ülesande.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
