---
title: Kinnitamiskomplektid
description: See artikkel selgitab, kuidas töötada kinnitamiskomplektide, taotluste ja nende toimingute alamhulkadega.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524911"
---
# <a name="approval-sets"></a>Kinnitamiskomplektid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Kinnitamiskomplektid rühmitavad kinnitamise taotlused kokku toimingute väiksemateks alamhulkadeks. See rühmitamine võimaldab kindlas järjekorras kinnitusi projekti kaupa töödelda ja võimaldab uusi katseid ning järjestamist. Kinnitamistaotluste kokku rühmitamine parandab kinnitamise töötlemise usaldusväärsust ja jälgitavust suure kinnitute mahu töötlemiseks.

Kinnituskomplektid näitavad nendega seotud kirjete üldist töötlemise olekut. Kui kinnituskirjet töödeldakse kinnituskomplekti abil, liigub kirje jaotisest **Edastatud** jaotisse **Kinnitatud** ja seda ei ole enam kinnituskomplektiga seotud. Kui kirje kinnitamiseks esitamine nurjub, jääb kirje olekusse **Esitatud** ja kinnituskomplekt on märgitud nurjunuks. Kinnitamiskomplekt logib nurjumise tõrketeate.

## <a name="processing-approvals-and-approval-sets"></a>Kinnituste ja kinnituskomplektide töötlemine
Töötlemiseks järjekorda pandud kinnitused kuvatakse vaates **Kinnituste töötlemine**. Süsteem töötleb kõiki kirjeid mitu korda asünkroonselt, sh proovib kinnitust uuesti, kui eelmised katsed nurjusid.

Välja **Kinnitamiskomplekti eluiga** salvestab katsete arvu, mis on komplekti töötlemiseks jäänud, enne kui see märgitakse nurjunuks.

Kinnituskomplekte töödeldakse perioodilise aktiveerimise kaudu, mis põhineb **Pilvevool** nimega **Project Service - Projektide kinnitamiskomplektide korduv ajakava**. Selle leiate **Lahendusest** nimega **Project Operations**. 

Veenduge, et voog oleks aktiveeritud, järgides järgmisi etappe.

1. Administraatorina logige sisse lehele [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Ülemises parempoolses nurgas lülituge keskkonda, mida kasutate Dynamics 365 Project Operationsi jaoks.
3. Valige **Lahendused**, et loetleda keskkonda installitud lahendused.
4. Valige lahenduse loendist **Project Operations**.
5. Muutke filter **Kõik** filtriks **Pilvevood**.
6. Veenduge, et voog **Project Service – Projektide kinnitamiskomplektide korduv ajakava** on seatud olekusse **Sees**. Kui see pole nii, valige voog ja seejärel **Lülita sisse**.
7. Kontrollige, et töötlemine toimub iga viie minuti tagant, vaadates üle oma Project Operations Dataverse keskkonnas loendi **Süsteemi tööd** jaotises **Sätted**.

## <a name="failed-approvals-and-approval-sets"></a>Nurjunud kinnitused ja kinnituskomplektid
Vaates **Nurjunud kinnitused** on loetletud kõik kasutaja sekkumist vajavad kinnitused. Avage seostatud kinnituskomplekti logid, et tuvastada nurjumise põhjus.
Valiku "**Proovi uuesti** valimine lisab kinnituskomplekti eluea loenduse, liigutab kinnituse tagasi olekusse **Töötleb** ja proovib töödelda ülejäänud kirjeid.

## <a name="configure-approval-sets"></a>Kinnituskomplektide konfigureerimine

### <a name="enable-the-approval-sets-feature"></a>Funktsiooni Kinnituskomplektid lubamine
Enne funktsiooni Kinnituskomplektid lubamist veenduge, et praegu ei töödeldaks ühtegi kinnitust. Pärast selle funktsiooni lubamist ei saa seda keelata.

- Avage leht **Projekti parameetrid** ja valige **Funktsiooni juhtimine** > **Luba kaasaegsed kinnitused**.

### <a name="configuring-the-asynchronous-threshold"></a>Asünkroonse lävendi konfigureerimine 
Kinnituskomplektide loomisel teisaldatakse töötlemine taustale, kui kinnitamiseks valitud kirjete arv ületab määratud läviväärtuse. Kasutage välja **Asünkroonne lävi** konfigureerimiseks, millal kinnitamise töötlemist tuleks käitada sünkroonselt või asünkroonselt. Valige üks järgmistest väärtustest.

  - Null: kõiki taotlusi tuleks töödelda asünkroonselt. 
  - Nullist suuremad arvud: kinnitusi töödeldakse asünkroonselt ainult juhul, kui esitatud kinnituste arv ületab selle väärtuse.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
