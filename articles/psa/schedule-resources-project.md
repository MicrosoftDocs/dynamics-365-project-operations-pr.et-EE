---
title: Projekti ressursside ajastamine
description: Projekti ressursside ajastamine Project Service'is
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132127"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="03678-103">Projekti ressursside ajastamine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="03678-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="03678-104">Saate kontrollida ressursi kättesaadavust, et näha ülevaadet oma ressursside reserveeritusest, või filtreerida vaadet oskuste, meeskonna, asukoha ja muude valikute järgi.</span><span class="sxs-lookup"><span data-stu-id="03678-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="03678-105">Ajakavapaneelil kuvatakse ressursside loend ja nende saadavus.</span><span class="sxs-lookup"><span data-stu-id="03678-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="03678-106">Valige saadavust ajavahemikus **Tunnid**, **Päev**, **Nädal** või **Kuu** kuvav vaaterežiim.</span><span class="sxs-lookup"><span data-stu-id="03678-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="03678-107">Enne ajakavapaneeli kasutamist peate selle seadistama.</span><span class="sxs-lookup"><span data-stu-id="03678-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="03678-108">Lisainfo saamiseks, vt jaotist [Ajakavapaneeli konfigureerimine (Field Service või Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="03678-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="03678-109">Kui kasutate vanemat versiooni, uurige ressursside saadavaloleku kohta teabe saamiseks artiklit [Ressursi saadavuse vaatamine](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="03678-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="03678-110">Kui soovite kasutada ajakavapaneeli broneerimise funktsioone, geokodeerimist ja asukohateenuseid, peate sisse lülitama kaartide kasutamise.</span><span class="sxs-lookup"><span data-stu-id="03678-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="03678-111">Valige põhimenüüs suvandid **Ressursiplaanimine** > **Haldus**.</span><span class="sxs-lookup"><span data-stu-id="03678-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="03678-112">Klõpsake valikut **Ajastamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="03678-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="03678-113">Avage kirje ja kerige jaotiseni **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="03678-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="03678-114">Väljal **Ühenda kaartidega** valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="03678-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="03678-115">Nõustuge tingimustega ja salvestage kirje.</span><span class="sxs-lookup"><span data-stu-id="03678-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="03678-116">Valige peamenüüst **Project Service** > **Ajakavapaneel**.</span><span class="sxs-lookup"><span data-stu-id="03678-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="03678-117">Broneeringunõude käsitsi ajastamiseks on siin mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="03678-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="03678-118">Valige meetod, mis teile sobib.</span><span class="sxs-lookup"><span data-stu-id="03678-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="03678-119">Saadaolevate ressursside leidmine</span><span class="sxs-lookup"><span data-stu-id="03678-119">Find available resources</span></span>

1.  <span data-ttu-id="03678-120">Loendis **Broneerimise nõuded** paremklõpsake plaanimata broneeringut ja valige üks järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="03678-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="03678-121">Ajakavapaneelil olevast loendist saadaoleva ressursi leidmiseks valige **Otsi kättesaadavust – praegused ressursid**.</span><span class="sxs-lookup"><span data-stu-id="03678-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="03678-122">Süsteemis olevatest ressurssidest saadaoleva ressursi leidmiseks valige **Otsi kättesaadavust – kõik ressursid**.</span><span class="sxs-lookup"><span data-stu-id="03678-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="03678-123">Kui toimite eelkirjeldatud viisil, kuvavad filtrid valitud broneeringunõude kohta valikuid.</span><span class="sxs-lookup"><span data-stu-id="03678-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="03678-124">Kui näete vaba vahemikku, paremklõpsake plaanimistahvlil ajavahemikku ja valige nupp **Broneeri siin**.</span><span class="sxs-lookup"><span data-stu-id="03678-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="03678-125">Võite ka broneeringunõude vabale ajavahemikule lohistada.</span><span class="sxs-lookup"><span data-stu-id="03678-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="03678-126">Ressursi broneerimine päevavaate abil ja vaatamine, kes on alabroneeritud</span><span class="sxs-lookup"><span data-stu-id="03678-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="03678-127">Ajakavapaneelil valige **Vaaterežiim** ja valige **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="03678-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="03678-128">Kuvatakse tabel, millest on näha, mitu tundi päevas on ressurss broneeritud ja millistel päevadel on see vaba.</span><span class="sxs-lookup"><span data-stu-id="03678-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="03678-129">Ressursi broneerimiseks klõpsake ressursi nime ja seejärel valige **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="03678-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="03678-130">Valige dialoogiboksist **Ressursi broneerimine (loo)** lisaks projektile, mille jaoks soovite ressurssi broneerida, ka broneerimismeetod ja algus- ja lõppkellaajad.</span><span class="sxs-lookup"><span data-stu-id="03678-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="03678-131">Kui olete lõpetanud, valige suvand **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="03678-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="03678-132">Ajakavapaneeli vaade</span><span class="sxs-lookup"><span data-stu-id="03678-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="03678-133">Valige ajastamata broneeringunõue allpool asuvast loendist.</span><span class="sxs-lookup"><span data-stu-id="03678-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="03678-134">Lohistage broneeringunõue ajakavapaneelil saadaoleva ressursi/aja lahtrisse.</span><span class="sxs-lookup"><span data-stu-id="03678-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="03678-135">Kui olete lõpetanud, valige suvand **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="03678-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="03678-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="03678-136">Additional resources</span></span>  
 [<span data-ttu-id="03678-137">Ressursihalduri juhend</span><span class="sxs-lookup"><span data-stu-id="03678-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
