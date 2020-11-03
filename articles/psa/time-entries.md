---
title: Ajakirjete loomine
description: Selles teemas kirjeldatakse, kuidas luua ajakirjeid.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075047"
---
# <a name="create-time-entries"></a><span data-ttu-id="a21c4-103">Ajakirjete loomine</span><span class="sxs-lookup"><span data-stu-id="a21c4-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a21c4-104">Varasemates Dynamics 365 Project Service Automation versioonides sisestati ajakirjeid kord nädalas.</span><span class="sxs-lookup"><span data-stu-id="a21c4-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="a21c4-105">Project Service Automation versioonis 3 sisestatakse ajakirjeid iga päev.</span><span class="sxs-lookup"><span data-stu-id="a21c4-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="a21c4-106">Kuid pärast paari ajakirje loomist saate neid luua või kopeerida hulgi kaupa.</span><span class="sxs-lookup"><span data-stu-id="a21c4-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="a21c4-107">Loo ajakirje</span><span class="sxs-lookup"><span data-stu-id="a21c4-107">Create a time entry</span></span>

<span data-ttu-id="a21c4-108">Ajakirje loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a21c4-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="a21c4-109">Valige lehel **Ajakirjed** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="a21c4-110">Sisestage dialoogiboksi **Kiirloomine: ajakirje** ajakirje kestus minutites, tundides või päevades.</span><span class="sxs-lookup"><span data-stu-id="a21c4-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="a21c4-111">Kestus tuleb sisestada järgmises vormingus: *x* minut(it), *x* tund(i) või *x* päev(a).</span><span class="sxs-lookup"><span data-stu-id="a21c4-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="a21c4-112">Tunde ja päevi saab sisestada ka kümnendkohtade kasutamisega, näiteks *x,x* tundi või *x,x* päeva.</span><span class="sxs-lookup"><span data-stu-id="a21c4-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="a21c4-113">Valige ajakirje tüüp ja projekt, mille jaoks ajakirjet sisestate.</span><span class="sxs-lookup"><span data-stu-id="a21c4-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="a21c4-114">Otsige väljast **Projektiülesanne** selle ajakirje jaoks sobiv ülesanne.</span><span class="sxs-lookup"><span data-stu-id="a21c4-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a21c4-115">Kui loote ajakirje ülesande jaoks, mis pole kasutajale määratud, valige väljast **Projektiülesanne** nupp **Otsi** , valige suvand **Muuda vaadet** ja valige seejärel kõigi ülesannete loendi nägemiseks suvand **Kõik aktiivsed projektiülesanded**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="a21c4-116">Kui on vaja sisestada kirjeldus, tehke seda, ja seejärel valige suvand **Salvesta ja Sule**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="a21c4-117">Pärast ajakirje loomist ja salvestamist saate seda redigeerida ajakirje ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="a21c4-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="a21c4-118">Ajakirje ruudustik toetab kahte vormingut.</span><span class="sxs-lookup"><span data-stu-id="a21c4-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="a21c4-119">Saate ajakirjed sisestada vormingus **hh:**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="a21c4-120">See vorming teisendatakse seejärel tundideks ja murdosadeks.</span><span class="sxs-lookup"><span data-stu-id="a21c4-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="a21c4-121">Saate otse sisestada tunnid ja murdosad.</span><span class="sxs-lookup"><span data-stu-id="a21c4-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="a21c4-122">Pange tähele, et tunni murdosad ei ole minutid.</span><span class="sxs-lookup"><span data-stu-id="a21c4-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="a21c4-123">Seega 1,5 tundi on 1 tund ja 30 minutit.</span><span class="sxs-lookup"><span data-stu-id="a21c4-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="a21c4-124">Sama reegel kehtib päeva murdosade kohta.</span><span class="sxs-lookup"><span data-stu-id="a21c4-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="a21c4-125">Üks päev on 24 tundi ja 0,5 päeva on 12 tundi.</span><span class="sxs-lookup"><span data-stu-id="a21c4-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="a21c4-126">Ajakirjete loomine hulgi kaupa</span><span class="sxs-lookup"><span data-stu-id="a21c4-126">Bulk create time entries</span></span>

<span data-ttu-id="a21c4-127">Pärast paari ajakirje loomist saate neid kopeerida, et luua hulgi kaupa veelgi ajakirjeid.</span><span class="sxs-lookup"><span data-stu-id="a21c4-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="a21c4-128">Valige lehel **Ajakirjed** suvand **Kopeeri nädal**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="a21c4-129">Ajakirjete kopeerimiseks määrake väljades **Perioodi algus** , **Alguskuupäev** ja **Lõppkuupäev** kuupäevavahemik.</span><span class="sxs-lookup"><span data-stu-id="a21c4-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="a21c4-130">Määrake väljades **Perioodi lõpp** ja **Alguskuupäev** kuupäev, mille jaoks soovite ajakirjeid luua.</span><span class="sxs-lookup"><span data-stu-id="a21c4-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="a21c4-131">Valige suvand **Kopeeri** , et luua nende ajakirjete koopia, mis vastavad väljal **Perioodi lõpp** määratud nädalapäevale.</span><span class="sxs-lookup"><span data-stu-id="a21c4-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="a21c4-132">Näiteks viimase nädala esmaspäeva ajakirje kopeeritakse selle nädala esmaspäeva, mis on määratud väljal **Perioodi lõpp**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="a21c4-133">Ajakirjete impordi andmed</span><span class="sxs-lookup"><span data-stu-id="a21c4-133">Import data for time entries</span></span>

<span data-ttu-id="a21c4-134">Saate importida projekti broneeringute ja ülesannete andmeid.</span><span class="sxs-lookup"><span data-stu-id="a21c4-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="a21c4-135">Andmete importimisel saate määrata imporditavate broneeringute kuupäevavahemiku ja seejärel eraldi valida broneeringud, mis tuleks luua ajakirjete **mustanditena**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="a21c4-136">Rühmitamise, sortimise, otsimise ja filtreerimise võimalused</span><span class="sxs-lookup"><span data-stu-id="a21c4-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="a21c4-137">Saate ajakirjeid rühmitada ja filtreerida veergudes määratud dimensioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="a21c4-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="a21c4-138">Valige väljast **Rühmitusalus** dimensioon, mida soovite ajakirjete filtreerimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="a21c4-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="a21c4-139">Saate ajakirjeid sortida ka tõusvas või kahanevas järjekorras, kasutades veerupäises olevat sortimisnoolt.</span><span class="sxs-lookup"><span data-stu-id="a21c4-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="a21c4-140">Peale selle saate ka kirjeid kuvada või peita, kui vajutate veerupäistes olevat nuppu **Filtreeri** ja sisestate seejärel väljale **Otsi** teksti, mida tuleks kasutada ajakirjete otsimiseks projekti nime, projekti ülesande, ajakirje või ressursi järgi.</span><span class="sxs-lookup"><span data-stu-id="a21c4-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
