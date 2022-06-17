---
title: Projekti lepingute ja projektide sünkroonimine otse Project Service Automationist rakendusse Finance
description: Selles artiklis kirjeldatakse malli ja selle aluseks olevaid ülesandeid, mida kasutatakse projektilepingute ja projektide sünkroonimiseks otse Microsoft Dynamics 365 Project Service Automation Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 62a24f3af823d474cbb4d63f8d079c708256a75e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933855"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Projekti lepingute ja projektide sünkroonimine otse Project Service Automationist rakendusse Finance 

[!include[banner](../includes/banner.md)]



Selles artiklis kirjeldatakse malli ja selle aluseks olevaid ülesandeid, mida kasutatakse projektilepingute ja projektide sünkroonimiseks otse Dynamics 365 Project Service Automation Dynamics 365 Finance.

> [!NOTE] 
> Kui kasutate rakendust Enterprise edition 7.3.0, peate installima KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Andmevoog rakendusest Project Service Automation rakendusse Finance

> [!NOTE]
> Enne, kui saate kasutada Project Service Automationist Finance'i integratsioonilahendust, peaksite olema tuttav Dynamics 365 andmete integreerimise funktsiooniga.

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt. Integreerimismall, mis on saadaval andmete integreerimise funktsiooniga võimaldab projekti lepingute, projektide, projekti lepinguridade vaheeesmärkide andmete voogu Project Service Automationist Finance’i.

Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Projektilepingute ja projektide sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integreerimine Dynamics 365 Project Service Automationv2.x-iga
- **Malli nimi andmeintegratsioonis:** projektid ja lepingud (Project Service Automationist Finance'i)
- **Ülesannete nimi projektis:**

    - Projekti lepingud Project Service Automationist Finance'i
    - Projektid Project Service Automationist Finance'i
    - Projekti lepinguread Project Service Automationist Finance'i
    - Projekti lepingurea vahe-etapid Project Service Automationist Finance'i
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integreerimine Dynamics 365 Project Service Automation v3.x-iga
Project Service Automationis on skeemimuutus, mis mõjutab projekti lepingurea vahe-eesmärgi malli ja vajalik on malli v2 versiooni kasutamine, et integreerida Project Service Automation v3.x Dynamics 365-ga.

- **Malli nimi andmeintegratsioonis:** projektid ja lepingud (Project Service Automationi versioonist 3.x rakendusse Finance) - v2
- **Ülesannete nimi projektis:**

    - Projekti lepingud Project Service Automationist Finance'i
    - Projektid Project Service Automationist Finance'i
    - Projekti lepinguread Project Service Automationist Finance'i
    - Projekti lepingurea vahe-etapid Project Service Automationist Finance'i

Enne kui projekti lepingute ja projektide sünkroonimine saab aset leida, peate sünkroonima kontod.

## <a name="entity-set"></a>Olemikogum

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Tellimused                           | Integratsiooniolem projektilepingu jaoks                |
| Projektid                         | Integratsiooniolem projekti jaoks                         |
| Tellimuse read                      | Integratsiooniolem projekti lepingurea jaoks           |
| Projekti lepingurea vahekokkuvõtted | Integratsiooniolem projekti lepingurea vahekokkuvõtte jaoks |

## <a name="entity-flow"></a>Olemi voog

Projektilepinguid hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projektilepigud. Integreerimismalli osana saate seada projektilepingu integreerimisallika Finance'is.

Aja- ja materjali ning fikseeritud hinnaga projekte hallatakse Project Service Automationis ja sünkroonitakse projektidena rakendusse Finance. Malli integreerimise osana saate rakenduses Finance seadistada projektile integratsiooniallika. Praegu toetatakse vaid aja- ja materjali ning fikseeritud hinnaga projekte.


Projekti lepinguridu hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui lepigu arvereeglid. Kui arvelduse meetod erineb vaike-projektitüübist, uuendab sünkroonimine lepingurea projekti projektitüübi ja projektirühma.

Projekti lepinguridade vahekokkuvõtteid hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui lepigu arvereeglite vahekokkuvõtted.

## <a name="project-service-automation-to-finance-integration-solution"></a>Integratsioonilahendus Project Service Automationist rakendusse Finance

Väli **Projektilepingu ID** on saadaval lehel **Projektilepingud**. See väli on muutnud integratsiooni toetamiseks loomuliku ja kordumatu võtme.

Uue projektilepingu loomisel juhul, kui **Projektilepingu ID** väärtust pole veel olemas, genereeritakse see automaatselt numbriseeria abil. Väärtus koosneb järjestusest **ORD**, millele järgneb astmeline numbriseeria ja seejärel kuue märgi järelliide. Siin on näide: **ORD-01022-Z4M9Q0**.

Väli **Projekti number** on saadaval lehel **Projektid**. See väli on muutnud integratsiooni toetamiseks loomuliku ja kordumatu võtme.

Uue projektilepingu loomisel juhul, kui **Projektinumbri** väärtust pole veel olemas, genereeritakse see automaatselt numbriseeria abil. Väärtus koosneb järjestusest **PRJ**, millele järgneb astmeline numbriseeria ja seejärel kuue märgi järelliide. Siin on näide: **PRJ-01049-CCNID0**.

Kui rakendatakse integreerimislahendust Project Service Automationist Finance'i, seab versiooniuuenduse skript välja **Projektilepingu ID** olemasolevatele projektilepingutele ja välja **Projektinumber** olemasolevatele projektidele Project Service Automationis.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastenduse seadistamine

- Enne kui projekti lepingute ja projektide sünkroonimine saab aset leida, peate sünkroonima kontod.
- Lisage seadistatud ühenduses väli integratsioonivõtme väli, mis vastendab **msdyn\_organizationalunits** ja **msdyn\_name \[Name\]**. Võimalik, et peate esmalt lisama projekti ühenduse komplektile. Lisateavet leiate teemast [Andmete integreerimine Common Data Service rakendustele](/powerapps/administrator/data-integrator).
- Lisage seadistatud ühenduses väli integratsioonivõtme väli, mis vastendab **msdyn\_projects** ja **msdynce\_projectnumber \[Project Number\]**. Võimalik, et peate esmalt lisama projekti ühenduse komplektile. Lisateavet leiate teemast [Andmete integreerimine Common Data Service rakendustele](/powerapps/administrator/data-integrator).
- Projekti lepingute ja projektide **SourceDataID**-d saab uuendada erineva väärtusega või eemaldada vastendusest. Malli vaikeväärtuseks on **Project Service Automation**.
- **PaymentTerms** vastendust tuleb värskendada nii, et see kajastaks kehtivaid maksetingimusi Finance'is. Vastenduse saate eemaldada ka projekti tööülesandest. Vaikeväärtuste vastendusel on demo andmete jaoks vaikeväärtused. Järgmises tabelis on toodud väärtused Project Service Automationis.

    | Väärtus | Kirjeldus   |
    |-------|---------------|
    | 1     | Makse 30 päeva jooksul        |
    | 2     | 2% 10 päeva, neto 30 päeva |
    | 3     | Makse 45 päeva jooksul        |
    | 4     | Makse 60 päeva jooksul        |

## <a name="power-query"></a>Power Query

Microsoft Power Query for Excel abil saate andmeid filtreerida, kui on täidetud järgmised tingimused.

- Teil on Dynamics 365 Salesis müügitellimused.
- Teil on Project Service Automationis mitu organisatsiooniüksust ja need üksused vastendatakse mitme juriidilise olemiga Finance'is.

Kui peate kasutama Power Query, järgige järgmisi juhiseid.

- Projektide ja lepingute (PSA-st Fin and Opsini) mallil on vaikefilter, mis sisaldab ainult **Tööde üksuse (msdyn\_ordertype = 192350001)** tüüpi müügitellimusi. See filter aitab tagada, et projektilepinguid ei loodaks Finance'is müügitellimustele. Kui loote oma malli, peate selle filtri lisama.
- Power Query Looge filter, mis hõlmab ainult lepingulisi organisatsioone, mis tuleks sünkroonida integratsiooniühenduse komplekti juriidilise isikuga. Näiteks projekti lepingud, mis on seotud Contoso USA lepingu organisatsioonilise üksusega, tuleb sünkroonida USSI juriidilise isikuga, kuid projektilepingud, mis teil on Contoso Global lepingu organisatsioonilise üksusega tuleb sünkroonida USMF-i juriidilise isikuga. Kui te ei lisa seda filtrit oma tööülesannete vastendamisel, sünkroonitakse kõik projektilepingud juriidilise isikuga, mis on määratletud ühenduse komplekti jaoks, olenemata lepingu organisatsioonilisest üksusest.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE] 
> Välju **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ja **AddressZipCode** ei kaasata projektilepingute jaoks vaikimisi vastendamiseks. Vastendusi saate lisada juhul, kui soovite, et need andmed oleks projektilepingutes sünkroonitud.
>
> Väljad **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ja **ProjectType** ei sisaldu projektide vaikevastendamises. Vastendusi saate lisada juhul, kui soovite, et need andmed oleks projektides sünkroonitud.

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näited. Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Projekti lepingumalli vastendus.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Projektimalli vastendus.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Projekti lepinguridade malli vastendus.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Projekti lepingurea vahe-eesmärgi malli vastendus.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projekti lepingurea vahekokkuvõtte kaardistamine Projektides ja lepingutes (PSA 3.x-st Dynamicsisse) – v2 mall:

[![Projekti lepingurea vahe-eesmärgi malli vastendus versiooni kaks malliga.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]