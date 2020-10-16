---
title: Ressursi prognoosid
description: See teema sisaldab teavet selle kohta, kuidas Project Operationsis ressursiprognoose arvutatakse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928558"
---
# <a name="resource-estimates"></a>Ressursi prognoosid

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Ressursiprognoosid pärinevad ajafaasiga jõupingutustest, mis on määratletud tööjaotuse struktuuris koos kohaldatavate hinnakujunduse dimensioonidega. Tavaliselt on arvutuseks **kiirus/hr iga rolli jaoks x tunnid.** Iga ressursi ajafaasiga jõupingutus salvestatakse ressursi määramise kirjesse. Hinnastus salvestatakse eelmääratletud hinnakirja. Ühiku teisendust rakendatakse vastavalt kehtivale hinnakirjale.

![Ressursi prognoosid](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Vaikimisi omahinna ja kulu valuuta

Omahinna vaikeväärtused määratakse organisatsiooni üksusest.

## <a name="default-bill-rate-and-sales-currency"></a>Arvelduskulu ja müügivaluuta vaikeväärtused

Müügihindu rakendatakse üks kord tehingu kohta. Müügihinna loendi vaikesätete hierarhia on järgmine.

1. Organisatsioon
2. Klient
3. Hinnapakkumine/leping
