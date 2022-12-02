---
title: Hankija arve oleku üleminekud
description: See artikkel selgitab hankija arve oleku üleminekuid rakenduses Microsoft Dynamics 365 Project Operations.
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

See artikkel selgitab hankija arve oleku üleminekuid rakenduses Microsoft Dynamics 365 Project Operations. Kasutatakse järgmisi olekuid: **Mustand**, **Läbivaatamisel**, **Kinnitatud**, **Ootel** ja **Tühistatud**.

Järgmised joonised näitavad olekute üleminekuid.

![Allhanke oleku ülemineku mudel.](../media/VI_State_Model.jpg)

Järgmine tabel selgitab, mida iga olek esindab rakenduse Project Operations hankija arve elutsüklis.

| Maakond | Kirjeldus | Lubatud üleminekud |
| --- | --- | --- |
| Mustand | See olek on hankija arve algolek. Read ja hinnakujundus võivad muutuda. Hankija arvet selles olekus ei saa redigeerida ega kustutada. | Protsessis |
| Ülevaatamisel | See olek tähistab hankija arve töötlemise olekut. Vähemalt ühe hankija arve rea kinnitusolek on **Pooleli**. | Kinnitatud, ootel |
| Kinnitatud | See olek tähistab hankija arve etappi, kus rakendus on loonud iga hankija arve rea jaoks kulude tegelikud näitajad. Kõik lingitud kulude tegelikud näitajad, mis sobitati hankija arveridadega, on tühistatud ja asendatud nende hankija arve ridade kulude tegelike näitajatega. Hankija arvet selles olekus ei saa redigeerida ega kustutada. Kinnitatud hankija arve tühistamiseks saate kasutada nuppu **Tühista**. Toiming Tühista muudab kinnitustoimingu mõju vastupidiseks. | Loobutud |
| Ootel | <p>See olek tähistab hankija arve etappi, kus hankija arvet ei saa arve või hankija olekuga seotud probleemi tõttu liigutada. Hankija arvet selles olekus ei saa tühistada, redigeerida ega kustutada.</p><p>Saate kasutada toimingut Ava uuesti, et teisaldada hankija arve olekusse **Mustand** või **Läbivaatamisel**. Kui hankija arvel on vähemalt ühe rea kinnitusolek **Pooleli** või **Lõpetatud**, avatakse hankija arve uuesti olekus **Läbivaatamisel**. Kui hankija arve kõigi ridade kinnitusolek on **Pole alustatud**, avatakse hankija arve uuesti olekus **Mustand**.</p> | Mustand, läbivaatamisel |
| Loobutud | See olek kujutab endast allhankelepingu etappi, kus materjalide ja/või tööde tegelik tarnimine allhankevahenditega ei ole enam nõutud. Sellises olekus allhankelepingut ei saa kasutada projekti ressursside ja materjalide vajaduste hindamiseks ja personali määramiseks, samuti ei saa sellele viidata projekti aja, kulu ja materjalikasutuse kohta. Sellises olekus allhankelepingut ei saa muuta ega kustutada. | Pole |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
