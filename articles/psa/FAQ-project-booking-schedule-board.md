---
title: Projekti reserveeringu loomine ajakavapaneelilt
description: Selles teemas kirjeldatakse, kuidas ajakavapaneelilt projekti reserveeringut luua.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122293"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="b397c-103">Projekti reserveeringu loomine ajakavapaneelilt</span><span class="sxs-lookup"><span data-stu-id="b397c-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="b397c-104">Te saate ressursi projektile reserveerida kas otse vahekaardil **Meeskond** või luues ressursinõude üldise meeskonnaliikme määrangust ja seejärel loodud nõuet projekti meeskonnaliikmega täites.</span><span class="sxs-lookup"><span data-stu-id="b397c-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="b397c-105">Samuti saate ressurssi projektile reserveerida otse ajakavapaneelilt.</span><span class="sxs-lookup"><span data-stu-id="b397c-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="b397c-106">Selle tegemiseks on kolm viisi:</span><span class="sxs-lookup"><span data-stu-id="b397c-106">There are three ways to do this:</span></span>

- <span data-ttu-id="b397c-107">**Broneerige loodud ressursinõudest:** saate luua ressursinõude pärast seda, kui loote üldise ressursi ja määrate projekti raames tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="b397c-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="b397c-108">**Broneerige esmasest nõudest:** esmased nõuded kuvatakse ajakavapaneelil vahekaardil **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b397c-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="b397c-109">**Broneerige uuest ressursinõudest:** saate luua ressursinõude nullist ja seostada selle projektiga.</span><span class="sxs-lookup"><span data-stu-id="b397c-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="b397c-110">Ajakavapaneelil kuvatakse ressursinõuet vahekaardil **Avatud nõuded**.</span><span class="sxs-lookup"><span data-stu-id="b397c-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="b397c-111">Loodud ressursinõude kaudu reserveerimine</span><span class="sxs-lookup"><span data-stu-id="b397c-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="b397c-112">Saate luua üldise ressursi ja määrata sellele projektis ülesande või mitu ülesannet.</span><span class="sxs-lookup"><span data-stu-id="b397c-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="b397c-113">Seejärel loote üldise meeskonnaliikme kaudu ressursinõude.</span><span class="sxs-lookup"><span data-stu-id="b397c-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="b397c-114">Ajakavapaneelil kuvatakse seda ressursinõuet vahekaardil **Avatud nõuded**. Kui teil on mitu avatud nõuet, võib teil ruudustikus vaja minna veerufiltrite abi.</span><span class="sxs-lookup"><span data-stu-id="b397c-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="b397c-115">![Nõude vahekaardi avamine ajakavapaneelil](media/FAQ-Project-Booking-Schedule-Board-1.png "Kuvatõmmis reserveeringute ja määrangute tabelist")</span><span class="sxs-lookup"><span data-stu-id="b397c-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="b397c-116">Valige nõue.</span><span class="sxs-lookup"><span data-stu-id="b397c-116">Select the requirement.</span></span> <span data-ttu-id="b397c-117">Valitud rea kohal avaneb vahekaart **Otsi kättesaadavust**.</span><span class="sxs-lookup"><span data-stu-id="b397c-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="b397c-118">Selle vahekaardi valimine käivitab ajakavapaneeli ajakava abi, mis filtreerib ressursinõudele vastavad saadavalolevad ressursid.</span><span class="sxs-lookup"><span data-stu-id="b397c-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="b397c-119">Pärast seda saate ressurssi reserveerida.</span><span class="sxs-lookup"><span data-stu-id="b397c-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="b397c-120">Samuti saate ajakavapaneeli all valitud rea pukseerida ülalolevas ruudustikus olevale ressursile.</span><span class="sxs-lookup"><span data-stu-id="b397c-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="b397c-121">Kui selle paigale asetate, avaneb paremal paneel **Ressursi reserveeringu loomine**.</span><span class="sxs-lookup"><span data-stu-id="b397c-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="b397c-122">Käsu **Reserveeri** valimine reserveerib ressursi projekti meeskonda.</span><span class="sxs-lookup"><span data-stu-id="b397c-122">Selecting **Book** books the resource onto the project team.</span></span>

![Ressursi broneeringu loomine](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="b397c-124">Peamisest nõudest reserveerimine</span><span class="sxs-lookup"><span data-stu-id="b397c-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="b397c-125">Projekti loomisel rakenduses Project Service luuakse automaatselt ressursinõue nimetusega peamine nõue.</span><span class="sxs-lookup"><span data-stu-id="b397c-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="b397c-126">Tegemist on tühja nõudega, mida kasutatakse ajakavapaneeli kaudu ressursi kiireks reserveerimiseks ilma nõude genereerimiseta või täiesti uue nõude loomiseta.</span><span class="sxs-lookup"><span data-stu-id="b397c-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="b397c-127">Kuna nõue on tühi, peate täpsustama nii kuupäevad kui ka eraldamismeetodi ja vajaduse korral tunnid.</span><span class="sxs-lookup"><span data-stu-id="b397c-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="b397c-128">Peamise nõudega ressursi reserveerimiseks ajakavapaneelil valige vahekaart **Projekt**. Kui teil on palju projekte, peate võib olla kasutama veerus **Projekt** veerufiltreid.</span><span class="sxs-lookup"><span data-stu-id="b397c-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="b397c-129">![Veerufiltrid ajakavapaneelil](media/FAQ-Project-Booking-Schedule-Board-2.png "Kuvatõmmis reserveeringute ja määrangute tabelist")</span><span class="sxs-lookup"><span data-stu-id="b397c-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="b397c-130">Valige nõue, mille nimeks on vaid projekti nimi ja kestus on null (0).</span><span class="sxs-lookup"><span data-stu-id="b397c-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="b397c-131">Valige rea kohal avanev vahekaart **Otsi kättesaadavust**.</span><span class="sxs-lookup"><span data-stu-id="b397c-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="b397c-132">See käivitab ajakavapaneeli ajakava abirežiimi ja näitab saadavalolevaid ressursse, mida saab projektile reserveerida.</span><span class="sxs-lookup"><span data-stu-id="b397c-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="b397c-133">Kuna **peamine nõue** on tühi nõue, mille kestus on null (0), peate kestuse määrama paneeli **Ressursi reserveeringu loomine** kaudu, kui valite ja reserveerite ressursi.</span><span class="sxs-lookup"><span data-stu-id="b397c-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="b397c-134">Samuti saate valida **projekti peamise nõude** ajakavapaneeli alt ja pukseerida selle ressursile, et reserveerida.</span><span class="sxs-lookup"><span data-stu-id="b397c-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="b397c-135">Kuna **peamine nõue** on tühi nõue, mille kestus on null (0), peate kestuse määrama paneeli **Ressursi reserveeringu loomine** kaudu, kui valite ja reserveerite ressursi.</span><span class="sxs-lookup"><span data-stu-id="b397c-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="b397c-136">Kui reserveerite ressurssi ajakavapaneeli **peamise nõude** kaudu, siis lisate selle projekti meeskonnale ilma ühegi määranguta.</span><span class="sxs-lookup"><span data-stu-id="b397c-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="b397c-137">Uue ressursinõude kaudu reserveerimine</span><span class="sxs-lookup"><span data-stu-id="b397c-137">Book from a new resource requirement</span></span>
<span data-ttu-id="b397c-138">Uue ressursinõude kaudu broneerimiseks täitke järgmised juhised.</span><span class="sxs-lookup"><span data-stu-id="b397c-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="b397c-139">Avage jaotis **Ressursinõuded** ja valige käsk **Uus**, et luua uus ressursinõue.</span><span class="sxs-lookup"><span data-stu-id="b397c-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="b397c-140">Valige vahekaardil **Projekt** projekti nõude seostamiseks projekt.</span><span class="sxs-lookup"><span data-stu-id="b397c-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="b397c-141">Seda uut nõuet kuvatakse ajakavapaneelil **avatud nõudena**, mida saate täita.</span><span class="sxs-lookup"><span data-stu-id="b397c-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="b397c-142">Reserveerige ressurss, et lisada see projekti meeskonda.</span><span class="sxs-lookup"><span data-stu-id="b397c-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="b397c-143">Nüüd, kui ressurss on reserveeritud, peate ülesandeid käsitsi määrama.</span><span class="sxs-lookup"><span data-stu-id="b397c-143">Now that the resource is booked, you must assign tasks manually.</span></span>

