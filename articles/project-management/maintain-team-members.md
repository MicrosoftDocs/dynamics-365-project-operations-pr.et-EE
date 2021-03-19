---
title: Meeskonnaliikmete haldamine
description: See teema pakub teavet projekti meeskondadele nimega ressursside broneerimise ja nende ülesannetele määramise kohta.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286828"
---
# <a name="maintain-team-members"></a><span data-ttu-id="a9594-103">Meeskonnaliikmete haldamine</span><span class="sxs-lookup"><span data-stu-id="a9594-103">Maintain team members</span></span>

<span data-ttu-id="a9594-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="a9594-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a9594-105">Saate lisada nimega ressursi oma projekti meeskonnale, kui broneerite neid otse meeskonnale.</span><span class="sxs-lookup"><span data-stu-id="a9594-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="a9594-106">Avage rakenduses Dynamics 365 Project Operations **Projektid** ja valige selle projekti avamine, mille jaoks broneerite.</span><span class="sxs-lookup"><span data-stu-id="a9594-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="a9594-107">Valige lehel **Projekt** vahekaardil **Meeskond** nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a9594-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="a9594-108">Valige dialoogiboksis **Kiirloomine: projekti meeskonnaliige** broneeritav ressurss.</span><span class="sxs-lookup"><span data-stu-id="a9594-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="a9594-109">Välja **Roll** täidetakse ressursi vaikerolliga, kui neil on selline määratud.</span><span class="sxs-lookup"><span data-stu-id="a9594-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="a9594-110">Saate rolli muuta.</span><span class="sxs-lookup"><span data-stu-id="a9594-110">You can change the role.</span></span> 
4. <span data-ttu-id="a9594-111">Valige ressursside vajalike kuupäevade algus- ja lõpukuupäevad ning valige ressursi võimsuse jaotamise meetod.</span><span class="sxs-lookup"><span data-stu-id="a9594-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="a9594-112">Kui soovite, et meeskonnaliige oleks projekti kinnitaja, valige väljal **Projekti kinnitaja** suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a9594-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="a9594-113">Meeskonnaliige saab kinnitada selle projekti jaoks esitatud aja- ja kulukirjeid.</span><span class="sxs-lookup"><span data-stu-id="a9594-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="a9594-114">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a9594-114">Select **Save**.</span></span>

<span data-ttu-id="a9594-115">Nüüd saate projekti tööülesannetele määrata broneeritud ressursi.</span><span class="sxs-lookup"><span data-stu-id="a9594-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="a9594-116">Määrake lehel **Projekt** vahekaardili **Ajakava** uuele ressursile tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="a9594-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="a9594-117">Ressursivalijat, mis käivitatakse ülesande ruudustikus väljal **Ressursid**, kuvab meeskonnaliikmed, keda saate valida.</span><span class="sxs-lookup"><span data-stu-id="a9594-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="a9594-118">Rakenduses Project Operations ei ole ressursi broneerimised ega ülesande määramised tihedalt seotud.</span><span class="sxs-lookup"><span data-stu-id="a9594-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="a9594-119">Kui kasutate ressursivalijat ajakavas, saate meeskonnaliikmetele määrata rohkem tööülesanded kui nende broneeringud projektis katavad.</span><span class="sxs-lookup"><span data-stu-id="a9594-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="a9594-120">Meeskonnaliikme broneeringute ja määramiste vahelised erinevused on näidatud vahekaartidel **Meeskond** ja **Ressursi vastavusseviimine**.</span><span class="sxs-lookup"><span data-stu-id="a9594-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="a9594-121">Samuti saate sobitada erinevused ressursside broneeringute ja määrangute vahel üksikasjalikumal tasemel.</span><span class="sxs-lookup"><span data-stu-id="a9594-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="a9594-122">Kasutage vahekaardil **Ajakava** ressursivalijat, et otsida ja valida broneeritavaid ressursse, mis pole juba projekti meeskonna osa.</span><span class="sxs-lookup"><span data-stu-id="a9594-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="a9594-123">Need ressursid kuvatakse ressursivalijas suvandina **Muud ressursid**.</span><span class="sxs-lookup"><span data-stu-id="a9594-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="a9594-124">Kui te teete valiku, lisatakse ressurss projekti meeskonda ja määratakse tööülesandele, kuid broneeringuid ei looda.</span><span class="sxs-lookup"><span data-stu-id="a9594-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="a9594-125">Ressursi võimsuse broneerimiseks projektile saate kasutada vahekaardi **Sobitamine** pikendatud broneerimise võimalust või vahekaarti **Ajakava**.</span><span class="sxs-lookup"><span data-stu-id="a9594-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="a9594-126">Pärast seda, kui meeskonnaliige on teie projektile broneeritud, saate kasutada suvandeid **Säilita broneeringud** või **Ajakavapaneel** otse, et hallata oma broneeringuid.</span><span class="sxs-lookup"><span data-stu-id="a9594-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]