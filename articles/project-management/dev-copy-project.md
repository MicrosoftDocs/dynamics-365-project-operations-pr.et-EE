---
title: Projekti mallide arendamine funktsiooniga Kopeeri projekt
description: See artikkel annab teavet selle kohta, kuidas kohandatud toimingut Kopeeri projekt kasutades projekti malle luua.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923827"
---
# <a name="develop-project-templates-with-copy-project"></a>Projekti mallide arendamine funktsiooniga Kopeeri projekt

_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_

Dynamics 365 Project Operations toetab võimalust kopeerida projekti ja ennistada kõik ülesanded tagasi üldistele rolli esindavatele ressurssidele. Kliendid saavad seda funktsiooni kasutada põhiliste projekti mallide loomiseks.

Kui valite suvandi **Kopeeri projekt**, värskendatakse sihtprojekti olekut. Kasutage suvandit **Oleku põhjus**, et määratleda, millal kopeerimise toiming lõpetada. Suvandi **Kopeeri projekt** valimine värskendab projekti alguskuupäeva praegusele alguskuupäevale, kui sihtprojekti olemis ei tuvastata sihtkuupäeva.

## <a name="copy-project-custom-action"></a>Kohandatud toiming Kopeeri projekt

### <a name="name"></a>Nimetus 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Sisendparameetrid

Olemas on kolm sisendparameetrit.

- **ReplaceNamedResources** või **ClearTeamsAndAssignments** – Määrake ainult üks suvanditest. Ärge määrake mõlemat.

    - **\{"ReplaceNamedResources":true\}** – Rakenduse Project Operations vaikekäitumine. Kõik nimetatud ressursid asendatakse üldiste ressurssidega.
    - **\{"ClearTeamsAndAssignments":tõene\}** – Project for the Webi vaikekäitumine. Kõik ülesanded ja meeskonnaliikmed eemaldatakse.

- **SourceProject** – Lähteprojekti olemiviide, millelt kopeerida. See parameeter ei saa olla nullväärtusega.
- **Sihtmärk** – Sihtprojekti olemiviide, millele kopeerida. See parameeter ei saa olla nullväärtusega.

Järgmises tabelis on kokkuvõte kolmest parameetrist.

| Parameeter                | Tüüp             | Väärtus                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Loogiline          | **Tõene** või **Väär**. |
| ClearTeamsAndAssignments | Loogiline          | **Tõene** või **Väär**. |
| SourceProject            | Olemi viide | Lähteprojekt    |
| Sihtkeel                   | Olemi viide | Sihtprojekt    |

Lisateavet toimingute vaikeväärtuste kohta leiate teemast [Veebi API toimingute kasutamine](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Kinnitused

Tehakse järgmised kinnitused.

1. Null kontrollib ja otsib lähte- ja sihtprojekte, et kinnitada mõlema projekti olemasolu organisatsioonis.
2. Süsteem kinnitab, et sihtprojekt on kopeerimiseks sobiv, kontrollides järgmisi tingimusi:

    - Projektil pole varasemaid tegevusi (sh vahekaardi **Ülesanded** valik) ja projekt on äsja loodud.
    - Eelmist koopiat pole, sellel projektil pole importimist taotletud ja projekti olek ei ole **Ebaõnnestunud**.

3. Toimingut ei kutsuta HTTP-d kasutades.

## <a name="specify-fields-to-copy"></a>Määrake kopeeritavad väljad

Kui tegevus valitakse, vaatav suvand **Kopeeri projekt** projektivaadet **Kopeeri projekti veerud**, et määratleda, millised väljad projekti kopeerimisel kopeeritakse.

### <a name="example"></a>Näide

Järgmine näide näitab, kuidas kutsuda **CopyProjectV3** kohandatud toimingut parameetrikomplektiga **removeNamedResources**.

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
