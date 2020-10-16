---
title: Ajavööndite haldamine
description: Projekti loomisel põhineb selle ajavöönd rakendatud töötunni mallis määratletud ajavööndil.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961850"
---
# <a name="manage-time-zones"></a><span data-ttu-id="c1950-103">Ajavööndite haldamine</span><span class="sxs-lookup"><span data-stu-id="c1950-103">Manage time zones</span></span>

<span data-ttu-id="c1950-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="c1950-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="c1950-105">Projektid</span><span class="sxs-lookup"><span data-stu-id="c1950-105">Projects</span></span>

<span data-ttu-id="c1950-106">Projekti loomisel põhineb selle ajavöönd rakendatud töötunni mallis määratletud ajavööndil.</span><span class="sxs-lookup"><span data-stu-id="c1950-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="c1950-107">**Projektis** on kuupäevad alati seotud igale vahekaardile sisse logitud kasutaja ajavööndiga, välja arvatud vahekaardil **Ülesanne**. Tööjaotuse struktuuri kuvamisel kuvatakse kuupäevad alati projekti ajavööndis.</span><span class="sxs-lookup"><span data-stu-id="c1950-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="c1950-108">Ülesanded</span><span class="sxs-lookup"><span data-stu-id="c1950-108">Tasks</span></span>

<span data-ttu-id="c1950-109">Ülesande loomisel kontrollivad algusaega, lõpuaega ja tundi/päeva projekti töötunnid.</span><span class="sxs-lookup"><span data-stu-id="c1950-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="c1950-110">Näiteks kui ülesanne luuakse projektiga, mille ajavöönd on –8 PST ja selle töötunnid on esmaspäevast reedeni 9.00–17.00, arvestavad kõik ülesanded, mis on loodud ilma määramiseta, projekti kalendri algusaja ja lõpuajaga.</span><span class="sxs-lookup"><span data-stu-id="c1950-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="c1950-111">Ajavöönditega ressursside haldamine</span><span class="sxs-lookup"><span data-stu-id="c1950-111">Manage resources with time zones</span></span>

<span data-ttu-id="c1950-112">Suvandi **Broneeringu pikendamine** kasutamisel täpsete ja prognoositavate tulemite jaoks on vaja täita kaks olulist eeltingimust.</span><span class="sxs-lookup"><span data-stu-id="c1950-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="c1950-113">Kasutaja peab konfigureerima oma seadme ajavööndi, et see vastaks süsteemi suvandis **Isikupärastamise sätted** määratletud ajavööndile.</span><span class="sxs-lookup"><span data-stu-id="c1950-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Ajavööndi sätted operatsioonisüsteemis Windows 10](media/reconcile-assignments-03.png)

  ![Ajavööndi sätted isikupärastamise sätetes](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="c1950-116">Broneeritaval ressursil peab olema vähemalt üks minut tööaega, mis kattub kontuuridega, mida kasutatakse taotletud laienduse määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="c1950-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="c1950-117">Näiteks järgmised ressursid, mille tööaeg jääb vahemikku 9.00–19.00.</span><span class="sxs-lookup"><span data-stu-id="c1950-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Ressursi kontuuride võrdlus](media/reconcile-assignments-05.png)

<span data-ttu-id="c1950-119">Järgnev tabel näitab järgmist.</span><span class="sxs-lookup"><span data-stu-id="c1950-119">The following table shows:</span></span>

- <span data-ttu-id="c1950-120">Projekti kalendri mall</span><span class="sxs-lookup"><span data-stu-id="c1950-120">A project calendar template</span></span>
- <span data-ttu-id="c1950-121">Ressurss A: sellel ressursil on sama kalender ja see on projektiga samas ajavööndis.</span><span class="sxs-lookup"><span data-stu-id="c1950-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="c1950-122">Broneeringute algusaeg on 9:00.</span><span class="sxs-lookup"><span data-stu-id="c1950-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="c1950-123">Ressurss B: see ressurss asub erinevas ajavööndis kui projekt ja alustab oma ajavööndis kell 7.00.</span><span class="sxs-lookup"><span data-stu-id="c1950-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="c1950-124">Kuid broneeringud algavad kell 9:00, kuna see on määramise kontuuri varaseim alguskellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c1950-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="c1950-125">Ressursid C ja D: ressursid asuvad erinevates ajavööndites, mõlemad erinevad üksteise ja projekti ajavööndist, ja nende broneeringud ei alga varem kui nende vastavad saadavuse algusajad.</span><span class="sxs-lookup"><span data-stu-id="c1950-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="c1950-126">Olem</span><span class="sxs-lookup"><span data-stu-id="c1950-126">Entity</span></span>  |<span data-ttu-id="c1950-127">Calendar</span><span class="sxs-lookup"><span data-stu-id="c1950-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="c1950-128">Projekti kalendri mall</span><span class="sxs-lookup"><span data-stu-id="c1950-128">Project calendar template</span></span>   | ![projekti kalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c1950-130">Ressurss A</span><span class="sxs-lookup"><span data-stu-id="c1950-130">Resource A</span></span>  | ![Ressursi A kalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c1950-132">Ressurss B</span><span class="sxs-lookup"><span data-stu-id="c1950-132">Resource B</span></span>  |  ![Ressursi B kalender](media/reconcile-assignments-07.png) |
|<span data-ttu-id="c1950-134">Ressurss C</span><span class="sxs-lookup"><span data-stu-id="c1950-134">Resource C</span></span>  |  ![Ressursi C kalender](media/reconcile-assignments-08.png) |
|<span data-ttu-id="c1950-136">Ressurss D</span><span class="sxs-lookup"><span data-stu-id="c1950-136">Resource D</span></span>  | ![Ressursi D kalender](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="c1950-138">Kui liigute vaatesse **Vastavusse viimine**, kuvatakse ressursi määramised ja seostatud broneeringu puudujäägid.</span><span class="sxs-lookup"><span data-stu-id="c1950-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vastavusseviimise vaade enne pikendamist](media/reconcile-assignments-10.png)

<span data-ttu-id="c1950-140">Kui iga ressursi jaoks on kasutatud broneeringu pikendamise funktsiooni, pikendatakse iga ressursi broneeringuid, kuna iga ressursi tööajad kattuvad puudujäägi kontuuridega.</span><span class="sxs-lookup"><span data-stu-id="c1950-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vastavusseviimise vaade pärast broneeringu pikendamist](media/reconcile-assignments-11.png) 

<span data-ttu-id="c1950-142">Pange tähele, et broneeringute üksikasjade täpsem vaatamine näitab, et broneeringute algusaeg on erinev.</span><span class="sxs-lookup"><span data-stu-id="c1950-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="c1950-143">Broneeringud ei alusta varem kui määramise kontuuri algusaeg ja mitte varem kui ressursi saadavuse algusaeg.</span><span class="sxs-lookup"><span data-stu-id="c1950-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Ajakavapaneelil olevate ressursside uued broneeringud](media/reconcile-assignments-12.png)
