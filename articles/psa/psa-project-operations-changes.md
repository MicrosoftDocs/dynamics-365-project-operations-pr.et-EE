---
title: Funktsioonide muudatused rakenduselt Project Service Automation rakendusele Project Operations üleminekul
description: See artikkel annab ülevaate funktsioonide muutustest Project Service Automationist rakendusele Dynamics 365 Project Operations.
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459921"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funktsioonide muudatused rakenduselt Project Service Automation rakendusele Project Operations üleminekul

Rakenduse Dynamics 365 Project Service Automation versiooniuuendus rakendusele Dynamics 365 Project Operations Lite tarnitakse kolmes etapis. See artikkel annab teavet peamiste muudatuste kohta, mida võite oodata pärast täiendamist.

| Täienduse kohaletoimetamine | 1. faas <br>(Jaanuar 2022) | 2. faas <br>(November 2022) | 3. faas  |
|------------------|------------------------|---------------------------|---------------------------|
| Ei sõltu projektide tööjaotuse struktuurist (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS kuulub praegu toetatavate Project Operationsi piirangute hulka. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS väljaspool Project Operationsi praegu toetatud piire, sealhulgas Project Desktop Clienti tugi. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektijuhtimine

Kõige olulisemad muudatused kasutajakogemuses toimuvad projektide planeerimise alal. Project Operations võtab kasutusele uue kaasaegse kogemuse tööjaotuse struktuuri (WBS) haldamiseks, võimendades ajastamisvõimalusi, mida pakub [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Erinevused ajakava koostamise kogemuses

Järgmine tabel võtab kokku Project Service Automationi ja Project Operationsi ajakavaerinevused.

|  Plaanimine     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektimallid – võimalus projekti loomisel määratleda ja rakendada projektimalle  |  &nbsp;    | :heavy_check_mark: |
| Projekti tööjaotuse struktuuri (WBS) integreerimine töölauakliendiga   |    &nbsp;  | :heavy_check_mark: |
| Piirangud – alustada mitte varem, lõpetada hiljemalt  | :heavy_check_mark: |   &nbsp;  |
| Vahekokkuvõtted – ülesanded, mille kestus on null   | :heavy_check_mark:  |  &nbsp;  |
| Ressursipõhised ülesanded arvestavad määratud ressursside saadavust   | :heavy_check_mark: |  &nbsp;    |
| Ajaline redigeerimine – plaanide redigeerimine ja igapäevane töötamine   |   &nbsp;  | :heavy_check_mark: |
| Automaatne/käsitsi ajastamine – kasutage projekti ajastamise mootorit ülesannete automaatseks või käsitsi ajastamiseks |  &nbsp; | :heavy_check_mark:  |
| Redigeerige suuri projekte otse kasutajaliideses: redigeeritavate plaanide suurus ei ole piiratud  | 500 ülesande piirang  | :heavy_check_mark:       |
| Täidetud protsent – märkige ülesande edenemine   | :heavy_check_mark:  |  &nbsp;  |
| [Projekti ajakavarežiimid](../project-management/scheduling-modes.md) – projekti määratlemine fikseeritud ühikute, fikseeritud jõupingutuste või fikseeritud kestusega | :heavy_check_mark: | &nbsp; |
| Ajaskaala – ajaskaala vaate koostamine ja kohandamine, et visualiseerida ajakava üksikasju ja suhelda huvirühmadega. | :heavy_check_mark:  | &nbsp; |
| Pingutuspõhised ülesanded – ajastamismootori tugi ülesande ajaplaneerimiseks tööjõupõhisena  | :heavy_check_mark:  | &nbsp; |
| **Ülesande teave** dialoogiboks – ülesande üksikasjade salvestamine dialoogiboksi abil | :heavy_check_mark:  |  &nbsp;  |
| Lohistamine – valige mitu ülesannet ja muutke nende asukohta WBS-is | :heavy_check_mark: | &nbsp;  |
| Paindlikud püsivad vaated – ülesande atribuutide üksikasjalikumate vaadete määratlemine   | :heavy_check_mark:  | &nbsp; |
| WBS-i sortimine ja filtreerimine  | :heavy_check_mark:  | &nbsp; |
| Tahvlivaade mitte-kaskaadprojekti edastamiseks  | :heavy_check_mark:   | &nbsp; |
| Ajajoonevaade – interaktiivne Gantti diagramm, mida kasutatakse WBS-i visualiseerimiseks ja redigeerimiseks   | :heavy_check_mark:  | &nbsp; |
| Klaviatuuri otseteed – kiirklahvide kasutamine levinumate toimingute jaoks, nt taane või sisestamine  | :heavy_check_mark:  |  &nbsp; |
| Mitmetasemeline tagasivõtmine – mis-oleks-kui-analüüs tegemine, et täielikult mõista muudatuste mõju, pöörates tagasi ja rakendades tervet toimingute komplekti | :heavy_check_mark: | &nbsp; |
| Lõika/kopeeri/kleebi – tehke ajakava väljatöötamisel koostööd, kopeerides ja kleepides ajakava üksikasju rakenduste vahel  | :heavy_check_mark: | &nbsp; |
| Tööülesannete kontroll-loendid – kuni 20 kontroll-loendi üksuse lisamine ülesandele   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekti kavandamine

Project Operationsi lehel **Projekt** on märkimisväärne hulk erinevusi võrreldes Project Service Automationi leheküljega **Projekt**.

Järgmised toimingud on 1. etapi versiooniuuenduse osana lehelt **Projektid** eemaldatud.

  - **Ava MS Projectis**
  - **Loo mall**
  - **Eemalda MS Projectiga linkimine**

Rakenduse Project Operations leht **Projekt** sisaldab järgmisi uusi vahekaarte.

- **Materjali prognoosid**
- **Ülesande arvelduse seadistus**

Vahekaart **Olek** on eemaldatud ja väli **Olek** on nüüd projekti ajastamisrežiimiga vahekaardil **Kokkuvõte**.

   ![Värskendused projekti lehel.](media/projectform.png)

Vahekaart **Ajakava** on ümber nimetatud vahekaardiks **Ülesanne** ja sellel on Project for the Webi uus projektiplaneerimise kogemus.

   ![Uus projektiülesannete vahekaart.](media/tasktab.png)

## <a name="scheduling-modes"></a>Plaanimisrežiimid

Project Operations on kasutusele võtnud uue funktsiooni [Ajastamisrežiimid](../project-management/scheduling-modes.md). Kõik olemasolevad Project Service Automationi projektid on rakenduses Project Operations vaikimisi väärtuseks **Fikseeritud kestus**. Uute projektide vaikesätet saab aga hallata, minnes **Sätted** > **Parameetrid** > **Parameeter** > **Ajastamisrežiim**.

   ![Projekti parameetrite sätted ajastamisrežiimi jaoks.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekti planeerimise piirangud

Project Operations tugineb kõigi projekti ajastamistoimingute jaoks Project for the Webile. Project for the Web haldab tööjaotuse struktuuri, kasutades järgmises tabelis toodud piiranguid.

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

Pärast Project Operationsi täiendamist peate kasutama projekti ajastamise API-sid, et käivitada loomis-, värskendamis- ja kustutamistoiminguid järgmistes olemites.

|   Olemi nimi           |   Olemi loogiline nimi       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekti ülesanne            | msdyn_projecttask           |
| Projekti ülesande sõltuvus | msdyn_projecttaskdependency |
| Ressursi määramine     | msdyn_resourceassignment    |
| Projektisalv          | msdyn_projectbucket         |
| Projektimeeskonna liige     | msdyn_projectteam           |

Kui teil on praegu neid üksusi hõlmavad kohandused, vaadake juurutamise juhiseid artiklist [Projekti ajakava API-de kasutamine toimingute tegemiseks ajastamisolemitega](../project-management/schedule-api-preview.md) for implementation guidance.

## <a name="data-model-changes"></a>Andmemudeli muudatused

1. täiendusfaasi osana tehakse andmemudelis muudatusi. Need muudatused on peamiselt olemasolevate olemite väljamuudatused. 1. faasis on olemid **msydn_project** ja **msdyn_projectteam** kohanduste refaktooring. 

> [!IMPORTANT]
> Seda jaotist ajakohastatakse täiendavate olemitega, kui tulevased ajakohastamisetapid on lõpule viidud.

Järgmised väljad on asendatud uute väljadega.

|   Entity          |   Vana loogiline nimi   |   Uus loogiline nimi    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualsales    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedsales   | msdyn_effort          |
| msdyn_project     | msdyn_remainingsales | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_duration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Lisatud on järgmised väljad.

|   Entity          |   Loogiline nimi                               |   Kirjeldus |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualsales                         | Näitab projekti tegelike tasude müügi kogumahtu. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_actualcost_base                     | Näitab projekti tegelike materjalikulude kogusummat. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_actualcost_base                    | Kuvab projekti tegeliku materjalimüügi koondsumma. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Selle projektiga seotud lepingu rida. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | See on süsteemi sisemine väli, mida kasutatakse **Projekti kopeerimine** jaoks, mis on seotud korrelatsiooni identifikaatoriga. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_copyprojectsessionid                   | See on süsteemi sisemine väli, mida kasutatakse **Projekti kopeerimine** jaoks, mis on seotud seansi identifikaatoriga. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Viimati sünkroonitud xRM globaalse redaktsiooni sõne projekti ajastamise teenusest. |
| msdyn_project     | msdyn_msprojectdocument                      | Microsoft Projecti dokument, mis kuulub projektile. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Projekti kavandatud materjalikulude koondsumma. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_plannedmaterialcost                   | Projekti raames kavandatud materjalide müügi koondmaht. Kasutatakse ainult Project Service Automationis. |
| msdyn_project     | msdyn_progress                                | Programm, millega see projekt seotud on. |
| msdyn_project     | msdyn_quotelineid                       | Selle projektiga seostatud hinnapakkumise rida. |
| msdyn_project     | msdyn_replaylogheader                        | Päis vastuselogide jaoks. |
| msdyn_project     | msdyn_scheduledend                           | Projekti kõikide ülesannete puhul kasutatav vaikimisi ajastamisrežiim.  |
| msdyn_project     | msdyn_taskearlieststart                      | Projekti mis tahes ülesande varaseim alguskuupäev.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projektimeeskonna liige, kellelt see projektimeeskonna liige kopeeriti. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirementname | Näitab, kas luua vastloodud üldisele meeskonnaliikmele ressursinõue.  |
| msdyn_projectteam | msdyn_deletestatus                           | Meeskonnaliikme kustutamise olek, et jälgida, kas projekti ajastamisteenusele on saadetud kustutustaotlus ja kas see saadab edukalt vastuse tagasi oodatud ajaakna jooksul. |
| msdyn_projectteam | msdyn_effortcompleted                        | Jälgib meeskonnaliikmete tehtud jõupingutusi nende ülesannete täitmisel. |
| msdyn_projectteam | msdyn_effortremaining                        | Jälgib meeskonnaliikme poolt oma ülesannetega seoses veel lõpuleviimata jõupingutusi. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Ooteaeg alates hetkest, mil meeskonnaliige saadab kustutustaotluse projekti ajastamisteenusele, kuni meeskonnaliikme tegeliku kustutamiseni rakenduses Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Ajatempel, mis salvestab, millal meeskonnaliikme kustutamistaotlus saadetakse projekti ajastamisteenusele. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Kuvab projektimeeskonna liikme, kellelt see projektimeeskonna liige kopeeriti.  |

## <a name="project-templates"></a>Projektimallid

Project Operations ei paku projektimallidele tuge. Siiski saate paljusid põhifunktsioone kopeerida [Projekti kopeerimise API](../project-management/dev-copy-project.md) abil.

## <a name="desktop-add-in-support"></a>Töölaua lisandmooduli tugi

Microsoft Projecti töölaua lisandmooduli tugi ei ole saadaval täienduse 2. esimeses etapis. 3. faasis saavad kliendid, kelle projektid on suuremad kui Project for the Webi praegu toetatavad piirangud, kasutada töölaua lisavõimalust.

## <a name="editing-resource-assignment-contours"></a>Ressursi määramise kontuuride redigeerimine

Võimalus muuta ressursside määramise kontuure on saadaval siis, kui uuenduse 2. faas on saadaval.

## <a name="billing-and-pricing"></a>Arveldamine ja hinnakujundus

Rakendusse Project Operations on lisatud järgmised uued funktsioonid. Need funktsioonid on loomult tigedad ega mõjuta Project Service Automationi andmemudelit.

- [Projektide ja projektiülesannete materjalikasutuse salvestamine](../material/material-usage-log.md)
- [Allhankelepingu haldus](../pro/subcontracting/managing-subcontracts-overview.md)
- [Ettemaksud või honoraril põhinevad lepingud](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Lepingu mitteületamise olek ja kinnitused](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Ülesandepõhine arveldamine](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Iganenud komponendid

Järgmistes tabelites on dokumenteeritud kõik iganenud väljad, mis teisaldatakse pärast täiendamist iganenud komponentide lahendusse. Lisateavet ja lahenduse lingi leiate artiklist [Dynamics 365 Project Service Automation 3x kuni Project Operations 4x iganenud komponendid](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoiceDetail

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
|msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Väljad                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_salescontractline                                                          |

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
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
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
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
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
| msdyn_project.msdyn_stagename                                                                 |
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
| msdyn_projecttask.msdyn_numberofresources                                                     |
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
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
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

