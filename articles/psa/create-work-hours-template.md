---
title: Töötundide malli loomine
description: Selles teemas kirjeldatakse, kuidas luua Project Service’is tööaja malli.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987386"
---
# <a name="create-a-work-hours-template-project-service"></a>Töötundide malli loomine (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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
3. Valige ressursi vahekaart **Tööaeg** ja järgige kalendrireeglite konfigureerimiseks [ressursi töötundide](/dynamics365/field-service/set-work-hours-resource.md) konfigureerimine suuniseid.

**Looge uus kalendrimall**

1. Avage **Sätted** \> **Kalendrimall**.
2. Valige **Uus** ning sisestage nimi, kirjeldus ja malliressurss.


> [!NOTE]
> Kui ressursile viidatakse kalendrimallis, seostatakse kalendrimalliga ressursi kalendri koopia. Kui kopeeritud malli tööaega muudetakse, ei laiene need muudatused kalendermallile.


### <a name="see-also"></a>Vt ka  
 [Ressursside seadistamine](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
