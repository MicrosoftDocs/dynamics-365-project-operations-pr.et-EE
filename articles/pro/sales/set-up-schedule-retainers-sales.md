---
title: Honorari ajakava seadistamine
description: See artikkel annab teavet selle kohta, kuidas häälestada rakenduses Project Operations honorari ajakava.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 077961d2f649754149315438252970609c246555
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927737"
---
# <a name="set-up-a-retainer-schedule"></a>Honorari ajakava seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Honoraride ajakavad häälestatakse rakenduse Dynamics 365 Project Operations lehel **Projektileping**.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]