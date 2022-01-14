---
title: Plaani juhatuse konfigureerimine lepinguliste töötajate ja alltöövõtu võimsuse kuvamiseks
description: Selles teemas kirjeldatakse, kuidas konfigureerida Microsofti ajakavatahvlit Dynamics 365 Project Operations kuvama alltöövõtu ressursivõimsust projekti ressursivajaduste personalimisel.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903644"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Plaani juhatuse konfigureerimine lepinguliste töötajate ja alltöövõtu võimsuse kuvamiseks 

[!include [banner](../../includes/dataverse-preview.md)]

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_

Microsofti Dynamics 365 Project Operations ajakavatahvlit saab ressursside otsimiseks kasutada kahel viisil.

- Üldine ressursiotsing ilma konkreetse projektipõhise ressursivajaduse kontekstita.
- Nõudepõhine ressursiotsing, kus projekti nõue annab soovitatud ressursside konteksti.

Alltöövõturessursside võimsuse ja lepinguliste töötajate ajakava juhatuse teavitamiseks peate uuendama ajakava juhatuse sätteid. Need värskendused on järgmised. 
- Värskendage üldise ressursiotsingu ajakavatahvli sätteid.
- Saate värskendada ajakava tahvli sätteid nõudepõhise ressursiotsingu jaoks.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Üldise ressursiotsingu ajakavatahvli sätete värskendamine
### <a name="update-filters-for-general-resource-search"></a>Üldise ressursiotsingu filtrite värskendamine
Ressursi otsimisel tuleks ajakava tahvlil saadaolevaid filtreid värskendada, et saaksite otsida ka väliseid ressursse, määrates mis tahes või kõik järgmistest.
  - Töötaja tüüp, olenemata sellest, kas näidatud ressursid peaksid olema lepingulised töötajad või töötajad.
  - Hankija ettevõte, kuhu ressurss peaks kuuluma.
  - Ressursid, mis kuuluvad kindlale allhanke- või alltöövõtuliinile.
    
### <a name="update-retrieve-resource-query"></a>Ressursipäringu toomise värskendamine
Otsinguks kasutatavat päringut tuleks värskendada ka nende täiendavate filtriatribuutide kasutamiseks. Üldise ressursiotsingu ajakavatahvli konfiguratsiooni värskendamiseks kasutage järgmisi juhiseid.  
1. Saate avada **ajakava tahvli sätted** kindla ajakavatahvli jaoks.
2. Avage **vahekaart Üldsätted** ja kerige jaotiseni **Muud sätted**.
3. Värskendage selle jaotise sätete loendis **filtri** **paigutust Project Operations Lite'i vaikefiltri paigutuseks**.
4. Värskendage **ressursipäringut** project **Operations Lite'i jaoks ressursipäringuks**.

![Üldise ressursiotsingu ajakavatahvli sätete värskendamine](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Plaanitahvli sätete värskendamine nõudepõhise ressursiotsingu jaoks
### <a name="update-filters-for-requirement-specific-resource-search"></a>Nõudepõhise ressursiotsingu filtrite värskendamine 
Ressursi otsimisel tuleks ajakava tahvlil saadaolevaid filtreid värskendada, et saaksite otsida ka väliseid ressursse, määrates mis tahes või kõik järgmistest.
 - Töötaja tüüp, olenemata sellest, kas näidatud ressursid peaksid olema lepingulised töötajad või töötajad.
 - Hankija ettevõte, kuhu ressurss peaks kuuluma.
 - Ressursid, mis kuuluvad kindlale allhanke- või alltöövõtuliinile.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Ressursipäringu värskendamine nõudepõhise ressursiotsingu jaoks 
Otsinguks kasutatavat päringut tuleks värskendada ka nende täiendavate filtriatribuutide kasutamiseks. Plaanitahvli konfiguratsiooni värskendamiseks nõudepõhise ressursiotsingu jaoks kasutage järgmisi juhiseid.

1. Avage **kindla** ajakavatahvli sätted ja seejärel valige **Nõudepõhise** otsingu sätete avamiseks Ava vaikesätted.
2. Avage **vahekaart Üldsätted** ja kerige jaotiseni **Muud sätted**.
3. Värskendage selle jaotise sätete loendis **filtri** **paigutust Project Operations Lite'i vaikefiltri paigutuseks**.
4. Värskendage **ressursipäringut** project **Operations Lite'i jaoks ressursipäringuks**.
5. Avage **vahekaart Ajakava tüübid** ja minge **projecti**.
6. Värskendage projecti sätete **alusel** **ajakavaabilise ressursipäringut** **projektitoimingute Lite'i jaoks mõeldud vaikeressursside päringuks** ja värskendage **ajakavaabilise toomise piirangute** päringut **project Operations Lite'i vaikesuvituspiirangute päringuks**.

![Plaanitahvli sätete värskendamine nõudepõhise ressursiotsingu jaoks](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
