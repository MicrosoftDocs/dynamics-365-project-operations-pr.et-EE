---
title: Projekti ülesannete sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevat tööülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288914"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projekti ülesannete sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malli ja aluseks olevat tööülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.

> [!NOTE]
> - Projekti ülesannete integreerimine, kulukande kategooriad, kuluprognoosid ja funktsioonide lukustamine on saadaval versioonis 8.0.
> - Kui kasutate rakendust Enterprise Edition 7.3.0 pärast KB 4132657 ja KB 4132660 installimist, on teil võimalik kasutada malle, et integreerida projekti tööülesanded, kuluarvestuse kategooriad, tunnihinnangud, kuluhinnangud ja tegelikud näitajad ning konfigureerida funktsioonide lukustamist. Kui te peate arvestuse jaotuse lähtestama, soovitasime ka installida KB 4131710.
> - Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Andmevoog rakendusest Project Service Automation rakendusse Finance

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt. Andmete integreerimise funktsiooniga saadaolev integreerimismall võimaldab projekti ülesannete andmete voogu Project Service Automationist Finance’i.

Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mall ja ülesanne

Mallile Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Projekti ülesannete sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Andmete migreerimise malli nimi:** projekti ülesanded (PSA-st Fini ja Opsi)
- **Ülesande nimi projektis:** projekti ülesanded

Enne kui projekti ülesannete sünkroonimine saab aset leida, peate sünkroonima projekti kontaktid ja projektid.

## <a name="entity-set"></a>Olemikogum

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Projekti ülesanded              | Integratsiooniolem projekti ülesande jaoks |

## <a name="entity-flow"></a>Olemi voog

Projekti ülesandeid hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti tegevused.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastenduse seadistamine

Enne kui projekti ülesannete sünkroonimine saab aset leida, peate sünkroonima projekti kontaktid ja projektid.

## <a name="power-query"></a>Power Query

Kui see tingimus on täidetud, siis peate kasutama andmete filtreerimiseks valikut Microsoft Power Query for Excel.

- Teil on projekti tööülesannete hulgas ressursiga seotud kirjed.

Kui peate kasutama Power Queryd, järgige seda suunist.

- Projekti tööülesannete (PSA-st kuni Fini ja Opsi) mallil on vaikefilter, mis välistab ressursile omased kirjed projekti ülesandest, seades filtri  **IsLineTask** olekule **väär**. Kui loote oma malli, peate selle filtri lisama.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näide. Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]