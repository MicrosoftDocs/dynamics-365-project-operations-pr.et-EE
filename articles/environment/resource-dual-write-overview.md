---
title: Project Operationsi topeltkirjutamise integreerimine
description: Selles teemas antakse ülevaade Project Operationsi topeltkirjutamise integreerimisest.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998676"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operationsi topeltkirjutamise integreerimise ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Project Operations kasutab [topeltkirjutamise võimalusi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), et sünkroonida andmed rakendustes Microsoft Dataverse ja Dynamics 365 Finance.

Järgmisel joonisel on näidatud, kuidas andmeid sünkroonitakse selle Dataverse’i ja Finance’i vahelise integreerimise osana.

![Project Operationsi andmevoogude ülevaade](./media/ProjectOperationsFlows.jpg)

Project Operations Dataverse’is pakub tänapäevast kasutajaliidest (UI) ja lihtsat koodita / madala koodiga laiendatavust, kasutades Power Platformi võimalusi. Projektijuhid, ressursihaldurid, projektimeeskonna liikmed ja muud peakontori töötajad teevad oma Project Operationsi tegevusi Dataverse’is.

Finance’i Project Operations pakub projekti raamatupidamist ja tulude kajastamise tuge. Project Operationsi lisandmoodulid liidavad finantsraamistiku Finance’is käibemaksu arvutamise, valuutavahetuskursside, finantsdimensioonide aruandluse ja muu jaoks. Projekti raamatupidaja kogemused põhinevad enamasti Finance’il.

Project Operationsi integreerimine koosneb järgmiste komponentide integreerimisest.


- [Rakenduse Project Operations häälestamise ja konfigureerimisandmete integreerimine](resource-dual-write-setup-integration.md) 
- [Projekti prognooside ja tegelike andmete integreerimine](resource-dual-write-estimates-actuals.md)
- [Projekti arved](resource-dual-write-project-invoice.md)
- [Kuluhaldus](resource-dual-write-expense.md)
- [Hankija arved](resource-dual-write-vendor-invoice.md)
