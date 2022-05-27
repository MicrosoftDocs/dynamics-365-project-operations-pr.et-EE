---
title: Projektikalendrite määratlemine
description: Selles teemas antakse teavet selle kohta, kuidas rakendada projektile kalendrimalli projekti ajakava jälgimiseks.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e31fcaf039ae214394b08b60b5d41987dc648e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578933"
---
# <a name="define-project-calendars"></a>Projektikalendrite määratlemine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Projekti loomiseks ja haldamiseks peate projektile rakendama kalendrimalli. Kalendrimallis määratletakse järgmised projektiatribuudid.

- Tööaeg (sh algus- ja lõppaeg)
- Tööpäevad
- Kalendri erandid (nt mitte-tööpäevad)

Projektile rakendatud kalendrimall on teie organisatsiooni sätetes määratletud kalendrimalli koopia.

> [!NOTE]
> Kui muudate kalendrimalli, siis need muudatused ei laiene projekti tööajale. Projekti tööaja muutmiseks tuleb rakendada uus mall.

Oma organisatsiooni jaoks kalendrimalli loomiseks on kaks põhinõuet.

- Määratlege malli soovitud tööaeg, kasutades uut või olemasolevat broneeritavat ressurssi.
- Looge uus kalendrimall ja seostage mall broneeritava ressursiga.

**Määratlege malli tööaeg**

1. Avage **Ressursid** \> **Ressursid**.
2. Looge kalendrimallis viidatav uus ressurss või valige olemasolev ressurss.
3. Valige ressursi vahekaart **Tööaeg** ja järgige kalendrireeglite konfigureerimiseks [ressursi töötundide](/dynamics365/field-service/set-work-hours-resource) konfigureerimine suuniseid.

**Looge uus kalendrimall**

1. Avage **Sätted** \> **Kalendrimall**.
2. Valige **Uus** ning sisestage nimi, kirjeldus ja malliressurss.

> [!NOTE]
> Kui ressursile viidatakse kalendrimallis, seostatakse kalendrimalliga ressursi kalendri koopia. Kui kopeeritud malli tööaega muudetakse, ei laiene need muudatused kalendermallile.

Nüüd saate seostada töömalli projektikalendri malliga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

