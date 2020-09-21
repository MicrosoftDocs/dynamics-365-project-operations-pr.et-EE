---
title: Projekti lepingute ja projektide sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevaid tööülesandeid, mida kasutatakse projektilepingute ja projektide sünkroonimiseks otse rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750915"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projekti lepingute ja projektide sünkroonimine otse rakendusest Project Service Automation rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malli ja aluseks olevaid tööülesandeid, mida kasutatakse projektilepingute ja projektide sünkroonimiseks otse rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.

> [!NOTE] 
> Kui kasutate rakendust Enterprise edition 7.3.0, peate installima KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Andmevoog rakendusest Project Service Automation rakendusse Finance

> [!NOTE]
> Enne, kui saate kasutada Project Service Automationist Finance'i integratsioonilahendust, peaksite olema tuttav Dynamics 365 andmete integreerimise funktsiooniga.

Project Service Automationist Finance’i integreerimise lahendus kasutab andmete integreerimise funktsiooni, et sünkroonida andmeid rakenduste Project Service Automation ja Finance olemite üleselt. Integreerimismall, mis on saadaval andmete integreerimise funktsiooniga võimaldab projekti lepingute, projektide, projekti lepinguridade vaheeesmärkide andmete voogu Project Service Automationist Finance’i.

Järgmisel joonisel on näidatud, kuidas andmeid rakenduste Project Service Automation ja Finance vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks rakendusega Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele Microsoft Power Appsi halduskeskuses juurdepääsuks valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Projektilepingute ja projektide sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integreerimine Dynamics 365 Project Service Automationv2.x-iga
- **Andmete integreerimise malli nimi:** Pprojektid ja lepingud (PSA-st Fin and Opsi)
- **Ülesannete nimi projektis:**

    - Projektilepingud PSA-st Fin and Opsi
    - Projektid PSA-st Fin and Opsi
    - Projekti lepinguread PSA-st Fin and Opsi
    - Projekti lepingurea vahe-eesmärgid PSA-st Fin and Opsi
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integreerimine Dynamics 365 Project Service Automation v3.x-iga
Project Service Automationis on skeemimuutus, mis mõjutab projekti lepingurea vahe-eesmärgi malli ja vajalik on malli v2 versiooni kasutamine, et integreerida Project Service Automation v3.x Dynamics 365-ga.

- **Andmete integreerimise malli nimi:** Projektid ja lepingud (PSA 3.x-st Fin and Opsi) - v2
- **Ülesannete nimi projektis:**

    - Projektilepingud PSA-st Fin and Opsi
    - Projektid PSA-st Fin and Opsi
    - Projekti lepinguread PSA-st Fin and Opsi
    - Projekti lepingurea vahe-eesmärgid PSA-st Fin and Opsi

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

Aja- ja materjaliprojekte ja fikseeritud hinnaga projekte hallatakse rakenduses Project Service Automation ja need sünkroonitakse rakendusega Finance kui projektid. Integreerimismalli osana saate seada projekti integreerimisallika Finance'is.

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
- Lisage seadistatud ühenduses väli integratsioonivõtme väli, mis vastendab **msdyn\_organizationalunits** ja **msdyn\_name \[Name\]**. Võimalik, et peate esmalt lisama projekti ühenduse komplektile. Lisateavet leiate teemast [Andmete integreerimine Common Data Service rakendustele](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Lisage seadistatud ühenduses väli integratsioonivõtme väli, mis vastendab **msdyn\_projects** ja **msdynce\_projectnumber \[Project Number\]**. Võimalik, et peate esmalt lisama projekti ühenduse komplektile. Lisateavet leiate teemast [Andmete integreerimine Common Data Service rakendustele](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Projekti lepingute ja projektide **SourceDataID**-d saab uuendada erineva väärtusega või eemaldada vastendusest. Malli vaikeväärtuseks on **Project Service Automation**.
- **PaymentTerms** vastendust tuleb värskendada nii, et see kajastaks kehtivaid maksetingimusi Finance'is. Vastenduse saate eemaldada ka projekti tööülesandest. Vaikeväärtuste vastendusel on demo andmete jaoks vaikeväärtused. Järgmises tabelis on toodud väärtused Project Service Automationis.

    | Väärtus | Kirjeldus   |
    |-------|---------------|
    | 1     | Makse 30 päeva jooksul        |
    | 2     | 2% 10 päeva, neto 30 päeva |
    | 3     | Makse 45 päeva jooksul        |
    | 4     | Makse 60 päeva jooksul        |

## <a name="power-query"></a>Power Query

Kui järgmised tingimused on täidetud, siis peate kasutama andmete filtreerimiseks valikut Microsoft Power Query for Excel.

- Teil on Dynamics 365 Salesis müügitellimused.
- Teil on Project Service Automationis mitu organisatsiooniüksust ja need üksused vastendatakse mitme juriidilise olemiga Finance'is.

Kui peate kasutama Power Queryd, järgige neid suuniseid.

- Projektide ja lepingute (PSA-st Fin and Opsini) mallil on vaikefilter, mis sisaldab ainult **Tööde üksuse (msdyn\_ordertype = 192350001)** tüüpi müügitellimusi. See filter aitab tagada, et projektilepinguid ei loodaks Finance'is müügitellimustele. Kui loote oma malli, peate selle filtri lisama.
- Peate looma Power Query filtri, mis hõlmab ainult neid lepingulisi organisatsioone, mis tuleb integratsiooni ühenduskomplekti juriidilise olemiga sünkroonida. Näiteks projekti lepingud, mis on seotud Contoso USA lepingu organisatsioonilise üksusega, tuleb sünkroonida USSI juriidilise isikuga, kuid projektilepingud, mis teil on Contoso Global lepingu organisatsioonilise üksusega tuleb sünkroonida USMF-i juriidilise isikuga. Kui te ei lisa seda filtrit oma tööülesannete vastendamisel, sünkroonitakse kõik projektilepingud juriidilise isikuga, mis on määratletud ühenduse komplekti jaoks, olenemata lepingu organisatsioonilisest üksusest.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE] 
> Välju **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ja **AddressZipCode** ei kaasata projektilepingute jaoks vaikimisi vastendamiseks. Vastendusi saate lisada juhul, kui soovite, et need andmed oleks projektilepingutes sünkroonitud.
>
> Väljad **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ja **ProjectType** ei sisaldu projektide vaikevastendamises. Vastendusi saate lisada juhul, kui soovite, et need andmed oleks projektides sünkroonitud.

Järgmisel joonisel on toodud andmete integratsioonis malli ülesande vastendamiste näited. Vastendus näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Malli vastendamine](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Malli vastendamine](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Malli vastendamine](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projekti lepingurea vahekokkuvõtte kaardistamine Projektides ja lepingutes (PSA 3.x-st Dynamicsisse) – v2 mall:

[![Malli vastendamine](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
