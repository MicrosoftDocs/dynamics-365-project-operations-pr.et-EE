---
title: Hankija arve oleku üleminekud
description: Selles artiklis selgitatakse Microsofti hankijaarve olekusiirdeid Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261011"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Hankija arve oleku üleminekud

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles artiklis selgitatakse Microsofti hankijaarve olekusiirdeid Dynamics 365 Project Operations. Kasutatakse järgmisi olekuid: **Mustand**, **Ülevaatamisel**, **Kinnitatud**, **Ootel** ja **Tühistatud**.

Järgmistel joonistel on kujutatud olekusiirded.

![Allhanke riigi ülemineku mudel.](../media/VI_State_Model.jpg)

Järgmises tabelis selgitatakse, mida iga olek esindab hankija arve elutsüklis Project Operationsis.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See olek on hankija arve algne olek. Liine ja hinnakujundust võidakse muuta. Selles olekus hankija arvet saab muuta ja kustutada. | Protsessis |
| Ülevaatamisel | See olek tähistab hankija arve töötlemisolekut. Vähemalt ühe hankija arve rea kinnitamise olek **on Pooleli**. | Kinnitatud, ootel |
| Kinnitatud | See olek tähistab hankija arve etappi, kus rakendus on loonud iga hankija arve rea jaoks tegelikud kuluandmed. Kõik hankija arve ridadele vastendatud seotud kulu tegelikud kulud on tühistatud ja asendatud nende hankija arve ridade tegelike kulusummadega. Selles olekus hankija arvet ei saa redigeerida ega kustutada. Kinnitatud hankijaarve tühistamiseks saate kasutada **nuppu Tühista**. Toiming Tühista tühistab toimingu Kinnita mõju. | Loobutud |
| Ootel | <p>See olek tähistab hankija arve etappi, kus hankija arvet ei saa arve või hankija olekuga seotud probleemi tõttu teisaldada. Selles olekus hankija arvet ei saa kinnitada, tühistada, muuta ega kustutada.</p><p>Saate kasutada toimingut Uuesti avamine hankija arve teisaldamiseks olekusse **Mustand** või **Ülevaatamisel**. Kui vähemalt ühe hankija arve rea kinnitamise olek **on Pooleli** või **Lõpetatud**, avatakse hankija arve uuesti olekus **Ülevaatamisel**. Kui hankija arve kõigi ridade kinnitamise olek **on Pole alustatud**, avatakse hankija arve uuesti olekus **Mustand**.</p> | Mustand, läbivaatamisel |
| Loobutud | See riik kujutab endast allhanke etappi, kus materjalide tegelik tarnimine ja/või töö allhankevahenditega ei ole enam vajalik. Selles olekus alltöövõttu ei saa kasutada ressursside ja materjalide projektinõuete hindamiseks ja personali jaoks ning samuti ei saa sellele viidata projekti aja, kulude ja materjalikasutuse kohta. Sellises olekus alltöövõttu ei saa redigeerida ega kustutada. | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
