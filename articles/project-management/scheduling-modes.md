---
title: Plaanimisrežiimid
description: Selles teemas antakse teavet arvete plaanimisrežiimide kohta.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981430"
---
# <a name="scheduling-modes"></a><span data-ttu-id="736af-103">Plaanimisrežiimid</span><span class="sxs-lookup"><span data-stu-id="736af-103">Scheduling modes</span></span>

<span data-ttu-id="736af-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="736af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="736af-105">Dynamics 365 Project Operations annab organisatsioonidele võimaluse määratleda, kuidas nad haldavad tööjaotuse struktuuris tööülesannete põhimuutujate muudatusi.</span><span class="sxs-lookup"><span data-stu-id="736af-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="736af-106">Lähtudes organisatsiooni konkreetsetest vajadustest, saavad projektijuhid projekti loomisel ajakava režiimis muudatusi teha.</span><span class="sxs-lookup"><span data-stu-id="736af-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="736af-107">Rakenduses Project Operations on saadaval kolm plaanimisrežiimi.</span><span class="sxs-lookup"><span data-stu-id="736af-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="736af-108">Fikseeritud kestus (see on vaikerežiim)</span><span class="sxs-lookup"><span data-stu-id="736af-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="736af-109">Fikseeritud töö</span><span class="sxs-lookup"><span data-stu-id="736af-109">Fixed work</span></span>
  - <span data-ttu-id="736af-110">Fikseeritud ühikud</span><span class="sxs-lookup"><span data-stu-id="736af-110">Fixed units</span></span>

<span data-ttu-id="736af-111">Kindla ajastamisrežiimi määratlusega seotud väärtused on määratletud järgmise valemiga.</span><span class="sxs-lookup"><span data-stu-id="736af-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="736af-112">Pingutus (*töö*) = kestus × ühikud</span><span class="sxs-lookup"><span data-stu-id="736af-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="736af-113">Projekti plaanimisrežiimi määratlemisel määrate ühe nendest väärtustest, mida ei saa seejärel muuta.</span><span class="sxs-lookup"><span data-stu-id="736af-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="736af-114">Selle väärtuse konstandina hoidmine seab sellele väärtusele prioriteedi, mis teavitab süsteemi seda mitte muutma, kui teised kaks väärtust muutuvad.</span><span class="sxs-lookup"><span data-stu-id="736af-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="736af-115">Järgnev tabel annab teavet konkreetse režiimi valimise mõjude kohta.</span><span class="sxs-lookup"><span data-stu-id="736af-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="736af-116">**Kinnita see ülesanne**</span><span class="sxs-lookup"><span data-stu-id="736af-116">**In this task**</span></span>             | <span data-ttu-id="736af-117">**Kui muudate ühikuid**</span><span class="sxs-lookup"><span data-stu-id="736af-117">**If you revise units**</span></span>   | <span data-ttu-id="736af-118">**Kui muudate kestust**</span><span class="sxs-lookup"><span data-stu-id="736af-118">**If you revise duration**</span></span> | <span data-ttu-id="736af-119">**Kui muudate pingutust**</span><span class="sxs-lookup"><span data-stu-id="736af-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="736af-120">Fikseeritud ühikutega ülesanne</span><span class="sxs-lookup"><span data-stu-id="736af-120">Fixed units task</span></span>     | <span data-ttu-id="736af-121">Kestus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-121">Duration is recalculated.</span></span> | <span data-ttu-id="736af-122">Jõupingutus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-122">Effort is recalculated.</span></span>    | <span data-ttu-id="736af-123">Kestus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="736af-124">Fikseeritud jõupingutusega ülesanne</span><span class="sxs-lookup"><span data-stu-id="736af-124">Fixed effort task</span></span>    | <span data-ttu-id="736af-125">Kestus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-125">Duration is recalculated.</span></span> | <span data-ttu-id="736af-126">Ühikud arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-126">Units are recalculated.</span></span>    | <span data-ttu-id="736af-127">Kestus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="736af-128">Fikseeritud kestusega ülesanne</span><span class="sxs-lookup"><span data-stu-id="736af-128">Fixed duration task</span></span>  | <span data-ttu-id="736af-129">Jõupingutus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-129">Effort is recalculated.</span></span>   | <span data-ttu-id="736af-130">Jõupingutus arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-130">Effort is recalculated.</span></span>    | <span data-ttu-id="736af-131">Ühikud arvutatakse ümber.</span><span class="sxs-lookup"><span data-stu-id="736af-131">Units are recalculated.</span></span>   |

<span data-ttu-id="736af-132">Lisateavet antud režiimi konfliktide kohta leiate teemast [Täpsema ajastamise jaoks ülesandetüübi muutmine](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="736af-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="736af-133">Teemas kasutatakse terminit **Töö** termini **Jõupingutus** asemel.</span><span class="sxs-lookup"><span data-stu-id="736af-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="736af-134">Ettevõtte plaanimisrežiimi muutmine</span><span class="sxs-lookup"><span data-stu-id="736af-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="736af-135">Ettevõtte plaanimisrežiimi määratlemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="736af-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="736af-136">Minge jaotisesse **Sätted** \> **Üldine** \> **Parameetrid** ja valige seejärel projekti parameeter.</span><span class="sxs-lookup"><span data-stu-id="736af-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="736af-137">Valige lehel **Projekti parameetrid** organisatsiooni jaoks ajastamise vaikerežiim ja seejärel määratlege võimalus, et projektijuht saab uue projekti loomisel selle sätte alistada.</span><span class="sxs-lookup"><span data-stu-id="736af-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="736af-138">Projekti plaanimisrežiimi sätte muutmine</span><span class="sxs-lookup"><span data-stu-id="736af-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="736af-139">Kui organisatsioon lubab projektijuhil ajastamise vaikerežiimi alistada, saab projektijuht selle muudatuse teha uue projekti loomisel.</span><span class="sxs-lookup"><span data-stu-id="736af-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="736af-140">Pärast projekti salvestamist ei saa plaanimisrežiimi muuta.</span><span class="sxs-lookup"><span data-stu-id="736af-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="736af-141">Kopeeritud projektid</span><span class="sxs-lookup"><span data-stu-id="736af-141">Copied projects</span></span>

<span data-ttu-id="736af-142">Kuna projekt luuakse projekti kopeerimistoimingu ajal, ei saa projektijuht plaanimisrežiimi seada.</span><span class="sxs-lookup"><span data-stu-id="736af-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="736af-143">Sihtprojekt on alati vaikimisi organisatsioonitasandil määratletud režiimil.</span><span class="sxs-lookup"><span data-stu-id="736af-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="736af-144">Kopeeritud tööülesanded</span><span class="sxs-lookup"><span data-stu-id="736af-144">Copied tasks</span></span>

<span data-ttu-id="736af-145">Kui tööülesanne kopeeritakse ühest projektist teise, pärib ülesanne sihtprojekti ajastamisrežiimi.</span><span class="sxs-lookup"><span data-stu-id="736af-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
