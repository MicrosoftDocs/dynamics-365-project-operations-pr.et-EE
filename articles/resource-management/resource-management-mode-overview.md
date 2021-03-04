---
title: Ressursihalduse režiimide ülevaade
description: Selles teemas antakse teavet ressursihalduse funktsionaalsusest Dynamics 365 Project Operationsis.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118513"
---
# <a name="resource-management-modes-overview"></a>Ressursihalduse režiimide ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Dynamics 365 Project Operations toetab kahte režiimi, et saaksite kogu reserveeringu voogu käivitada. Haldusrežiim määratletakse projekti parameetrina ja seda saab muuta juhul, kui teie äritegevus vajab muutmist.    

## <a name="central-mode"></a>Keskne režiim
Organisatsioonidele, kes tsentraliseerivad ressursside eraldamise projektidele, pakub keskne režiim võimalust, kuidas tagada, et projektijuhid saavad määratleta ressursinõude projekti tasandil. Ressursinõuete täitmine delegeeritakse ressursihaldurile. Projektijuhid saavad ressursihalduri poolt pakutud ressursse aktsepteerida või tagasi lükata.

![Keskne režiim](./media/resource-management-central.png)

Ressursside haldamiseks keskses režiimis vaadake järgmist.

- [Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimega ressursside broneerimine ressursinõuetest](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Ressursitaotluse esitamine](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Ressursinõude täitmine](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Pakutud projekti ressursi ressursitaotlusest kinnitamine või tagasilükkamine](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hübriidrežiim
Organisatsioonides, kes vajavad ressursside eraldamisel paindlikkust, võimaldab hübriidrežiim nii projektijuhtidele kui ka ressursihalduritele ressursside broneerimist.

![Hübriidrežiim](./media/resource-management-hybrid.png)

Lisaks toetatud keskse režiimi protsessile vaadake järgmisi teemasid kõigi teiste toetatud broneerimisvoogude haldamise kohta hübriidrežiimis.

Ressursi otse projektile broneerimine.
- [Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Ressursi broneerimine ressursinõudest.
- [Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimega ressursside broneerimine ressursinõuetest](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]