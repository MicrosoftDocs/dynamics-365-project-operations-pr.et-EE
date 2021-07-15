---
title: Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks
description: Selles teemas on toodud teave ja näited projekti ajakava API-de kasutamise kohta.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293222"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

> [!IMPORTANT] 
> Osad või kõik selles teemas märgitud funktsioonid on saadaval suunatud kasutajatele osana eelversiooni väljaandest. Sisu ja funktsioonid võivad muutuda. 

## <a name="scheduling-entities"></a>Olemite ajastamine

Projekti ajakava API-d annavad võimaluse teha **ajastamise olemitega** loomise, värskendamise ja kustutamise toiminguid. Neid olemeid hallatakse veebirakenduse Project ajastamise mootori kaudu. Suvandiga **Olemite ajastamine** toimingute loomine, värskendamine ja kustutamine oli rakenduse Dynamics 365 Project Operations varasemates väljaannetes piiratud.

Järgmises tabelid on toodud projekti ajakava olemite täielik loend.

| Olemi nimi  | Olemi loogiline nimi |
| --- | --- |
| Project | msdyn_project |
| Projekti ülesanne  | msdyn_projecttask  |
| Projekti ülesande sõltuvus  | msdyn_projecttaskdependency  |
| Ressursi määramine | msdyn_resourceassignment |
| Projektisalv  | msdyn_projectbucket |
| Projektimeeskonna liige | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet on tööühiku muster, mida saab kasutada juhul, kui kandes tuleb töödelda mitut ajakava mõjutavat taotlust.

## <a name="project-schedule-apis"></a>Projekti ajakava API-d

Järgnev on praeguste projekti ajakava API-de loend.

- **msdyn_CreateProjectV1**: seda API-d saab kasutada projekti loomiseks. Projekt ja vaikimisi projektisalv luuakse kohe.
- **msdyn_CreateTeamMemberV1**: seda API-d saab kasutada projektimeeskonna liikme loomiseks. Meeskonnaliikme kirje luuakse kohe.
- **msdyn_CreateOperationSetV1**: seda API-d saab kasutada mitme taotluse ajastamiseks, mis tuleb kande sees teha.
- **msdyn_PSSCreateV1**: seda API-d saab kasutada olemi loomiseks. Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab loomistoimingut.
- **msdyn_PSSUpdateV1**: seda API-d saab kasutada olemi uuendamiseks. Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab värskendamistoimingut.
- **msdyn_PSSDeleteV1**: seda API-d saab kasutada olemi kustutamiseks. Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab kustutamistoimingut.
- **msdyn_ExecuteOperationSetV1**: seda API-d kasutatakse antud toimingute komplektis kõikide toimingute täitmiseks.

## <a name="using-project-schedule-apis-with-operationset"></a>Projekti ajakava API-de kasutamine väärtusega OperationSet

Kuna nii API **CreateProjectV1** kui ka **CreateTeamMemberV1** kirjed luuakse kohe, ei saa neid API-sid olemis **OperationSet** otse kasutada. Samas saate kasutada API-d, et luua vajalikke kirjeid, luua üksuse **OperationSet** ja kasutada seejärel neid eelnevalt loodud kirjeid üksuses **OperationSet**.

## <a name="supported-operations"></a>Toetatud toimingud

| Olemi ajastamine | Koosta | Värskendus | Kustutusklahv (Delete) | Olulised kaalutlused |
| --- | --- | --- | --- | --- |
Projekti ülesanne | Ja | Ja | Ja | Pole |
| Projektiülesande sõltuvus | Ja | Ja | | Projektiülesande sõltuvuskirjeid ei värskendata. Selle asemel saab vana kirje kustutada ja luua uue kirje. |
| Ressursi määramine | Ja | Ja | | Järgmiste väljadega toiminguid ei toetata: **BookableResourceID** (Broneeritava ressursi ID), **Effort** (Panus), **EffortCompleted** (Lõpule viidud panus), **EffortRemaining** (Järelejäänud panus) ja **PlannedWork** (Planeeritud töö). Ressursi määramise kirjeid ei värskendata. Selle asemel saab vana kirje kustutada ja luua uue kirje. |
| Projektisalv | Puudub | Puudub | Puudub | Vaikesalv luuakse API-d **CreateProjectV1** kasutades. |
| Projektimeeskonna liige | Ja | Ja | Ja | Kasutage loomistoiminguks API-d **CreateTeamMemberV1**. |
| Project | Ja | Ja | Puudub | Järgmiste väljadega toiminguid ei toetata: **StateCode** (Olekukood), **BulkGenerationStatus** (Hulgiloomise olek), **GlobalRevisionToken** (Üldine redaktsioonitõend), **CalendarID** (Kalendri ID), **Effort** (Panus), **EffortCompleted** (Lõpule jõudnud panus), **EffortRemaining** (Järelejäänud panus), **Progress** (Edenemine), **Finish** (Lõpp), **TaskEarliestStart** (Ülesande varajaseim algus) ja **Duration** (Kestus). |

Neid API-sid saab kutsuda olemiobjektidega, mis sisaldavad kohandatud välju.

ID atribuut on valikuline. Kui see on antud, proovib süsteem seda kasutada ja loob erandi, kui seda ei saa kasutada. Kui seda ei ole antud, loob süsteem selle.

## <a name="restricted-fields"></a>Piiratud väljad

Järgmistes tabelites määratletakse väljad, mille **loomine** ja **redigeerimine** on piiratud.

### <a name="project-task"></a>Projekti ülesanne

| **Loogiline nimi**                       | **Saab luua** | **Saab redigeerida**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ei             | ei               |
| msdyn_actualcost_base                  | ei             | ei               |
| msdyn_actualend                        | ei             | ei               |
| msdyn_actualsales                      | ei             | ei               |
| msdyn_actualsales_base                 | ei             | ei               |
| msdyn_actualstart                      | ei             | ei               |
| msdyn_costatcompleteestimate           | ei             | ei               |
| msdyn_costatcompleteestimate_base      | ei             | ei               |
| msdyn_costconsumptionpercentage        | ei             | ei               |
| msdyn_effortcompleted                  | ei             | ei               |
| msdyn_effortestimateatcomplete         | ei             | ei               |
| msdyn_iscritical                       | ei             | ei               |
| msdyn_iscriticalname                   | ei             | ei               |
| msdyn_ismanual                         | ei             | ei               |
| msdyn_ismanualname                     | ei             | ei               |
| msdyn_ismilestone                      | ei             | ei               |
| msdyn_ismilestonename                  | ei             | ei               |
| msdyn_LinkStatus                       | ei             | ei               |
| msdyn_linkstatusname                   | ei             | ei               |
| msdyn_msprojectclientid                | ei             | ei               |
| msdyn_plannedcost                      | ei             | ei               |
| msdyn_plannedcost_base                 | ei             | ei               |
| msdyn_plannedsales                     | ei             | ei               |
| msdyn_plannedsales_base                | ei             | ei               |
| msdyn_pluginprocessingdata             | ei             | ei               |
| msdyn_progress                         | ei             | ei (jah P4W jaoks) |
| msdyn_remainingcost                    | ei             | ei               |
| msdyn_remainingcost_base               | ei             | ei               |
| msdyn_remainingsales                   | ei             | ei               |
| msdyn_remainingsales_base              | ei             | ei               |
| msdyn_requestedhours                   | ei             | ei               |
| msdyn_resourcecategory                 | ei             | ei               |
| msdyn_resourcecategoryname             | ei             | ei               |
| msdyn_resourceorganizationalunitid     | ei             | ei               |
| msdyn_resourceorganizationalunitidname | ei             | ei               |
| msdyn_salesconsumptionpercentage       | ei             | ei               |
| msdyn_salesestimateatcomplete          | ei             | ei               |
| msdyn_salesestimateatcomplete_base     | ei             | ei               |
| msdyn_salesvariance                    | ei             | ei               |
| msdyn_salesvariance_base               | ei             | ei               |
| msdyn_scheduleddurationminutes         | ei             | ei               |
| msdyn_scheduledend                     | ei             | ei               |
| msdyn_scheduledstart                   | ei             | ei               |
| msdyn_schedulevariance                 | ei             | ei               |
| msdyn_skipupdateestimateline           | ei             | ei               |
| msdyn_skipupdateestimatelinename       | ei             | ei               |
| msdyn_summary                          | ei             | ei               |
| msdyn_varianceofcost                   | ei             | ei               |
| msdyn_varianceofcost_base              | ei             | ei               |

### <a name="project-task-dependency"></a>Projektiülesande sõltuvus

| **Loogiline nimi**              | **Saab luua** | **Saab redigeerida** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ei             | ei           |
| msdyn_linktypename            | ei             | ei           |
| msdyn_predecessortask         | jah            | ei           |
| msdyn_predecessortaskname     | jah            | ei           |
| msdyn_project                 | jah            | ei           |
| msdyn_projectname             | jah            | ei           |
| msdyn_projecttaskdependencyid | jah            | ei           |
| msdyn_successortask           | jah            | ei           |
| msdyn_successortaskname       | jah            | ei           |

### <a name="resource-assignment"></a>Ressursi määramine

| **Loogiline nimi**             | **Saab luua** | **Saab redigeerida** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | jah            | ei           |
| msdyn_bookableresourceidname | jah            | ei           |
| msdyn_bookingstatusid        | ei             | ei           |
| msdyn_bookingstatusidname    | ei             | ei           |
| msdyn_committype             | ei             | ei           |
| msdyn_committypename         | ei             | ei           |
| msdyn_effort                 | ei             | ei           |
| msdyn_effortcompleted        | ei             | ei           |
| msdyn_effortremaining        | ei             | ei           |
| msdyn_finish                 | ei             | ei           |
| msdyn_plannedcost            | ei             | ei           |
| msdyn_plannedcost_base       | ei             | ei           |
| msdyn_plannedcostcontour     | ei             | ei           |
| msdyn_plannedsales           | ei             | ei           |
| msdyn_plannedsales_base      | ei             | ei           |
| msdyn_plannedsalescontour    | ei             | ei           |
| msdyn_plannedwork            | ei             | ei           |
| msdyn_projectid              | jah            | ei           |
| msdyn_projectidname          | ei             | ei           |
| msdyn_projectteamid          | ei             | ei           |
| msdyn_projectteamidname      | ei             | ei           |
| msdyn_start                  | ei             | ei           |
| msdyn_taskid                 | ei             | ei           |
| msdyn_taskidname             | ei             | ei           |
| msdyn_userresourceid         | ei             | ei           |

### <a name="project-team-member"></a>Projektimeeskonna liige

| **Loogiline nimi**                                 | **Saab luua** | **Saab redigeerida** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ei             | ei           |
| msdyn_creategenericteammemberwithrequirementname | ei             | ei           |
| msdyn_deletestatus                               | ei             | ei           |
| msdyn_deletestatusname                           | ei             | ei           |
| msdyn_effort                                     | ei             | ei           |
| msdyn_effortcompleted                            | ei             | ei           |
| msdyn_effortremaining                            | ei             | ei           |
| msdyn_finish                                     | ei             | ei           |
| msdyn_hardbookedhours                            | ei             | ei           |
| msdyn_hours                                      | ei             | ei           |
| msdyn_markedfordeletiontimer                     | ei             | ei           |
| msdyn_markedfordeletiontimestamp                 | ei             | ei           |
| msdyn_msprojectclientid                          | ei             | ei           |
| msdyn_percentage                                 | ei             | ei           |
| msdyn_requiredhours                              | ei             | ei           |
| msdyn_softbookedhours                            | ei             | ei           |
| msdyn_start                                      | ei             | ei           |

### <a name="project"></a>Project

| **Loogiline nimi**                       | **Saab luua** | **Saab redigeerida** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ei             | ei           |
| msdyn_actualexpensecost_base           | ei             | ei           |
| msdyn_actuallaborcost                  | ei             | ei           |
| msdyn_actuallaborcost_base             | ei             | ei           |
| msdyn_actualsales                      | ei             | ei           |
| msdyn_actualsales_base                 | ei             | ei           |
| msdyn_contractlineproject              | jah            | ei           |
| msdyn_resourceorganizationalunitid     | jah            | ei           |
| msdyn_contractorganizationalunitidname | jah            | ei           |
| msdyn_costconsumption                  | ei             | ei           |
| msdyn_costatcompleteestimate           | ei             | ei           |
| msdyn_costestimateatcomplete_base      | ei             | ei           |
| msdyn_costvariance                     | ei             | ei           |
| msdyn_costvariance_base                | ei             | ei           |
| msdyn_duration                         | ei             | ei           |
| msdyn_effort                           | ei             | ei           |
| msdyn_effortcompleted                  | ei             | ei           |
| msdyn_effortestimateatcompleteeac      | ei             | ei           |
| msdyn_effortremaining                  | ei             | ei           |
| msdyn_finish                           | jah            | jah          |
| msdyn_globalrevisiontoken              | ei             | ei           |
| msdyn_islinkedtomsprojectclient        | ei             | ei           |
| msdyn_islinkedtomsprojectclientname    | ei             | ei           |
| msdyn_linkeddocumenturl                | ei             | ei           |
| msdyn_msprojectdocument                | ei             | ei           |
| msdyn_msprojectdocumentname            | ei             | ei           |
| msdyn_plannedexpensecost               | ei             | ei           |
| msdyn_plannedexpensecost_base          | ei             | ei           |
| msdyn_plannedlaborcost                 | ei             | ei           |
| msdyn_plannedlaborcost_base            | ei             | ei           |
| msdyn_plannedsales                     | ei             | ei           |
| msdyn_plannedsales_base                | ei             | ei           |
| msdyn_progress                         | ei             | ei           |
| msdyn_remainingcost                    | ei             | ei           |
| msdyn_remainingcost_base               | ei             | ei           |
| msdyn_remainingsales                   | ei             | ei           |
| msdyn_remainingsales_base              | ei             | ei           |
| msdyn_replaylogheader                  | ei             | ei           |
| msdyn_salesconsumption                 | ei             | ei           |
| msdyn_salesestimateatcompleteeac       | ei             | ei           |
| msdyn_salesestimateatcompleteeac_base  | ei             | ei           |
| msdyn_salesvariance                    | ei             | ei           |
| msdyn_salesvariance_base               | ei             | ei           |
| msdyn_scheduleperformance              | ei             | ei           |
| msdyn_scheduleperformancename          | ei             | ei           |
| msdyn_schedulevariance                 | ei             | ei           |
| msdyn_taskearlieststart                | ei             | ei           |
| msdyn_teamsize                         | ei             | ei           |
| msdyn_teamsize_date                    | ei             | ei           |
| msdyn_teamsize_state                   | ei             | ei           |
| msdyn_totalactualcost                  | ei             | ei           |
| msdyn_totalactualcost_base             | ei             | ei           |
| msdyn_totalplannedcost                 | ei             | ei           |
| msdyn_totalplannedcost_base            | ei             | ei           |


## <a name="limitations-and-known-issues"></a>Piirangud ja teadaolevad probleemid
Järgnevalt on toodud piirangute ja teadaolevate probleemide loend.

- Projekti ajakava API-sid saavad kasutada ainult **Microsoft Projecti litsentsiga kasutajad**. Neid ei saa kasutada järgnevad.
    - Rakenduse kasutajad
    - Süsteemi kasutajad
    - Integratsiooni kasutajad
    - Teised kasutajad, kes ei oma nõutavat litsentsi
- Igal suvandil **OperationSet** saab olla maksimaalselt 100 toimingut.
- Igal kasutajal saab maksimaalselt olla 10 avatud suvandit **OperationSet**.
- Project Operations toetab praegu projektil kokku maksimaalselt 500 ülesannet.
- Suvandi **OperationSet** tõrkeolek ja tõrkelogid pole hetkel saadaval.
- [Projektide ja tööülesannete piirangud ja piirid](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Tõrketöötlus

   - Toimingukomplektide põhjal loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **Toimingutekomplekt**.
   - Projekti ajastamisteenuses loodud tõrgete läbivaatamiseks minge jaotisse **Sätted** \> **Ajakava integreerimine** \> **PSS-i tõrkelogid**.

## <a name="sample-scenario"></a>Näidisstsenaarium

Selles stsenaariumis loote projekti, meeskonnaliikme, neli ülesannet ja kaks ressursi määramist. Järgmisena värskendate ühte ülesannet, värskendate projekti, kustutate ühe ülesande, kustutate ühe ressursi määramise ja loote ülesande sõltuvuse.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Täiendavad näited

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
