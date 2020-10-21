---
title: Tootepõhiste hinnapakkumiste ridade kuluarvutus
description: Selles teemas antakse teavet tootepõhisele hinnapakkumise reale omahinna rakendamise kohta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906134"
---
# <a name="costing-product-based-quote-lines"></a>Tootepõhiste hinnapakkumiste ridade kuluarvutus

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Rakenduse Dynamics 365 Project Operations projektipõhised hinnapakkumise ridadel on ka väli **Omahind**. Seda välja kasutatakse hinnapakkumise real ja allavooli tasuvuse arvutustes toote omahinna jälgimiseks.

Kui kataloogitoote jaoks on loodud projektipõhine hinnapakkumise rida, võetakse projektipõhise hinnapakkumise rea kulu vaikimisi tootekataloogi väljalt **Standardne kulu**. Tootekataloogi standardkulu väli seadistatakse organisatsiooni põhivaluutas. Tootepõhise hinnapakkumise rea vaikimisi ühiku kulu teisendatakse hinnapakkumise müügi valuutasse.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Tootepõhise hinnapakkumise rea ühiku kulu

Tootepõhise hinnapakkumise rea üksuse kulu omamise eesmärk oon võimaldada iga toote müügi jaoks erinevad kulud. See pole tavaline stsenaarium, kuid mõnikord võib tarnija sõltuvalt lõpliku müügi kliendist alandada toote maksumust.

Näiteks:

Fabrikami robootika installib ettevõtte A Datum Corporation koosteliinidele robotõlgasid. Fabrikami pakub paigaldusteenused, kuid robotõlgade tootja on Trey robootika. Kui ettevõtte A Datum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey robotõlgade jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.

Sel juhul loob Fabrikam robotõlgade jaoks tootepõhise hinnapakkumise rea ja sisestab selle hinnapakumise jaoks ühiku maksumuse jaoks erihinna. See maksumus erineb ettevõtte Trey robotõlgade tavamaksumusest.
