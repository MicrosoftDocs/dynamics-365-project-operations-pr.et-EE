---
title: Töötundide malli loomine
description: Selles teemas kirjeldatakse, kuidas luua Project Service’is tööaja malli.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981250"
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
3. Valige ressursi vahekaart **Tööaeg** ja järgige kalendrireeglite konfigureerimiseks [ressursi töötundide](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) konfigureerimine suuniseid.

**Looge uus kalendrimall**

1. Avage **Sätted** \> **Kalendrimall**.
2. Valige **Uus** ning sisestage nimi, kirjeldus ja malliressurss.


> [!NOTE]
> Kui ressursile viidatakse kalendrimallis, seostatakse kalendrimalliga ressursi kalendri koopia. Kui kopeeritud malli tööaega muudetakse, ei laiene need muudatused kalendermallile.


### <a name="see-also"></a>Vt ka  
 [Ressursside seadistamine](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
