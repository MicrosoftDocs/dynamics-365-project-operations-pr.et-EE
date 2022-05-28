---
title: Projekti mallide arendamine funktsiooniga Kopeeri projekt
description: Selles teemas antakse teavet selle kohta, kuidas kohandatud toimingut Kopeeri projekt kasutades projekti malle luua.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590893"
---
# <a name="develop-project-templates-with-copy-project"></a>Projekti mallide arendamine funktsiooniga Kopeeri projekt

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations toetab võimalust kopeerida projekti ja ennistada kõik ülesanded tagasi üldistele rolli esindavatele ressurssidele. Kliendid saavad seda funktsiooni kasutada põhiliste projekti mallide loomiseks.

Kui valite suvandi **Kopeeri projekt**, värskendatakse sihtprojekti olekut. Kasutage suvandit **Oleku põhjus**, et määratleda, millal kopeerimise toiming lõpetada. Suvandi **Kopeeri projekt** valimine värskendab projekti alguskuupäeva praegusele alguskuupäevale, kui sihtprojekti olemis ei tuvastata sihtkuupäeva.

## <a name="copy-project-custom-action"></a>Kohandatud toiming Kopeeri projekt

### <a name="name"></a>Nimetus 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Sisendparameetrid

Olemas on kolm sisendparameetrit.

- **ReplaceNamedResources** või **ClearTeamsAndAssignments** – määrake ainult üks suvanditest. Ära sea mõlemat.

    - **\{"ReplaceNamedResources":true\}** – Project Operationsi vaikekäitumine. Kõik nimetatud ressursid asendatakse üldiste ressurssidega.
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Web vaikekäitumine. Kõik ülesanded ja meeskonnaliikmed eemaldatakse.

- **SourceProject** – lähteprojekti olemiviide, millest kopeerida. See parameeter ei saa olla tühine.
- **Sihtmärk** – sihtprojekti olemiviide, kuhu kopeerida. See parameeter ei saa olla tühine.

Järgmises tabelis on esitatud kokkuvõte kolmest parameetrist.

| Parameeter                | Tüüp             | Väärtus                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Loogiline          | **Tõene** või **väär** |
| ClearTeamsAndAssignments | Loogiline          | **Tõene** või **väär** |
| SourceProject            | Olemi viide | Lähteprojekt    |
| Sihtkeel                   | Olemi viide | Sihtprojekt    |

Toimingute vaikesätete kohta leiate lisateavet teemast [Veebi API toimingute](/powerapps/developer/common-data-service/webapi/use-web-api-actions) kasutamine.

### <a name="validations"></a>Valideerimised

Järgmised valideerimised on tehtud.

1. Null kontrollib ja toob lähte- ja sihtprojektid, et kinnitada mõlema projekti olemasolu organisatsioonis.
2. Süsteem kinnitab, et sihtprojekt kehtib kopeerimiseks, kontrollides järgmisi tingimusi.

    - Projektis pole varasemat tegevust (sh vahekaardi Tööülesanded **valimine**) ja projekt on äsja loodud.
    - Varasemat koopiat pole, selles projektis pole importi taotletud ja projektil pole olekut **Nurjunud**.

3. Toimingut ei kutsuta HTTP abil.

## <a name="specify-fields-to-copy"></a>Määrake kopeeritavad väljad

Kui tegevus valitakse, vaatav suvand **Kopeeri projekt** projektivaadet **Kopeeri projekti veerud**, et määratleda, millised väljad projekti kopeerimisel kopeeritakse.

### <a name="example"></a>Näide

Järgmises näites on näidatud, kuidas helistada **copyProjectV3** kohandatud toimingule parameetrikomplektiga **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
