---
title: Materjalide oma- ja müügihindade seadistamine
description: Selles teemas antakse teavet, kuidas seadistada projektides kasutatavate materjalide kulu- ja müügihindu.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1b1b679f15662d922804deefb6372adcdf4d4839
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576863"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Materjalide oma- ja müügihindade seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Toodete kulu- ja müügihindu saate häälestada rakenduses Dynamics 365 Project Operations. Toodete kulu- ja müügihinnad saab loetleda ainult ühes valuutas, mis peab olema hinnakirja päisega sama valuuta.

Toodete kulu- ja müügihindade häälestamiseks tehke järgmist. 

1. Uue hinnakirja loomiseks avage **Müük** > **Kliendid** > **Hinnakirjad** ja valige **Uus**. 
2. Valige suvandis **Hinnakirjaüksused** alamruudustiku menüüs valik **Uus hinnakirjaüksus**. 
3. Sisestage lehel **Kiirloomine** toode ja ühik, mille jaoks uue hinna loote.

Kataloogiüksuste hindade määratlemise kohta leiate lisateavet teemast [Toote hinnakujunduse määratlemine hinnakirjade ja hinnakirja kaupadega](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) ning [kümnendtäpsus valuutas ja hinnakujunduses](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations ei toeta kõiki toodete hinnakujundusmeetodeid nagu Dynamics 365 Sales. Ainus hinnameetod, mida projektides kasutatavate toodete puhul toetatakse, on *valuuta summa*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
