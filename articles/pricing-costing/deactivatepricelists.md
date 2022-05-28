---
title: Hinnakirjade inaktiveerimine
description: Selles teemas kirjeldatakse, kuidas kasutamata või vanad hinnakirjad inaktiveerida või eemaldada.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ab790764f7a99118fd42bc76934105389173ff88
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596878"
---
# <a name="deactivate-price-lists"></a>Hinnakirjade inaktiveerimine 

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Vanade või kasutamata hinnakirjade rakendusest Dynamics 365 Project Operations eemaldamiseks peate läbima kaks etappi. 

1. Eemaldage või kustutage hinnakiri konkreetsetelt lehtedelt.
2. Inaktiveerige või kustutage hinnakiri lehe **Hinnakirjad** aktiivsete hinnakirjade seast.

>[!IMPORTANT]
> Hinnakirja täielikuks eemaldamiseks peate läbima mõlemad toimingud. Ainult 2. etapi läbimisel, mis on mõeldud hinnakirja vaates Aktiivsed hinnakirjad otseseks kustutamiseks või inaktiveerimiseks, pole piisav. Peate kustutama ka kõik selle hinnakirja seosed kõikide 1. etapis mainitud kohtadest.

## <a name="delete-the-price-list-from-specific-pages"></a>Hinnakirja kustutamine konkreetsetel saitidel
1. Hinnakirja kustutamiseks Project Operationsist minge järgmistele lehtedele.  

      - Leht **Projekti parameetrid** > vahekaart **Hinnakirjad**
      - Leht **Organisatsiooniüksus** > ruudustik **Hinnakirjad**
      - Leht **Konto** > ruudustik **Projekti hinnakirjad**
      - Leht **Projekti hinnapakkumised** > ruudustik **Projekti hinnakirjad**: see rakendub kõikidele aktiivsetele projekti hinnapakkumistele.
      - Leht **Projektilepingud** > ruudustik **Projekti hinnakirjad**: see rakendub kõikidele aktiivsetele projektilepingutele.

 2. Peate iga lehe jaoks valima hinnakirja, mille soovite kustutada, ja seejärel valima nupu **Kustuta**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Hinnakirja kustutamine või inaktiveerimine lehel Hinnakirjad
 
1. Hinnakirja kustutamiseks aktiivsete hinnakirjade seast, avage **Müük** > **Kohandatud** > **Hinnakirjad**. 
2. Valige hinnakiri, mille soovite kustutada, ja seejärel valima nupu **Kustuta**. Kui hinnakiri viitab mis tahes olemasolevale tehingule, ei saa te seda kustutada. Kui nii juhtub, saate hinnakirja inaktiveerida, et seda ei kuvataks üheski vaates. 
3. Hinnakirja inaktiveerimiseks valige hinnakiri uuesti ja valige seejärel **Inaktiveeri**.   
