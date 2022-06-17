---
title: Kuluhalduse töövoog
description: Selles artiklis selgitatakse, kuidas saate rakenduses 365 Finance töövoosüsteemi Microsoft Dynamics kasutada kuluhalduse kuluaruannete ülevaatamise protsessi seadistamiseks.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71efc89d9167ef1ee546c67c123efeb37125cc02
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929715"
---
# <a name="expense-management-workflow"></a>Kuluhalduse töövoog

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]