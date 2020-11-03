---
title: Project Service Automationi integreerimise parameetrid
description: Selles teemas selgitatakse, kuidas konfigureerida seda, kuidas rakenduse Microsoft Dynamics 365 for Project Service Automation rakendusega Microsoft Dynamics 365 Finance integreerimisel vaikeandmed sisestatakse.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a0cee090e0ecb306aa3bda62c79a57dfade93c0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075096"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automationi integreerimise parameetrid

[!include[banner](../includes/banner.md)]

Lehel **Project Service Automationi integreerimise parameetrid** saate konfigureerida, kuidas sisestatakse rakenduse Dynamics 365 Project Service Automation rakendusega Dynamics 365 Finance integreerimisel vaikeandmed. Projektide edukaks sünkroonimiseks rakendusest Project Service Automation rakendusse Finance peate seadistama järgmised väljad.

Lehe **Project Service Automationi integreerimise parameetrid** avamiseks minge suvandisse **Projektihaldus ja raamatupidamine** \> **Häälestamine** \> **Dynamics 365 for Project Service Automationi integreerimise parameetrid**. 

> [!NOTE]
> - Projekti ülesannete integreerimine, kulukande kategooriad, kuluprognoosid ja funktsioonide lukustamine on saadaval versioonis 8.0.
> - Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.


| Tabeldusklahv                    | Väli                | Kirjeldus |
|------------------------|----------------------|-------------|
| Üldist                | Projekti vaiketüüp | Valige projekti vaiketüüp. Kui projektid sünkroonitakse rakendusest Project Service Automation, kasutatakse seda väärtust juhul, kui te ei sisestanud integreerimise mallile vaikeväärtust. Sünkroonimise ajal seatakse uute projektide väli **Projekti tüüp** sellele väärtusele. Samas võidakse seda väärtust uuendada, kui projekti lepinguread sünkroonitakse rakendusest Project Service Automation. |
|                        | Ajakategooria        | Valige vaikimisi ajakategooria. Seda väärtust kasutatakse juhul, kui tööaja prognoosid sünkroonitakse rakendusest Project Service Automation. Kui prognoositud töötunnid ja tegelikud töötunnid rakendusest Project Service Automation sünkroonitakse, seatakse rakenduses Finance uue projekti tööaja prognooside väli **Kategooria** sellele väärtusele. |
|                        | Tasu kategooria         | Valige vaikimisi tasu kategooria. Seda väärtust kasutatakse juhul, kui tasu tegelikud näitajad sünkroonitakse rakendusest Project Service Automation. Kui tasu tegelikud näitajad rakendusest Project Service Automation sünkroonitakse, seatakse rakenduses Finance uus tasu kannete väli **Kategooria** sellele väärtusele. |
| Projektirühma vaikesätted | Projekti tüüp         | Klõpsake nuppu **Uus** , et lisada rida, kus saate valida projekti tüübi, mille jaoks projektirühm määrata. Kindel projekti tüüp on võimalik konfiguratsioonis valida ainult üks kord. |
|                        | Projekti rühm        | Valige valitud projekti tüübi jaoks vaikimisi projektirühm. Kui uusi projekte sünkroonitakse rakendusest Project Service Automation, seatakse väli **Projektirühm** projekti tüübi jaoks vaikeväärtusele, kui te ei esitanud integreerimise mallis vaikeväärtust. |
| Arveldustüübi vaikesätted  | Arvelduse tüüp         | Klõpsake nuppu **Uus** , et lisada rida, kus saate valida arvelduse tüübi, mille jaoks määrata vaikimisi rea atribuut. Kindel arvelduse tüüp on võimalik konfiguratsioonis valida ainult üks kord. |
|                        | Rea atribuut        | Valige valitud arvelduse tüübi jaoks vaikimisi rea atribuut. Kui uued tööaja prognoosid, uued kuluprognoosid ja uued tegelikud näitajad rakendusest Project Service Automation sünkroonitakse, seatakse väli **Rea atribuut** arveldustüübi vaikeväärtuses. |
| Funktsioonide lukustamine  | Pole rakendatav       | Valige funktsioon, et keelata rakenduses Finance projektid ja lepingud, mis pärinevad rakenduselt Project Service Automation. Näiteks saate välja lülitada võimaluse muuta lepinguid ja projekte, luua tööjaotuse struktuure ning sisestada Finance'is ajatabelid. Raamatupidamisega seotud väljad on jätkuvalt saadaval, isegi kui need on parameetri sätte poolt muudetud mitte kättesaadavaks. Vaikimisi on kõik funktsioonid lubatud. |
