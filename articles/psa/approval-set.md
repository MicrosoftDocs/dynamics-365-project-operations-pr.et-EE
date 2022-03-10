---
title: Kinnitamiskomplektid rakenduses Project Service Automation
description: Selles teemas antakse teavet kinnituskomplektide, taotluste ja nende toimingute alamkomplektide kohta.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323546"
---
# <a name="approval-sets-in-project-service-automation"></a>Kinnitamiskomplektid rakenduses Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kinnitamiskomplektid rühmitavad kinnitamise taotlused kokku toimingute väiksemateks alamhulkadeks. See rühmitamine võimaldab projektil kinnitusi töödelda tellimuse järgi ja võimaldab neid uuesti teha ja järjestada. Rühmitamine parandab suurte kinnituse koguste puhul kinnituse töötlemise usaldusväärsust ja jälgitavust.

Kinnituskomplektid näitavad nendega seotud kirjete üldist töötlemise olekut. Kui kinnituse kirjet töödeldakse kinnituskomplekti abil, liigub kirje olekust **Esitatud** olekusse **Kinnitatud** ja ühendatakse kinnituskomplekti küljest lahti. Kui kirje kinnitamiseks esitamine nurjub, jääb kirje olekusse **Esitatud** ja kinnituskomplekt on märgitud nurjunuks. Kinnitamiskomplekt logib nurjumise tõrketeate.

## <a name="processing-approvals-and-approval-sets"></a>Kinnituste ja kinnituskomplektide töötlemine
Töötlemiseks järjekorda pandud kinnitused kuvatakse vaates **Kinnituste töötlemine**. Süsteem proovib kõiki kirjeid mitu korda asünkroonselt töödelda, sh kui eelmised katsed nurjusid, proovib see uuesti proovida kinnitada.

Välja **Kinnitamiskomplekti eluiga** salvestab katsete arvu, mis on komplekti töötlemiseks jäänud, enne kui see märgitakse nurjunuks.

## <a name="failed-approvals-and-approval-sets"></a>Nurjunud kinnitused ja kinnituskomplektid
Vaates **Nurjunud kinnitamised** on loetletud kõik kasutaja sekkumist vajavad kinnitused. Avage seostatud kinnituskomplekti logid, et tuvastada nurjumise põhjus.
Valiku "**Proovi uuesti** valimine lisab kinnituskomplekti eluea loenduse, liigutab kinnituse tagasi olekusse **Töötleb** ja proovib töödelda ülejäänud kirjeid.

## <a name="configure-approval-sets"></a>Kinnituskomplektide konfigureerimine

###  <a name="enable-the-approval-sets-feature"></a>Funktsiooni Kinnituskomplektid lubamine
Enne funktsiooni Kinnituskomplektid lubamist veenduge, et praegu ei töödeldaks ühtegi kinnitust.

- Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Luba kaasaegsed kinnitused**.

### <a name="turn-off-the-approval-sets-feature"></a>Funktsiooni Kinnituskomplektid väljalülitamine
Enne funktsiooni Kinnituskomplektid väljalülitamist veenduge, et praegu ei töödeldaks ühtegi kinnitust.

- Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Keela kaasaegsed kinnitused**.

### <a name="configuring-the-asynchronous-threshold"></a>Asünkroonse lävendi konfigureerimine 
Kinnituskomplektide loomisel teisaldatakse töötlemine taustale, kui kinnitamiseks valitud kirjete arv ületab määratud läviväärtuse. Kasutage välja **Asünkroonne lävi** konfigureerimiseks, millal kinnitamise töötlemist tuleks käitada sünkroonselt või asünkroonselt.
Kehtivad väärtused on järgmised.

  - Null: kõiki taotlusi tuleks töödelda asünkroonselt. 
  - Nullist suuremad arvud: kinnitusi töödeldakse asünkroonselt ainult juhul, kui esitatud kinnituste arv ületab selle väärtuse.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
