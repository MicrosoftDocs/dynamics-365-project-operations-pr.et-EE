---
title: Allhankelepingute põhimõisted
description: Selles teemas kirjeldatakse mõningaid põhimõisteid, mis kehtivad rakenduse Microsoft Dynamics 365 Project Operations allhankelepingutele.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578106"
---
# <a name="key-concepts-in-subcontracting"></a>Allhankelepingute põhimõisted

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Teema selgitab mõningaid põhimõisteid, mida peate enne rakenduse Microsoft Dynamics 365 Project Operations allhankelepingute funktsionaalsuse kasutama hakkamist teadma.

## <a name="contracting-unit-on-the-subcontract"></a>Allhankelepingu lepingut sõlmiv üksus

Lepingut sõlmiv üksus esindab allüksust või tava, kellele kuulub lõpp-projekti kohaletoimetamine. Lepingut sõlmiv üksus on ka allüksus, mis sõlmib hankijaga lepingusuhte.

## <a name="purchase-currency"></a>Ostuvaluuta

Rakenduses Project Operations on ostuvaluutaks valuuta, milles allhankeleping sõlmiti. Samuti on see valuuta, milles talletatakse alltöövõtja projektikulud. Ostuvaluuta võib projekti valuutast erineda ja projekti valuuta võib omakorda müügivaluutast erineda.

## <a name="billing-methods-on-subcontract-lines"></a>Allhankelepingu ridade arveldusviisid

Projektidel on tavaliselt fikseeritud tasu ja tarbimisel põhinevad lepingumudelid. Rakendus Project Operations toetab neid arveldusviise müügi- ja ostukontekstides. Ostmisel toimivad arveldusviisid järgmiselt.

- **Aeg ja materjal** – kui allhankelepingu rida kasutab arveldusviisi **Aeg ja materjal**, talletatakse ajakulu projektis kui alltöövõtjad projekti kallal töötavad ja aega kirja panevad. Need alltöövõtjate kulukanded vastendatakse hankija arvete reaüksustega. Selles mudelis saavad projektihaldurid, kes kasutavad rakendust Project Operations, vastendada ja kinnitada hankija arveridu alltöövõtjate salvestatud ning kinnitatud aja suhtes. Pärast kontrolli lõpetamist tühistatakse eelmised tegelikud kulud, mis talletati pärast kinnitamist, ja projektis luuakse uued tegelikud kulud, mis põhinevad hankija arvel.
- **Fikseeritud hind** – fikseeritud tasuga lepingumudelis põhinevad hankija arved fikseeritud vahe-eesmärkidel. Samas võivad alltöövõtjate ressursid samuti aega teatada. Seejärel vaatab projektijuht ajakirjed üle ja kinnitab need. Pärast kinnitamist loob rakendus Project Operations projektis ajutised tegelikud kulud. Kui hankija on vahe-eesmärgi jaoks arve saatnud, saab projektijuht vastendada varem salvestatud tegelikud kulud vahe-eesmärgi andmetega. Kui kontroll on lõpetatud, siis tegelikud kulud tühistatakse ja vahe-eesmärgi põhine kulu talletatakse.

## <a name="project-price-lists-on-subcontracts"></a>Projekti hinnakirjad allhankelepingutes

Projekti hinnakirjad on hinnakirjad, mida kasutatakse aja, kulu ja muude projektiga seotud komponentide ostuhinna seadistamiseks. Hinnakirju võib olla mitu, millest igal võib rakenduses Project Operations olla oma kehtivuskuupäevaga allhankeleping. Project Operations ei toeta allhankelepingute projekti hinnakirjade puhul kattuvaid kehtivuskuupäevi.

## <a name="transaction-classes-on-subcontracts"></a>Allhankelepingute tehinguklassid

Project Operations toetab nelja tüüpi kandeklasse.

- Aeg
- Kulu
- Materjal
- Tasu

Ostukulusid saab hinnata ja tekitada ainult tehinguklassides **Aeg**, **Kulu** ja **Materjal**. **Tasu** on ainult tulu tehinguklass, mis ei ole ostukontekstis saadaval.

## <a name="purchase-pricing-dimensions"></a>Ostuhinnakirja dimensioonid

Hinnakirja dimensioonid võimaldavad teil otsustada, milliseid atribuute ostuhinna seadistamisel ja ajakannete lähtestamisel kasutatakse. Ostmisega seoses toetab Project Operations ostuhinna seadistamisel ja lähtestamisel ainult fikseeritud dimensioonikogumeid. Ostuhinna seadistamiseks ja lähtestamiseks allhankelepingu ridadel ning allhankelepingu ajakannetel on atribuutideks **Roll** ja **Broneeritav ressurss**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
