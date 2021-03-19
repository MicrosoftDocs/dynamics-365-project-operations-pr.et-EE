---
title: Projekti kulukategooriate sünkroonimine rakenduste Finance and Operations ja Project Service Automation vahel
description: Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289634"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekti kulukategooriate sünkroonimine rakenduste Finance and Operations ja Project Service Automation vahel

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.

> [!NOTE]
> - Projekti ülesannete integreerimine, kulukande kategooriad, kuluprognoosid ja funktsioonide lukustamine on saadaval versioonis 8.0.
> - Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.
> - Kui kasutate rakendust Enterprise Edition 7.3.0 pärast KB 4132657 ja KB 4132660 installimist, on teil võimalik kasutada malle, et integreerida projekti tööülesanded, kuluarvestuse kategooriad, tunnihinnangud, kuluhinnangud ja tegelikud näitajad ning konfigureerida funktsioonide lukustamist. Kui te peate arvestuse jaotuse lähtestama, soovitame installida ka KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Andmevoog rakendustele Project Service Automation ja Finance.

Project Service Automationi ja Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt. Andmete integreerimise funktsiooniga saadaolevad integreerimise mallid võimaldavad projekti kandekategooria andmete voogu Finance'i ja Project Service Automationi vahel.

Kui projekti kulukategooriad on Finance'is määratud, toimub kõigepealt integratsioonivoog Finance'ist Project Service Automatitioni. Projekti kulukategooriate integreerimise ID-d värskendatakse sünkroonimise kaudu rakendusest Project Service Automation Finance'i.

Kui projekti kulukategooriad on Project Service Automationis määratud, toimub kõigepealt integratsioonivoog Project Service Automatitionist Finance'i.. Projekti kategooriad peavad Finance'is konfigureeritud juba enne Project Service Automationist sünkroonimist. Seejärel sünkroonige rakendusest Finance tagasi Project Service Automationisse ja seejärel rakendusest Project Service Automation tagasi Finance'i. Sel viisil saate tagada, et kategooriad on lingitud ja duplikaate ei looda.

> [!NOTE]
> Tavaliselt projekti kulukategooriad määratakse Finance'is. Kuid kui nad ei ole või kui kulukategooriad on juba loodud rakendusega Project Service Automation, peate esmalt sünkroonima kasutades projekti kulukannete kategooriate (PSA FIN-i ja Opsi) malli abil. Seejärel sünkroonitakse, kasutades projekti kulukannete kategooriate (Fin ja Ops PSA-sse) malli. Seejärel peaksite käivitama sünkroonimise rakendusest Project Service Automation rakendusse Finance veel üks kord.
>
> Kui sünkroonite esmalt rakendusest Project Service Automation, peavad enne sünkroonimise käivitamist olema Finance'is täidetud järgmised nõuded.
>
> - Ühiskasutusega kategooria, mis vastab Project Service Automationis seadistatud projektikategooriale peab olemas olema, ja see peab olema lubatud nii **projekti** kui ka **kulu** jaoks.
> - Iga Finance'i juriidilise isiku jaoks, mis peab olema integreeritud, peavad olemas olema järgmised projektikategooriad.
>
>     - **Projekti kategooria** on olemas. 
>     - **Kasutamine kulus** on lubatud.
>     - **Aktiivne töölehel** on lubatud.
>     - **Kandetüübiks** on seatud **kulu**.

Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projekti kulukategooria sünkroonimine rakendustest Finance rakendusse Project Service Automation

### <a name="template-and-task"></a>Mall ja ülesanne

Mallile Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Projekti kulukategooriate sünkroonimiseks Finance'ist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Andmete integreerimise malli nimi:** projekti kulukannete kategooriad (Finist ja Opsist PSA-sse)
- **Tööülesande nimi projektis:** kategooriate sünkroonimine PSA-sse

### <a name="entity-set"></a>Olemikogum

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategooriate integreerimise olem | Kandekategooriad     |

### <a name="entity-flow"></a>Olemi voog

Projekti kulukategooriaid hallatakse rakenduses Finance ja need sünkroonitakse rakendusega Project Service Automation kandekategooriad.

### <a name="power-query"></a>Power Query

Kui sünkroonite rakendusega Project Service automation, peate kasutama rakendust Microsoft Power Query Exceli jaoks, et määrata arvetüüp kandekategoorias. Projekti kulukannete kategooriate (Fin ja Ops PSA-sse) mallis on vaikeveerg ja vastendus. Kui loote oma malli, peate lisama tingimusliku veeru Power Query'is. Toimige järgmiselt.

1. Klõpsake noolt, et avada projekti kulu kategooriate ülesande vastendus projekti kulukategooriate (Fin ja Ops PSA-le) malliga.
2. Klõpsake linki **Täpsem päring ja filtreerimine**, et avada Power Query.
2. Valige **Lisa tingimuslik veerg**.
3. Sisestage uue veeru nimi (nt **ArvelduseTüüp)**.
4. Sisestage järgmine tingimus: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klõpsake veerus **OK**.
6. Vastendage see uus veerg kindlasti vastenduse lehel.

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide. Vastendus näitab välja teavet, mis sünkroonitakse Finance'ist Project Service Automationisse.

[![Projekti kulukategooria malli vastendamine rakendusse Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projekti kulukategooria sünkroonimine rakendustest Project Service Automation rakendusse Finance

### <a name="template-and-task"></a>Mall ja ülesanne

Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance'i kasutatakse järgmist malli ja aluseks olevat ülesannet.

- **Andmete integreerimise malli nimi:** projekti kulukannete kategooriad (PSA-st Fini ja Opsi)
- **Tööülesande nimi projektis:** sünkroonimiskategooriad Fin-si Ops-i

### <a name="entity-set"></a>Olemikogum

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Kandekategooriad     | Kategooriate integreerimise olem |

### <a name="entity-flow"></a>Olemi voog

Projekti kulukategooriaid hallatakse rakenduses Finance ja need sünkroonitakse rakendusega Project Service Automation kandekategooriad. Finance'i sünkroonimine värskendab Finance'i projektikategooria Finance'is Project Service Automationi integratsiooni ID-ga.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide.

> [!NOTE]
> Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine Project Service Automationist rakendusse Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]