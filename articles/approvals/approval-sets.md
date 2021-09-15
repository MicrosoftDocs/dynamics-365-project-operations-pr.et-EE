---
title: Kinnitamiskomplektid
description: Selles teemas kirjeldatakse, kuidas kinnitamiskomplektide, taotluste ja nende toimingute alamhulkadega töötada.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323231"
---
# <a name="approval-sets"></a>Kinnitamiskomplektid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kinnitamiskomplektid rühmitavad kinnitamise taotlused kokku toimingute väiksemateks alamhulkadeks. See rühmitamine võimaldab kindlas järjekorras kinnitusi projekti kaupa töödelda ja võimaldab uusi katseid ning järjestamist. Kinnitamistaotluste kokku rühmitamine parandab kinnitamise töötlemise usaldusväärsust ja jälgitavust suure kinnitute mahu töötlemiseks.

Kinnituskomplektid näitavad nendega seotud kirjete üldist töötlemise olekut. Kui kinnituskirjet töödeldakse kinnituskomplekti abil, liigub kirje jaotisest **Edastatud** jaotisse **Kinnitatud** ja seda ei ole enam kinnituskomplektiga seotud. Kui kirje kinnitamiseks esitamine nurjub, jääb kirje olekusse **Esitatud** ja kinnituskomplekt on märgitud nurjunuks. Kinnitamiskomplekt logib nurjumise tõrketeate.

## <a name="processing-approvals-and-approval-sets"></a>Kinnituste ja kinnituskomplektide töötlemine
Töötlemiseks järjekorda pandud kinnitused kuvatakse vaates **Kinnituste töötlemine**. Süsteem töötleb kõiki kirjeid mitu korda asünkroonselt, sh proovib kinnitust uuesti, kui eelmised katsed nurjusid.

Välja **Kinnitamiskomplekti eluiga** salvestab katsete arvu, mis on komplekti töötlemiseks jäänud, enne kui see märgitakse nurjunuks.

## <a name="failed-approvals-and-approval-sets"></a>Nurjunud kinnitused ja kinnituskomplektid
Vaates **Nurjunud kinnitused** on loetletud kõik kasutaja sekkumist vajavad kinnitused. Avage seostatud kinnituskomplekti logid, et tuvastada nurjumise põhjus.
Valiku "**Proovi uuesti** valimine lisab kinnituskomplekti eluea loenduse, liigutab kinnituse tagasi olekusse **Töötleb** ja proovib töödelda ülejäänud kirjeid.

## <a name="configure-approval-sets"></a>Kinnituskomplektide konfigureerimine

### <a name="enable-the-approval-sets-feature"></a>Funktsiooni Kinnituskomplektid lubamine
Enne funktsiooni Kinnituskomplektid lubamist veenduge, et praegu ei töödeldaks ühtegi kinnitust.

- Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Luba kaasaegsed kinnitused**.

### <a name="turn-off-the-approval-sets-feature"></a>Funktsiooni Kinnituskomplektid väljalülitamine
Enne funktsiooni Kinnituskomplektid väljalülitamist veenduge, et praegu ei töödeldaks ühtegi kinnitust.

- Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Keela kaasaegsed kinnitused**.

### <a name="configuring-the-asynchronous-threshold"></a>Asünkroonse lävendi konfigureerimine 
Kinnituskomplektide loomisel teisaldatakse töötlemine taustale, kui kinnitamiseks valitud kirjete arv ületab määratud läviväärtuse. Kasutage välja **Asünkroonne lävi** konfigureerimiseks, millal kinnitamise töötlemist tuleks käitada sünkroonselt või asünkroonselt. Valige üks järgmistest väärtustest.

  - Null: kõiki taotlusi tuleks töödelda asünkroonselt. 
  - Nullist suuremad arvud: kinnitusi töödeldakse asünkroonselt ainult juhul, kui esitatud kinnituste arv ületab selle väärtuse.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
