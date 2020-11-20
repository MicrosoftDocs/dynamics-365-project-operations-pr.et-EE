---
title: Projekti sätted
description: Selles teemas antakse teavet projektihalduse sätete kohta.
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123103"
---
# <a name="project-settings"></a><span data-ttu-id="94353-103">Projekti sätted</span><span class="sxs-lookup"><span data-stu-id="94353-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="94353-104">Projekti plaanimise funktsioonidele juurdepääsemiseks kasutage järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="94353-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="94353-105">Töömall</span><span class="sxs-lookup"><span data-stu-id="94353-105">Work template</span></span>

<span data-ttu-id="94353-106">Projekti ajakava loomiseks peate looma projektikalendri malli, mis määratleb töötundide arvu päevas ja kõik äri lõpetamised.</span><span class="sxs-lookup"><span data-stu-id="94353-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="94353-107">Projektikalendri malli loomiseks seostage projekti väljaga **Kalendrimall** töömall.</span><span class="sxs-lookup"><span data-stu-id="94353-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="94353-108">Töömalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="94353-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="94353-109">Klõpsake rakenduse PSA vasakpoolsel navigeerimispaanil nuppu **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="94353-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="94353-110">Avage loendilehel **Ressursid** kasutajakirje ja seejärel tehke valik **Kuva töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="94353-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="94353-111">Veenduge, et brauseriaknas oleks hüpikaknad lubatud.</span><span class="sxs-lookup"><span data-stu-id="94353-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="94353-112">Nii saate vaadata ressursi jaoks määratud töötunde.</span><span class="sxs-lookup"><span data-stu-id="94353-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="94353-113">Klõpsake vahekaardil **Kuuvaade** nuppu **Seadista**.</span><span class="sxs-lookup"><span data-stu-id="94353-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="94353-114">Kuvatakse kolme suvandiga loend.</span><span class="sxs-lookup"><span data-stu-id="94353-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="94353-115">Uus nädalagraafik</span><span class="sxs-lookup"><span data-stu-id="94353-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="94353-116">Ühe päeva töögraafik</span><span class="sxs-lookup"><span data-stu-id="94353-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="94353-117">Vaba aeg</span><span class="sxs-lookup"><span data-stu-id="94353-117">Time Off</span></span>

> ![Suvandite seadistamine](media/project-13.png)

4. <span data-ttu-id="94353-119">Tehke valik **Uus nädalagraafik** ja seejärel määrake selle ressurside ajakava suvandid.</span><span class="sxs-lookup"><span data-stu-id="94353-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="94353-120">Saate määrata korduva nädalagraafiku, iga päeva tunniparameetrid, äri lõpetamised ja muud.</span><span class="sxs-lookup"><span data-stu-id="94353-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="94353-121">Määrake kuupäevavahemik, tehke valik **Salvesta** ja seejärel klõpsake käsku **Sule**.</span><span class="sxs-lookup"><span data-stu-id="94353-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="94353-122">Minge tagasi loendilehele **Ressursid** ja valige ressurss, mille jaoks töötunde määrate.</span><span class="sxs-lookup"><span data-stu-id="94353-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="94353-123">Töömalli määramiseks tehke valik **Seadista kalender nimega**.</span><span class="sxs-lookup"><span data-stu-id="94353-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="94353-124">Sisestage dialoogiboksis **Töömall** töömalli nimi ja seejärel tehke valik **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="94353-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="94353-125">Nüüd saate seostada töömalli projektikalendri malliga.</span><span class="sxs-lookup"><span data-stu-id="94353-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="94353-126">Ressursirollid</span><span class="sxs-lookup"><span data-stu-id="94353-126">Resource roles</span></span>

<span data-ttu-id="94353-127">Mõiste *ressursiroll* viitab oskuste, pädevuste ja sertide komplektile, mis peavad isikul olema, et teha projekti jaoks teatud ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="94353-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="94353-128">Rakendus PSA võimaldab teil vastavalt rollile, millega ressurss seotud on, ressursi ajakulu arvesse võtta ja sellega arveldada.</span><span class="sxs-lookup"><span data-stu-id="94353-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="94353-129">Kõik organisatsioonid peavad need rollid seadistama, kasutades selleks menüü **Project Service** vasakpoolset navigeerimist.</span><span class="sxs-lookup"><span data-stu-id="94353-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="94353-130">Kõik organisatsioonid peavad need rollid seadistama lehel **Aktiivsed ressursikategooriad**.</span><span class="sxs-lookup"><span data-stu-id="94353-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="94353-131">Selle lehe avamiseks valige vasakpoolsel navigeerimispaanil suvand **Ressursirollid**.</span><span class="sxs-lookup"><span data-stu-id="94353-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="94353-132">Hinnakirjad</span><span class="sxs-lookup"><span data-stu-id="94353-132">Price lists</span></span>

<span data-ttu-id="94353-133">Hinnakirjad võimaldavad teil määrata organisatsioonis ressursirollide, kulukategooriate, toodete ja muude elementide jaoks oma- ning müügihinnad.</span><span class="sxs-lookup"><span data-stu-id="94353-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="94353-134">Enne, kui määrate projekti jaoks edastatava töö finantskalkulatsioonid, peate looma tugikulud ja müügihinnakirja.</span><span class="sxs-lookup"><span data-stu-id="94353-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="94353-135">Peate parameetrite jaotises seadistama ka vaikimisi kulu- ja müügihinnakirja, mis rakendub kõigile organisatsioonis loodavatele projektidele.</span><span class="sxs-lookup"><span data-stu-id="94353-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="94353-136">Seadistage kindlasti lehel **Aktiivsed projektiparameetrid** vaikimisi kulu- ja müügihinnakiri.</span><span class="sxs-lookup"><span data-stu-id="94353-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
