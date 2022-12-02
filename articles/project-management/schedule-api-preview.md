---
title: Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks
description: Selles artiklis on toodud teave ja näited projekti ajakava API-de kasutamise kohta.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541119"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projekti ajakava API-de kasutamine ajastamise olemitega toimingute tegemiseks

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_


**Olemite ajastamine**

Projekti ajakava API-d annavad võimaluse teha **ajastamise olemitega** loomise, värskendamise ja kustutamise toiminguid. Neid olemeid hallatakse veebirakenduse Project ajastamise mootori kaudu. Suvandiga **Olemite ajastamine** toimingute loomine, värskendamine ja kustutamine oli rakenduse Dynamics 365 Project Operations varasemates väljaannetes piiratud.

Järgmises tabelid on toodud projekti ajakava olemite täielik loend.

| **Olemi nimi**         | **Olemi loogiline nimi**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekti ülesanne            | msdyn_projecttask           |
| Projekti ülesande sõltuvus | msdyn_projecttaskdependency |
| Ressursi määramine     | msdyn_resourceassignment    |
| Projektisalv          | msdyn_projectbucket         |
| Projektimeeskonna liige     | msdyn_projectteam           |
| Projekti kontroll-loendid      | msdyn_projectchecklist      |
| Projekti silt           | msdyn_projectlabel          |
| Projekti ülesanne sildile   | msdyn_projecttasktolabel    |
| Projekti sprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet on tööühiku muster, mida saab kasutada juhul, kui kandes tuleb töödelda mitut ajakava mõjutavat taotlust.

**Projekti ajakava API-d**

Järgnev on praeguste projekti ajakava API-de loend.

| **API**                                 | Kirjeldus                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Seda API-t kasutatakse projekti loomiseks. Projekt ja vaikimisi projektisalv luuakse kohe.                         |
| **msdyn_CreateTeamMemberV1**            | Seda API-t kasutatakse projektimeeskonna liikme loomiseks. Meeskonnaliikme kirje luuakse kohe.                                  |
| **msdyn_CreateOperationSetV1**          | Seda API-t saab kasutada mitme taotluse ajastamiseks, mis tuleb kande sees teha.                                        |
| **msdyn_PssCreateV1**                   | Seda API-t kasutatakse olemi loomiseks. Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab loomistoimingut. |
| **msdyn_PssUpdateV1**                   | Seda API-t kasutatakse olemi värskendamiseks. Olem võib olla mis tahes projekti ajastamise olemitest, mis toetab värskendamistoimingut  |
| **msdyn_PssDeleteV1**                   | Seda API-t kasutatakse olemi kustutamiseks. Olem võib olla mis tahes priekti ajastamise olemitest, mis toetab kustutamistoimingut. |
| **msdyn_ExecuteOperationSetV1**         | Seda API-t kasutatakse antud toimingute komplektis kõikide toimingute täitmiseks.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Seda API-t kasutatakse ressursi määramise plaanitud töö kontuuri värskendamiseks.                                                        |



**Projekti ajakava API-de kasutamine väärtusega OperationSet**

Kuna nii API **CreateProjectV1** kui ka **CreateTeamMemberV1** kirjed luuakse kohe, ei saa neid API-sid olemis **OperationSet** otse kasutada. Samas saate kasutada API-d, et luua vajalikke kirjeid, luua üksuse **OperationSet** ja kasutada seejärel neid eelnevalt loodud kirjeid üksuses **OperationSet**.

**Toetatud toimingud**

| **Olemi ajastamine**   | **Koosta** | **Värskendus** | **Kustutusklahv (Delete)** | **Olulised kaalutlused**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projekti ülesanne            | Ja        | Ja        | Ja        | Välja **Progress**, **EffortCompleted** ja **EffortRemaining** saab redigeerida rakenduses Project for the Web, kuid neid ei saa muuta rakenduses Project Operations.                                                                                                                                                                                             |
| Projektiülesande sõltuvus | Ja        | No         | Ja        | Projektiülesande sõltuvuskirjeid ei värskendata. Selle asemel saab vana kirje kustutada ja luua uue kirje.                                                                                                                                                                                                                                 |
| Ressursi määramine     | Ja        | Jah\*      | Ja        | Järgmiste väljadega toiminguid ei toetata: **BookableResourceID** (Broneeritava ressursi ID), **Effort** (Panus), **EffortCompleted** (Lõpule viidud panus), **EffortRemaining** (Järelejäänud panus) ja **PlannedWork** (Planeeritud töö). Ressursi määramise kirjeid ei värskendata. Selle asemel saab vana kirje kustutada ja luua uue kirje. Ressursi määramise kontuuride värskendamiseks on saadaval eraldi API. |
| Projektisalv          | Ja        | Ja        | Ja        | Vaikesalv luuakse **CreateProjectV1** API-t kasutades. Värskendusväljaandes 16 lisati projektisalvede loomise ja kustutamise tugi.                                                                                                                                                                                                   |
| Projektimeeskonna liige     | Ja        | Ja        | Ja        | Kasutage loomistoiminguks API-d **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ja        | Ja        |            | Järgmiste väljadega toiminguid ei toetata: **StateCode** (Olekukood), **BulkGenerationStatus** (Hulgiloomise olek), **GlobalRevisionToken** (Üldine redaktsioonitõend), **CalendarID** (Kalendri ID), **Effort** (Panus), **EffortCompleted** (Lõpule jõudnud panus), **EffortRemaining** (Järelejäänud panus), **Progress** (Edenemine), **Finish** (Lõpp), **TaskEarliestStart** (Ülesande varajaseim algus) ja **Duration** (Kestus).                                                                                       |
| Projekti kontroll-loendid      | Ja        | Ja        | Ja        |                                                                                                                                                                                                                                                                                                                                                         |
| Projekti silt           | No         | Ja        | No         | Sildinimesid saab muuta. See funktsioon on saadaval ainult Project for the Webile.                                                                                                                                                                                                                                                                      |
| Projekti ülesanne sildile   | Ja        | No         | Ja        | See funktsioon on saadaval ainult Project for the Webile.                                                                                                                                                                                                                                                                                                  |
| Projekti sprint          | Ja        | Ja        | Ja        | Väljal **Algus** kuupäev peab olema varasem kui väljal **Lõpp**. Sama projekti sprindid ei saa üksteisega kattuda. See funktsioon on saadaval ainult Project for the Webile.                                                                                                                                                                    |




ID atribuut on valikuline. Kui see on antud, proovib süsteem seda kasutada ja loob erandi, kui seda ei saa kasutada. Kui seda ei ole antud, loob süsteem selle.

**Piirangud ja teadaolevad probleemid**

Järgnevalt on toodud piirangute ja teadaolevate probleemide loend.

-   Projekti ajakava API-sid saavad kasutada ainult **Microsoft Projecti litsentsiga kasutajad**. Neid ei saa kasutada järgnevad.
    -   Rakenduse kasutajad
    -   Süsteemi kasutajad
    -   Integratsiooni kasutajad
    -   Teised kasutajad, kes ei oma nõutavat litsentsi
-   Igal suvandil **OperationSet** saab olla maksimaalselt 100 toimingut.
-   Igal kasutajal saab maksimaalselt olla 10 avatud suvandit **OperationSet**.
-   Project Operations toetab praegu projektil kokku maksimaalselt 500 ülesannet.
-   Iga värskenduse ressursi määramise kontuuri toiming loetakse üheks toiminguks.
-   Iga värskendatud kontuuride loend võib sisaldada maksimaalselt 100 ajalõiku.
-   Suvandi **OperationSet** tõrkeolek ja tõrkelogid pole hetkel saadaval.
-   Ühe projekti kohta on maksimaalselt 400 sprinti.
-   [Projektide ja tööülesannete piirangud ja piirid](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Sildid on hetkel saadaval ainult Project for the Webile.

**Tõrketöötlus**

-   Toimingukomplektide põhjal loodud tõrgete ülevaatamiseks minge jaotisesse **Sätted** \> **Kavanda integreerimine** \> **Toimingutekomplekt**.
-   Projekti ajastamisteenuses loodud tõrgete läbivaatamiseks minge jaotisse **Sätted** \> **Ajakava integreerimine** \> **PSS-i tõrkelogid**.

**Ressursi määramise kontuuride redigeerimine**

Erinevalt kõigist teistest olemit värskendavatest projekti ajastamise API-dest vastutab ressursi määramise kontuuri API ainuüksi ühe välja msdyn_plannedwork värskenduste eest ühel olemil, msydn_resourceassignment.

Antud ajakavarežiim on:

-   **fikseeritud ühikud**
-   projekti kalender on 9-17 on 9-5, E, T, N, R (KOLMAPÄEVITI TÖÖD EI OLE)
-   ja ressursside kalender on 9-1p PST E–R

See ülesanne on üks nädal, neli tundi päevas. Seda seetõttu, et ressursikalender on kell 9–1 PST ehk neli tundi päevas.

| &nbsp;     | Toiming | Alguskuupäev | Lõpukuupäev  | Kogus | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 töötaja |  T1  | 13.06.2022  | 17.06.2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Näiteks kui soovite, et töötaja töötaks sel nädalal iga päev ainult kolm tundi ja jätaks ühe tunni muude ülesannete jaoks.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours valimikoormus:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

See on määramine pärast kontuuri ajakava värskendamise API käitamist.

| &nbsp;     | Toiming | Alguskuupäev | Lõpukuupäev  | Kogus | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 töötaja | T1   | 13.06.2022  | 17.06.2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Näidisstsenaarium**

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

** Täiendavad näited

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
