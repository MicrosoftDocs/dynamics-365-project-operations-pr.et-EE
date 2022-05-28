---
title: Project Operationsi topeltkirjutamise integreerimine
description: Selles teemas antakse ülevaade Project Operationsi topeltkirjutamise integreerimisest.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582751"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operationsi topeltkirjutamise integreerimise ülevaade

_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_

Project Operations kasutab [andmete sünkroonimiseks Dynamics 365 Finance ja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) Dynamics 365 Finance kahe kirjutamise võimalusi Microsoft Dataverse.

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
