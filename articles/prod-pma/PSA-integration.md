---
title: Project Service Automationi ülevaade
description: Selles teemas antakse teavet rakenduse Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance integreerimise lahenduse kohta.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642448"
---
# <a name="project-service-automation-overview"></a>Project Service Automationi ülevaade

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida teenuse Common Data Service kaudu andmeid rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation olemite üleselt. Integreerimismallid, mis on saadaval andmete integreerimise funktsiooniga, võimaldavad projektide, projekti lepingute, projekti lepinguridade, projekti lepingurea vahe-eesmärkide, projekti ülesannete, kulu tehingukategooriate, tööaja prognooside ja kuluprognooside voogu Project Service Automationist Finance’i.

> [!NOTE]
> - Kui kasutate versiooni 7.3.0, peate installima KB 4074835. Seejärel saate integreerida fikseeritud hinnaga projekte.
> - Kui kasutate versiooni 7.3.0 ja toote tasulised tehingud Project Service Automationist üle, peate installima KB 4345320, et kaasata need tasud projekti arvesse.
> - Kui kasutate versiooni 8.0, saate kasutada projekti ülesannete integreerimist, kulu kandekategooriaid, tööaja prognoose, kuluprognoose ja funktsioonide lukustamist.
> - Kui kasutate versiooni 8.0.1 või uuemat, on teil võimalik tegelikud näitajad sünkroonida.

Enne, kui saate integreerida Project Service Automationi rakendusse Finance, peate konfigureerima Project Service Automationi integreerimise parameetrid. Lisateavet vt: [Project Service Automationi integreerimise parameetrid](PSA-parameters.md).

See integratsiooni lahendus võimaldab otsest sünkroonimist järgmistel juhtudel.

- Säilitage projektilepingud rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Looge projekte rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Säilitage projekti lepinguread rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Säilitage projekti lepingurea vaheetapid rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Säilitage projekti ülesanded rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Säilitage kulude kandekategooriaid Finance’is ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Looge projektide kestusprognoose rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Looge projektide kuluprognoose rakenduses Project Service Automation ja sünkroonige need otse rakendusest Project Service Automation rakendusse Finance.
- Looge Project Service Automationis projekti aja, kulu ja tasu tegelikud näitajad ning looge Project Service Automationi integreerimise töölehel projekti kanded, et neid saaks Finance’i postitada.

## <a name="data-synchronization"></a>Andmete sünkroonimine

Järgmisel joonisel on näidatud, kuidas andmeid integratsiooni osana rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

> [!NOTE]
> Kõik mallid pole hetkel saadaval. Mallid väljastatakse, kui need lõpetatakse.

[![Project Service Automationi integreerimine rakendusega Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance’i süsteeminõuded

Rakendusest Project Service Automation rakendusse Finance integreerimise lahenduse kasutamiseks peate installima Enterprise’i versiooni 7.3 koos Platformi värskendusega 12 või uuemaga.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automationi süsteeminõuded

Rakendusest Project Service Automation rakendusse Finance integreerimise lahenduse kasutamiseks peate installima järgmised komponendid.

- Dynamics 365 Project Service Automation’i versioon 9.0.0.0 või uuem
- Sularahas lahenduse tõenäosus rakenduses Dynamics 365 Sales, versioon 1.14.0.0 (ver 14) või uuem
- Project Service Automationist Finance’i lahendus rakenduse Dynamics 365 Project Service Automation versiooni 1.0.0.0 või hilisema jaoks

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installige Project Service Automationist Finance’i integreerimise lahendus oma Project Service Automationi olemisse

Laadige Project Service Automationist Finance’i integreerimise lahendus alla [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=57016) ja järgige juhiseid, mis on lahendusega kaasas.
