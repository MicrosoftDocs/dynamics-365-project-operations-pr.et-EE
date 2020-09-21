---
title: Uue töötundide malli loomine
description: Töötundide malli loomine Project Service'is
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750992"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="6715d-103">Töötundide malli loomine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6715d-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6715d-104">Enne projekti ajakavade loomist tuleb seadistada projektikalender, mis määratleb ajakavas töötundide arvu päevas ja kõik puhkepäevad.</span><span class="sxs-lookup"><span data-stu-id="6715d-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="6715d-105">Seda saab teha töötundide malliga, mis sisaldab päeva töötundide, vabade päevade ja muude puhkepäevade andmeid.</span><span class="sxs-lookup"><span data-stu-id="6715d-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="6715d-106">Projekti loomisel seote töömalli projektikalendriga ajakava rakendamiseks projektile.</span><span class="sxs-lookup"><span data-stu-id="6715d-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="6715d-107">Töötundide malli loomiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="6715d-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="6715d-108">Töötundide malli loomine ressursi kalendri põhjal.</span><span class="sxs-lookup"><span data-stu-id="6715d-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="6715d-109">Uue töötundide malli loomine.</span><span class="sxs-lookup"><span data-stu-id="6715d-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="6715d-110">Töötundide malli loomine ressursi kalendri põhjal</span><span class="sxs-lookup"><span data-stu-id="6715d-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="6715d-111">Minge jaotisse **Project Service > Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="6715d-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="6715d-112">Valige ressurss, millel teie töötunnid peaksid põhinema.</span><span class="sxs-lookup"><span data-stu-id="6715d-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="6715d-113">Klõpsake käsku **Salvesta kalender nimega**, sisestage töötundide malli nimi ja klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6715d-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="6715d-114">Kui olete valikute muutmise lõpetanud, klõpsake käsku **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="6715d-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="6715d-115">Klõpsake nuppu **Salvesta** ekraani alumises paremas nurgas.</span><span class="sxs-lookup"><span data-stu-id="6715d-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="6715d-116">Uue töötundide malli loomine</span><span class="sxs-lookup"><span data-stu-id="6715d-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="6715d-117">Minge jaotisse **Project Service > Töötundide mallid**.</span><span class="sxs-lookup"><span data-stu-id="6715d-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="6715d-118">Klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6715d-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="6715d-119">Sisestage töötundide malli nimi.</span><span class="sxs-lookup"><span data-stu-id="6715d-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="6715d-120">Valige ressurss, millel töötunnid peaksid põhinema, ja klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6715d-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6715d-121">Vt ka</span><span class="sxs-lookup"><span data-stu-id="6715d-121">See Also</span></span>  
 [<span data-ttu-id="6715d-122">Ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="6715d-122">Set up resources</span></span>](../project-service/set-up-resources.md)
