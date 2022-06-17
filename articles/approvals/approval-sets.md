---
title: Kinnitamiskomplektid
description: Selles artiklis selgitatakse, kuidas töötada kinnituskomplektide, taotluste ja nende toimingute alamhulkadega.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918077"
---
# <a name="approval-sets"></a>Kinnitamiskomplektid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kinnitamiskomplektid rühmitavad kinnitamise taotlused kokku toimingute väiksemateks alamhulkadeks. See rühmitamine võimaldab kindlas järjekorras kinnitusi projekti kaupa töödelda ja võimaldab uusi katseid ning järjestamist. Kinnitamistaotluste kokku rühmitamine parandab kinnitamise töötlemise usaldusväärsust ja jälgitavust suure kinnitute mahu töötlemiseks.

Kinnituskomplektid näitavad nendega seotud kirjete üldist töötlemise olekut. Kui kinnituskirjet töödeldakse kinnituskomplekti abil, liigub kirje jaotisest **Edastatud** jaotisse **Kinnitatud** ja seda ei ole enam kinnituskomplektiga seotud. Kui kirje kinnitamiseks esitamine nurjub, jääb kirje olekusse **Esitatud** ja kinnituskomplekt on märgitud nurjunuks. Kinnitamiskomplekt logib nurjumise tõrketeate.

## <a name="processing-approvals-and-approval-sets"></a>Kinnituste ja kinnituskomplektide töötlemine
Töötlemiseks järjekorda pandud kinnitused kuvatakse vaates **Kinnituste töötlemine**. Süsteem töötleb kõiki kirjeid mitu korda asünkroonselt, sh proovib kinnitust uuesti, kui eelmised katsed nurjusid.

Välja **Kinnitamiskomplekti eluiga** salvestab katsete arvu, mis on komplekti töötlemiseks jäänud, enne kui see märgitakse nurjunuks.

Kinnituskomplekte töödeldakse perioodilise aktiveerimise kaudu, mis põhineb pilvevool **nimega** **Project Service - Projekti kinnitamise komplektide korduv ajastamine**. See on leitud lahendusest **nimega** **Projektitoimingud**. 

Veenduge, et voog oleks aktiveeritud, täites järgmised juhised.

1. Administraatorina logige flow.microsoft.com [sisse](https://powerautomate.microsoft.com).
2. Paremas ülanurgas aktiveerige keskkond, mida kasutate Dynamics 365 Project Operations rakenduses.
3. Keskkonda installitud lahenduste loetlemiseks valige **Lahendused**.
4. Valige lahenduseloendis **Project Operations (Project Operations).**
5. Muutke filter olekust **Kõik** pilvevoogudeks **·**.
6. Veenduge, et **projektiteenus – projektikinnituskomplektide** voo korduva ajastamine on seatud olekusse **Sees**. Kui see nii ei ole, valige voog ja seejärel valige **Lülita sisse**.
7. Veenduge, et töötlemine toimuks iga viie minuti järel, **vaadates üle loendi Süsteemitööd** project Operationsi **keskkonnas olevas** jaotises Sätted Dataverse.

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
