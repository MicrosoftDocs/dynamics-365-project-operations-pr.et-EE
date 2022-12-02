---
title: Ressursihalduse režiimide ülevaade
description: See artikkel annab teavet ressursihalduse funktsionaalsuse kohta rakenduses Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928427"
---
# <a name="resource-management-modes-overview"></a>Ressursihalduse režiimide ülevaade

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


Dynamics 365 Project Operations toetab kahte režiimi, üldise broneerimisvoo käivitamiseks. Haldusrežiim määratletakse projekti parameetrina ja seda saab muuta juhul, kui teie äritegevus vajab muutmist.    

## <a name="central-mode"></a>Keskne režiim
Organisatsioonidele, kes tsentraliseerivad ressursside eraldamise projektidele, pakub keskne režiim võimalust, kuidas tagada, et projektijuhid saavad määratleta ressursinõude projekti tasandil. Ressursinõuete täitmine delegeeritakse ressursihaldurile. Projektijuhid saavad ressursihalduri poolt pakutud ressursse aktsepteerida või tagasi lükata.

![Keskne režiim.](./media/resource-management-central.png)

Ressursside haldamiseks keskses režiimis vaadake järgmist.

- [Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimega ressursside broneerimine ressursinõuetest](/dynamics365/project-service/book-named-resource)
- [Ressursitaotluse esitamine](/dynamics365/project-service/submit-resource-request)
- [Ressursinõude täitmine](/dynamics365/project-service/resource-management-fulfill-requests)
- [Pakutud projekti ressursi ressursitaotlusest kinnitamine või tagasilükkamine](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hübriidrežiim
Organisatsioonides, kes vajavad ressursside eraldamisel paindlikkust, võimaldab hübriidrežiim nii projektijuhtidele kui ka ressursihalduritele ressursside broneerimist.

![Hübriidrežiim.](./media/resource-management-hybrid.png)

Lisaks toetatud keskse režiimi protsessile vaadake järgmisi artikleid kõigi teiste toetatud broneerimisvoogude haldamise kohta hübriidrežiimis.

Ressursi otse projektile broneerimine.
- [Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid](/dynamics365/project-service/assign-named-bookable-resource)

Ressursi broneerimine ressursinõudest.
- [Ülesandele üldiste broneeritavate ressursside määramine ja ressursinõuete loomine](/dynamics365/project-service/assign-generic-bookable-resource)
- [Nimega ressursside broneerimine ressursinõuetest](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]