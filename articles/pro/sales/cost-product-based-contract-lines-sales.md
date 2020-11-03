---
title: Tootepõhiste lepinguridade kuluarvutus
description: Selles teemas antakse teavet loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4075187"
---
# <a name="costing-product-based-contract-lines"></a>Tootepõhiste lepinguridade kuluarvutus

_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_


Dynamics 365 Project Operationsi tootepõhised lepinguread sisaldavad välja **Omahind** , mis salvestab toote omahinna tootmisahela järgmise etapi kasumi arvutamiseks.

Kui kataloogitoote jaoks on loodud projektipõhine lepingurida, võetakse projektipõhise lepingurea kulu vaikimisi tootekataloogi väljalt **Standardne kulu**. Tootekataloogi väli **Standardkulu** seadistatakse organisatsiooni põhivaluutas. Kui ühiku omahind on lepingureal vaikimisi määratud, teisendatakse see lepingus toodud müügivaluutaks.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Tootepõhise lepingurea ühiku omahind

Tootepõhise lepingurea ühiku omahind võimaldada iga ühiku müügi jaoks erineva toote omahinna. Kuigi see ei ole alati vajalik, on olemas teatud stsenaariumid, mille korral tarnija teeb toote omahinna osas kliendile allahindluse. Siin on ühe võimaliku stsenaariumi näide.

Fabrikami robootika installib ettevõtte Adatum Corporation koosteliinidele robotõlgasid. Fabrikami pakub paigaldusteenused, kuid robotõlgade tootja on Trey Research. Kui ettevõtte Adatum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey Research jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse. Sel juhul loob Fabrikam tootepõhise lepingurea robotõlgadele ja sisenditele, mis on seotud selle lepingu ühe ühiku omahinnaga, mis erineb robotõlgade jaoks määratud standardsest omahinnast Trey Researchis.
