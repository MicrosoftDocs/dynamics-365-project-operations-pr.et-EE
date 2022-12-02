---
title: Modernsete kinnituste kaalutlused versioonitäiendusel
description: Artikkel hõlmab punkte, mida administraatorid peaksid kaasaegsete kinnituste funktsiooni lubamisel arvestama.
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
# <a name="upgrade-considerations-for-modern-approvals"></a>Modernsete kinnituste kaalutlused versioonitäiendusel 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

2022. aasta aprilli laine 1. väljalaske osana on kaasaegsete kinnituste funktsioon vaikimisi lubatud. See funktsioon parandab kinnitusloogika usaldusväärsust ja tagab, et saate kindlaks teha põhjuse, kui kinnitusloogika ebaõnnestub.

Selle muudatuse osana värskendatakse projekti kinnituste olekumuudatusi. Olek läheb nüüd otse olekust **Edastatud** olekusse **Kinnitatud**. **Ootel** pole enam kinnitamise olek. Kinnituse ooteloleku kindlakstegemiseks veenduge, et kinnitus on kinnituskomplekti osa, ja vaadake üle lisatud kinnituskomplekti olek.

## <a name="before-you-upgrade"></a>Enne täiendamist

Enne modernsetele kinnitustele täiendamist veenduge, et teil poleks ootel kinnitusi. Uudsed kinnitused ei kasuta olekut **Ootel**. Seetõttu ei töödelda kinnitusi, mis on pärast täiendamist endiselt märgistatud kui **Ootel**.

## <a name="after-you-upgrade"></a>Pärast täiendamist

Pärast Uudse kinnituse täiendamist peab administraator kinnitama, et kinnitusi töötlev pilvevoog on lubatud.

1. Logige sisse saidile [flow.microsoft.com](https://flow.microsoft.com).
2. Lülitage lehe paremas ülanurgas keskkond ümber uuendatud keskkonnale.
3. Valige **Lahendused**, et loetleda keskkonda installitud lahendused.
4. Valige lahendusloendis rakendus **Project Operations** või **Project Service**.
5. Muutke filter **Kõik** filtriks **Pilvevood**.
6. Veenduge, et suvand **Project Service – Projekti kinnitamise komplektide korduv ajastamine** on seatud väärtusele **Sees**. Kui see pole nii, valige voog ja seejärel **Lülita sisse**.
7. Kontrollige, et töötlemine toimuks iga viie minuti järel, vaadates üle **Süsteemi tööd** loendi **Sätted** piirkonnas.

## <a name="short-term-rollback"></a>Lühiajaline tagasipööramine

Kui te ei saa muudatusi kasutusele võtta või kui teil tekib selle funktsiooniga tõsine probleem, saate ajutiselt naasta algse kinnitusvoo juurde, toimides järgmiselt.
1. Logige oma keskkonda sisse ja veenduge, et kinnitusi ootel poleks.
2. Avage **Sätted** > **Projekti parameetrid**.
3. Valige **Funktsioonikontroll** ja seejärel valige **Uudsed kinnitused** funktsiooni väljalülitamiseks.

## <a name="removing-the-feature-flag"></a>Funktsiooni lipu eemaldamine

2022. aasta oktoobri laine 2. värskendusega kaob võimalus seda funktsiooni välja lülitada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
