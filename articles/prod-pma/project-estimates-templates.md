---
title: Projekti prognooside sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kestuse prognooside ja projekti kuluprognooside sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999711"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projekti prognooside sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid tööülesandeid, mida kasutatakse projekti kestuse prognooside ja projekti kuluprognooside sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.

> [!NOTE]
> - Projekti ülesannete integreerimine, kulukande kategooriad, kestuse prognoosi ja funktsioonide lukustamine on saadaval versioonis 8.0.
> - Tegelike näitajate integreerimine on saadaval versioonis 8.0.1 või hilisemates.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Andmevoog rakendusest Project Service Automation rakendusse Finance

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt. Andmete integreerimise funktsiooniga saadaolevad integreerimise mallid võimaldavad projekti kestuse prognooside ja projekti kuluprognooside andmete voogu Project Service Automationist Finance’i.

Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekti kestuse prognoosid

### <a name="template-and-tasks"></a>Mall ja ülesanded

Saadaolevatele mallidele Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Projekti kestuse prognooside sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete migreerimise malli nimi:** projekti kestuse prognoosid (PSA-st Fini ja Opsi)
- **Ülesannete nimi projektis:**

    - Kande seosed
    - Kuluprognoosid

### <a name="entity-set"></a>Olemikogum

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Projekti ülesanded              | Projekti kestuse prognooside integratsiooni olem |

### <a name="entity-flow"></a>Olemi voog

Projekti kestuse prognoose hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti kestuse prognoosid.

### <a name="prerequisites"></a>Eeltingimused

Enne projekti kestuse prognooside sünkroonimise toimumist peate sünkroonima projektid, projekti ülesanded ja projekti kulukande kategooriad.

### <a name="power-query"></a>Power Query

Projekti kestuse prognooside mallil peate kasutama lisandmoodulit Microsoft Power Query for Excel, et lõpetada järgmised ülesanded.

- Määrake vaikimisi prognoosimudeli ID, mida kasutatakse, kui integratsioon loob uue kestuse prognoosid.
- Filtreerige ülesandest välja kõik ressursile omased kirjed, mis kestuse prognoosi integreerimises nurjuvad.
- Filtreerige välja kõik tühjad kandekategooria read. Selle ülesande mitte lõpetamine võib põhjustada valesid kestuse prognoose.

#### <a name="set-the-default-forecast-model-id"></a>Vaikimisi prognoosi mudeli ID määramine

Mallis vaikeprognoosi mudeli ID värskendamiseks klõpsake noolt **Vastenda**, et avada vastendamine. Seejärel valige link **Täpsem päring ja filtreerimine**.

- Kui kasutate vaikimisi Projecti kestuse hinnangu (PSA-st Finile ja Opsile) malli, valige loendis **Rakendatud sammud** suvand **Sisestatud tingimus**. Kirjes **Funktsioon** asendage osa **O\_forecast** prognoosi mudeli ID nimega, mida peaks integratsiooniga koos kasutama. Vaikemallil pärineb prognoosi mudeli ID demoandmetest.
- Uue malli loomisel peate selle veeru lisama. Valige Power Querys suvand **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **MudeliID**. Sisestage veeru jaoks tingimus, et kui projektiülesanne ei ole tühi, siis \<enter the forecast model ID\>; muul juhul tühi.

#### <a name="filter-out-resource-specific-records"></a>Ressursikohaste kirjete filtreerimine

Projecti kestuse prognooside (PSA-st Fini ja Opsi) mallil on vaikimisi filter, mis eemaldab kõik ressursile omased kirjed. Kui loote oma malli, peate selle filtri lisama. Valige link **Täpsem pärin ja filtreerimine**, et filtreerida veergu **msdyn\_islinetask**, et ainult kirjed olekuga **Väär** oleksid hõlmatud.

#### <a name="filter-out-empty-transaction-category-rows"></a>Tühjade kandekategooria ridade välja filtreerimine

Peate lisama filtri, et eemaldada kõik read, kus kandekategooriad on tühjad. See toiming on nõutav olenemata sellest, kas kasutate vaikemalli või loote oma malli. See filter eemaldab rakendusest Project Service Automation kõik kokkuvõtteread, mille tõttu rakenduse Finance kestuse prognoos võib olla vale. Valige link **Täpsem päring ja filtreerimine**, et filtreerida välja null-kirjed veerus **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamise näide. Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli ülesande vastendamine andmete integratsioonis](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projekti kuluprognoosid

### <a name="template-and-tasks"></a>Mall ja ülesanded

Projekti kuluprognooside sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete migreerimise malli nimi:** projekti kuluprognoosid (PSA-st Fini ja Opsi)
- **Ülesannete nimi projektis:**

    - Kande seosed 
    - Kuluprognoosid

### <a name="entity-set"></a>Olemikogum

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Kande ühendused    | Projekti kande seoste integratsiooni olem |
| Prognoosiread             | Projekti kuluprognooside integratsiooni olem         |

### <a name="entity-flow"></a>Olemi voog

Projekti kuluprognoose hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projekti kuluprognoosid.

### <a name="prerequisites"></a>Eeltingimused

Enne projekti kuluprognooside sünkroonimise toimumist peate sünkroonima projektid, projekti ülesanded ja projekti kulukande kategooriad.

### <a name="power-query"></a>Power Query

Projekti kuluprognooside mallil peate kasutama lisandmoodulit Power Quer, et lõpetada järgmised ülesanded.

- Filter, et kaasata ainult kuluprognoosi rea kirjeid.
- Määrake vaikimisi prognoosimudeli ID, mida kasutatakse, kui integratsioon loob uue kestuse prognoosid.
- Teisendage arvelduse tüübid.
- Teisendage kandetüübid.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filter, et kaasata ainult kuluprognoosi read

Projecti kuluprognooside (PSA-st Fini ja Opsi) mallil on vaikefilter, mis sisaldab integratsioonis ainult kuluridu. Kui loote oma malli, peate selle filtri lisama. Valige ülesanne **Kande seosed** ja klõpsake seejärel noolt **Vastenda**, et avada vastendamine. Valige link **Täpsem päring ja filtreerimine**. Filtreerige veergu **msdyn\_transactiontype1**, et see sisaldaks ainult atribuuti **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Vaikimisi prognoosi mudeli ID määramine

Mallis vaikeprognoosi mudeli ID värskendamiseks valige ülesanne **Kuluprognoosid** ja klõpsake seejärel noolt **Vastenda**, et avada vastendamine. Valige link **Täpsem päring ja filtreerimine**.

- Kui kasutate vaikimisi Projecti kuluhinnangu (PSA-st Finile ja Opsile) malli, siis valige Power Querys jaotisest **Rakendatud sammud** esimene suvand **Sisestatud tingimus**. Kirjes **Funktsioon** asendage osa **O\_forecast** prognoosi mudeli ID nimega, mida peaks integratsiooniga koos kasutama. Vaikemallil pärineb prognoosi mudeli ID demoandmetest.
- Uue malli loomisel peate selle veeru lisama. Valige Power Querys suvand **Lisa tingimuslik veerg** ja sisestage uue veeru nimi, näiteks **MudeliID**. Sisestage veeru jaoks tingimus, et kui prognoosi rea ID ei ole tühi, siis \<enter the forecast model ID\>; muul juhul tühi.

#### <a name="transform-the-billing-types"></a>Arvelduse tüüpide teisendamine

Projecti kuluprognooside (PSA-st Fini ja Opsi) mall sisaldab tingimusliku veergu, mida kasutatakse integreerimise ajal Project Service Automationist saadud arvelduse tüüpide teisendamiseks. Kui loote oma malli, peate selle tingimusliku veeru lisama. Valige link **Täpsem päring ja filtreerimine** ja valige seejärel **Lisa tingimuslik veerg**. Sisestage uue veeru nimi (nt **ArvelduseTüüp)**. Seejärel sisestage järgmine tingimus.

Kui **msdyn\_billingtype** = 192350000, siis **NonChargeable**  
vastasel juhul kui **msdyn\_billingtype** = 192350001, siis **Chargeable**  
vastasel juhul kui **msdyn\_billingtype** = 192350002, siis **Complimentary**  
vastasel juhul **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Kandetüüpide teisendamine

Projecti kuluprognooside (PSA-st Fini ja Opsi) mall sisaldab tingimusliku veergu, mida kasutatakse integreerimise ajal Project Service Automationist saadud kandetüüpide teisendamiseks. Kui loote oma malli, peate selle tingimusliku veeru lisama. Valige link **Täpsem päring ja filtreerimine** ja valige seejärel **Lisa tingimuslik veerg**. Sisestage uue veeru nimi (nt **Kandetüüp)**. Seejärel sisestage järgmine tingimus.

Kui **msdyn\_transactiontypecode** = 192350000, siis **Kulu**  
vastasel juhul kui **msdyn\_transactiontypecode** = 192350005, siis **Müük**  
vastasel juhul **null**

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näited. Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Kuluprognoosi kannete malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Kuluprognoosi malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]