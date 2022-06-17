---
title: Kinnitatud tegelike andmetega hankija arvete kinnitamine
description: Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 Project Operations kontrollib projektijuhte hankija arveid tegelikega, mis kinnitati töövõtjatena, kes tegid tööd ja salvestatud aega, ning kulusid ja materjale, mida projektimeeskonna liikmed kasutasid.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914213"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Kinnitatud tegelike andmetega hankija arvete kinnitamine

[!include [banner](../../includes/dataverse-preview.md)]

_ **Kehtib:** Lite juurutus - proforma arvelduse tehing

Microsoft Dynamics 365 Project Operations võimaldab projektijuhtidel hankija arveridu kontrollida järgmistel viisidel.

- **Kasutage hankija arve ridadel välja Kinnita olek**.
- Kui hankija arve read viitavad alltöövõtureale, linkige kulu tegelikud summad allhankija tegevusest nende hankija arve ridadega. Link luuakse, sobitades kulu tegelikud summad hankija arve ridadega.

    > [!NOTE]
    > Kuigi kinnitamise olekut saab jälgida hankija arve ridade puhul, mis ei viita alltöövõtule, ei saa kulu tegelikke andmeid nende hankija arve ridadega linkida.

## <a name="verification-status"></a>Kinnitamise olek

**Hankija arve rea väli Kinnita olek** näitab seda kinnitamise olekut. Toetatakse järgmisi olekuid.

1. Pole käivitatud
2. Edenemisel
3. Lõpetatud

Hankija arve ridu, mille kinnitamisolekuks **pole käivitatud**, saab redigeerida.

Hankija arve ridu, mille kinnituse olek on **Pooleli**, ei saa enam redigeerida. Hankija arverea puhul, mis viitab allhankele, seatakse kinnitamise olekuks **automaatselt Pooleli** kohe, kui esimene tegelik kulu on sobitatud hankija arvereaga.

Hankija arve ridu, mille kinnitamisolek **on Lõpetatud**, ei saa enam redigeerida. Kui kõigil hankija arve ridadel on see kinnitamisolek, saab hankija arve kinnitada.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Kulude tegelikud vastendamine hankija arve ridadega

Kuluarvude sobitamine aitab hankija arvereal kinnitusprotsessi. Kulu tegelike kulude vastendamiseks hankija arvereaga tehke järgmist.

1. Avage hankija arve rida ja valige **vahekaart Tasakaalustamata kulu tegelikud** andmed. Ruudustikus kuvatakse kulu tegelike kulude loend, mis viitab hankija arve reale samale alltöövõtureale.
2. Valige üks või mitu kuluvaste ja seejärel valige ruudustiku kohal oleval tööriistaribal **Vaste**. Süsteem kinnitab, et valitud kulu tegelikud summad on sobitatud. Pärast valideerimise edastamist lingitakse kulu tegelikud summad hankija arvereale.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Valideerimiskriteeriumid, mida kasutatakse kuluarvude linkimiseks hankija arve ridadega

Sobitamisprotsessi käigus saab luua seose tegeliku kulu ja hankija arve rea vahel ainult siis, kui on täidetud mõlemad järgmised tingimused.

- Iga **valitud tegeliku kulu väli Täpsustus olek** peab olema tühi. Teisisõnu, kulu tegelikud andmed ei tohi olla tagasikutsumise, kinnitamise tühistamise või parandustöölehe protsessi ajal asendatud muude kulunäitajatega.
- Järgmiste väljade väärtused sobitatakse hankija arve rea ja valitud tegeliku kulu vahel. Kui hankija arve real pole ühtegi välja määratud, ei arvestata seda vastendamiseks.

    - Projekti leping
    - Projekti lepingurida
    - Kande klass
    - Project
    - Toiming
    - Ressursikategooria
    - Kande kategooria
    - Toode
    - Alltöövõtu rida
    - Broneeritav ressurss

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Hankija arve realt saate kulu tegelikud summad kokku võtta

Kulutäpsete tegelike vastendamiste tühistamine võib aidata ka hankija arvel kinnitamisprotsessis, lubades eemaldada varem loodud lingid. Kulu tegelikud andmed saab tasakaalustamata ainult hankija arve ridadelt, mille kinnituse olek **on Pooleli**. Hankija arverealt kulu tegelike kulude vastendamiseks tehke järgmist.

1. Avage hankija arve rida ja valige **vahekaart Vastendatud kulu tegelikud** . Ruudustikus kuvatakse hankija arve reale viitavate kuluarvude loend.
2. Valige üks või mitu kuluvastevast ja seejärel valige ruudustiku kohal oleval tööriistaribal käsk **Tühista vastendamine**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
