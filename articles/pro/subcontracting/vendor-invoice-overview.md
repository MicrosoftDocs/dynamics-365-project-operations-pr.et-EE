---
title: Hankija arveldamine – mõiste ja loomine
description: Selles artiklis kirjeldatakse hankija arvete mõistet, kasutusstsenaariume ja hankija arvete loomist Microsoftis Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911453"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Hankija arveldamine – mõiste ja loomine

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Hankija arveldamist Microsoftis Dynamics 365 Project Operations saab kasutada hankijate poolt projekti teenuste ja/või materjalide tarnete kulude kirjendamiseks.

Kui teenused ja/või materjalid tellitakse hankijalt allhanke korras, esindab alltöövõtt selle hankijaga sõlmitud lepingulepingut. Kuna hankija pakub teenuseid või materjalid võetakse vastu ja neid kasutatakse projektiülesannete täitmiseks, kirjendatakse projekti kulud. Perioodiliselt saadab hankija arveid, mis on kinnitatud ja sobitatud projektile salvestatud kuludega. Pärast kinnitamisprotsessi lõppu kinnitatakse hankija arve ja väljastatakse maksmiseks.

## <a name="scenarios-for-use"></a>Kasutusstsenaariumid

Hankija arveid Project Operationsis saab kasutada kahe erineva stsenaariumi toetamiseks.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kliendid kasutavad kõiki alltöövõtu kogemusi

Hankija arve funktsioonid pakuvad võimalust kontrollida ja sobitada ajakandeid, materjalikasutust ja kulukandeid, mis viitavad allhanke komponentidele hankija arve ridadega. Seda protsessi saab kasutada hankija arveridade täpsuse kontrollimiseks. Pärast kinnitamisprotsessi lõpuleviimist ja hankija arve kinnitamist tühistab sidumine kinnitatud aja-, kulu- ja materjali kasutuslogidega salvestatud tegelikud tegelikud andmed ning loob hankija arveridade abil uued kulu tegelikud.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kliendid ei kasuta kõiki alltöövõtuvõimalusi, kuid soovivad projektitoimingute projektide kuludest ühtset ülevaadet

Kui jälgite alltöövõtuprotsessi kolmanda osapoole süsteemis, saate selle kolmanda osapoole süsteemi kulud project Operationsi kirjendada, luues hankija arveid, mis ei viita alltöövõtulepingutele. Sel viisil saavad teie projektijuhid olla ühe ja ühtse ülevaate kõigist konkreetse projekti kuludest.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Hankija arvete loomine Project Operationsis

Hankija arveid saab luua kahel viisil.

- Hankija arveloendi lehelt või ühe hankija arve üksikasjade lehelt
- Alltöövõtu loendi lehelt või ühe allhanke üksikasjade lehelt

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Hankija arveloendi lehe või üksikasjade lehe loomine

1. **Avage hankija arvete ostmine** \> **·**.
2. Uue hankija arve arve loomiseks valige hankija arve loendi lehel või ühe hankijaarve üksikasjade lehel suvand **Uus**.

Sel viisil loodud hankija arved võivad viidata ka alltöövõtule.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Alltöövõtu loendi lehelt või üksikasjade lehelt loomine

1. Minge jaotisse **Alltöövõtu** ostmine \>**·**.
2. Valige üks või mitu allhankelepingut.
3. Uue hankijaarve loomiseks valige alltöövõtu loendi lehel või ühe allhanke üksikasjade lehel suvand **Loo hankija arve**.

Iga valitud allhanke jaoks luuakse uus hankija arve olekus **Mustand**.

Sel viisil loodud hankija arved viitavad alati hankija arve päises olevale alltöövõtule. Iga allhanke rida, millel on aja- ja materjaliarve meetod, põhjustab hankija arvele rea loomise. Iga allhanke rida, millel on fikseeritud hinna arveldamise meetod, põhjustab hankija arvel rea loomise iga allhankerea vahesposti jaoks, mille olek **on Arveldamiseks** valmis.

Järgmised väljad ja seostuvad kirjed kopeeritakse allhankelepingust hankija arve päisesse.

- Hankija.
- Seostuvad hinnakirjad kopeeritakse hankija arvele hinnakirjadena.
- Valuuta:
- Lepinguline üksus.
- Maksetingimuste.

Aja ja materjali alltöövõtu ridade puhul kopeeritakse alltöövõturealt hankija arve reale järgmised väljad ja seostuvad kirjed.

- Alltöövõtu- ja alltöövõturea viited
- Kande klass
- Roll
- Kande kategooria
- Tooteväljad
- Project
- Toiming
- Broneeritav ressurss

Fikseeritud hinnaga alltöövõturidade puhul kopeeritakse alltöövõturealt ja alltöövõturea vahe-alalt hankija arve reale järgmised väljad.

- Alltöövõtu- ja alltöövõturea viited.
- Kandeklass. Vaikimisi on **väärtus Verstapost**.
- Verstaposti nimi ja summa kopeeritakse seotud alltöövõtu rea verstapostist.
- Kasutaja saab hankija arvereal valida projekti ja ülesande.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
