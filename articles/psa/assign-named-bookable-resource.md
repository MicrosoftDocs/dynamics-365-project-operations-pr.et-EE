---
title: Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid
description: See teema pakub teavet projekti meeskondadele nimega ressursside broneerimise ja nende ülesannetele määramise kohta.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6169f2bdc107e63d666fb32d34f531fd5d472c2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291434"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="997a9-103">Broneerige projekti meeskonnale nimega broneeritavad ressursid ja määrake ülesandeid</span><span class="sxs-lookup"><span data-stu-id="997a9-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="997a9-104">Saate lisada nimega ressursi oma projekti meeskonnale, kui broneerite neid otse meeskonnale.</span><span class="sxs-lookup"><span data-stu-id="997a9-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="997a9-105">Selle tegemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="997a9-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="997a9-106">Avage rakenduses Project Service Automation suvand **Projektid**, ja valige selle projekti avamine, mille jaoks broneerite.</span><span class="sxs-lookup"><span data-stu-id="997a9-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="997a9-107">Klõpsake lehel **Projekt** vahekaardil **Meeskond** nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="997a9-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Meeskonnaliikme lisamine meeskonna vahekaardi kaudu](media/RM-how-to-1.png)

3. <span data-ttu-id="997a9-109">Valige dialoogiboksis **Kiirloomine: projekti meeskonnaliige** broneeritav ressurss.</span><span class="sxs-lookup"><span data-stu-id="997a9-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="997a9-110">Välja **Roll** täidetakse ressursi vaikerolliga, kui neil on selline määratud.</span><span class="sxs-lookup"><span data-stu-id="997a9-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="997a9-111">Vajaduse korral saate rolli muuta.</span><span class="sxs-lookup"><span data-stu-id="997a9-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="997a9-112">Valige ressursside vajalike kuupäevade algus- ja lõppkuupäevad ning valige ressursi võimsuse jaotamise meetod.</span><span class="sxs-lookup"><span data-stu-id="997a9-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="997a9-113">Kui soovite, et meeskonnaliige oleks projekti kinnitaja, valige väljal **Projekti kinnitaja** suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="997a9-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="997a9-114">See tähendab, et meeskonnaliige saab kinnitada selle projekti jaoks esitatud aja- ja kulukirjeid.</span><span class="sxs-lookup"><span data-stu-id="997a9-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="997a9-115">Klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="997a9-115">Click **Save**.</span></span>

![Meeskonnaliikme lisamine kiirloomise vormile](media/RM-how-to-2.png)


<span data-ttu-id="997a9-117">Nüüd saate projekti tööülesannetele määrata broneeritud ressursi.</span><span class="sxs-lookup"><span data-stu-id="997a9-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="997a9-118">Klõpsake lehel **Projekt** vahekaarti **Ajakava**, et määrata tööülesanded uuele ressursile.</span><span class="sxs-lookup"><span data-stu-id="997a9-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="997a9-119">Ressursivalijat, mis käivitatakse ülesande ruudustikus väljal **Ressursid**, kuvab meeskonnaliikmed, keda saate valida.</span><span class="sxs-lookup"><span data-stu-id="997a9-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Meeskonnaliikme määramine tööülesandele ajakava vahekaardil](media/RM-how-to-3.png)

<span data-ttu-id="997a9-121">Rakenduse Project Service Automation (PSA) versioonis 3 pole ressursi broneerimised ja määrangud tihedalt ühendatud.</span><span class="sxs-lookup"><span data-stu-id="997a9-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="997a9-122">See tähendab, et kui kasutate ressursivalijat ajakavas, saate meeskonnaliikmetele määrata rohkem tööülesanded kui nende broneeringud projektis katavad.</span><span class="sxs-lookup"><span data-stu-id="997a9-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="997a9-123">Meeskonnaliikmete broneerimiste ja määrangute vahelisi erinevusi saate vaadata vahekaardilt **Meeskond** või vahekaardilt **Ressursi sobitamine**. Samuti saate sobitada erinevused ressursside broneeringute ja määrangute vahel üksikasjalikumal tasemel.</span><span class="sxs-lookup"><span data-stu-id="997a9-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Ressursi sobitamise vahekaart](media/RM-how-to-4.png)

<span data-ttu-id="997a9-125">Vahekaardil **Ajakava** saate kasutada ka ressursivalijat, et otsida ja valida broneeritavaid ressursse, mis pole juba projekti meeskonna osa.</span><span class="sxs-lookup"><span data-stu-id="997a9-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="997a9-126">Need kuvatakse ressursivalijas suvandina **Muud ressursid**.</span><span class="sxs-lookup"><span data-stu-id="997a9-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Meeskonnavälise liikme ressursi määramine ülesandele](media/RM-how-to-5.png)

<span data-ttu-id="997a9-128">Kui te seda teete, lisatakse ressurss projekti meeskonda ja määratakse tööülesandele, kuid broneeringuid ei looda.</span><span class="sxs-lookup"><span data-stu-id="997a9-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Meeskonnaliige määrangute ja broneeringutega](media/RM-how-to-6.png)

<span data-ttu-id="997a9-130">Ressursi võimsuse broneerimiseks projektile saate kasutada vahekaardi **Sobitamine** pikendatud broneerimise võimalust või vahekaarti **Ajakava**.</span><span class="sxs-lookup"><span data-stu-id="997a9-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Meeskonnaliikme broneeringu pikendamine ressursi sobitamise vahekaardil](media/RM-how-to-7.png)

<span data-ttu-id="997a9-132">Pärast seda, kui meeskonnaliige on teie projektile broneeritud, saate broneeringuid säilitada või kasutada graafikut otse, et hallata oma broneeringuid.</span><span class="sxs-lookup"><span data-stu-id="997a9-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]