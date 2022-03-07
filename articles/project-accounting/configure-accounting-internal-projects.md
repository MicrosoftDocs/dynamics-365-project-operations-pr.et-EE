---
title: Sisemiste projektide raamatupidamise konfigureerimine
description: Selles teemas antakse teavet, kuidas seadistada Project Operationsis sisemiste projektide raamatupidamistavasid.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005521"
---
# <a name="configure-accounting-for-internal-projects"></a>Sisemiste projektide raamatupidamise konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Sisemised projektid lubavad ettevõtetel jälgida kulusid, mis on seotud tegevustega, mille kohta kliendile arvet ei esitata. Sisemiste projektide näited on järgmised.

- Toote, näiteks mobiilirakenduse, arendamine ja arendusega seostatud kulu jälgimine.
- Eelmüügi aja ja kulu haldamine. Selle eelmüügi sisemise projekti saab hiljem, kui hinnapakkumine on võidetud, arveldatavaks projektiks teisendada.

Mis tahes projekti, mis pole rakenduse Dynamics 365 Project Operations lepinguga seostatud, käsitletakse sisemisena. Projekti kulu ja tulu profiile ei kasutata projekti raamatupidamise reeglite määramiseks. Sisemise projekti kulu sisestatakse alati kasumi ja kahjumi põhimõtete abil. Sisestuste pearaamatu kontod on määratletud lehel **Pearaamatu sisestuste seadistamise**.

- Aja tehingud sisestatakse, kui debiteeritakse konto **Kulu** ja krediteeritakse konto **Palgaarvestuse jaotus**.
- Kulu tehingud sisestatakse, kui debiteeritakse konto **Kulu** ja krediteeritakse konto **Kulu tasaarvelduskonto**.
- Kaubatehingud sisestatakse debiteerides kontot **Kulu** ja krediteerides kontot **Kulu – üksus**.

Pärast seda, kui tehingud on projekti sisestatud, kui projekt on projekti lepinguga seostatud, tühistab süsteem kõik akumuleeritud tehingud ja loob uued arveldatavad tehingud. Arveldatavad tehingud järgivad vastava projekti kulu ja tulu profiilis määratletud raamatupidamise reegleid.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
