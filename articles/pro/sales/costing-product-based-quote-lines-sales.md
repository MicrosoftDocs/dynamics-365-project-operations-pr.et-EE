---
title: Tootepõhiste hinnapakkumiste ridade kuluarvutus
description: Selles teemas antakse teavet tootepõhisele hinnapakkumise reale omahinna rakendamise kohta.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c08ac3b0f24dda19489bad6e667a50b67b8ce3ec
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273643"
---
# <a name="costing-product-based-quote-lines"></a>Tootepõhiste hinnapakkumiste ridade kuluarvutus

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Tootepõhistel hinnapakkumise ridadel on rakenduses Dynamics 365 Project Operations ka väli **Omahind**. Seda välja kasutatakse hinnapakkumise real ja allavooli tasuvuse arvutustes toote omahinna jälgimiseks.

Kui kataloogitoote jaoks on loodud projektipõhine hinnapakkumise rida, võetakse projektipõhise hinnapakkumise rea kulu vaikimisi tootekataloogi väljalt **Standardne kulu**. Tootekataloogi standardkulu väli seadistatakse organisatsiooni põhivaluutas. Tootepõhise hinnapakkumise rea vaikimisi ühiku kulu teisendatakse hinnapakkumise müügi valuutasse.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Tootepõhise hinnapakkumise rea ühiku kulu

Tootepõhise hinnapakkumise rea üksuse kulu omamise eesmärk oon võimaldada iga toote müügi jaoks erinevad kulud. See pole tavaline stsenaarium, kuid mõnikord võib tarnija sõltuvalt lõpliku müügi kliendist alandada toote maksumust.

Näiteks:

Fabrikami robootika installib ettevõtte A Datum Corporation koosteliinidele robotõlgasid. Fabrikami pakub paigaldusteenused, kuid robotõlgade tootja on Trey robootika. Kui ettevõtte A Datum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey robotõlgade jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.

Sel juhul loob Fabrikam robotõlgade jaoks tootepõhise hinnapakkumise rea ja sisestab selle hinnapakumise jaoks ühiku maksumuse jaoks erihinna. See maksumus erineb ettevõtte Trey robotõlgade tavamaksumusest.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]