---
title: Kuluhalduse töövoog
description: Selles teemas kirjeldatakse, kuidas kasutada rakenduses Microsoft Dynamics 365 Finance töövoo süsteemi, et seadistada kuluhalduses kuluaruannete ülevaatamise protsessi.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075111"
---
# <a name="expense-management-workflow"></a>Kuluhalduse töövoog

[!include [banner](../includes/banner.md)]

Saate kasutada töövoo süsteemi, et seadistada kuluhalduses kuluaruannete ülevaatamise protsessi. Saate seadistada töövoo, mis kasutab järgmisi kriteeriume, et määratleda, kes võib kuluaruande kinnitada.

- Töötaja aruannete hierarhia ja eelmääratletud kinnitamise piirid
- Mitmetasandiline kinnitamine, mis toetab ajutisi kinnitusi ja lõplikku kinnitajat
- Finantsdimensioonid ja projekti vastutusala
- Määramine kindlatele kasutajatele või kasutajarühmadele

Töövoo kinnitamised saab luua kuluaruannete, reisitellimuste, sularaha ettemaksete ja käibemaksu (VAT) taastamise jaoks.

**Näide**

Järgmine protsess on näiteks kuluaruande kuluhalduse töövoost.

1. Töötaja loob ja salvestab kuluaruande.
2. Töötaja esitab kuluaruande kinnitamiseks. Kinnitaja tuvastatakse töövoo seadistamisel määratletud reeglite põhjal.
3. Kinnitaja saab teate, et kuluaruanne on kinnitamiseks valmis. Kinnitaja vaatab kuluaruande üle ja kontrollib, kas järgmised tingimused on täidetud.

    - Kulud ei riku ühtegi kulupoliitikat. Kui kulu rikub poliitikat, kontrollib kinnitaja, et kuluaruanne sisaldaks kehtivat äriõigustust.
    - Kuluaruandele lisatakse elektroonilised kviitungid.

4. Kinnitaja kinnitab kuluaruande heaks.
5. Kuluaruanne määratakse sisestamiseks ostureskontro koordinaatorile.
6. Olenevalt sellest, kas automaatne sisestamine on konfigureeritud, kuvatakse üks järgmistest toimingutest.

    - Kui automaatne sisestamine on konfigureeritud, töödeldakse kuluaruanne tasumiseks ja värskendatakse kuluaruande olekut.
    - Kui automaatset sisestamist ei konfigureerita, kontrollib ostureskontro koordinaator, et kõik algsed kviitungid oleksid esitatud ja et sissetulekud oleksid joondatud kuluaruande kuludega. Kõigi kuluaruandesse sisestatud maksukoodide õigsust tuleb kontrollida.

Pärast nende nõuete kontrollimist sisestatakse kuluaruanne.

Pärast kuluaruande sisestamist on kuluaruande jaoks lubatud maksta ja töötajale makstakse hüvitis.
