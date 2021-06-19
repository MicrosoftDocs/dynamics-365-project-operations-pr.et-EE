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
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="7e11b-103">Projekti mallide arendamine funktsiooniga Kopeeri projekt</span><span class="sxs-lookup"><span data-stu-id="7e11b-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="7e11b-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="7e11b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7e11b-105">Dynamics 365 Project Operations toetab võimalust kopeerida projekti ja ennistada kõik ülesanded tagasi üldistele rolli esindavatele ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="7e11b-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="7e11b-106">Kliendid saavad seda funktsiooni kasutada põhiliste projekti mallide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="7e11b-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="7e11b-107">Kui valite suvandi **Kopeeri projekt**, värskendatakse sihtprojekti olekut.</span><span class="sxs-lookup"><span data-stu-id="7e11b-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="7e11b-108">Kasutage suvandit **Oleku põhjus**, et määratleda, millal kopeerimise toiming lõpetada.</span><span class="sxs-lookup"><span data-stu-id="7e11b-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="7e11b-109">Suvandi **Kopeeri projekt** valimine värskendab projekti alguskuupäeva praegusele alguskuupäevale, kui sihtprojekti olemis ei tuvastata sihtkuupäeva.</span><span class="sxs-lookup"><span data-stu-id="7e11b-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="7e11b-110">Kohandatud toiming Kopeeri projekt</span><span class="sxs-lookup"><span data-stu-id="7e11b-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="7e11b-111">Nimetus</span><span class="sxs-lookup"><span data-stu-id="7e11b-111">Name</span></span> 

<span data-ttu-id="7e11b-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="7e11b-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="7e11b-113">Sisendparameetrid</span><span class="sxs-lookup"><span data-stu-id="7e11b-113">Input parameters</span></span>
<span data-ttu-id="7e11b-114">Olemas on kolm sisendparameetrit.</span><span class="sxs-lookup"><span data-stu-id="7e11b-114">There are three input parameters:</span></span>

| <span data-ttu-id="7e11b-115">Parameeter</span><span class="sxs-lookup"><span data-stu-id="7e11b-115">Parameter</span></span>          | <span data-ttu-id="7e11b-116">Tüüp</span><span class="sxs-lookup"><span data-stu-id="7e11b-116">Type</span></span>   | <span data-ttu-id="7e11b-117">Väärtused</span><span class="sxs-lookup"><span data-stu-id="7e11b-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="7e11b-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="7e11b-118">ProjectCopyOption</span></span>  | <span data-ttu-id="7e11b-119">String</span><span class="sxs-lookup"><span data-stu-id="7e11b-119">String</span></span> | <span data-ttu-id="7e11b-120">**{"removeNamedResources":true}** või **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="7e11b-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="7e11b-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="7e11b-121">SourceProject</span></span>      | <span data-ttu-id="7e11b-122">Olemi viide</span><span class="sxs-lookup"><span data-stu-id="7e11b-122">Entity Reference</span></span> | <span data-ttu-id="7e11b-123">Algne projekt</span><span class="sxs-lookup"><span data-stu-id="7e11b-123">Source Project</span></span> |
| <span data-ttu-id="7e11b-124">Sihtmärk</span><span class="sxs-lookup"><span data-stu-id="7e11b-124">Target</span></span>             | <span data-ttu-id="7e11b-125">Olemi viide</span><span class="sxs-lookup"><span data-stu-id="7e11b-125">Entity Reference</span></span> | <span data-ttu-id="7e11b-126">Sihtprojekt</span><span class="sxs-lookup"><span data-stu-id="7e11b-126">Target Project</span></span> |


- <span data-ttu-id="7e11b-127">**{"clearTeamsAndAssignments":true}**: veebi projekti vaikekäitumine ja see eemaldab kõik ülesanded ja meeskonnaliikmed.</span><span class="sxs-lookup"><span data-stu-id="7e11b-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="7e11b-128">**{"removeNamedResources":true}** Project Operationsi vaikekäitumine ja see ennistab määramised üldistele ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="7e11b-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="7e11b-129">Lisateavet toimingute vaikeväärtuste kohta leiate teemast [Veebi API toimingute kasutamine](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="7e11b-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="7e11b-130">Määrake kopeeritavad väljad</span><span class="sxs-lookup"><span data-stu-id="7e11b-130">Specify fields to copy</span></span> 
<span data-ttu-id="7e11b-131">Kui tegevus valitakse, vaatav suvand **Kopeeri projekt** projektivaadet **Kopeeri projekti veerud**, et määratleda, millised väljad projekti kopeerimisel kopeeritakse.</span><span class="sxs-lookup"><span data-stu-id="7e11b-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="7e11b-132">Näide</span><span class="sxs-lookup"><span data-stu-id="7e11b-132">Example</span></span>
<span data-ttu-id="7e11b-133">Järgmine näide näitab, kuidas kutsuda **CopyProsource'i** kohandatud toimingut parameetrikomplektiga **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="7e11b-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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