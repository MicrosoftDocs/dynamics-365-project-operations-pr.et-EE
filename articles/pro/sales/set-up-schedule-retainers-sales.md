---
title: Honorari ajakava seadistamine – liht
description: See teema sisaldav teavet selle kohta, kuidas häälestada rakenduses Project Operations honorari ajakava.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181267"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Honorari ajakava seadistamine – liht

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Honoraride ajakava häälestatakse rakenduse Dynamics 365 Project Operations lehel **Projektileping**.

1. Valige lehe **Projektileping** vahekaardil **Ettemaksed ja honorarid** suvand **Honorari ajakava seadistamine**.
2. Avanevas dialoogiboksis kuvatakse järgmises tabelis toodud väljad. Tabel annab ülevaate, kudas sisestatud väärtused mõjutavad loodavat honorari ajakava.

| Väli | Kirjeldus | Allavoolu mõjud |
| --- | --- | --- |
| Projektilepingu klient | Lepingu klient, kellele selle honorari või avansi eest arve esitatakse. | Kui teil on lepingus mitu klienti ja soovite peate esitama igale neist konkreetse honorari või avansi summa, looge iga kliendi jaoks käsitsi üks arve. |
| Honorari ajakava algus | Sisestage ettemakse ajakava alguskuupäev ja -kellaaeg. | See päev ei pea olema esimese honorari või avansi loomise päev. Kuupäeva, millal esimene honorar või avanss luuakse, mõjutab ka arveldamise sagedus. |
| Honorari ajakava lõpp | Sisestage ettemakse ajakava lõpukuupäev ja -kellaaeg. | See päev ei pea olema viimase honorari või avansi loomise päev. Kuupäeva, millal viimane honorar või avanss luuakse, mõjutab ka arveldamise sagedus. |
| Loodavate honoraride arv | Kui sisestate loodavate honoraride arvu, kasutab süsteem arvu loomiseks sellel väljal olevat alguskuupäeva ja sagedust. | Kui see väli on käsitsi värskendatud, ignoreerib süsteem väärtust, mis on väljal **Honorari lõpukuupäev**, ja selle asemel luuakse teatud arv honorare või avansse. |
| Arve sagedus | Kui sageli rakendus honorare ja avansse loob. | See väärtus mõjutab otseselt honoraride ja avansside arvu ning loomise kuupäevi. |
| Kogusumma | Kogusumma on summa, mis on jaotatud üksikuteks loodavateks honorari- või avansimakseteks. | Sellel väljal puudub allavoolu mõju. |
