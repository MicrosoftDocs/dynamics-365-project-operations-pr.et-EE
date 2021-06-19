---
title: Projekti mallide arendamine funktsiooniga Kopeeri projekt
description: Selles teemas antakse teavet selle kohta, kuidas kohandatud toimingut Kopeeri projekt kasutades projekti malle luua.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005651"
---
# <a name="develop-project-templates-with-copy-project"></a>Projekti mallide arendamine funktsiooniga Kopeeri projekt

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations toetab võimalust kopeerida projekti ja ennistada kõik ülesanded tagasi üldistele rolli esindavatele ressurssidele. Kliendid saavad seda funktsiooni kasutada põhiliste projekti mallide loomiseks.

Kui valite suvandi **Kopeeri projekt**, värskendatakse sihtprojekti olekut. Kasutage suvandit **Oleku põhjus**, et määratleda, millal kopeerimise toiming lõpetada. Suvandi **Kopeeri projekt** valimine värskendab projekti alguskuupäeva praegusele alguskuupäevale, kui sihtprojekti olemis ei tuvastata sihtkuupäeva.

## <a name="copy-project-custom-action"></a>Kohandatud toiming Kopeeri projekt 

### <a name="name"></a>Nimetus 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Sisendparameetrid
Olemas on kolm sisendparameetrit.

| Parameeter          | Tüüp   | Väärtused                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** või **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Olemi viide | Algne projekt |
| Sihtmärk             | Olemi viide | Sihtprojekt |


- **{"clearTeamsAndAssignments":true}**: veebi projekti vaikekäitumine ja see eemaldab kõik ülesanded ja meeskonnaliikmed.
- **{"removeNamedResources":true}** Project Operationsi vaikekäitumine ja see ennistab määramised üldistele ressurssidele.

Lisateavet toimingute vaikeväärtuste kohta leiate teemast [Veebi API toimingute kasutamine](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Määrake kopeeritavad väljad 
Kui tegevus valitakse, vaatav suvand **Kopeeri projekt** projektivaadet **Kopeeri projekti veerud**, et määratleda, millised väljad projekti kopeerimisel kopeeritakse.


### <a name="example"></a>Näide
Järgmine näide näitab, kuidas kutsuda **CopyProsource'i** kohandatud toimingut parameetrikomplektiga **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]