---
title: Allhankelepingu oleku üleminekud
description: Selles artiklis selgitatakse microsofti Dynamics 365 Project Operations allhankeriigi üleminekuid allhanke korras, kuna alltöövõtt luuakse, käivitatakse ja suletakse.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919733"
---
# <a name="state-transitions-on-a-subcontract"></a>Allhankelepingu oleku üleminekud 

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles artiklis selgitatakse Microsofti allhankeriigi üleminekuid Dynamics 365 Project Operations. Iga olek on esindatud kas mustandina, kinnitatud, suletud või tühistatud olekuna. Järgmine pilt tähistab oleku üleminekuid.

![Alltöövõtu oleku mudel](../media/SubconStates.png)  

Järgmises tabelis on toodud kirjeldus selle kohta, mida iga riik projektitoimingute alltöövõtu elutsüklis esindab.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See on allhanke esialgne olukord. Läbirääkimised müüjaga on käimas. Ridu ja hinnakujundust muudetakse. Selle riigi allhankelepingut saab kasutada ressursside ja materjalide projektinõuete hindamiseks ja personalitööks. Sellele võib viidata ka projekti aja- ja kulukasutusele. Selle oleku allhankelepingut saab redigeerida ja kustutada. | Kinnitatud |
| Kinnitatud | See on alltöövõtu etapp pärast seda, kui läbirääkimised hankijaga hinnakujunduse ja ostetavate reakaupade üle on lõpule viidud. Materjalide ja/või töö tegelik tarnimine allhankevahenditest on siiski veel pooleli. Selle riigi allhankelepingut saab kasutada ressursside ja materjalide projektinõuete hindamiseks ja personalitööks. Sellele võib viidata ka projekti aja- ja kulukasutusele. Selle oleku allhankelepingut ei saa redigeerida ega kustutada. Nupp **Tühista** võimaldab teil kinnitatud alltöövõtu tühistada. Nupp **Uuesti avamine** võimaldab teil allhanke uuesti avada, et tuua see tagasi mustandi **olekusse**. **Kinnitatud alltöövõtu sulgemiseks kasutage nuppu Sule**. | Suletud <br> Loobutud <br> Mustand |
| Suletud | See kujutab endast allhanke etappi, kui materjalide tegelik tarnimine ja/või töö allhankevahenditega on lõpule viidud. Selle riigi allhankelepingut ei saa enam kasutada ressursside ja materjalide projektinõuete hindamiseks ja personalitööks. Samuti ei saa sellele enam viidata projekti aja, kulu ja materjalikasutuse kohta. Selle oleku allhankelepingut ei saa redigeerida ega kustutada. | Pole |
| Loobutud | See kujutab endast allhankeetappi, kui materjalide tegelik tarnimine ja/või töö allhankevahenditega ei ole enam vajalik. Selle riigi allhankelepingut ei saa kasutada ressursside ja materjalide projektinõuete hindamiseks ja personalitööks, samuti ei saa sellele viidata projekti õigeaegsele, kulule ja materjalikasutusele. Selle oleku allhankelepingut ei saa redigeerida ega kustutada. | Pole |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
