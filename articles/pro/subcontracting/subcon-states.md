---
title: Allhankelepingu oleku üleminekud
description: See artikkel selgitab allhankelepingu oleku üleminekuid rakenduses Microsoft Dynamics 365 Project Operations allhankelepingu loomisel, täitmisel ja sulgemisel.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522930"
---
# <a name="state-transitions-on-a-subcontract"></a>Allhankelepingu oleku üleminekud 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

See artikkel selgitab allhankelepingu oleku üleminekuid rakenduses Microsoft Dynamics 365 Project Operations. Iga osariik on esitatud mustandi, kinnitatud, suletud või tühistatud kujul. Järgmine pilt kujutab oleku üleminekuid.

![Allhanke olekumudel](../media/SubconStates.png)  

Järgmises tabelis kirjeldatakse, mida iga olek esindab rakenduse Project Operations allhankelepingu elutsüklis.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See tähistab allhankelepingu algseisu. Läbirääkimised müüjaga käivad. Read ja hinnakujundus võivad muutuda. Selles olekus allhankelepingut saab kasutada ressursside ja materjalide vajaduste hindamiseks ja personaliprojektide jaoks. Seda saab viidata ka projekti aja, kulu ja materjalikasutuse kohta. Selles olekus allhankelepingut saab muuta ja kustutada. | Kinnitatud |
| Kinnitatud | See on allhankelepingu etapp pärast seda, kui läbirääkimised hankijaga hinnakujunduse ja ostetavate reaüksuste üle on lõppenud. Materjalide ja/või tööde tegelik tarnimine allhanke vahenditega siiski alles käib. Selles olekus allhankelepingut saab kasutada ressursside ja materjalide vajaduste hindamiseks ja personaliprojektide jaoks. Seda saab viidata ka projekti aja, kulu ja materjalikasutuse kohta. Sellises olekus allhankelepingut ei saa muuta ega kustutada. Nupuga **Tühista** saate kinnitatud allhankelepingu tühistada. Nupp **Ava uuesti** võimaldab teil allhankelepingu uuesti avada, et viia see tagasi olekusse **Mustand**. Kinnitatud allhankelepingu sulgemiseks kasutage nuppu **Sulge**. | Suletud <br> Loobutud <br> Mustand |
| Suletud | See kujutab endast allhankelepingu etappi, mil materjalide ja/või tööde tegelik tarnimine allhankevahenditega on lõpetatud. Selles olekus allhankelepingut ei saa enam ressursside ja materjalide vajaduste hindamiseks ja personaliprojektide jaoks kasutada. Seda ei saa ka enam viidata projekti aja, kulu ja materjalikasutuse kohta. Sellises olekus allhankelepingut ei saa muuta ega kustutada. | Pole |
| Loobutud | See kujutab endast allhankelepingu etappi, mil materjalide ja/või tööde tegelik tarnimine allhankevahenditega ei ole enam vajalik. Sellises olekus allhankelepingut ei saa kasutada projekti ressursside ja materjalide vajaduste hindamiseks ja personali määramiseks, samuti ei saa sellele viidata projekti aja, kulu ja materjalikasutuse kohta. Sellises olekus allhankelepingut ei saa muuta ega kustutada. | Pole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
