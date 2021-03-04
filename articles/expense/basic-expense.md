---
title: Kulukirje (liht)
description: Selles teemas sisaldub teave selle kohta, kuidas töötada kulukirjega lihtjuurutuses.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590941"
---
# <a name="expense-entry-lite"></a>Kulukirje (liht)

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Põhiline või lihtne kuluhaldus on võimalus kirjendada lihtkulusid. Saate kirjendada kulusid projekti suhtes ja seejärel vaatab projekti kinnitaja need läbi ja kinnitab need.

Lisateavet kuluarvestuse võimaluste kohta lahenduses Dynamics 365 Project Operations leiate teemast [Kulude ülevaade](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Põhikulu jäädvustamine

Saate oma kulud jäädvustada, et saaksite need kinnitajale edastada.

1. Avage suvand **Kulud** ja valige **Uus**.
2. Sisestage lehel **Uus kulu** nõutav kuluga seotud teave ja valige seejärel suvand **Salvesta**.

## <a name="submit-a-basic-expense"></a>Põhikulu esitamine

Kui olete lõpetanud kõikide kulude jäädvustamise ja olete valmis need lasta kinnitada, siis te peate need esitama.

1. Avage suvand **Kulud** ja valige kulu. Või valige kõik kulud, kasutades päises olevat märkeruutu.
2. Valige käsk **Esita**. Süsteem töötleb valitud kirjeid ja loob seejärel kulu kinnitamise taotlused.

## <a name="add-an-attachment"></a>Lisa manus

Võimalik, et peate kinnitamiseks oma kulude kohta esitama lisadokumente. Kviitungi saate lisada kulukande ajajoonele. Valige **Redigeeri** ja jaotis **Ajaskaala** ning seejärel valige kviitungi manustamiseks kirjaklambri ikoon.

## <a name="recall-a-basic-expense"></a>Põhikulu tagasi kutsumine

Kui esitate kulu eklikult, saate selle tagasi kutsuda. Kulukirje tagasikutsumiseks vajalik aeg oleneb selle kinnitamise etapist.  Kui kinnitaja pole kirjet veel kinnitanud, võib tagasikutsumine toimuda kohe. Samas kui kirje on juba kinnitatud, palutakse kinnitajal kinnitada tagasikutsumine ja tühistada tehing.

1. Avage **Kulud** ja valige seejärel kulude loendist tagasi kutsumiseks kulu.
2. Tehke valik **Kutsu tagasi**. Kui kulukirjet pole veel kinnitatud, siis kutsub süsteem selle kohe tagasi. Kui kulukirje on juba kinnitatud, luuakse tagasikutsumise taotlus, et teavitada kinnitajat, et soovite kulu tagasi kutsuda. Kinnitaja kinnitab seejärel, et tagasikutsumine on võimalik, ja kirje tagastatakse.

## <a name="delete-a-basic-expense"></a>Põhikulu kustutamine

Veel esitamata kulusid on võimalik kustutada. Juba esitatud kulu kustutamiseks peate selle esmalt tagasi kutsuma.

## <a name="see-also"></a>Vt ka

- [Kinnituste ülevaade](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]