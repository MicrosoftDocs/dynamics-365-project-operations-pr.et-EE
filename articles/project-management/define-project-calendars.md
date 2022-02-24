---
title: Projektikalendrite määratlemine
description: Selles teemas antakse teavet selle kohta, kuidas rakendada projektile kalendrimalli projekti ajakava jälgimiseks.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981295"
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
3. Valige ressursi vahekaart **Tööaeg** ja järgige kalendrireeglite konfigureerimiseks [ressursi töötundide](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) konfigureerimine suuniseid.

**Looge uus kalendrimall**

1. Avage **Sätted** \> **Kalendrimall**.
2. Valige **Uus** ning sisestage nimi, kirjeldus ja malliressurss.

> [!NOTE]
> Kui ressursile viidatakse kalendrimallis, seostatakse kalendrimalliga ressursi kalendri koopia. Kui kopeeritud malli tööaega muudetakse, ei laiene need muudatused kalendermallile.

Nüüd saate seostada töömalli projektikalendri malliga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

