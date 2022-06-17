---
title: Ajakavapaneeli konfigureerimine lepinguliste töötajate ja allhankelepinguga ressursiruumi näitamiseks
description: Selles artiklis kirjeldatakse, kuidas konfigureerida Ajakava tahvlit Microsoftis Dynamics 365 Project Operations, et kuvada allhanke ressursimaht projekti ressursivajaduste personalitööl.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919825"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Ajakavapaneeli konfigureerimine lepinguliste töötajate ja allhankelepinguga ressursiruumi näitamiseks 

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations ajakavatahvlit saab ressursside otsimiseks kasutada kahel viisil.

- Üldine ressursiotsing ilma konkreetse projektipõhise ressursinõude kontekstita.
- Nõudepõhine ressursiotsing, kus projekti nõue annab soovitatud ressursside konteksti.

Allhankeressursside võimsuse ja lepinguliste töötajate graafikute nõukogu teavitamiseks peate uuendama ajakavanõukogu sätteid. Need värskendused on järgmised. 
- Üldise ressursiotsingu ajagraafiku tahvli sätete värskendamine.
- Saate uuendada plaanimistahvli sätteid nõudepõhise ressursiotsingu jaoks.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Üldise ressursiotsingu ajakavatahvli sätete värskendamine
### <a name="update-filters-for-general-resource-search"></a>Filtrite värskendamine üldise ressursiotsingu jaoks
Ressursi otsimisel tuleks ajakava tahvlil olevaid filtreid uuendada, et saaksite otsida ka väliseid ressursse, määrates kõikvõi kõik järgmised.
  - Töötaja tüüp, olenemata sellest, kas kuvatavad ressursid peaksid olema lepingulised töötajad või töötajad.
  - Hankija ettevõte, kuhu ressurss peaks kuuluma.
  - Ressursid, mis kuuluvad konkreetsele alltöövõtu- või alltöövõtureale.
    
### <a name="update-retrieve-resource-query"></a>Toomisressursi päringu värskendamine
Nende täiendavate filtriatribuutide kasutamiseks tuleks värskendada ka otsimiseks kasutatavat päringut. Üldise ressursiotsingu ajakavatahvli konfiguratsiooni värskendamiseks tehke järgmist.  
1. Avage **konkreetse ajakavatahvli jaoks plaanimistahvli sätted**.
2. Avage **vahekaart Üldsätted** ja kerige jaotisse **Muud sätted**.
3. Värskendage **selle jaotise sätete loendis filtripaigutust** **projektitoimingute Lite** filtri vaikepaigutuseks.
4. Värskendage **ressursside päring** **project Operations Lite'i** ressursiotsingu vaikepäringusse.

![Üldise ressursiotsingu ajakavatahvli sätete värskendamine](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Plaanitahvli sätete värskendamine nõudepõhise ressursiotsingu jaoks
### <a name="update-filters-for-requirement-specific-resource-search"></a>Filtrite värskendamine nõudepõhise ressursiotsingu jaoks 
Ressursi otsimisel tuleks ajakava tahvlil olevaid filtreid uuendada, et saaksite otsida ka väliseid ressursse, määrates kõikvõi kõik järgmised.
 - Töötaja tüüp, olenemata sellest, kas kuvatavad ressursid peaksid olema lepingulised töötajad või töötajad.
 - Hankija ettevõte, kuhu ressurss peaks kuuluma.
 - Ressursid, mis kuuluvad konkreetsele alltöövõtu- või alltöövõtureale.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ressursipäringu värskendamine nõudepõhise ressursiotsingu jaoks 
Nende täiendavate filtriatribuutide kasutamiseks tuleks värskendada ka otsimiseks kasutatavat päringut. Nõudepõhise ressursiotsingu ajakavatahvli konfiguratsiooni värskendamiseks tehke järgmist.

1. Avage **konkreetse ajakava tahvli sätted** ja seejärel valige Nõudepõhise otsingu sätete avamiseks suvand **Ava vaikesätted**.
2. Avage **vahekaart Üldsätted** ja kerige jaotisse **Muud sätted**.
3. Värskendage **selle jaotise sätete loendis filtripaigutust** **projektitoimingute Lite** filtri vaikepaigutuseks.
4. Värskendage **ressursside päring** **project Operations Lite'i** ressursiotsingu vaikepäringusse.
5. Avage **vahekaart Ajakava tüübid** ja minge jaotisse **Project**.
6. Värskendage projecti sätetes **ajakava assistendi toomispäringut** **projektitoimingute ressursipäringule Lite'i** ressursside vaikepäring ja värskendage **ajakava abi abi toomispiirangute päringut** **project Operations Lite'i** jaoks.**·**

![Plaanitahvli sätete värskendamine nõudepõhise ressursiotsingu jaoks](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
