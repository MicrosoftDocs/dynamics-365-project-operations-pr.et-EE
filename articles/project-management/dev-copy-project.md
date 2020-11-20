---
title: Projekti mallide arendamine funktsiooniga Kopeeri projekt
description: Selles teemas antakse teavet selle kohta, kuidas kohandatud toimingut Kopeeri projekt kasutades projekti malle luua.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131608"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="e149e-103">Projekti mallide arendamine funktsiooniga Kopeeri projekt</span><span class="sxs-lookup"><span data-stu-id="e149e-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="e149e-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="e149e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e149e-105">Dynamics 365 Project Operations toetab võimalust kopeerida projekt ja ennistada kõik tööülesanded tagasi üldistele ressurssidele, mis rolli esindavad.</span><span class="sxs-lookup"><span data-stu-id="e149e-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="e149e-106">Kliendid saavad seda funktsiooni kasutada põhiliste projekti mallide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e149e-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="e149e-107">Kui valite suvandi **Kopeeri projekt**, värskendatakse sihtprojekti olekut.</span><span class="sxs-lookup"><span data-stu-id="e149e-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="e149e-108">Kasutage suvandit **Oleku põhjus**, et määratleda, millal kopeerimise toiming lõpetada.</span><span class="sxs-lookup"><span data-stu-id="e149e-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="e149e-109">Suvandi **Kopeeri projekt** valimine värskendab projekti alguskuupäeva praegusele alguskuupäevale, kui sihtprojekti olemis ei tuvastata sihtkuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e149e-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="e149e-110">Kohandatud toiming Kopeeri projekt</span><span class="sxs-lookup"><span data-stu-id="e149e-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="e149e-111">Nimetus</span><span class="sxs-lookup"><span data-stu-id="e149e-111">Name</span></span> 

<span data-ttu-id="e149e-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="e149e-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="e149e-113">Sisendparameetrid</span><span class="sxs-lookup"><span data-stu-id="e149e-113">Input parameters</span></span>
<span data-ttu-id="e149e-114">Olemas on kolm sisendparameetrit.</span><span class="sxs-lookup"><span data-stu-id="e149e-114">There are three input parameters:</span></span>

| <span data-ttu-id="e149e-115">Parameeter</span><span class="sxs-lookup"><span data-stu-id="e149e-115">Parameter</span></span>          | <span data-ttu-id="e149e-116">Tüüp</span><span class="sxs-lookup"><span data-stu-id="e149e-116">Type</span></span>   | <span data-ttu-id="e149e-117">Väärtused</span><span class="sxs-lookup"><span data-stu-id="e149e-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="e149e-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="e149e-118">ProjectCopyOption</span></span>  | <span data-ttu-id="e149e-119">String</span><span class="sxs-lookup"><span data-stu-id="e149e-119">String</span></span> | <span data-ttu-id="e149e-120">**{"removeNamedResources":true}** või **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="e149e-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="e149e-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="e149e-121">SourceProject</span></span>      | <span data-ttu-id="e149e-122">Olemi viide</span><span class="sxs-lookup"><span data-stu-id="e149e-122">Entity Reference</span></span> | <span data-ttu-id="e149e-123">Algne projekt</span><span class="sxs-lookup"><span data-stu-id="e149e-123">Source Project</span></span> |
| <span data-ttu-id="e149e-124">Sihtmärk</span><span class="sxs-lookup"><span data-stu-id="e149e-124">Target</span></span>             | <span data-ttu-id="e149e-125">Olemi viide</span><span class="sxs-lookup"><span data-stu-id="e149e-125">Entity Reference</span></span> | <span data-ttu-id="e149e-126">Sihtprojekt</span><span class="sxs-lookup"><span data-stu-id="e149e-126">Target Project</span></span> |


- <span data-ttu-id="e149e-127">**{"clearTeamsAndAssignments":true}**: veebi projekti vaikekäitumine ja see eemaldab kõik ülesanded ja meeskonnaliikmed.</span><span class="sxs-lookup"><span data-stu-id="e149e-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="e149e-128">**{"removeNamedResources":true}** Project Operationsi vaikekäitumine ja see ennistab määramised üldistele ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="e149e-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="e149e-129">Lisateavet toimingute vaikeväärtuste kohta leiate teemast [Veebi API toimingute kasutamine](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="e149e-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="e149e-130">Määrake kopeeritavad väljad</span><span class="sxs-lookup"><span data-stu-id="e149e-130">Specify fields to copy</span></span> 
<span data-ttu-id="e149e-131">Kui tegevus valitakse, vaatav suvand **Kopeeri projekt** projektivaadet **Kopeeri projekti veerud**, et määratleda, millised väljad projekti kopeerimisel kopeeritakse.</span><span class="sxs-lookup"><span data-stu-id="e149e-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
