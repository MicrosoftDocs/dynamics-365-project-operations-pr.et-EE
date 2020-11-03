---
title: Projekti müügi ja kulude hindamine, kui brobeeritav ressurss täidab projektis mitut rolli
description: Selles teemas antakse teavet, kuidas hinnakujunduse dimensioone saab kasutada hinnakujunduse ja kuluarvestuse toetamiseks ressursi jaoks, mis täitab projektil mitut rolli.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075008"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="5c2eb-103">Projekti müügi ja kulude hindamine, kui brobeeritav ressurss täidab projektis mitut rolli</span><span class="sxs-lookup"><span data-stu-id="5c2eb-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="5c2eb-104">Projektipõhiselt tegutsevate ettevõtete puhul peab üks ressurss sageli täitma projektis mitut rolli.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="5c2eb-105">Kõikide nende rollide hinna ja kulu saab määrata eraldi, mis tähendab, et iga rolli arveldus- ja kulumäärast olenevalt, võidakse samal ressursil projektile kulunud aega hinnata rahaliselt erinevalt.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="5c2eb-106">Rakendus Project Service Automation võimaldab meeskonnaliikme kirjel nimetatud ressursside väärtuste häälestamist ja võimaldab iga meeskonnaliikmele määratud ülesande puhul erinevaid alistamisi.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="5c2eb-107">Järgmises näites on selgitatud, kuidas selle väärtuse lihtne alistamine võimaldab ressursil omada projektis mitut rolli koos erinevate kulu- ja arveldusmääraga.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="5c2eb-108">Ülesannete loomine</span><span class="sxs-lookup"><span data-stu-id="5c2eb-108">Create tasks</span></span>
<span data-ttu-id="5c2eb-109">Looge kaks projekti ülesannet (ülesanne A ja ülesanne B), kumbki 40 tundi. Valige ülesanne A ülesande B eelkäijaks.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="5c2eb-110">Üldise projektimeeskonna liikme jaoks rolli ja organisatsiooni üksuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="5c2eb-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="5c2eb-111">Valige lehel **Ajakava** ülesande A jaoks rida **Ülesanne**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="5c2eb-112">Valige väljal **Ressursid** ripploendist suvand **Loo**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="5c2eb-113">Lejel **Meeskonnaliikme kiirloomine** määrake atribuudid üldisele meeskonnaliikmele, kes saab selle ülesande sooritada.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="5c2eb-114">Valige sobiv roll ja organisatsiooniüksus, seejärel valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="5c2eb-115">Luuakse üldine meeskonnaliige ja määratakse sellele ülesandele.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="5c2eb-116">Korrake neid samme ülesande B jaoks ja veenduge, et ülesande B jaoks loodud üldise meeskonnaliikme roll ja organisatsiooniüksus erineksid ülesande A omast.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="5c2eb-117">Projekti ülesande jaoks rolli ja organisatsiooniüksuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="5c2eb-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="5c2eb-118">Pärast ülesande A loomist valige ülesanne ja valige seejärel **Redigeeri ülesannet**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="5c2eb-119">Lehel **Ülesande üksikasjad** leidke väljad **Roll** ja **Organisastioooniüksus** , lisage väärtused, mis on nõutavad ressursilt, kes selle ülesande sooritab.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="5c2eb-120">Kui läbite selle stsenaariumi kasutades rakenduse Project Service Automation demoandmeid, valige rolliks **Konsulteeriv müügivihje** ja organisatsiooniüksuseks **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="5c2eb-121">Valige ülesanne B ja valige seejärel **Redigeeri ülesannet**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="5c2eb-122">Lehel **Ülesande üksikasjad** leidke väljad **Roll** ja **Organisastioooniüksus** , lisage väärtused, mis on nõutavad ressursilt, kes selle ülesande sooritab.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="5c2eb-123">Veenduge, et ülesande B ja ülesande A väljade **Roll** ja **Organisatsiooniüksus** väärtused oleksid erinevad.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="5c2eb-124">Kui läbite selle stsenaariumi kasutades rakenduse Project Service Automation demoandmeid, valige rolliks **Võrgutehnik** ja organisatsiooniüksuseks **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="5c2eb-125">Salvestage ja sulgege leht **Ülesande üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="5c2eb-126">Meeskonnaliige ja prognooside käitumine</span><span class="sxs-lookup"><span data-stu-id="5c2eb-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="5c2eb-127">Lehel **Ülesande üksikasjad** suvandis **Meeskonnaliige** valige kaks üldist meeskonnaliiget ja valige seejärel **Loo nõuded**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="5c2eb-128">See loob ressursinõuded.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="5c2eb-129">Valige suvandi **Konsulteeriv müügivihje** jaoks meeskonnaliige ja valige seejärel **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="5c2eb-130">Avaneb ajakavapaneel ja broneerib selle nõude jaoks ressursi.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="5c2eb-131">Valige suvandi **Võrgutehnik** jaoks meeskonnaliige ja valige **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="5c2eb-132">Avaneb ajakavapaneel ja broneerib selle nõude jaoks sama ressursi.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="5c2eb-133">Meeskonnaliikme ruudustik</span><span class="sxs-lookup"><span data-stu-id="5c2eb-133">Team Member grid</span></span> 
<span data-ttu-id="5c2eb-134">Pange tähele, et ruudustikus **Meeskonnaliige** on kaks üldist meeskonnaliikme kirjet kustutatud ja asendatud ühe ressursiga.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="5c2eb-135">Selle ressursi jaoks on üks väärtuste komplekt, mis kuvab väljade **Roll** ja **Organisatsiooniüksus** jaoks vaikimisi väärtuste komplekti.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="5c2eb-136">Kui te selle meeskonnaliikme kirje rida laiendate, näete meeskonnaliikme kirjes mõlema selle ülesande jaoks eraldi määramist.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="5c2eb-137">Igal ülesandereal on väljade **Roll** ja **Organisatsiooniüksus** jaoks konkreetsed ülesande väärtused.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="5c2eb-138">Prognooside ruudustik</span><span class="sxs-lookup"><span data-stu-id="5c2eb-138">Estimates grid</span></span> 
<span data-ttu-id="5c2eb-139">Kui te navigeerite ruudustikku **Prognoosid** , siis märkate, et sama ressursi mõlemad määramised on erineva hinnakirjaga.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="5c2eb-140">Ülesande A ressursi määramise hind on tehtud kindlaks kasutades atribuudi **Roll** väärtust suvandist **Konsulteeriv müügivihje**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="5c2eb-141">Ülesande B sama ressursi määramise hind on tehtud kindlaks kasutades atribuudi **Roll** väärtust suvandist **Võrgutehnik**.</span><span class="sxs-lookup"><span data-stu-id="5c2eb-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





