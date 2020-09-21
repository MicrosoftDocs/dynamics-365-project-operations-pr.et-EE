---
title: Projektimalli loomine
description: Projektimalli loomine Project Service'is
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750924"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="f8147-103">Projektimalli loomine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f8147-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f8147-104">Projektimallid säästavad teie aega, kui ettevõte teeb regulaarselt pakkumisi sarnast tüüpi projektidele.</span><span class="sxs-lookup"><span data-stu-id="f8147-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="f8147-105">Need pakuvad projekti tüübi puhul standardset rollikomplekti ja hinnangulist tundide arvu.</span><span class="sxs-lookup"><span data-stu-id="f8147-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="f8147-106">Kontohaldurid ja projektijuhid saavad luua projektimalli alusel projekte või kopeerida malli ja luua enda oma.</span><span class="sxs-lookup"><span data-stu-id="f8147-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="f8147-107">Projektimalli komponendid</span><span class="sxs-lookup"><span data-stu-id="f8147-107">Components of project template</span></span>
 <span data-ttu-id="f8147-108">Projektimall koosneb kolmest osast.</span><span class="sxs-lookup"><span data-stu-id="f8147-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="f8147-109">**Tööjaotuse struktuur**: projektimalli tööjaotuse struktuur sisaldab sama elemendikomplekti mis projekt.</span><span class="sxs-lookup"><span data-stu-id="f8147-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="f8147-110">Saate luua ülesannete hierarhia, seostada rolle ülesandega, määratleda ajakava atribuute, määrata sõltuvusi ja kuvada kõik andmed Gantti diagrammil.</span><span class="sxs-lookup"><span data-stu-id="f8147-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="f8147-111">Projektimallide tööjaotuse struktuur toetab ka iga ülesande puhul ülesanderežiime.</span><span class="sxs-lookup"><span data-stu-id="f8147-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="f8147-112">Projektimalli ja projekti vahel pole töö ajakava loomisel mingit erinevust.</span><span class="sxs-lookup"><span data-stu-id="f8147-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="f8147-113">**Projektiprognoosid**: mallide projektiprognoosid toimivad samal moel, nagu projektides, välja arvatud see, et hinnakirjad oma- ja müügihindade vaikeväärtuste määramiseks on alati funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameetrites määratletud omahinna ja müügihinna vaikehinnakirjad.</span><span class="sxs-lookup"><span data-stu-id="f8147-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="f8147-114">Ülejäänud funktsioonid on samad mis projektis.</span><span class="sxs-lookup"><span data-stu-id="f8147-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="f8147-115">**Projektimeeskonna moodustamine**: projektimalli jaoks projektimeeskonna moodustamisel ei saa mallis broneerida nimelist ressurssi.</span><span class="sxs-lookup"><span data-stu-id="f8147-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="f8147-116">Saate kasutada tööjaotuse struktuuris olevat valikut **Projektimeeskonna loomine**, et luua üldiste ressursside kogum.</span><span class="sxs-lookup"><span data-stu-id="f8147-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="f8147-117">Saate ka määrata üldiste ressursside puhul nõutavad oskused ja pädevused.</span><span class="sxs-lookup"><span data-stu-id="f8147-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="f8147-118">Projektimallides ei saa üldist ressurssi asendada reserveeritava ressursiga.</span><span class="sxs-lookup"><span data-stu-id="f8147-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="f8147-119">Projekti loomine mallist</span><span class="sxs-lookup"><span data-stu-id="f8147-119">Create a project from a template</span></span>  
 <span data-ttu-id="f8147-120">Malli põhjal projekti loomiseks on järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="f8147-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="f8147-121">Projekti loomisel hinnapakkumisest saate valida projektimalli projekti kiirloomise vormil.</span><span class="sxs-lookup"><span data-stu-id="f8147-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="f8147-122">Projekti loomisel, klõpsates valikut **Uus projekt**, kuvatakse enne kirje salvestamist projektivorm.</span><span class="sxs-lookup"><span data-stu-id="f8147-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="f8147-123">Siin saate klõpsata välja **Valige mall**, et valida soovitud mall teie organisatsioonis eelmääratletud projektimallide loendist.</span><span class="sxs-lookup"><span data-stu-id="f8147-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="f8147-124">Klõpsake lehel **Projektimall** valikut **Projekti loomine mallist**, et luua projekt mallist.</span><span class="sxs-lookup"><span data-stu-id="f8147-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="f8147-125">Malli komponentide kopeerimine projekti.</span><span class="sxs-lookup"><span data-stu-id="f8147-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="f8147-126">Malli komponentide kopeerimisel projekti peate teadma järgmist.</span><span class="sxs-lookup"><span data-stu-id="f8147-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="f8147-127">**Tööjaotuse struktuuri kopeerimine**: kui kopeerite projektimallist tööjaotuse struktuuri ja projektil on mallist erinev kalender, rakendatakse ülesannete ajakavale projekti kalendrist pärit töötunnid.</span><span class="sxs-lookup"><span data-stu-id="f8147-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="f8147-128">See kohandab ajakava projekti varukalendri järgi.</span><span class="sxs-lookup"><span data-stu-id="f8147-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="f8147-129">Samamoodi rakendub tööjaotuse struktuuri esimesele ülesandele projekti alguskuupäev, nii et ülesandehierarhia ajakava ülejäänud osa värskendatakse malli tööjaotuse struktuuris määratud kestuse ja sõltuvuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="f8147-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="f8147-130">**Projektiprognooside kopeerimine**: kui kopeerite kogu projektiprognoosi ridade ulatuses, värskendatakse hinnakirju omahinnakirja puhul projekti omanikust üksuse põhjal ja müügihinnakirja puhul kliendi põhjal.</span><span class="sxs-lookup"><span data-stu-id="f8147-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="f8147-131">Ühiku omahind ja müügihind määratakse nende hinnakirjade põhjal müügiüksusega seostatud projektidele.</span><span class="sxs-lookup"><span data-stu-id="f8147-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="f8147-132">**Projektimeeskonna kopeerimine**: projektimeeskonna kopeerimisel mallist projekti kopeeritakse üldised ressursid koos mallis määratletud oskuste ja pädevustega.</span><span class="sxs-lookup"><span data-stu-id="f8147-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="f8147-133">Säilitatakse ka üldised ressursimäärangud, nagu need on projektimallis.</span><span class="sxs-lookup"><span data-stu-id="f8147-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f8147-134">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f8147-134">See Also</span></span>  
 [<span data-ttu-id="f8147-135">Projektijuhi juhend</span><span class="sxs-lookup"><span data-stu-id="f8147-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
