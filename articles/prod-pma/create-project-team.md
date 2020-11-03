---
title: Projektimeeskonna loomine
description: Selles teemas antakse teavet projektimeeskonna loomise ja haldamise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075121"
---
# <a name="create-a-project-team"></a><span data-ttu-id="59023-103">Projektimeeskonna loomine</span><span class="sxs-lookup"><span data-stu-id="59023-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59023-104">Varem projektis seadistatud rollide kasutamiseks peab projektijuht seostama rollid projektiga.</span><span class="sxs-lookup"><span data-stu-id="59023-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="59023-105">Projektile võib määrata mitu rolli.</span><span class="sxs-lookup"><span data-stu-id="59023-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="59023-106">Segaduse vältimiseks sildistatakse need rollid reserveerimise ajal automaatselt.</span><span class="sxs-lookup"><span data-stu-id="59023-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="59023-107">Näiteks kui projektijuht nõuab kolme tarkvarainseneri, luuakse automaatselt kolm rolli Tarkvarainsener, millel on sildid **tarkvarainsener 1** , **tarkvarainsener 2** ja **tarkvarainsener 3** , kuna nende sildid luuakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="59023-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1** , **software engineer 2** , and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="59023-108">Kui rolli omadused olid varem rollile määratud, rakendatakse need ressursi otsingu ajal justkui filter.</span><span class="sxs-lookup"><span data-stu-id="59023-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="59023-109">Otsingu veelgi täpsemaks muutmiseks saab lisada vastavalt vajadusele täiendavaid tunnuseid.</span><span class="sxs-lookup"><span data-stu-id="59023-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="59023-110">Kuvamissätteid saab samuti kohandada, et anda ressursi saadavusest parem vaade.</span><span class="sxs-lookup"><span data-stu-id="59023-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="59023-111">Saadavust võib kuvada tundide, päevade, nädalate, kuude, kvartalite ja aastate lõikes.</span><span class="sxs-lookup"><span data-stu-id="59023-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="59023-112">Lisaks on olemas võimalus kuvada ressursside saadaolev ja allesjäänud võimsus.</span><span class="sxs-lookup"><span data-stu-id="59023-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="59023-113">See suvand on kasulik ajahalduse jaoks, kui prognoosite saadaolevat aega tegevuste või ressursi kättesaadavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="59023-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="59023-114">Projektijuht saab valida lehel rolli ja seejärel vaba ressursi olemasolul, mis nõudega ühtib, valida ressursi reserveerimine rolli täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="59023-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="59023-115">Pange tähele, et ressursse ei pea kavandamise etapis sellel hetkel reserveerima.</span><span class="sxs-lookup"><span data-stu-id="59023-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="59023-116">WBS-i loomisel saate rolle asendada projekti töötajate ressurssidega.</span><span class="sxs-lookup"><span data-stu-id="59023-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="59023-117">Kui rollid asendatakse WBS-is töötajatest ressurssidega, siis ressursi seadistus värskendab automaatselt projektimeeskonda loendit ja ajakava.</span><span class="sxs-lookup"><span data-stu-id="59023-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="59023-118">[![Projektimeeskonna loend, mis sisaldab nii rolle kui ka tegelikke ressursse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="59023-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="59023-119">Projektijuhil on mitmeid võimalusi projekti jaoks ressursi broneerimiseks, nagu **Järelejäänud võimsus** , **Täisvõimsus** , **Võimsuse protsent** ja **Konkreetsed tunnid**.</span><span class="sxs-lookup"><span data-stu-id="59023-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity** , **Full capacity** , **Capacity percentage** , and **Specify hours**.</span></span> <span data-ttu-id="59023-120">Kui ressursi määramised muutuvad, saab neid broneeringu võimalusi igal ajal tühistada.</span><span class="sxs-lookup"><span data-stu-id="59023-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="59023-121">Toetatud on kahte tüüpi broneeringud.</span><span class="sxs-lookup"><span data-stu-id="59023-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="59023-122">**Fikseeritud broneering** – ressursi broneerimine kiideti heaks ja kinnitati, et teatud aja jooksul töötab seal.</span><span class="sxs-lookup"><span data-stu-id="59023-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="59023-123">**Esialge broneerimine** – ressursi broneerimised määrati esialgu töötama konkreetse aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="59023-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="59023-124">Järgmises toimingus kirjeldatakse, kuidas luua projektimeeskonda.</span><span class="sxs-lookup"><span data-stu-id="59023-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="59023-125">Projektimeeskonna loomine</span><span class="sxs-lookup"><span data-stu-id="59023-125">Create a project team</span></span>

1. <span data-ttu-id="59023-126">Loendi lehel **Kõik projektid** valige projekt ja valige seejärel **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="59023-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="59023-127">Vahekaardil **Projektimeeskond ja ajastamine** väljal **Ajakava lõpukuupäev** sisestage ajakava algusaeg pluss üks kuu.</span><span class="sxs-lookup"><span data-stu-id="59023-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="59023-128">Näiteks kui ajakava alguskuupäev on 24. juuni 2017 (24.6.2017), sisestage **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="59023-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="59023-129">Valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="59023-129">Select **Add**.</span></span>
4. <span data-ttu-id="59023-130">Paanil **Projektile rollide lisamine** väljal **Roll** valige **Vanem-projektihaldur**.</span><span class="sxs-lookup"><span data-stu-id="59023-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="59023-131">Valige **Nõutav pädevus**.</span><span class="sxs-lookup"><span data-stu-id="59023-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="59023-132">Lehel **Omaduste valimine** valitakse vaikimisi eelnevalt vanem-projektijuhi rollile määratud omadused.</span><span class="sxs-lookup"><span data-stu-id="59023-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="59023-133">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="59023-133">Select **OK**.</span></span>
7. <span data-ttu-id="59023-134">Lehel **Projektile rollide lisamine** väljale **Ressursside arv** sisestage **1**.</span><span class="sxs-lookup"><span data-stu-id="59023-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="59023-135">Väljal **Ressurss** näitab otsing kõiki ressursse, millel on nõutavad omadused olemas.</span><span class="sxs-lookup"><span data-stu-id="59023-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="59023-136">Valige suvad **Daniel Kangur** ja seejärel valige käsk **Loo**.</span><span class="sxs-lookup"><span data-stu-id="59023-136">Select **Daniel Goldschmidt** , and then select **Create**.</span></span>
9. <span data-ttu-id="59023-137">Lehel **Projekt** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="59023-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="59023-138">Paanil **Projektile rollide lisamine** väljal **Roll** valige **Meeskonnaliige**.</span><span class="sxs-lookup"><span data-stu-id="59023-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="59023-139">Väljale **Ressursside arv** sisestage **5**.</span><span class="sxs-lookup"><span data-stu-id="59023-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="59023-140">Valige käsk **Loo**.</span><span class="sxs-lookup"><span data-stu-id="59023-140">Select **Create**.</span></span>
12. <span data-ttu-id="59023-141">Lehel **Projektid** valige **Täida ressurss**.</span><span class="sxs-lookup"><span data-stu-id="59023-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="59023-142">Projektimeeskondade jälgimine</span><span class="sxs-lookup"><span data-stu-id="59023-142">Monitor project teams</span></span>
1. <span data-ttu-id="59023-143">Lehel **Kõik projektid** valige link **Projekti ID** projekti **XYZ värskenduse 2. etapp** jaoks.</span><span class="sxs-lookup"><span data-stu-id="59023-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="59023-144">Kiirkaardil **Projektimeeskond ja ajastamine** veenduge, et loetletud projektiressursid oleksid õiged.</span><span class="sxs-lookup"><span data-stu-id="59023-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
