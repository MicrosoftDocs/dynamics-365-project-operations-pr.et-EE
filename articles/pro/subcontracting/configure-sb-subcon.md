---
title: Ajakavapaneeli konfigureerimine lepinguliste töötajate ja allhankelepinguga ressursiruumi näitamiseks
description: See artikkel kirjeldab, kuidas rakenduses Microsoft Dynamics 365 Project Operations konfigureerida Ajakava tahvel, et näidata projekti ressursinõuete personalivajaduse määramisel alltöövõtjate ressursivõimsust.
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

Teenuses Microsoft Dynamics 365 Project Operations saab Ajakava tahvlit ressursside otsimiseks kasutada kahel viisil:

- Üldine ressursiotsing ilma konkreetse projektipõhise ressursinõude kontekstita.
- Nõudepõhine ressursiotsing, kus projekti nõue annab konteksti soovitatud ressurssidele.

Selleks, et teavitada ajakava tahvlit alltöövõtjate ressursivõimsusest ja lepingulistest töötajatest, peate ajakohastama ajakava tahvli sätted. Need värskendused hõlmavad järgmist: 
- Ajakava tahvli sätete värskendamine üldiseks ressursiotsinguks.
- Värskendage Ajakava tahvli sätteid nõudepõhiseks ressursiotsinguks.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Ajakava tahvli sätete värskendamine üldiseks ressursiotsinguks
### <a name="update-filters-for-general-resource-search"></a>Üldise ressursiotsingu filtrite värskendamine
Kui otsite ressurssi, tuleks ajakava tahvlil saadaolevaid filtreid värskendada, et saaksite otsida ka väliseid ressursse, määrates ühe või kõik järgmistest:
  - Töötaja tüüp, kas kuvatavad ressursid peaksid olema tähtajalise lepinguga töötajad või töötajad.
  - Hankija ettevõte, kuhu ressurss peaks kuuluma.
  - Ressursid, mis kuuluvad konkreetsele allhankelepingule või allhankelepingu reale.
    
### <a name="update-retrieve-resource-query"></a>Ressursi toomise päringu värskendamine
Nende täiendavate filtriatribuutide kasutamiseks tuleks värskendada ka otsinguks kasutatavat päringut. Kasutage järgmisi etappe, et uuendada ajakava tahvli konfiguratsiooni üldiseks ressursiotsinguks:  
1. Avage **Ajakava tahvli sätted** konkreetse Ajakava tahvli jaoks.
2. Avage vahekaart **Üldsätted** ja kerige jaotiseni **Muud sätted**.
3. Värskendage selle jaotise sätete loendis **Filtri paigutus** väärtuseks **Project Operations Lite’i filtri vaikepaigutus**.
4. Värskendage **Ressursside toomise päring** väärtuseks **Ressursi toomise vaikepäring Project Operations Lite’i jaoks**.

![Ajakava tahvli sätete värskendamine üldiseks ressursiotsinguks](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Värskendage Ajakava tahvli sätteid nõudepõhiseks ressursiotsinguks
### <a name="update-filters-for-requirement-specific-resource-search"></a>Värskendage filtreid nõuetepõhiseks ressursiotsinguks 
Kui otsite ressurssi, tuleks ajakava tahvlil saadaolevaid filtreid värskendada, et saaksite otsida ka väliseid ressursse, määrates ühe või kõik järgmistest:
 - Töötaja tüüp, kas kuvatavad ressursid peaksid olema tähtajalise lepinguga töötajad või töötajad.
 - Hankija ettevõte, kuhu ressurss peaks kuuluma.
 - Ressursid, mis kuuluvad konkreetsele allhankelepingule või allhankelepingu reale.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Värskendage ressursi päringut nõudepõhiseks ressursiotsinguks 
Nende täiendavate filtriatribuutide kasutamiseks tuleks värskendada ka otsinguks kasutatavat päringut. Kasutage järgmisi etappe, et uuendada ajakava tahvli konfiguratsiooni nõudepõhiseks ressursiotsinguks:

1. Avage **Ajakava tahvli sätted** konkreetse Ajakava tahvli jaoks ja seejärel valige **Ava vaikesätted**, et avada nõudepõhise otsingu sätted.
2. Avage vahekaart **Üldsätted** ja kerige jaotiseni **Muud sätted**.
3. Värskendage selle jaotise sätete loendis **Filtri paigutus** väärtuseks **Project Operations Lite’i filtri vaikepaigutus**.
4. Värskendage **Ressursside toomise päring** väärtuseks **Ressursi toomise vaikepäring Project Operations Lite’i jaoks**.
5. Avage vahekaart **Ajakava tüübid** ja valige **Projekt**.
6. **Projekti** sätete all värskendage **Assistendi ressursside toomise päringu ajastamine** **Project Operations Lite’i ressursside vaikimisi toomise päringuks** ja värskendage **Assistendi piirangute toomise päring** **Project Operations Lite’i piirangute vaikimisi toomise päringuks**.

![Värskendage Ajakava tahvli sätteid nõudepõhiseks ressursiotsinguks](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
