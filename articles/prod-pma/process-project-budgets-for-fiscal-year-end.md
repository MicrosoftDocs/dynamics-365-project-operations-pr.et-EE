---
title: Projekti eelarvete ülekandmine finantsaasta lõpus
description: Selles artiklis kirjeldatakse kuidas viia allesolevaid eelarve summasid tulevastesse aastatesse ja luua eelarve registri üksikasju.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075089"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="28790-103">Projekti eelarvete ülekandmine finantsaasta lõpus</span><span class="sxs-lookup"><span data-stu-id="28790-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28790-104">Mitmeaastase projektiga töötamisel võib finantsaasta lõpus olla allesolev eelarve.</span><span class="sxs-lookup"><span data-stu-id="28790-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="28790-105">Saate allesolevad eelarve summad tulevasse aastasse üle viia ja luua eelarve registri üksikasjad pearaamatu seotud kontode summade jaoks.</span><span class="sxs-lookup"><span data-stu-id="28790-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="28790-106">Enne allesolevate summade ülekandmist vaadake üle ja analüüsige allesolevaid eelarve summasid.</span><span class="sxs-lookup"><span data-stu-id="28790-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="28790-107">Allesolevate eelarve summade ülevaatamine ja analüüs</span><span class="sxs-lookup"><span data-stu-id="28790-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="28790-108">Projektide aasta lõpu eelarve summade üle vaatamiseks toimige järgmiselt, kuid ärge kandke summasid üle.</span><span class="sxs-lookup"><span data-stu-id="28790-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="28790-109">Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Eelarved** > **Ülekantavad eelarved**.</span><span class="sxs-lookup"><span data-stu-id="28790-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="28790-110">Kontrollige lehe **Projekti eelarve ülekandmise protsess** vahekaardil **Aasta lõpu võimalused** , et suvand **Kanna allesjäänud projekti eelarve summad edasi** pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="28790-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="28790-111">Valige vahekaardi **Parameetrid** väljal **Projekti eelarve aasta** finantsaasta, mille allesolevat eelarve summat soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="28790-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="28790-112">Valige väljal **Finantsaasta avamine** finantsaasta, mille allesolevat eelarve summat soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="28790-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="28790-113">Valige väljal **Prognoosimudelist** väärtus **Allesolev eelarve**.</span><span class="sxs-lookup"><span data-stu-id="28790-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="28790-114">Kui soovite kaasata projekte, mis vastavad teie valitud kriteeriumidele ja millel pole allesolevat eelarvet, valige suvand **Kuva ilma allesolevata**.</span><span class="sxs-lookup"><span data-stu-id="28790-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="28790-115">Valige vahekaardil **Vali eelarved** käsku **Too kõik eelarved** , et laadida kõik eelarved, mis vastavad teie valitud kriteeriumidele, ja seejärel valige **Töötle**.</span><span class="sxs-lookup"><span data-stu-id="28790-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="28790-116">Sellise andmebaasi päringu loomiseks, mis laadib teatud eelarvete kogumi paanile, valige käsk **Too valitud eelarved**.</span><span class="sxs-lookup"><span data-stu-id="28790-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="28790-117">Paani kindla rea kohta lisateabe saamiseks valige rida ja seejärel valige suvand **Kuva eelarve üksikasjad** või **Kuva kontod**.</span><span class="sxs-lookup"><span data-stu-id="28790-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="28790-118">Allesolevate eelarve summade ülekandmine</span><span class="sxs-lookup"><span data-stu-id="28790-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="28790-119">Allesolevate eelarve summade töötlemisel saate luua pearaamatusse ülekantavatele summadele kanded.</span><span class="sxs-lookup"><span data-stu-id="28790-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="28790-120">Pearaamatu kannete loomiseks täitke juhised jaotises [Eelarve summade ülekandmine ja pearaamatu kannete loomine](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="28790-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="28790-121">Ülekantud eelarvelised summad kantakse edasi prognoosimudelisse, mis on lehel **Prognoosimudelid** ülekandmise prognoosi mudeliks valitud.</span><span class="sxs-lookup"><span data-stu-id="28790-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="28790-122">Eelarve summade ülekandmine ja pearaamatu kannete loomine</span><span class="sxs-lookup"><span data-stu-id="28790-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="28790-123">Valige **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Eelarved** > **Ülekantavad eelarved**.</span><span class="sxs-lookup"><span data-stu-id="28790-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="28790-124">Valige lehel **Projekti eelarve ülekandmise protsess** väärtus **Aastalõpp** ja lubage seejärel suvandid **Kanna üle allesolevad projekti eelarve summad** ja **Loo pearaamatusse eelarve registri kanded**.</span><span class="sxs-lookup"><span data-stu-id="28790-124">On the **Project budget carry-forward process** page, select **Year-end** , and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="28790-125">Valige vahekaardil **Parameetrid** väljade rühmas **Projekti parameetrid** järgnev.</span><span class="sxs-lookup"><span data-stu-id="28790-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="28790-126">**Projekti eelarve aasta** : valige selle finantsaasta algus, mille allesolevaid eelarve summasid soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="28790-126">**Project budget year** : Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="28790-127">**Kasum ja kahjum** : pearaamatusse kasumi- ja kahjumi kannete loomine.</span><span class="sxs-lookup"><span data-stu-id="28790-127">**Profit and loss** : Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="28790-128">**WIP** : pearaamatusse käimasoleva töö (WIP) kannete loomine.</span><span class="sxs-lookup"><span data-stu-id="28790-128">**WIP** : Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="28790-129">**Palgaarvestuse** : pearaamatusse palgaarvestuse jaotuse kannete loomine.</span><span class="sxs-lookup"><span data-stu-id="28790-129">**Payroll** : Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="28790-130">Esitage väljade rühma **Pearaamat** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="28790-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="28790-131">Valige väljal **Finantsaasta avamine** finantsaasta, millele soovite projektide allesolevad eelarve summad kanda.</span><span class="sxs-lookup"><span data-stu-id="28790-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="28790-132">Vaikeväärtus on üks aasta pärast välja **Projekti eelarve aasta**.</span><span class="sxs-lookup"><span data-stu-id="28790-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="28790-133">Valige väljal **Ülekandmise periood** periood, millele soovite pearaamatus eelarve registri üksikasjad luua.</span><span class="sxs-lookup"><span data-stu-id="28790-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="28790-134">See on tavaliselt finantsaasta esimene periood.</span><span class="sxs-lookup"><span data-stu-id="28790-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="28790-135">Esitage väljade rühma **Kopeeri kust/kuhu** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="28790-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="28790-136">Valige väljal **Prognoosimudelist** projekti prognoosimudel, mis on seotud allesolevate eelarve summadega, mida soovite projektidele üle kanda.</span><span class="sxs-lookup"><span data-stu-id="28790-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="28790-137">Valige väljal **Pearaamatu eelarve mudelisse** pearaamatu eelarvemudel, mis on seotud eelarve summadega, mida soovite pearaamatusse üle kanda.</span><span class="sxs-lookup"><span data-stu-id="28790-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="28790-138">Valige **Kanna üle müügi valuuta** , et kasutada projekti müügi valuutat pearaamatu kannete jaoks, mis on loodud eelarve summade edastamisel projektidele.</span><span class="sxs-lookup"><span data-stu-id="28790-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="28790-139">Kui suvand pole valitud, kasutavad kanded arvestusvaluutat.</span><span class="sxs-lookup"><span data-stu-id="28790-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="28790-140">Valige **Kuva ilma allesolevata** , et kaasata projektid, milles ei ole allesolevaid eelarve summasid, aga mis vastavad teistele kriteeriumidele, mille olete valinud alumisel paanil kuvatud projektides.</span><span class="sxs-lookup"><span data-stu-id="28790-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="28790-141">Valige vahekaardil **Vali eelarved** käsk **Too kõik eelarved** , et laadid kõik eelarved, mis vastavad teie valitud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="28790-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="28790-142">Kui eelistate luua sellise andmebaasi päringu, mis laadib teatud projekti eelarvete kogumi paanile, valige käsk **Too valitud eelarved**.</span><span class="sxs-lookup"><span data-stu-id="28790-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="28790-143">Valige iga projekti jaoks, mida soovite töödelda, projekti rea alguses soovitud suvand.</span><span class="sxs-lookup"><span data-stu-id="28790-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="28790-144">Kõigi või enamiku projektide valimiseks märkige ülemises vasakus nurgas olev märkeruut.</span><span class="sxs-lookup"><span data-stu-id="28790-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="28790-145">Mistahes projekti töötlemise välistamiseks tühjendage selle projekti ruut.</span><span class="sxs-lookup"><span data-stu-id="28790-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="28790-146">Valitud projektide allesolevate eelarve summade ülekandmiseks valitud finantsaastasse ja pearaamatusse eelarve registri üksikasjade loomiseks valige **Töötle**.</span><span class="sxs-lookup"><span data-stu-id="28790-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="28790-147">Eelarve summade ülekandmine pearaamatu kandeid loomata</span><span class="sxs-lookup"><span data-stu-id="28790-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="28790-148">Minge jaotisse **Projektijuhtimine ja raamatupidamine** > **Perioodiline** > **Eelarved** > **Ülekantavad eelarved**.</span><span class="sxs-lookup"><span data-stu-id="28790-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="28790-149">Valige lehe **Projekti eelarve ülekandmise protsess** väljal **Aasta lõpu võimalused** , et suvand **Kanna allesjäänud projekti eelarve summad edasi**.</span><span class="sxs-lookup"><span data-stu-id="28790-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="28790-150">Valige rühma **Parameetrid** väljal **Projekti eelarve aasta** finantsaasta, mille allesolevaid eelarve summasid soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="28790-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="28790-151">Esitage rühma **Kopeeri kust/kuhu** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="28790-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="28790-152">Valige väljal **Prognoosimudelist** projekti prognoosimudel, mis on seotud allesolevate eelarve summadega, mida soovite projektidele üle kanda.</span><span class="sxs-lookup"><span data-stu-id="28790-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="28790-153">Valige **Kuva ilma allesolevata** , et kaasata projektid, millel ei ole allesolevaid eelarve summasid, aga mis vastavad teistele valitud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="28790-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="28790-154">Valige rühmas **Vali eelarved** käsk **Too kõik eelarved** , et laadid kõik eelarved, mis vastavad teie valitud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="28790-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="28790-155">Sellise andmebaasi päringu loomiseks, mis laadib teatud projekti eelarvete kogumi paanile, valige käsk **Too valitud eelarved**.</span><span class="sxs-lookup"><span data-stu-id="28790-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="28790-156">Valige iga projekti jaoks, mida soovite töödelda, projekti rea alguses soovitud suvand.</span><span class="sxs-lookup"><span data-stu-id="28790-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="28790-157">Valige **Töötle** , et kanda valitud projektide allesolevad eelarve summad üle valitud finantsaastasse.</span><span class="sxs-lookup"><span data-stu-id="28790-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

