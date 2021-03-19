---
title: Uue projekti loomine
description: Selles teemas antakse teavet uue projekti loomise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270718"
---
# <a name="create-a-new-project"></a><span data-ttu-id="925db-103">Uue projekti loomine</span><span class="sxs-lookup"><span data-stu-id="925db-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="925db-104">Uue projekti loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="925db-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="925db-105">Lehel **Projektihaldus** valige **Uus projekt** ja sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="925db-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="925db-106">**Projekti tüüp:** aeg ja materjal</span><span class="sxs-lookup"><span data-stu-id="925db-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="925db-107">**Projekti nimi:** XYZ värskenduse 2. etapp</span><span class="sxs-lookup"><span data-stu-id="925db-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="925db-108">**Projekti rühm:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="925db-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="925db-109">**Projekti lepingu ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="925db-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="925db-110">Valige käsk **Loo projekt**.</span><span class="sxs-lookup"><span data-stu-id="925db-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="925db-111">Ressursi määramine projektile</span><span class="sxs-lookup"><span data-stu-id="925db-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="925db-112">Lehel **Töötajad** loendis **Töötajad** valige töötaja, kelle jaoks oskuseid seadistasite, ja avage töötaja kirje.</span><span class="sxs-lookup"><span data-stu-id="925db-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="925db-113">Valige toimingupaanil vahekaardil **Projekt** rühmas **Seadistamine** suvand **Määra projekt**.</span><span class="sxs-lookup"><span data-stu-id="925db-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="925db-114">Vahekaardi **Ressursi valideerimise projekti ülesanded** vahekaardi **Projektid** väljal **Lisa projekt valitud projektide hulka** filtreerige projektil **XYZ värskenduse 2. etapp**.</span><span class="sxs-lookup"><span data-stu-id="925db-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="925db-115">Paanil **Ülejäänud projektid** valige projekt ja valige seejärel noolenupp, et lisada see paanile **Valitud projektid** .</span><span class="sxs-lookup"><span data-stu-id="925db-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="925db-116">Saate ressursile määrata kategooriaid ka vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="925db-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="925db-117">Kategooria tüüp on kas **Kulu** või **Tulu**.</span><span class="sxs-lookup"><span data-stu-id="925db-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="925db-118">Kategooria tüübi määrab teie organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="925db-118">The category type is determined by your organization.</span></span> <span data-ttu-id="925db-119">Kui ühtegi kategooriat pole ressursi jaoks määratud, otsib rakendus Finance vaikimisi kategooriat tunnihinna ja tulu kohta.</span><span class="sxs-lookup"><span data-stu-id="925db-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="925db-120">Projekti ressursi ja rolli omaduste seadistamine</span><span class="sxs-lookup"><span data-stu-id="925db-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="925db-121">Projektijuht saab projekti jaoks vajalike rollide loomiseks kasutada projekti ressursside funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="925db-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="925db-122">Rolle saab kasutada juhul, kui kinnitatud ressursid on ressursside reserveerimisel endiselt tundmatud.</span><span class="sxs-lookup"><span data-stu-id="925db-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="925db-123">Rolle saab ajutiselt reserveerida plaanitud ressurssidena, et saaksite projekti kavandamise etappidega jätkata.</span><span class="sxs-lookup"><span data-stu-id="925db-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="925db-124">[![Rolli näide](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="925db-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="925db-125">**Stsenaarium:** Contoso palgati lõpetama aja- ja materjalikulu projekti, millel on kinnitatud projekti põhikiri.</span><span class="sxs-lookup"><span data-stu-id="925db-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="925db-126">Noorem-projektijuht endiselt lõpetab projekti ulatust.</span><span class="sxs-lookup"><span data-stu-id="925db-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="925db-127">Ressursihaldur määratleb praegu konkreetsed ressursid, mis reserveeritakse uue projektiga töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="925db-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="925db-128">Projekti kriitilise iseloomu tõttu taotles projekti sponsor ühe rollina vanem-projektijuhti.</span><span class="sxs-lookup"><span data-stu-id="925db-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="925db-129">Ressursihaldur peab hankima uue ressursi ja määrama süsteemis rolli juhul, kui noorem-projektijuht vajab projekti kavandamise ajal ressursi teavet.</span><span class="sxs-lookup"><span data-stu-id="925db-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="925db-130">Järgmised juhised näitavad, kuidas ressursihaldur saab seadistada vanem-projektijuhi rolli ja seostada ressursi omadused sellega.</span><span class="sxs-lookup"><span data-stu-id="925db-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="925db-131">Hiljem saab rolli kasutada saadaolevate ressursside otsimiseks, mis vastavad ressursi nõutavatele pädevustele.</span><span class="sxs-lookup"><span data-stu-id="925db-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="925db-132">Lehel **Seadistamise rollid** valige **Uus projekt** ja sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="925db-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="925db-133">**Rolli ID:** vanem-projektijuht</span><span class="sxs-lookup"><span data-stu-id="925db-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="925db-134">**Kirjeldus:** vanem-projektijuht</span><span class="sxs-lookup"><span data-stu-id="925db-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="925db-135">Valige käsk **Loo**.</span><span class="sxs-lookup"><span data-stu-id="925db-135">Select **Create**.</span></span>
3. <span data-ttu-id="925db-136">Valige roll **Vanem-projektijuht** ja valige seejärel **Konfigureeri tunnused**.</span><span class="sxs-lookup"><span data-stu-id="925db-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="925db-137">Väljal **Tunnuste tüüp** valige **Oskus**.</span><span class="sxs-lookup"><span data-stu-id="925db-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="925db-138">Väljale **Saadaolevad tunnused** sisestage otsitav oskus.</span><span class="sxs-lookup"><span data-stu-id="925db-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="925db-139">Väljal **Tunnuse tüüp** valige **Sertifikaat**.</span><span class="sxs-lookup"><span data-stu-id="925db-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="925db-140">Väljale **Saadaolevad tunnused** sisestage otsitav sertifikaadi tüüp.</span><span class="sxs-lookup"><span data-stu-id="925db-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="925db-141">Projekti ressursi määramine projektile</span><span class="sxs-lookup"><span data-stu-id="925db-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="925db-142">Lehel **Kõik projektid** valige projekt **XYZ värskenduse 2. etapp**.</span><span class="sxs-lookup"><span data-stu-id="925db-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="925db-143">Vahekaardil **Projektimeeskond ja kavandamine** valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="925db-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="925db-144">Väljale **Roll** sisestage **Meeskonnaliige**.</span><span class="sxs-lookup"><span data-stu-id="925db-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="925db-145">Valige suvand **Broneeri kalendrist**.</span><span class="sxs-lookup"><span data-stu-id="925db-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="925db-146">Lehel **Ressursi saadavus** valige **Kuva sätted**.</span><span class="sxs-lookup"><span data-stu-id="925db-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="925db-147">Lehel **Redigeeri kuvamissätted** sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="925db-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="925db-148">**Kuupäeva vahemiku vaate vorming:** päev</span><span class="sxs-lookup"><span data-stu-id="925db-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="925db-149">**Kuva saadaolevad kirjeldused:** jah</span><span class="sxs-lookup"><span data-stu-id="925db-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="925db-150">**Kuva allesjäänud võimsus:** jah</span><span class="sxs-lookup"><span data-stu-id="925db-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="925db-151">Valige ressursside loendist ressurss.</span><span class="sxs-lookup"><span data-stu-id="925db-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="925db-152">Valige **Fikseeritud reserveering** ja **Täisvõimsus**.</span><span class="sxs-lookup"><span data-stu-id="925db-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="925db-153">Ressursi määramine vaikerollile</span><span class="sxs-lookup"><span data-stu-id="925db-153">Assign a resource to a default role</span></span>

<span data-ttu-id="925db-154">Projekti või ressursi haldamisega abistamiseks võivad juhid veelgi rohkem minna süvitsi ressursside puhul, mida saab projekti jaoks broneerida.</span><span class="sxs-lookup"><span data-stu-id="925db-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="925db-155">Saate seostada vaike-rolli olemasoleva ressursiga või värskelt omandatud ressursiga.</span><span class="sxs-lookup"><span data-stu-id="925db-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="925db-156">Näiteks, kui Daniel palgati, olid tal kogemus ja oskused täita ärianalüütiku rolli.</span><span class="sxs-lookup"><span data-stu-id="925db-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="925db-157">Ressursihaldur määras selle rolli Danielile vaike-rolliks.</span><span class="sxs-lookup"><span data-stu-id="925db-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="925db-158">Seega lisaks ressursihaldur Daneli ärianalüütikute kogumile, kes olid saadaval projektidega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="925db-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="925db-159">Ressursi reserveerimise ajal saavad projektijuhid filtreerida projektidega töötamiseks saadaolevate rollidega ressursse.</span><span class="sxs-lookup"><span data-stu-id="925db-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="925db-160">Nad saavad kasutada seda teavet ühe kriteeriumina, kui nad teostavad ressursi täitmisel mitme tunnusega otsuste analüüsimist.</span><span class="sxs-lookup"><span data-stu-id="925db-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="925db-161">Nad saavad lisada filtrile ka teisi ressursi omadusi, et otsida teatud projekti jaoks konkreetsete oskuste, hariduse ja kogemusega ressursse.</span><span class="sxs-lookup"><span data-stu-id="925db-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="925db-162">**Stsenaarium:** kinnitatud projekt on käivitatud ja vanem-projektijuhi roll oli reserveeritud planeeritud ressursina projekti kavandamise etapis.</span><span class="sxs-lookup"><span data-stu-id="925db-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="925db-163">Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="925db-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="925db-164">Lehel **Ressursside loend** valige **Daniel Kangur**.</span><span class="sxs-lookup"><span data-stu-id="925db-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="925db-165">Lehel **Ressursi roll** valige **Uus projekt** ja sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="925db-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="925db-166">**Jõustub:** sisestage praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="925db-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="925db-167">**Aegub:** sisestage **Mitte kunagi**.</span><span class="sxs-lookup"><span data-stu-id="925db-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="925db-168">**Roll:** sisestage **Vanem-projektijuht**.</span><span class="sxs-lookup"><span data-stu-id="925db-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="925db-169">Valige käsk **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="925db-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="925db-170">Vahekaardil **Pädevused** lisage oskus **Projektihaldus** ja sertifikaat **PMP**.</span><span class="sxs-lookup"><span data-stu-id="925db-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]