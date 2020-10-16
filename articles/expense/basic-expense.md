---
title: Kulukirje (liht)
description: Selles teemas sisaldub teave selle kohta, kuidas töötada kulukirjega lihtjuurutuses.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965768"
---
# <a name="expense-entry-lite"></a>Kulukirje (liht)

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Põhiline või lihtne kuluhaldus on võimalus kirjendada lihtkulusid. Saate kirjendada kulusid projekti suhtes ja seejärel vaatab projekti kinnitaja need läbi ja kinnitab need.

Lisateavet rakenduse Dynamics 365 Project Operations kulu võimaluste kohta vaadake teemast [Kulu ülevaade](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Põhikulu jäädvustamine

Saate oma kulud jäädvustada, et saaksite need kinnitajale edastada.

1. Avage suvand **Kulud** ja valige **Uus**.
2. Sisestage lehel **Uus kulu** nõutav kuluga seotud teave ja valige seejärel suvand **Salvesta**.

## <a name="submit-a-basic-expense"></a>Põhikulu esitamine

Kui olete lõpetanud kõikide kulude jäädvustamise ja olete valmis need lasta kinnitada, siis te peate need esitama.

1. Avage suvand **Kulud** ja valige kulu. Või valige kõik kulud, kasutades päises olevat märkeruutu.
2. Valige käsk **Esita**. Süsteem töötleb valitud kirjeid ja loob seejärel kulu kinnitamise taotlused.

## <a name="recall-a-basic-expense"></a>Põhikulu tagasi kutsumine

Kui esitate kulu eklikult, saate selle tagasi kutsuda. Kulukirje tagasikutsumiseks vajalik aeg oleneb selle kinnitamise etapist.  Kui kinnitaja pole kirjet veel kinnitanud, võib tagasikutsumine toimuda kohe. Samas kui kirje on juba kinnitatud, palutakse kinnitajal kinnitada tagasikutsumine ja tühistada tehing.

1. Avage **Kulud** ja valige seejärel kulude loendist tagasi kutsumiseks kulu.
2. Tehke valik **Kutsu tagasi**. Kui kulukirjet pole veel kinnitatud, siis kutsub süsteem selle kohe tagasi. Kui kulukirje on juba kinnitatud, luuakse tagasikutsumise taotlus, et teavitada kinnitajat, et soovite kulu tagasi kutsuda. Kinnitaja kinnitab seejärel, et tagasikutsumine on võimalik, ja kirje tagastatakse.

## <a name="delete-a-basic-expense"></a>Põhikulu kustutamine

Veel esitamata kulusid on võimalik kustutada. Juba esitatud kulu kustutamiseks peate selle esmalt tagasi kutsuma.

## <a name="see-also"></a>Vt ka

- [Kinnituste ülevaade](../approvals/approvals-overview.md)
