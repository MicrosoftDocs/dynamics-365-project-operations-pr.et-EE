---
title: Sisemiste projektide raamatupidamise konfigureerimine
description: Selles teemas antakse teavet, kuidas seadistada Project Operationsis sisemiste projektide raamatupidamistavasid.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012851"
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
