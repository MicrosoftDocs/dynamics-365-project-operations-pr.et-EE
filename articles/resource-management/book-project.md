---
title: Projektile reserveerimine
description: Selles teemas kirjeldatakse projektile ressursi broneerimist.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dff8107864f95c87d25a421dfeeafe9081e98e25
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279989"
---
# <a name="book-to-a-project"></a><span data-ttu-id="60cfb-103">Projektile reserveerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-103">Book to a project</span></span>

<span data-ttu-id="60cfb-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="60cfb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="60cfb-105">Mõnikord peab projektijuht või ressursihaldur määrama projektile ressursi ilma üldise meeskonnaliikme konkreetset nõuet määratlemata.</span><span class="sxs-lookup"><span data-stu-id="60cfb-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="60cfb-106">Seda on võimalik saavutada ühel kolmest viisist.</span><span class="sxs-lookup"><span data-stu-id="60cfb-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="60cfb-107">Meeskonnaliikme ruudustikus broneerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-107">Book from the team member grid</span></span>
- <span data-ttu-id="60cfb-108">Ajakavapaneeli kaudu broneerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-108">Book from the schedule board</span></span>
- <span data-ttu-id="60cfb-109">Vormilt **Projekt** broneerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="60cfb-110">Meeskonnaliikme ruudustikus broneerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-110">Book from the team member grid</span></span>

<span data-ttu-id="60cfb-111">Kui teie organisatsioon tegutseb ressursieralduse hübriidrežiimis, saab projektijuht broneerida ressursi projektile otse, tehes järgnevat.</span><span class="sxs-lookup"><span data-stu-id="60cfb-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="60cfb-112">Minge projektist meeskonnaliikme ruudustikku ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="60cfb-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="60cfb-113">Määratlege ressursi ametikoha nimetus ja roll.</span><span class="sxs-lookup"><span data-stu-id="60cfb-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="60cfb-114">Valige saadaolevast otsingust broneeritav ressurss.</span><span class="sxs-lookup"><span data-stu-id="60cfb-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="60cfb-115">Pärast ressursi valimist määratlege ressursi broneerimiseks järgmine välja teave.</span><span class="sxs-lookup"><span data-stu-id="60cfb-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="60cfb-116">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="60cfb-116">Start date</span></span>
    - <span data-ttu-id="60cfb-117">Lõpukuupäev</span><span class="sxs-lookup"><span data-stu-id="60cfb-117">Finish date</span></span>
    - <span data-ttu-id="60cfb-118">Eraldamismeetod</span><span class="sxs-lookup"><span data-stu-id="60cfb-118">Allocation method</span></span>
    - <span data-ttu-id="60cfb-119">Tunnid, kui on kohaldatav</span><span class="sxs-lookup"><span data-stu-id="60cfb-119">Hours, if applicable</span></span>
    - <span data-ttu-id="60cfb-120">Projekti kinnitaja</span><span class="sxs-lookup"><span data-stu-id="60cfb-120">Project approver</span></span>

6. <span data-ttu-id="60cfb-121">Valige **Salvesta ja sule**</span><span class="sxs-lookup"><span data-stu-id="60cfb-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="60cfb-122">Ajakavapaneeli kaudu broneerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-122">Book from the schedule board</span></span>

<span data-ttu-id="60cfb-123">Kui ressursihaldur peab broneerima ressursi projekti jaoks otse, saavad nad kasutada ajakavapaneeli ja projekti nõuet.</span><span class="sxs-lookup"><span data-stu-id="60cfb-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="60cfb-124">Projekti nõue on ressursi nõue, mille suhtes broneerimine on alati võimalik.</span><span class="sxs-lookup"><span data-stu-id="60cfb-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="60cfb-125">Ressursi ajakavapaneelilt projekti jaoks otse broneerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="60cfb-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="60cfb-126">Liikuge ajakavapaneelil ja filtreerige vasakpoolsel lehel ressursid, mida te nõude jaoks kaalute.</span><span class="sxs-lookup"><span data-stu-id="60cfb-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="60cfb-127">Valige alumisel paanil vahekaart **Projekt**, et kuvada projekti nõuete loend.</span><span class="sxs-lookup"><span data-stu-id="60cfb-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="60cfb-128">Lohistage nõue ressursile ja määratlege järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="60cfb-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="60cfb-129">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="60cfb-129">Start date</span></span>
    - <span data-ttu-id="60cfb-130">Lõpukuupäev</span><span class="sxs-lookup"><span data-stu-id="60cfb-130">Finish date</span></span>
    - <span data-ttu-id="60cfb-131">Broneerigu olek</span><span class="sxs-lookup"><span data-stu-id="60cfb-131">Booking status</span></span>
    - <span data-ttu-id="60cfb-132">Broneerimismeetod</span><span class="sxs-lookup"><span data-stu-id="60cfb-132">Booking method</span></span>
    - <span data-ttu-id="60cfb-133">Kestus</span><span class="sxs-lookup"><span data-stu-id="60cfb-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="60cfb-134">Vormilt Projekt broneerimine</span><span class="sxs-lookup"><span data-stu-id="60cfb-134">Book from the Project form</span></span>

<span data-ttu-id="60cfb-135">Projektijuhina võita tahta broneerida projektile ressursi, kuid teate ressursi nime asemel ainult kriteeriume.</span><span class="sxs-lookup"><span data-stu-id="60cfb-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="60cfb-136">Täitke järgmised juhised, et kasutada ajakavaabilist, et leida resurss mis tahes saadaolevate ressursi atribuutide põhjal.</span><span class="sxs-lookup"><span data-stu-id="60cfb-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="60cfb-137">Liikuge projektile ja valige **Broneeri**, et avada ajakavaabiline.</span><span class="sxs-lookup"><span data-stu-id="60cfb-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="60cfb-138">Kasutades ajakavaabilises vasakul küljel olevaid filtreir, kitsendage kriteeriume ja valige suvand **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="60cfb-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="60cfb-139">Tulemites tagastatud ressursside põhjal saate broneerida ressursi.</span><span class="sxs-lookup"><span data-stu-id="60cfb-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="60cfb-140">See meetod ei loo ressursi jaoks ühtegi broneeringut.</span><span class="sxs-lookup"><span data-stu-id="60cfb-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="60cfb-141">Selle asemel lisab see ressursi meeskonnale.</span><span class="sxs-lookup"><span data-stu-id="60cfb-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="60cfb-142">Pärast meeskonnaliikme projektle lisamist saab projektijuht kasutada broneeringu haldamist või broneeringu pikendamist, et lisada nõutavad broneeringud ressursile.</span><span class="sxs-lookup"><span data-stu-id="60cfb-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]