---
title: Allhankelepingu oleku üleminekud
description: Selles artiklis selgitatakse Microsofti Dynamics 365 Project Operations allhankeriigi üleminekuid allhanke loomisel, käivitamisel ja sulgemisel.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261187"
---
# <a name="state-transitions-on-a-subcontract"></a>Allhankelepingu oleku üleminekud 

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles artiklis selgitatakse Microsofti allhankeriigi üleminekuid Dynamics 365 Project Operations. Iga osariik on esindatud kas mustandina, kinnitatud, suletud või tühistatud. Järgmine pilt tähistab oleku üleminekuid.

![Allhanke riigimudel](../media/SubconStates.png)  

Järgmises tabelis on toodud kirjeldus selle kohta, mida iga riik projektitoimingute alltöövõtu elutsüklis esindab.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See näitab allhanke esialgset olekut. Läbirääkimised müüjaga on käimas. Liine ja hinnakujundust võidakse muuta. Selles olekus alltöövõttu saab kasutada ressursside ja materjalide projektinõuete hindamiseks ja personali jaoks. Sellele saab viidata ka projekti aja, kulude ja materjalikasutuse kohta. Sellises olekus alltöövõttu saab redigeerida ja kustutada. | Kinnitatud |
| Kinnitatud | See tähistab allhanke etappi pärast seda, kui läbirääkimised hankijaga hinnakujunduse üle ja ostetavad reakaubad on lõpule viidud. Materjalide ja/või tööde tegelik tarnimine allhankevahenditega on siiski veel pooleli. Selles olekus alltöövõttu saab kasutada ressursside ja materjalide projektinõuete hindamiseks ja personali jaoks. Sellele saab viidata ka projekti aja, kulude ja materjalikasutuse kohta. Sellises olekus alltöövõttu ei saa redigeerida ega kustutada. Nupp **Tühista** võimaldab teil kinnitatud allhankelepingu tühistada. Nupp **Re-open** võimaldab teil alltöövõtulepingu uuesti avada, et viia see tagasi mustandi **olekusse**. **Kasutage kinnitatud alltöövõtulepingu sulgemiseks nuppu Sule**. | Suletud <br> Loobutud <br> Mustand |
| Suletud | See tähistab alltöövõtu etappi, mil materjalide ja/või tööde tegelik tarnimine allhankeressursside abil on lõpule viidud. Sellises olekus alltöövõttu ei saa enam kasutada ressursside ja materjalide projektinõuete hindamiseks ja personaliks. Samuti ei saa sellele enam viidata projekti ajale, kuludele ja materjalikasutusele. Sellises olekus alltöövõttu ei saa redigeerida ega kustutada. | Pole |
| Loobutud | See on allhanke etapp, kus materjalide ja/või tööde tegelik tarnimine allhankeressursside abil ei ole enam vajalik. Sellises olekus alltöövõttu ei saa kasutada ressursside ja materjalide vajaduste hindamiseks ja personaliprojektiks, samuti ei saa sellele viidata projekti aja, kulude ja materjalikasutuse kohta. Sellises olekus alltöövõttu ei saa redigeerida ega kustutada. | Pole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
