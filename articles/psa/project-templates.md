---
title: Projektimallid
description: Selles teemas antakse teavet selle kohta, kuidas kasutada projektimalle kiireks projekti seadistamiseks.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148053"
---
# <a name="project-templates"></a><span data-ttu-id="d422a-103">Projektimallid</span><span class="sxs-lookup"><span data-stu-id="d422a-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d422a-104">Projektimall on eelmääratletud raamistik, mis aitab teil projekti alustada kiiresti ja hõlpsalt.</span><span class="sxs-lookup"><span data-stu-id="d422a-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="d422a-105">Eelmääratletud malli abil saate luua uue projekti ühe klõpsuga.</span><span class="sxs-lookup"><span data-stu-id="d422a-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="d422a-106">Nagu projektidegi puhul peate projektimallidele määratlema eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="d422a-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="d422a-107">Peate igale projektimallile määratlema projektikalendri ja organisatsioonis tuleb eelmääratleda rollid ning hinnakirjad, et malli komponendid sisaldaksid kasulikke andmeid.</span><span class="sxs-lookup"><span data-stu-id="d422a-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="d422a-108">Projektimall koosneb kolmest komponendist: ajakava, projekti prognoosid ja projektimeeskonna liikmed.</span><span class="sxs-lookup"><span data-stu-id="d422a-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="d422a-109">Kavanda</span><span class="sxs-lookup"><span data-stu-id="d422a-109">Schedule</span></span>

<span data-ttu-id="d422a-110">Projektimalli ajakava elemendid on samad, nagu projekti ajakavas.</span><span class="sxs-lookup"><span data-stu-id="d422a-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="d422a-111">Saate luua ülesannete hierarhia, seostada rolle ülesannetega, määratleda ajakava atribuute ja määrata sõltuvusi.</span><span class="sxs-lookup"><span data-stu-id="d422a-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="d422a-112">Projektimalli ajakava toetab ka iga ülesande jaoks ülesande režiime.</span><span class="sxs-lookup"><span data-stu-id="d422a-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="d422a-113">Seetõttu toetab see kavandamismootorit.</span><span class="sxs-lookup"><span data-stu-id="d422a-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="d422a-114">Projektiga tuleb seostada projektikalender.</span><span class="sxs-lookup"><span data-stu-id="d422a-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="d422a-115">Töögraafiku loomisel pole projektimalli ja projekti vahel mingit erinevust.</span><span class="sxs-lookup"><span data-stu-id="d422a-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="d422a-116">Projekti prognoosid</span><span class="sxs-lookup"><span data-stu-id="d422a-116">Project estimates</span></span>

<span data-ttu-id="d422a-117">Projektimalli projektiprognoosid töötavad sarnaselt projekti projektiprognoosidele.</span><span class="sxs-lookup"><span data-stu-id="d422a-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="d422a-118">Kuid oma- ja müügihinnad võetakse parameetrites määratletud vaikimisi kulu- ning müügihinnakirjadest.</span><span class="sxs-lookup"><span data-stu-id="d422a-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="d422a-119">Projekti loomine mallist</span><span class="sxs-lookup"><span data-stu-id="d422a-119">Creating a project from a template</span></span>
 
<span data-ttu-id="d422a-120">Projekti loomiseks projektimallist on mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="d422a-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="d422a-121">Projekti loomisel hinnapakkumisest saate valida dialoogiboksis **Kiirloomine: projekt** projektimalli.</span><span class="sxs-lookup"><span data-stu-id="d422a-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dialoogiboks Kiirloomine: projekt](media/project-11.png)

- <span data-ttu-id="d422a-123">Projekti loomisel suvandiga **Uus projekt**, kuvatakse enne kirje salvestamist leht **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d422a-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="d422a-124">Valige väljal **Vali mall** üks organisatsiooni eelmääratletud projektimallidest.</span><span class="sxs-lookup"><span data-stu-id="d422a-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="d422a-125">Kasutage lehel **Malliolem** suvandit **Loo projekt mallist**.</span><span class="sxs-lookup"><span data-stu-id="d422a-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="d422a-126">Mallikomponentide kopeerimine projekti</span><span class="sxs-lookup"><span data-stu-id="d422a-126">Copying components of template to project</span></span>

<span data-ttu-id="d422a-127">Projektimalli komponentide kopeerimisel projekti võib projekti sätetest olenevalt ilmneda mõni erand.</span><span class="sxs-lookup"><span data-stu-id="d422a-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="d422a-128">Ajakava kopeerimine</span><span class="sxs-lookup"><span data-stu-id="d422a-128">Copying the schedule</span></span>

<span data-ttu-id="d422a-129">Kui projektil on mallist erinev projektikalender, rakendatakse ajakava kopeerimisel projektimallist ülesande ajakavale projekti kalendrist pärinevad töötunnid.</span><span class="sxs-lookup"><span data-stu-id="d422a-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="d422a-130">Sel viisil kohandatakse ajakava ühtivaks projekti varukalendriga.</span><span class="sxs-lookup"><span data-stu-id="d422a-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="d422a-131">Sellele sarnaselt rakendub ajakava esimesele ülesandele projekti alguskuupäev ja ülejäänud hierarhia ajakava värskendatakse mallis toodud kestuse ning sõltuvuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="d422a-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="d422a-132">Projekti prognooside kopeerimine</span><span class="sxs-lookup"><span data-stu-id="d422a-132">Copying project estimates</span></span> 

<span data-ttu-id="d422a-133">Projekti prognoosiridade üleselt kopeerimisel värskendatakse hinnakirju.</span><span class="sxs-lookup"><span data-stu-id="d422a-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="d422a-134">Kulude hinnakirja korral põhinevad need värskendused projekti omaval üksusel.</span><span class="sxs-lookup"><span data-stu-id="d422a-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="d422a-135">Müügihinnakirja korral põhinevad need kliendil.</span><span class="sxs-lookup"><span data-stu-id="d422a-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="d422a-136">Müügiolemiga seotud projektide korral määratakse ühiku oma- ja müügihinnad nende hinnakirjade põhjal.</span><span class="sxs-lookup"><span data-stu-id="d422a-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="d422a-137">Projektimeeskonna kopeerimine</span><span class="sxs-lookup"><span data-stu-id="d422a-137">Copying a project team</span></span>

<span data-ttu-id="d422a-138">Projektimeeskonna kopeerimisel projektimallist projekti kopeeritakse üldised ressursid koos mallis määratletud oskuste ja pädevustega.</span><span class="sxs-lookup"><span data-stu-id="d422a-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="d422a-139">Üldiseid ressursi määramisi säilitatakse samamoodi, nagu nad olid projektimallis.</span><span class="sxs-lookup"><span data-stu-id="d422a-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="d422a-140">Nimega ressursse projektimallides ei toetata.</span><span class="sxs-lookup"><span data-stu-id="d422a-140">Named resources aren't supported in project templates.</span></span>
