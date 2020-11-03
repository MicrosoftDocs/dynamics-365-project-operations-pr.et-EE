---
title: Föderaalse rahastamise kulude ajakava päring
description: Selles teemas antakse teavet föderaalse rahastamise päringu kulude ajakava kohta.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074940"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0bd60-103">Föderaalse rahastamise kulude ajakava päring</span><span class="sxs-lookup"><span data-stu-id="0bd60-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bd60-104">Vastavalt Office of Management and Budgeti ringkirjale A-133, kohaldatakse föderaalseid rahalisi vahendeid saanud agentuuridele auditeerimise nõudeid, mida nimetatakse ka ühekordseteks audititeks.</span><span class="sxs-lookup"><span data-stu-id="0bd60-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="0bd60-105">Auditeerimise protsessi abil antakse regulaarselt ülevaade föderaalsete toetuste tuludest ja kuludest.</span><span class="sxs-lookup"><span data-stu-id="0bd60-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="0bd60-106">Ühekordse auditi aruande osa sisaldab föderaalse rahastamise kulude ajakava (SEFA).</span><span class="sxs-lookup"><span data-stu-id="0bd60-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="0bd60-107">Föderaalse rahastamise kulude ajakava päring sisaldab Föderaalse riigiabi kataloogi (CFDA) pealkirja ja numbrit, toetuse numbrit, toetuse aastat, vahendeid pakkuva föderaalagentuuri nime ja vaheüksuse nime.</span><span class="sxs-lookup"><span data-stu-id="0bd60-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="0bd60-108">Päring on määratud perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="0bd60-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="0bd60-109">Tavaliselt on see periood sama, kui finantsaruande periood, milleks on finantsaasta.</span><span class="sxs-lookup"><span data-stu-id="0bd60-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="0bd60-110">Päring hõlmab toetusi, mille kavandatavad kuupäevad on valitud kuupäevavahemikus.</span><span class="sxs-lookup"><span data-stu-id="0bd60-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="0bd60-111">Päringu veerg **Väljastav agentuur** näitab toetuse klienti või vahendatava toetuse korral väljastavat agentuuri.</span><span class="sxs-lookup"><span data-stu-id="0bd60-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="0bd60-112">Vahendatava toetuse puhul kuvatakse veerus **Vahendav agentuur** toetuse klienti.</span><span class="sxs-lookup"><span data-stu-id="0bd60-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="0bd60-113">Kui toetus ei ole vahendatav toetus, on veerg **Vahendav agentuur** tühi.</span><span class="sxs-lookup"><span data-stu-id="0bd60-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="0bd60-114">CFDA klastrite seadistus</span><span class="sxs-lookup"><span data-stu-id="0bd60-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="0bd60-115">Peate föderaalse rahastamise kulude ajakava päringus seadistama CFDA klastrid, mida saab seostada CFDA numbritega.</span><span class="sxs-lookup"><span data-stu-id="0bd60-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="0bd60-116">Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Seadistamine \> Toetused \> Föderaalse riigiabi kataloogi klastrid**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="0bd60-117">CFDA klastri loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="0bd60-118">Sisestage klastri nimi.</span><span class="sxs-lookup"><span data-stu-id="0bd60-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="0bd60-119">Muudatuste salvestamiseks valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="0bd60-120">CFDA numbrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="0bd60-120">Set up CFDA numbers</span></span>

<span data-ttu-id="0bd60-121">Peate föderaalse rahastamise kulude ajakava päringus seadistama CFDA numbrid, mida saab toetustele lisada.</span><span class="sxs-lookup"><span data-stu-id="0bd60-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="0bd60-122">Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Seadistamine \> Toetused \> Föderaalse riigiabi kataloogi numbrid**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="0bd60-123">CFDA numbri loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="0bd60-124">Sisestage CFDA number veergu **Number**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="0bd60-125">Vajutage tabeldusklahvi **Tab**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="0bd60-126">Sisestage CFDA pealkiri veergu **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="0bd60-127">Vajutage tabeldusklahvi **Tab**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="0bd60-128">Valikuline: sisestage sobiv CFDA klaster väljale **Programmi klaster**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="0bd60-129">Muudatuste salvestamiseks valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0bd60-130">Föderaalse rahastamise kulude ajakava päringule aruandluseks toetuste seadistamine</span><span class="sxs-lookup"><span data-stu-id="0bd60-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="0bd60-131">Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Toetused \> Toetused** ning valige olemasolev toetus.</span><span class="sxs-lookup"><span data-stu-id="0bd60-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="0bd60-132">Määrake kiirvahekaardil **Seadistamine** väljal **Föderaalse riigiabi kataloog** CFDA-le number.</span><span class="sxs-lookup"><span data-stu-id="0bd60-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="0bd60-133">Toetuse CFDA number määratleb aruandluse jaoks CFDA klastri.</span><span class="sxs-lookup"><span data-stu-id="0bd60-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="0bd60-134">Sisestage kiirvahekaardile **Kontaktteave** väljastaja andmed, toimides järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0bd60-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="0bd60-135">Sisestage väljale **Toetuse klient** toetuse eest vastutav klient.</span><span class="sxs-lookup"><span data-stu-id="0bd60-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="0bd60-136">Olemasoleva toetuse puhul võib see teave olla juba sisestatud.</span><span class="sxs-lookup"><span data-stu-id="0bd60-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="0bd60-137">Määrake, kas toetuse klient on rahastaja.</span><span class="sxs-lookup"><span data-stu-id="0bd60-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="0bd60-138">Kui toetuse klient on rahastaja, jätke märkeruut **Vahendaja** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="0bd60-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="0bd60-139">Kui mõni teine klient on rahastaja ja toetuse klient vastutab raha kulutamise ja jälgimise eest, valige märkeruut **Vahendaja**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="0bd60-140">Kui valisite eelmises etapis märkeruudu **Vahendaja** sisestage väljale **Väljastav agentuur** toetuse andnud klient.</span><span class="sxs-lookup"><span data-stu-id="0bd60-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="0bd60-141">Väljastav agentuur ja toetuse klient ei saa olla sama klient.</span><span class="sxs-lookup"><span data-stu-id="0bd60-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="0bd60-142">Siin on näide vahendatava toetuse kohta.</span><span class="sxs-lookup"><span data-stu-id="0bd60-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="0bd60-143">Föderaalvalitsus rahastas riigi jaoks infrastruktuuri projekti.</span><span class="sxs-lookup"><span data-stu-id="0bd60-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="0bd60-144">Föderaalvalitsus andis raha riigile kulutamiseks.</span><span class="sxs-lookup"><span data-stu-id="0bd60-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="0bd60-145">Sellel juhul on föderaalvalitsus väljastavaks agentuuriks ja riik on toetuse klient.</span><span class="sxs-lookup"><span data-stu-id="0bd60-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="0bd60-146">Funktsiooni esmakordsel sisselülitamisel sisestatakse esialgsed CFDA numbrid, kasutades toetustel olemasolevaid numbreid.</span><span class="sxs-lookup"><span data-stu-id="0bd60-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="0bd60-147">SEFA aruandlusest toetuste välja jätmine vastavalt toetuse tüübile</span><span class="sxs-lookup"><span data-stu-id="0bd60-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="0bd60-148">Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Seadistamine \> Toetused \> Toetuste tüübid**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="0bd60-149">Valige kiirvahekaardil **Vaiketeave** märkeruut **Jäta föderaalse rahastamise kulude ajakavast välja**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="0bd60-150">Muudatuste salvestamiseks valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0bd60-151">Föderaalse rahastamise kulude ajakava päringu käivitamine</span><span class="sxs-lookup"><span data-stu-id="0bd60-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="0bd60-152">Minge jaotisse **Projektijuhtimine ja raamatupidamine \> Päringud ja aruanded \> Toetuse päring \> Föderaalsete rahastamise kulude ajakava**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="0bd60-153">Järgige jaotises **Parameetrid** järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="0bd60-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="0bd60-154">Valige väljal **Kuupäevaintervall** kuupäevaintervalli kood.</span><span class="sxs-lookup"><span data-stu-id="0bd60-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="0bd60-155">Teise võimalusena määratlege kuupäevaintervall väljadel **Alguskuupäev** ja **Lõpukuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="0bd60-156">Valikuline: kui soovite päringusse tuluna kaasata ainult arveldatud tehinguid, määrake suvand **Kaasa ainult arveldatud tulud** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0bd60-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="0bd60-157">Tulbad</span><span class="sxs-lookup"><span data-stu-id="0bd60-157">Columns</span></span>

<span data-ttu-id="0bd60-158">Föderaalse rahastamise kulude ajakava päring sisaldab järgmisi veerge.</span><span class="sxs-lookup"><span data-stu-id="0bd60-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="0bd60-159">Föderaalse riigiabi kataloogi klastri nimi</span><span class="sxs-lookup"><span data-stu-id="0bd60-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="0bd60-160">Väljastav agentuur</span><span class="sxs-lookup"><span data-stu-id="0bd60-160">Grantor agency</span></span>
- <span data-ttu-id="0bd60-161">Vahendav agentuur</span><span class="sxs-lookup"><span data-stu-id="0bd60-161">Pass-through agency</span></span>
- <span data-ttu-id="0bd60-162">Toetuse nimi</span><span class="sxs-lookup"><span data-stu-id="0bd60-162">Grant name</span></span>
- <span data-ttu-id="0bd60-163">Toetuse ID</span><span class="sxs-lookup"><span data-stu-id="0bd60-163">Grant ID</span></span>
- <span data-ttu-id="0bd60-164">Toetuse taotluse ID</span><span class="sxs-lookup"><span data-stu-id="0bd60-164">Grant application ID</span></span>
- <span data-ttu-id="0bd60-165">Föderaalse riigiabi kataloogi</span><span class="sxs-lookup"><span data-stu-id="0bd60-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="0bd60-166">Kviitungid</span><span class="sxs-lookup"><span data-stu-id="0bd60-166">Receipts</span></span>
- <span data-ttu-id="0bd60-167">Kulutused</span><span class="sxs-lookup"><span data-stu-id="0bd60-167">Expenditures</span></span>
