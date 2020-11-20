---
title: Sisemiste projektide raamatupidamise konfigureerimine
description: Selles teemas antakse teavet, kuidas seadistada Project Operationsis sisemiste projektide raamatupidamistavasid.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132373"
---
# <a name="configure-accounting-for-internal-projects"></a>Sisemiste projektide raamatupidamise konfigureerimine

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Sisemised projektid lubavad ettevõtetel jälgida kulusid, mis on seotud tegevustega, mille kohta kliendile arvet ei esitata. Sisemiste projektide näited on järgmised.

- Toote, näiteks mobiilirakenduse, arendamine ja arendusega seostatud kulu jälgimine.
- Eelmüügi aja ja kulu haldamine. Selle eelmüügi sisemise projekti saab hiljem, kui hinnapakkumine on võidetud, arveldatavaks projektiks teisendada.

Mis tahes projekti, mis pole seotud Dynamics 365 Project Operationsiga, käsitletakse sisemisena. Projekti kulu ja tulu profiile ei kasutata projekti raamatupidamise reeglite määramiseks. Sisemise projekti kulu sisestatakse alati kasumi ja kahjumi põhimõtete abil. Sisestuste pearaamatu kontod on määratletud lehel **Pearaamatu sisestuste seadistamise**.

- Aja tehingud sisestatakse, kui debiteeritakse konto **Kulu** ja krediteeritakse konto **Palgaarvestuse jaotus**.
- Kulu tehingud sisestatakse, kui debiteeritakse konto **Kulu** ja krediteeritakse konto **Kulu tasaarvelduskonto**.

Pärast seda, kui tehingud on projekti sisestatud, kui projekt on projekti lepinguga seostatud, tühistab süsteem kõik akumuleeritud tehingud ja loob uued arveldatavad tehingud. Arveldatavad tehingud järgivad vastava projekti kulu ja tulu profiilis määratletud raamatupidamise reegleid.


