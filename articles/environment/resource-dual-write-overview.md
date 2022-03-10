---
title: Project Operationsi topeltkirjutamise integreerimine
description: Selles teemas antakse ülevaade Project Operationsi topeltkirjutamise integreerimisest.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007906"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operationsi topeltkirjutamise integreerimise ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Project Operations kasutab [topeltkirjutamise võimalusi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), et sünkroonida andmed rakendustes Microsoft Dataverse ja Dynamics 365 Finance.

Järgmisel joonisel on näidatud, kuidas andmeid sünkroonitakse selle Dataverse’i ja Finance’i vahelise integreerimise osana.

![Project Operationsi andmevoogude ülevaade.](./media/ProjectOperationsFlows.jpg)

Project Operations Dataverse’is pakub tänapäevast kasutajaliidest (UI) ja lihtsat koodita / madala koodiga laiendatavust, kasutades Power Platformi võimalusi. Projektijuhid, ressursihaldurid, projektimeeskonna liikmed ja muud peakontori töötajad teevad oma Project Operationsi tegevusi Dataverse’is.

Finance’i Project Operations pakub projekti raamatupidamist ja tulude kajastamise tuge. Project Operationsi lisandmoodulid liidavad finantsraamistiku Finance’is käibemaksu arvutamise, valuutavahetuskursside, finantsdimensioonide aruandluse ja muu jaoks. Projekti raamatupidaja kogemused põhinevad enamasti Finance’il.

Project Operationsi integreerimine koosneb järgmiste komponentide integreerimisest.


- [Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine](resource-dual-write-setup-integration.md) 
- [Projekti prognooside ja tegelike andmete integreerimine](resource-dual-write-estimates-actuals.md)
- [Projekti arved](resource-dual-write-project-invoice.md)
- [Kuluhaldus](resource-dual-write-expense.md)
- [Hankija arved](resource-dual-write-vendor-invoice.md)
