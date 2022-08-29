---
title: Hankija arveldamine – mõiste ja loomine
description: Selles artiklis kirjeldatakse hankija arvete mõistet, kasutusstsenaariume ja seda, kuidas microsoftis hankija arveid luua Dynamics 365 Project Operations.
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

Microsofti hankija arveldust Dynamics 365 Project Operations saab kasutada hankijate poolt projekti teenuste ja/või materjalide tarnete kulude registreerimiseks.

Kui teenused ja/või materjalid tellitakse allhanke korras hankijalt, tähistab alltöövõtt selle hankijaga sõlmitud lepingut. Kui hankija osutab teenuseid või materjalid võetakse vastu ja neid kasutatakse projekti ülesannetes, kajastatakse kulud projektis. Hankija saadab perioodiliselt arveid, mis on kinnitatud ja sobitatud projektis salvestatud kuludega. Kui kinnitusprotsess on lõpule viidud, kinnitatakse hankija arve ja väljastatakse maksmiseks.

## <a name="scenarios-for-use"></a>Kasutatavad stsenaariumid

Hankija arveid saab project operationsis kasutada kahe erineva stsenaariumi toetamiseks.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kliendid kasutavad kõiki allhankekogemusi

Hankija arve kasutuskogemused võimaldavad kontrollida ja sobitada ajakandeid, materjalikasutust ja kulukandeid, mis viitavad allhanke komponentidele hankija arve ridadega. Seda protsessi saab kasutada hankija arve ridade täpsuse kontrollimiseks. Kui kinnitusprotsess on lõpule viidud ja hankija arve kinnitatud, tühistab rakendus kinnitatud aja-, kulu- ja materjalikasutuse logidega salvestatud tegelikud andmed ning loob hankija arve ridade abil uued kulu tegelikud kulud.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kliendid ei kasuta täielikke allhankekogemusi, kuid soovivad saada ühtset vaadet project operationsi projektide kulude kohta

Kui jälgite allhankeprotsessi kolmanda osapoole süsteemis, saate salvestada kulud sellest kolmanda osapoole süsteemist Project Operationsisse, luues hankija arved, mis ei viita allhankele. Sel viisil saab teie projektijuhtidel olla ühtne ülevaade kõigi konkreetse projekti kulude kohta.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Hankija arvete loomine rakenduses Project Operations

Hankija arveid saab luua kahel viisil:

- Hankija arve loendi lehelt või ühe hankija arve üksikasjade lehelt
- Alltöövõtu loendilehelt või ühe alltöövõtu üksikasjade lehelt

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Loomine hankija arvete loendilehelt või üksikasjade lehelt

1. Avage **Hankija arvete ostmine** \> **·**.
2. Valige hankija arve loendi lehel või ühe hankija arve üksikasjade lehel Uus **,** et luua uus hankija arve.

Sel viisil loodud hankijaarved võivad viidata ka allhankele.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Loomine allhanke loendilehelt või üksikasjade lehelt

1. Avage **Allhankelepingute** ostmine \>**·**.
2. Valige üks või mitu allhanget.
3. Valige alltöövõtu loendi lehel või ühe alltöövõtu **üksikasjade lehel uue hankijaarve** loomiseks suvand Loo hankija arve.

Iga valitud allhanke jaoks luuakse uus hankijaarve olekus **Mustand**.

Sel viisil loodud hankija arved viitavad hankija arve päises alati allhankele. Iga alltöövõtu rida, millel on aja ja materjali arveldusmeetod, põhjustab hankija arvele rea loomise. Iga alltöövõtu rea puhul, millel on fikseeritud hinnaga arveldusmeetod, luuakse hankija arvel rida iga allhankerea verstaposti jaoks, mille olek **on arveldamiseks** valmis.

Järgmised väljad ja seotud kirjed kopeeritakse allhankelepingust hankija arve päisesse.

- Hankija.
- Seotud hinnakirjad kopeeritakse hankija arvele hinnakirjadena.
- Valuuta:
- Lepinguline üksus.
- Maksetingimuste.

Aja ja materjali allhanke ridade puhul kopeeritakse järgmised väljad ja seotud kirjed allhankerealt hankija arve reale.

- Alltöövõtu ja alltöövõtuliinide viited
- Kande klass
- Roll
- Kande kategooria
- Toote väljad
- Project
- Toiming
- Broneeritav ressurss

Fikseeritud hinnaga allhankeridade puhul kopeeritakse järgmised väljad allhankerealt ja allhanke rea verstapostilt hankija arve reale.

- Alltöövõtu ja alltöövõtuliinide viited.
- Tehingu klass. Vaikimisi on väärtuseks **Milestone**.
- Verstaposti nimi ja summa kopeeritakse seotud allhankerea verstapostist.
- Kasutaja saab hankija arve real valida projekti ja ülesande.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
