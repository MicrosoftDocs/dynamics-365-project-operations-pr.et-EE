---
title: Ajakavapaneeli konfigureerimine lepinguliste töötajate ja allhankelepinguga ressursiruumi näitamiseks
description: Selles artiklis kirjeldatakse, kuidas konfigureerida Microsoftis Dynamics 365 Project Operations ajakavatahvlit, et see näitaks allhanke ressursi võimsust projekti ressursinõuete täitmisel.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262211"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Ajakavapaneeli konfigureerimine lepinguliste töötajate ja allhankelepinguga ressursiruumi näitamiseks 

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations ajakavapaneeli saab ressursside otsimiseks kasutada kahel viisil:

- Üldine ressursiotsing ilma konkreetse projektipõhise ressursinõude kontekstita.
- Nõudepõhine ressursiotsing, kus projekti nõue annab soovitatud ressurssidele konteksti.

Ajakavapaneeli teavitamiseks allhanke ressursivõimsusest ja lepingulistest töötajatest peate värskendama ajakava nõukogu sätteid. Need värskendused hõlmavad järgmist. 
- Värskendage ajakava nõukogu sätteid üldise ressursiotsingu jaoks.
- Värskendage ajatamisnõukogu sätteid nõudepõhise ressursiotsingu jaoks.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ajatamisnõukogu sätete värskendamine üldise ressursiotsingu jaoks
### <a name="update-filters-for-general-resource-search"></a>Üldise ressursiotsingu filtrite värskendamine
Ressursi otsimisel tuleks ajakavapaneelil saadaolevaid filtreid värskendada, et saaksite otsida ka väliseid ressursse, määrates ühe või kõik järgmistest.
  - Töötaja liik, olenemata sellest, kas näidatud ressursid peaksid olema lepingulised töötajad või töötajad.
  - Hankijaettevõte, kuhu ressurss peaks kuuluma.
  - Ressursid, mis kuuluvad kindlale allhanke- või allhankeliinile.
    
### <a name="update-retrieve-resource-query"></a>Ressursipäringu värskendamine
Otsimiseks kasutatavat päringut tuleks samuti värskendada, et kasutada neid täiendavaid filtriatribuute. Kasutage üldise ressursiotsingu ajakavapaneeli konfiguratsiooni värskendamiseks järgmisi samme.  
1. Avage **ajakavapaneeli sätted** konkreetse ajakavatahvli jaoks.
2. **Avage vahekaart Üldised seaded** ja kerige jaotiseni **Muud seaded**.
3. Värskendage **selle jaotise sätete loendis filtripaigutus** väärtuseks **Project Operations Lite’i** filtri vaikepaigutus.
4. Värskendage **ressursside toomise päringut**, et see oleks **vaikimisi allalaaditav ressursside päring Project Operations Lite’i** jaoks.

![Ajatamisnõukogu sätete värskendamine üldise ressursiotsingu jaoks](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Ajatamisnõukogu sätete värskendamine nõudepõhise ressursiotsingu jaoks
### <a name="update-filters-for-requirement-specific-resource-search"></a>Filtrite värskendamine nõudepõhise ressursiotsingu jaoks 
Ressursi otsimisel tuleks ajakavapaneelil saadaolevaid filtreid värskendada, et saaksite otsida ka väliseid ressursse, määrates ühe või kõik järgmistest.
 - Töötaja liik, olenemata sellest, kas näidatud ressursid peaksid olema lepingulised töötajad või töötajad.
 - Hankijaettevõte, kuhu ressurss peaks kuuluma.
 - Ressursid, mis kuuluvad kindlale allhanke- või allhankeliinile.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ressursipäringu värskendamine nõudepõhise ressursiotsingu jaoks 
Otsimiseks kasutatavat päringut tuleks samuti värskendada, et kasutada neid täiendavaid filtriatribuute. Kasutage järgmisi samme, et värskendada ajatamispaneeli konfiguratsiooni nõudepõhise ressursiotsingu jaoks.

1. Avage **kindla ajakavapaneeli jaoks ajakavapaneeli sätted** ja seejärel valige **Nõudepõhise otsingu sätete avamiseks käsk Ava vaikesätted**.
2. **Avage vahekaart Üldised seaded** ja kerige jaotiseni **Muud seaded**.
3. Värskendage **selle jaotise sätete loendis filtripaigutus** väärtuseks **Project Operations Lite’i** filtri vaikepaigutus.
4. Värskendage **ressursside toomise päringut**, et see oleks **vaikimisi allalaaditav ressursside päring Project Operations Lite’i** jaoks.
5. **Avage vahekaart Ajakava tüübid** ja minge jaotisse **Projekt**.
6. Värskendage Projecti **sätete** all ajastamise assistendi ressursside toomise päringut **, et see tooks** ressursid vaikimisi alla Query for Project Operations Lite **ja värskendage** ajaskaala assistendi toomise piirangute päringut **, et** saada vaikimisi alla Retrieve Constraints Query for Project Operations Lite **.**

![Ajatamisnõukogu sätete värskendamine nõudepõhise ressursiotsingu jaoks](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
