---
title: Kinnitatud tegelike andmetega hankija arvete kinnitamine
description: See artikkel selgitab, kuidas rakendus Microsoft Dynamics 365 Project Operations võimaldab projektijuhtidel kinnitada hankija arveid tegelike näitajatega, mis kinnitati, kuna töövõtjad tegid tööd ja salvestasid aega, ning kulusid ja materjale, mida projektimeeskonna liikmed kasutasid.
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

Rakendus Microsoft Dynamics 365 Project Operations võimaldab projektijuhtidel kinnitada hankija arve ridu järgmistel viisidel.

- Kasutage hankija arve ridadel välja **Kinnitusolek**.
- Kui hankija arve read viitavad allhankelepingureale, linkige alltöövõtja tegevuse kulude tegelikud näitajad nende hankija arve ridadega. Link luuakse kulude tegelike näitajate vastavusse viimisel hankija arve ridadega.

    > [!NOTE]
    > Kuigi kinnitusolekut saab jälgida hankija arve ridade puhul, mis ei viita allhankelepingule, ei saa tegelikke kulusid nende hankija arve ridadega linkida.

## <a name="verification-status"></a>Kinnituse olek

Hankija arve real olev väli **Kinnitusolek** näitab seda kinnituse olekut. Toetatakse järgmisi olekuid:

1. Pole käivitatud
2. Edenemisel
3. Lõpetatud

Hankija arve ridu, mille kinnitusolek on **Pole alustatud**, saab muuta.

Hankija arve ridu, mille kinnitusolek on **Pooleli**, ei saa enam muuta. Hankija arve rea puhul, mis viitab allhankelepingule, määratakse kinnitusolekuks automaatselt **Pooleli** niipea, kui esimene kulu tegelik näitaja on vastavusse viidud hankija arve reale.

Hankija arve ridu, mille kinnitusolek on **Lõpule viidud**, ei saa enam muuta. Kui hankija arve kõikidel ridadel on see kinnitusolek, ei saa hankija arvet kinnitada.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Viige kulude tegelikud näitajad vastavusse hankija arve ridadega

Kulude tegelike näitajate vastavusse viimine aitab hankija arve real kinnitamise protsessi. Kulude tegelike näitajate vastavusse viimiseks hankija arve reaga järgige neid samme.

1. Avage hankija arve rida ja valige vahekaart **Vastavusse viimata kulude tegelikud näitajad**. Ruudustik näitab loendit kulude tegelikest näitajatest, mis viitavad samale allhankelepingu reale kui hankija arve rida.
2. Valige üks või mitu kulu tegelikku näitajat ja seejärel valige ruudustiku kohal oleval tööriistaribal **Vaste**. Süsteem kinnitab, et valitud kulude tegelikke näitajaid saab vastavusse viia. Pärast kinnitamise läbimist lingitakse kulude tegelikud näitajad hankija arve reaga.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Valideerimiskriteeriumid, mida kasutatakse kulude tegelike näitajate sidumiseks hankija arve ridadega

Vastavusse viimise protsessi käigus saab seose kulu tegeliku näitaja ja hankija arve rea vahel luua ainult siis, kui on täidetud mõlemad järgmised tingimused.

- Iga valitud kulu tegeliku näitaja väli **Korrigeerimise olek** peab olema tühi. Teisisõnu, kulude tegelikud näitajaid ei tohi olla tagasikutsumise, kinnitamise tühistamise või parandustöölehe protsessi käigus asendatud muude kulude tegelike näitajatega.
- Järgmiste väljade väärtused on vastavuses hankija arve rea ja valitud kulu tegeliku näitajaga. Kui mõni väli pole hankija arve real määratud, ei arvestata seda sobivaks.

    - Projekti leping
    - Projekti lepingurida
    - Kande klass
    - Project
    - Toiming
    - Ressursikategooria
    - Kande kategooria
    - Toode
    - Allhankelepingu rida
    - Broneeritav ressurss

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Vabastage hankija arve rea kulude tegelike näitajad vastavusest

Kulu tegelike näitajate vastavusest vabastamine võib aidata ka hankija arve kinnitamisel, võimaldades eelnevalt loodud linkide eemaldamist. Kulu tegelikke näitajaid saab võrrelda ainult hankija arve ridadelt, mille kinnitusolek on **Pooleli**. Kulude tegelike näitajate vastavusest vabastamiseks hankija arve reaga järgige neid samme.

1. Avage hankija arve rida ja valige vahekaart **Vastavusse viidud kulu tegelikud näitajad**. Ruudustik näitab kulu tegelike näitajate loendit, mis viitavad hankija arve reale.
2. Valige üks või mitu kulu tegelikku näitajat ja seejärel valige ruudustiku kohal oleval tööriistaribal **Vastavusest vabastamine**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
