---
title: Hankija arve riigi üleminekud
description: Selles teemas selgitatakse Microsofti hankijaarve olekusiirdeid Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584683"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Hankija arve riigi üleminekud

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Selles teemas selgitatakse Microsofti hankijaarve olekusiirdeid Dynamics 365 Project Operations. Kasutatakse järgmisi olekuid: **Mustand**, **Ülevaatamine**, **Kinnitatud**, **Ootel** ja **Tühistatud**.

Järgmistel illustratsioonidel on näidatud oleku üleminekud.

![Alltöövõtu oleku ülemineku mudel.](../media/VI_State_Model.jpg)

Järgmises tabelis selgitatakse, mida iga olek projektitoimingutes hankija arve elutsüklis esindab.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See olek on hankija arve algne olek. Ridu ja hinnakujundust muudetakse. Selle oleku hankija arvet saab redigeerida ja kustutada. | Pooleli |
| Ülevaatamisel | See olek tähistab hankija arve töötlemisolekut. Vähemalt ühel hankija arvereal on kinnituse olek **Pooleli**. | Kinnitatud, Ootel |
| Kinnitatud | See olek tähistab hankija arve etappi, kus sidumine on loonud iga hankija arverea jaoks kulu tegelikud. Kõik lingitud kulu tegelikud summad, mis sobitati hankija arve ridadega, on tühistatud ja asendatud nende hankija arveridade kuluarvudega. Selles olekus hankija arvet ei saa redigeerida ega kustutada. Kinnitatud hankija arve tühistamiseks saate kasutada **nuppu Tühista**. Toiming Tühista tühistamine tühistab toimingu Kinnita mõju. | Loobutud |
| Ootel | <p>See olek tähistab hankija arve etappi, kus hankija arve ei saa arve või hankija oleku probleemi tõttu teisaldada. Selle oleku hankija arvet ei saa kinnitada, tühistada, redigeerida ega kustutada.</p><p>Toimingu Uuesti avamine abil saate hankija arve teisaldada olekusse **Mustand** või **Läbivaatus.** Kui vähemalt ühel hankija arve real on kinnituse olek Pooleli või Lõpetatud, avatakse hankija arve uuesti olekus **Läbivaatus**.**·** **·** Kui kõigil hankija arve ridadel on kinnitamisolek **Pole alustatud**, avatakse hankija arve uuesti olekus **Mustand**.</p> | Mustand, Läbivaatamisel |
| Loobutud | See riik kujutab endast allhanke etappi, kus materjalide tegelik tarnimine ja/või töö allhankevahenditega ei ole enam vajalik. Selle oleku alltöövõttu ei saa kasutada ressursside ja materjalide projektinõuete hindamiseks ja personalitööks ning sellele ei saa viidata ka projekti õigeaegsele, kulule ja materjalikasutusele. Selle oleku alltöövõttu ei saa redigeerida ega kustutada. | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
