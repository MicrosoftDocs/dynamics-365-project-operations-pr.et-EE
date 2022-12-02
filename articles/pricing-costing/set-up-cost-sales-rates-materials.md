---
title: Materjalide oma- ja müügihindade seadistamine
description: See artikkel annab teavet, kuidas seadistada projektides kasutatavate materjalide kulu- ja müügihindu.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911775"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Materjalide oma- ja müügihindade seadistamine

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Toodete kulu- ja müügihindu saate häälestada rakenduses Dynamics 365 Project Operations. Toodete kulu- ja müügihinnad saab loetleda ainult ühes valuutas, mis peab olema hinnakirja päisega sama valuuta.

Toodete kulu- ja müügihindade häälestamiseks tehke järgmist. 

1. Uue hinnakirja loomiseks avage **Müük** > **Kliendid** > **Hinnakirjad** ja valige **Uus**. 
2. Valige suvandis **Hinnakirjaüksused** alamruudustiku menüüs valik **Uus hinnakirjaüksus**. 
3. Sisestage lehel **Kiirloomine** toode ja ühik, mille jaoks uue hinna loote.

Lisateabe saamiseks selle kohta, kuidas kataloogiüksuste jaoks hindu määratleda, vaadake teemasid [Toodete hinnakujunduse määratlemine hinnakirjade ja hinnakirjapunktide abil](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) ja [Valuuta ja hinna täpsuse kümnendkohtade arv](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Rakendus Dynamics 365 Project Operations ei toeta kõiki toodete hinnakujundusmeetodeid nagu rakendus Dynamics 365 Sales. Ainus hinnakujundusmeetod, mida toetatakse projektides kasutatavate toodete puhul, on *Valuutasumma*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
