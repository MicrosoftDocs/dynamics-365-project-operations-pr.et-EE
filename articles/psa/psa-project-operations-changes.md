---
title: Funktsioonimuudatused projekti teenuse automatiseerimisest projektitoiminguteks
description: Selles teemas antakse ülevaade funktsiooni muudatustest project service automationist rakendusse Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595401"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funktsioonimuudatused projekti teenuse automatiseerimisest projektitoiminguteks

Üleminek Dynamics 365 Project Service Automation Lite'ile Dynamics 365 Project Operations tarnitakse kolmes etapis. See teema annab teavet peamiste muudatuste kohta, mida võite oodata, kui täiendus on lõpule viidud.

| Täienduse kohaletoimetamine | 1. etapp <br>(Jaanuar 2022) | 2. etapp <br>(Aprill Wave 2022) | 3. etapp  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektide puhul ei sõltuta tööjaotuse struktuurist (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS sisaldub projektitoimingute praegu toetatavates piirides. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool projektitoimingute praegu toetatud piiranguid, sh projekti töölauakliendi tugi. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektijuhtimine

Kõige olulisemad muudatused kasutajakogemuses on projekti planeerimise valdkonnas. Project Operations võtab kasutusele uue kaasaegse kogemuse tööjaotuse struktuuri (WBS) haldamiseks, kasutades ära Project for the Webi pakutavaid [planeerimisvõimalusi](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Sõiduplaani kogemuse erinevused

Järgmises tabelis on kokku võetud projektiteenuse automatiseerimise ja projektitoimingute plaanimiserinevused.

|  Plaanimine     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektimallid – võime määratleda ja rakendada projektimalle projekti loomisel  |  &nbsp;    | :heavy_check_mark: |
| Projekti tööjaotuse struktuuri (WBS) integreerimine töölauakliendiga   |    &nbsp;  | :heavy_check_mark: |
| Piirangud – alustage mitte varem kui, lõpetage hiljemalt  | :heavy_check_mark: |   &nbsp;  |
| Vahe-eesmärgid – nullkestusega ülesanded   | :heavy_check_mark:  |  &nbsp;  |
| Ressursipõhised ülesanded järgivad määratud ressursside kättesaadavust   | :heavy_check_mark: |  &nbsp;    |
| Etapiviisiline redigeerimine – plaanide redigeerimine ja igapäevane töötamine   |   &nbsp;  | :heavy_check_mark: |
| Automaatne/käsitsi planeerimine – projekti plaanimismootori kasutamine ülesannete automaatseks või käsitsi ajatamiseks |  &nbsp; | :heavy_check_mark:  |
| Suurte projektide redigeerimine otse kasutajaliideses: redigeeritavate plaanide suurus ei ole piiratud  | 500 ülesandelimiit  | :heavy_check_mark:       |
| Lõpetatud protsent – ülesande edenemise märkimine   | :heavy_check_mark:  |  &nbsp;  |
| [Projekti ajakava režiimid](../project-management/scheduling-modes.md) – määratlege projekt fikseeritud ühikute, fikseeritud pingutuse või fikseeritud kestusena. | :heavy_check_mark: | &nbsp; |
| Ajaskaala – ajaskaala vaate koostamine ja kohandamine ajakava üksikasjade visualiseerimiseks ja sidusrühmadega suhtlemiseks. | :heavy_check_mark:  | &nbsp; |
| Pingutustest ajendatud ülesanded – mootori toe plaanimine ülesande kavandamiseks pingelisena  | :heavy_check_mark:  | &nbsp; |
| **Dialoogiboks Tööülesandeteave** – ülesande üksikasjade salvestamine dialoogiboksi abil | :heavy_check_mark:  |  &nbsp;  |
| Lohistamine – mitme valikuga ülesanded ja nende asukoha muutmine WBS-is | :heavy_check_mark: | &nbsp;  |
| Paindlikud püsivad vaated – ülesandeatribuutide üksikasjalikumate vaadete määratlemine   | :heavy_check_mark:  | &nbsp; |
| WBS-i sortimine ja filtreerimine  | :heavy_check_mark:  | &nbsp; |
| Plaatide vaade mitte-juga projekti kohaletoimetamiseks  | :heavy_check_mark:   | &nbsp; |
| Ajaskaala vaade – interaktiivne Gantti diagramm, mida kasutatakse WBS-i visualiseerimiseks ja redigeerimiseks   | :heavy_check_mark:  | &nbsp; |
| Kiirklahvid – kiirklahvide kasutamine levinud toimingute puhul (nt taane või lisamine)  | :heavy_check_mark:  |  &nbsp; |
| Mitmetasandiline tagasivõtmine - tehke mis-kui-analüüs, et täielikult mõista muutuste mõju, tühistades ja rakendades uuesti kogu toimingute komplekti | :heavy_check_mark: | &nbsp; |
| Lõikamine/kopeerimine/kleepimine – tehke koostööd ajakava väljatöötamisel, kopeerides ja kleepides ajakava üksikasjad rakenduste vahel  | :heavy_check_mark: | &nbsp; |
| Ülesande kontroll-loendid – ülesandele kuni 20 kontroll-loendiüksuse lisamine   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekti kavandamine

**Projektitoimingute lehel Projekt** on projektitoimingutes võrreldes projektiteenuste automatiseerimise lehega Project **märkimisväärseid erinevusi**.

1. etapi täienduse käigus on lehelt **Projektid** eemaldatud järgmised toimingud.

  - **Ava MS Projectis**
  - **Loo mall**
  - **Eemalda MS Projectiga linkimine**

Project Operationsi **leht Projekt** sisaldab järgmisi uusi vahekaarte.

- **Materjali prognoosid**
- **Ülesande arvelduse seadistus**

Vahekaart **Olek** on eemaldatud ja **väli Olek** on nüüd projekti plaanimisrežiimi vahekaardil **Kokkuvõte**.

   ![Projekti lehe värskendused.](media/projectform.png)

Vahekaart **Ajakava** on ümber nimetatud vahekaardile **Ülesanne** ja see sisaldab uut projektiplaneerimise kogemust project for the Webiga.

   ![Vahekaart Uued projektiülesanded.](media/tasktab.png)

## <a name="scheduling-modes"></a>Plaanimisrežiimid

Project Operations on kasutusele võtnud uue funktsiooni [Plaanimisrežiimid](../project-management/scheduling-modes.md). Kõik olemasolevad projektiteenuste automatiseerimise projektid vaikimisi olekusse **Fikseeritud kestus** projektitoimingutes. Uute projektide vaikeväärtust saab siiski hallata **seadete** > **parameetrite parameetrite ajakava** > **režiimi** > **avamisega**.

   ![Plaanimisrežiimi projektiparameetri sätted.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekti planeerimise limiidid

Projektitoimingud tuginevad kõigi projekti planeerimise toimingute puhul Project for the Web'ile. Veebiprojekt haldab tööjaotuse struktuuri, kasutades järgmises tabelis olevaid piiranguid.

| **Väli**                                          | **Piirang**             |
|----------------------------------------------------|-----------------------|
| Projekti ülesannete maksimaalne koguarv                  | 500                   |
| Projekti maksimaalne kogukestus               | 3650 päeva (10 aastat)  |
| Projekti ressursside maksimaalne koguarv              | 300                   |
| Projekti linkide maksimaalne koguarv (ainult järglane) | 600                   |
| Projekti kohandatud väljade maksimaalne koguarv          | 10                    |
| Maksimaalne hierarhiatase                            | 10 taset             |
| Maksimaalne linkide arv (eelkäija + järglane)            | 20                    |
| Lehe ülesande maksimaalne kestus                      | 1250 päeva             |
| Kokkuvõtva ülesande maksimaalne kestus                 | 3650 päeva (10 aastat)  |
| Ülesandele määratud maksimaalne ressursside arv               | 20 ressurssi          |
| Ülesande toetatud kuupäevavahemik                    | 1/1/2000–12/31/2149 |
| Kontroll-loendi üksused                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projekti planeerimise laiendatavus ja arendamine

Pärast project Operationsile üleminekut peate kasutama projekti plaanimise API-sid, et käivitada järgmiste olemite loomise, värskendamise ja kustutamise toimingud.

|   Olemi nimi           |   Olemi loogiline nimi       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekti ülesanne            | msdyn_projecttask           |
| Projekti ülesande sõltuvus | msdyn_projecttaskdependency |
| Ressursi määramine     | msdyn_resourceassignment    |
| Projektisalv          | msdyn_projectbucket         |
| Projektimeeskonna liige     | msdyn_projectteam           |

Kui teil on praegu neid olemeid hõlmavaid kohandusi, lugege teemat [Projekti ajakava API-de kasutamine operatsioonide tegemiseks plaanimisolemitega](../project-management/schedule-api-preview.md) juurutusjuhiste saamiseks.

## <a name="data-model-changes"></a>Andmemudeli muudatused

Täiendusetapi 1 osana on andmemudelis muudatusi. Need muudatused on peamiselt olemasolevate olemite väljamuudatused. 1. etapis on olemid, **msydn_project** ja **msdyn_projectteam** kohanduste ümberpaigutamine. 

> [!IMPORTANT]
> Seda jaotist värskendatakse täiendavate olemitega, kui tulevased versioonitäiendusetapid on lõpule viidud.

Järgmised väljad on asendatud uute väljadega.

|   Entity          |   Vana loogiline nimi   |   Uus loogiline nimi    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Lisatud on järgmised väljad.

|   Entity          |   Loogiline nimi                               |   Kirjeldus |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Kuvab projekti tegeliku tasumüügi kogusumma. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_actualmaterialcost                     | Kuvab projekti tegeliku materjalikulu kokkuvõtte. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_actualmaterialsales                    | Kuvab projekti tegeliku materjalimüügi koondandmed. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Selle projektiga seotud lepingurida. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | See on sisemine süsteemiväli, mida kasutatakse korrelatsiooni identifikaatoriga seotud projekti **kopeerimiseks**. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_copyprojectsessionid                   | See on sisemine süsteemiväli, mida kasutatakse seansi identifikaatoriga seotud projekti **kopeerimiseks**. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Viimane sünkroonimine xRM-i globaalne revisjoniluba projekti planeerimise teenusest. |
| msdyn_project     | msdyn_msprojectdocument                      | Projekti kuuluv Microsoft Projecti dokument. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Projekti plaanitud materjalikulu kogusumma. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Projekti plaanitud materjalimüügi kogusumma. Kasutamiseks ainult Project Service Automationis. |
| msdyn_project     | msdyn_program                                | Programm, millega see projekt seotud on. |
| msdyn_project     | msdyn_quotelineproject                       | Selle projektiga seotud hinnapakkumisrida. |
| msdyn_project     | msdyn_replaylogheader                        | Taasesituslogide päis. |
| msdyn_project     | msdyn_schedulemode                           | Vaikeplaneerimisrežiim, mida kasutatakse projekti kõigi ülesannete jaoks.  |
| msdyn_project     | msdyn_taskearlieststart                      | Projekti mis tahes ülesande varaseim alguskuupäev.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projektimeeskonna liige, kellelt see projektimeeskonna liige kopeeriti. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Näitab, kas luua ressursinõue vastloodud üldisele meeskonnaliikmele.  |
| msdyn_projectteam | msdyn_deletestatus                           | Meeskonnaliikme kustutamise olek, et jälgida, kas projekti plaanimisteenusele saadetakse kustutamistaotlus ja kas see saadab vastuse oodatud aja jooksul edukalt tagasi. |
| msdyn_projectteam | msdyn_effortcompleted                        | Jälgib meeskonnaliikme pingutusi oma ülesannete täitmisel. |
| msdyn_projectteam | msdyn_effortremaining                        | Jälgib jõupingutusi, mida meeskonnaliige peab oma ülesannete täitmisel veel lõpule viima. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Ooteaeg alates hetkest, mil meeskonnaliige saadab projekti plaanimisteenusele kustutamistaotluse, kuni meeskonnaliige tegelikult rakenduses kustutatakse Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Ajatempel, mis salvestatakse, kui meeskonnaliikme kustutamistaotlus projekti plaanimisteenusele saadetakse. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Kuvab projektimeeskonna liikme, kellelt see projektimeeskonna liige kopeeriti.  |

## <a name="project-templates"></a>Projektimallid

Projektitoimingud ei toeta projektimalle. Kuid projekti koopia API abil saate kopeerida suure osa [põhifunktsioonidest](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Töölaua lisandmooduli tugi

Microsoft Project Desktopi lisandmooduli tugi pole versioonitäienduse kahes esimeses etapis saadaval. 3. etapis saavad kliendid, kelle projektid on suuremad kui Project for the Webi praegu toetatud limiidid, kasutada töölaua lisandmoodulit.

## <a name="editing-resource-assignment-contours"></a>Ressursimääramise kontuuride redigeerimine

Ressursimääramise kontuure redigeerimise võimalus on saadaval siis, kui versioonitäienduse 2. etapp on saadaval.

## <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Project Operationsi on lisatud järgmised uued funktsioonid. Need funktsioonid on oma olemuselt lisaained ja ei mõjuta projekti teenuse automatiseerimise andmemudelit.

- [Materjalikasutuse salvestamine projektides ja projektiülesannetes](../material/material-usage-log.md)
- [Alltöövõtu haldamine](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Leping, mis ei ületa olekut ja valideerimisi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Ülesandepõhine arveldamine](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Aegunud komponendid

Järgmistes tabelites dokumenteeritakse kõik aegunud väljad, mis teisaldatakse aegunud komponentide lahenduse juurdetäienduse konteerimise järel. Lisateavet ja linki lahendusele leiate teemast [Dynamics 365 Project Service Automation 3x versioonile Project Operations 4x aegunud komponendid](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entitynimi                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exporttatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_summethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagenimi                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_number ofources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantssaadav                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

