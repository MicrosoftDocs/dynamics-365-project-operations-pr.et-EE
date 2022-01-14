---
title: Riigi üleminekud allhanke korras
description: Selles teemas selgitatakse Microsofti allhanke oleku üleminekuid Dynamics 365 Project Operations allhanke loomisel, käivitamisel ja sulgemisel.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903646"
---
# <a name="state-transitions-on-a-subcontract"></a>Riigi üleminekud allhanke korras 

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas selgitatakse Microsofti allhanke oleku üleminekuid Dynamics 365 Project Operations. Iga olek on esindatud kui mustand, kinnitatud, suletud või tühistatud. Järgmine pilt tähistab oleku üleminekuid.

![Alltöövõtu olekumudel](../media/SubconStates.png)  

Järgmises tabelis kirjeldatakse, mida iga olek Project Operationsi alltöövõtutsüklis esindab.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See kujutab endast allhanke algset olekut. Läbirääkimised müüjaga on käimas. Read ja hinnad võivad muutuda. Selle riigi allhankeid saab kasutada ressursside ja materjalide projektinõuete hindamiseks ja personaliks. Sellele võib viidata ka projekti aja, kulu ja materjalikasutuse kohta. Selle oleku allhankeid saab redigeerida ja kustutada. | Kinnitatud |
| Kinnitatud | See tähistab allhanke etappi pärast seda, kui läbirääkimised hankijaga hinnakujunduse ja ostetavate reakaupade üle on lõpule viidud. Materjalide ja/või tööde tegelik tarnimine allhankeressurssidega on siiski veel pooleli. Selle riigi allhankeid saab kasutada ressursside ja materjalide projektinõuete hindamiseks ja personaliks. Sellele võib viidata ka projekti aja, kulu ja materjalikasutuse kohta. Selle oleku allhankeid ei saa redigeerida ega kustutada. **Nupp Tühista võimaldab teil kinnitatud** allhanke tühistada. **Nupp Ava uuesti võimaldab teil** allhanke uuesti avada, et tuua see tagasi **mustandi** olekusse. Kinnitatud **alltöövõtu** sulgemiseks kasutage nuppu Sule. | Suletud <br> Loobutud <br> Mustand |
| Suletud | See kujutab endast allhanke etappi, kui materjalide ja/või tööde tegelik tarnimine allhankeressurssidega on lõpule viidud. Allhankeid selles olekus ei saa enam kasutada ressursside ja materjalide projektinõuete hindamiseks ja personaliks. Samuti ei saa sellele enam viidata projekti aja, kulu ja materjalikasutuse kohta. Selle oleku allhankeid ei saa redigeerida ega kustutada. | Pole |
| Loobutud | See on allhanke etapp, kui materjalide ja/või tööde tegelikku tarnimist allhankeressurssidega ei ole enam vaja. Allhankeid selles olekus ei saa kasutada ressursside ja materjalide projektinõuete hindamiseks ja personaliks, samuti ei saa sellele viidata projekti õigeaegselt, kulul ja materjali kasutamisel. Selle oleku allhankeid ei saa redigeerida ega kustutada. | Pole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
