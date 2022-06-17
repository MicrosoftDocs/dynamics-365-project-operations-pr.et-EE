---
title: Kaasaegsete kinnituste kaalutluste täiendamine
description: Artikkel hõlmab punkte, mida administraatorid peaksid arvestama, kui nad lubavad kaasaegse kinnituse funktsiooni.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931739"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Kaasaegsete kinnituste kaalutluste täiendamine 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

2022. aasta aprilli Wave 1 väljalaske osana lubatakse vaikimisi kaasaegsete kinnituste funktsioon. See funktsioon parandab kinnitamise loogika usaldusväärsust ja tagab, et saate määrata kinnitamise loogika nurjumise põhjuse.

Selle muudatuse osana värskendatakse projekti kinnituste olekumuudatusi. Olek läheb nüüd otse olekust **Esitatud** olekusse **Kinnitatud**. **Ootel** pole enam kinnituste olek. Selleks et teha kindlaks, kas kinnitamine on ootel, kontrollige, kas kinnitamine on osa kinnituskomplektist, ja vaadake üle lisatud kinnituskomplekti olek.

## <a name="before-you-upgrade"></a>Enne täiendamist

Enne kaasaegsetele kinnitustele üleminekut veenduge, et teil pole ootel kinnitusi. Kaasaegsed kinnitused ei kasuta olekut **Ootel**. Seetõttu ei töödelda kõiki kinnitusi, mis on pärast täiendamist endiselt märgitud olekusse **Ootel**.

## <a name="after-you-upgrade"></a>Pärast täiendamist

Pärast versioonile Modern Approvals üleminekut peab administraator kinnitama, et kinnitusi töötlev pilvevoog on lubatud.

1. flow.microsoft.com [sisselogimine](https://flow.microsoft.com)
2. Lülitage lehe paremas ülanurgas oma keskkond täiendatavale keskkonnale.
3. Keskkonda installitud lahenduste loetlemiseks valige **Lahendused**.
4. Valige lahenduseloendist **Project Operations või** Project Service ( Project **Operations**).
5. Muutke filter olekust **Kõik** pilvevoogudeks **·**.
6. Veenduge, et **suvand Project Service – Projekti kinnitamiskomplektide** korduv ajastamine on seatud olekusse **Sees**. Kui see nii ei ole, valige voog ja seejärel valige **Lülita sisse**.
7. Veenduge, et töötlemine toimub iga viie minuti järel, **vaadates üle loendi Süsteemitööd** alas **Sätted**.

## <a name="short-term-rollback"></a>Lühiajaline tagasipööramine

Kui te ei saa muudatusi kasutusele võtta või kui teil tekib selle funktsiooniga tõsine probleem, saate ajutiselt algse kinnitusvoo juurde naasta, tehes järgmist.
1. Logige oma keskkonda sisse ja veenduge, et ootel kinnitusi pole.
2. **Avage sätted** > **Projekti parameetrid**.
3. Funktsiooni väljalülitamiseks valige **Funktsiooni juhtelement** ja seejärel valige **Funktsiooni väljalülitamiseks kaasaegsed kinnitused**.

## <a name="removing-the-feature-flag"></a>Funktsioonilipu eemaldamine

2022. aasta oktoobri Wave 2 värskenduses eemaldatakse võimalus see funktsioon välja lülitada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
