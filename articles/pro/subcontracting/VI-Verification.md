---
title: Kinnitatud tegelike andmetega hankija arvete kinnitamine
description: Selles artiklis selgitatakse, kuidas Microsofti Dynamics 365 Project Operations projektijuhid kontrollivad hankija arveid tegelike arvetega, mis kinnitati töövõtjate tehtud töödeks ja salvestatud ajaks, ning kulude ja materjalidega, mida projektimeeskonna liikmed kasutasid.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522933"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Kinnitatud tegelike andmetega hankija arvete kinnitamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Microsoft Dynamics 365 Project Operations võimaldab projektijuhtidel kontrollida hankija arve ridu järgmistel viisidel.

- **Kasutage hankija arve ridadel välja Kinnitamise olek**.
- Kui hankija arve read viitavad alltöövõtureale, linkige allhankija tegevuse tegelikud kulud nende hankija arve ridadega. Link luuakse tegelike kulusummade sobitamisel hankija arve ridadega.

    > [!NOTE]
    > Kuigi kinnitamise olekut saab jälgida hankija arve ridadel, mis ei viita allhankele, ei saa tegelikke kulusummasid nende hankija arve ridadega siduda.

## <a name="verification-status"></a>Kontrollimise olek

Väli **Kontrollimise olek** hankija arve real näitab kinnitamise olekut. Toetatakse järgmisi olekuid.

1. Pole käivitatud
2. Edenemisel
3. Lõpetatud

Hankija arve ridu, mille kinnitamise olek **on Pole alustatud**, saab redigeerida.

Hankija arve ridu, mille kinnitamise olek **on Pooleli,** ei saa enam redigeerida. Hankija arve rea puhul, mis viitab allhankele, määratakse kinnitamise olek automaatselt olekule **Pooleli** niipea, kui esimene tegelik kulu on hankija arve reale vastendatud.

Hankija arve ridu, mille kinnitamise olek on Lõpetatud, **ei** saa enam redigeerida. Kui hankija arve kõigil ridadel on see kinnitusolek, saab hankija arve kinnitada.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Tegelike kulusummade vastavusse viimine hankija arve ridadega

Tegelike kulude vastavusse viimine aitab hankija arve real kinnitusprotsessi. Tegelike kulusummade vastendamiseks hankija arve reaga toimige järgmiselt.

1. Avage hankija arve rida ja valige **vahekaart Tasakaalustamata kulu tegelikud** kulud. Ruudustik kuvab tegelike kuluartiklite loendi, mis viitab hankija arve reaga samale allhankereale.
2. Valige üks või mitu tegelikku kulusummat ja seejärel valige **ruudustiku kohal oleval tööriistaribal Vastenda**. Süsteem kinnitab, et valitud tegelikke kulusid saab sobitada. Pärast valideerimise läbimist seotakse tegelikud kulusummad hankija arve reale.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Valideerimiskriteeriumid, mida kasutatakse tegelike kulude linkimiseks hankija arve ridadega

Vastavusse viimise protsessi käigus saab seose tegeliku kulu ja hankija arve rea vahel luua ainult siis, kui on täidetud mõlemad järgmised tingimused.

- Korrigeerimise **oleku** väli iga valitud tegeliku kulu kohta peab olema tühi. Teisisõnu, tegelikud kulud ei tohi olla tagasikutsumise, kinnitamise tühistamise või parandustöölehe protsessi ajal asendatud muude tegelike kuludega.
- Järgmiste väljade väärtused vastendatakse hankija arve rea ja valitud tegeliku kulu vahel. Kui hankija arve real pole ühtegi välja määratud, ei arvestata seda vastendamisel.

    - Projekti leping
    - Projekti lepingurida
    - Kande klass
    - Project
    - Toiming
    - Ressursside kategooria
    - Kande kategooria
    - Toode
    - Allhanke liin
    - Broneeritav ressurss

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Tegelike kulude vastendamine hankija arve realt

Tegelike kulude vastendamine võib aidata kaasa ka hankija arve kinnitusprotsessile, võimaldades varem loodud linkide eemaldamist. Tegelike kulude summasid saab vastendamata jätta ainult hankija arve ridadelt, mille kinnitamise olek **on Pooleli**. Kulu tegelike kulude vastendamise tühistamiseks hankija arve realt toimige järgmiselt.

1. Avage hankija arve rida ja valige **vahekaart Sobitatud kulu tegelikud** kulud. Ruudustik kuvab tegelike kuluartiklite loendi, mis viitab hankija arve reale.
2. Valige üks või mitu tegelikku kulusummat ja seejärel valige ruudustiku kohal oleval tööriistaribal suvand **Tühista** vastendus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
