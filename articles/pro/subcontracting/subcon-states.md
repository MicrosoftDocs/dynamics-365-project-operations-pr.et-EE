---
title: Allhankelepingu oleku üleminekud
description: Selles artiklis selgitatakse Microsofti Dynamics 365 Project Operations allhankeriigi üleminekuid allhanke loomisel, käivitamisel ja sulgemisel.
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
