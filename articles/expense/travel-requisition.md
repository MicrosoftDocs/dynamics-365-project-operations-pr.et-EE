---
title: Reisitellimused
description: Selles teemas antakse teavet reisitellimuste kohta.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: e05f54349eaa09dd22331ff07950542dd326e711
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001736"
---
# <a name="travel-requisitions"></a><span data-ttu-id="cc1cc-103">Reisitellimused</span><span class="sxs-lookup"><span data-stu-id="cc1cc-103">Travel requisitions</span></span>

<span data-ttu-id="cc1cc-104">_**Kehtib:** ressursipõhiste/mitteladustatavate stsenaariumite jaoks_</span><span class="sxs-lookup"><span data-stu-id="cc1cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cc1cc-105">Reisitellimus loetleb kulud, mis on tekkinud reisimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="cc1cc-106">Reisitellimus esitatakse läbivaatamiseks ja seda saab kasutada kulude lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="cc1cc-107">Võimalik, et teil tuleb esitada reisitellimus enne seda, teete organisatsiooni tasutavaid kulusid.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="cc1cc-108">Seda nõuet kohaldatakse, olenemata sellest, kas tasute kulude eest ettevõtte krediitkaardiga, kulutate ettemaksuks saadud raha või tasute kulude eest oma taskust, mis hiljem organisatsiooni poolt hüvitatakse.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="cc1cc-109">Reisitellimusi ja poliitikaid saab kasutada organisatsiooni kulude haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="cc1cc-110">Kui teie organisatsioon töötab näiteks fikseeritud hinnaga projektiga, mis nõuab reisimist, peavad projekti meeskonnaliikmete sõidukulud vastama projekti eelarvele.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="cc1cc-111">Nõudes, et reisikulud kinnitatakse enne nende tekkimist, saab organisatsioon aidata tagada, et projekt jääb eelarve piiresse.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="cc1cc-112">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="cc1cc-112">Configuration</span></span> 

<span data-ttu-id="cc1cc-113">Reisitellimusi saab konfigureerida kui "kohustuslik", lubades kuluhalduse parameetrite all parameetri "Reisimise eelnev lubamine on kohustuslik".</span><span class="sxs-lookup"><span data-stu-id="cc1cc-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="cc1cc-114">Reisitellimuse loomine ja esitamine</span><span class="sxs-lookup"><span data-stu-id="cc1cc-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="cc1cc-115">Avage **Minu kulud: reisitellimus** ja valige **Uus reisitellimus**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="cc1cc-116">Sisestage tellimuse eesmärk ja sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="cc1cc-117">Sisestage täiendav teave väljale **Reisi kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="cc1cc-118">Iga eeldatava kulu kohta, nagu näiteks lend, eined või autorent, looge kulu reaüksus.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="cc1cc-119">Lisage iga kulu eeldatav päev, eeldatav summa ja valuuta.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="cc1cc-120">Kui olete eeldatavate kulude lisamise lõpetanud, valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="cc1cc-121">Kui olete valmis reisitellimust esitama, valige **Töövoog** > **Esita**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="cc1cc-122">Oma heakskiidetud reisitellimusi saate vaadata jaotises **Minu kulud: reisitellimus**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="cc1cc-123">Kuva saadaolevad reisitellimused</span><span class="sxs-lookup"><span data-stu-id="cc1cc-123">View available travel requisitions</span></span>

<span data-ttu-id="cc1cc-124">Kõiki oma reisitellimusi saate vaadata jaotises **Minu kulud: reisitellimused**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="cc1cc-125">Reisitellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="cc1cc-125">Approve travel requisitions</span></span>

<span data-ttu-id="cc1cc-126">Valige reisitellimus, mida soovite kinnitada, ja seejärel valige **Töövoog** > **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="cc1cc-127">Kuluaruande esitamine kinnitatud reisitellimuse abil</span><span class="sxs-lookup"><span data-stu-id="cc1cc-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="cc1cc-128">Looge uus kuluaruanne ja kuluaruande päises ning heakskiidetud reiside loendist valige **Vastendage reisitellimusega**.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="cc1cc-129">Väli **Reisitellimuse summa** värskendatakse kuluaruande päises automaatselt.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="cc1cc-130">Lisage kõik reisi jaoks tehtud kulutused.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="cc1cc-131">Kui väli **Eelautoriseeritud** on lubatud, värskendatakse konkreetse kulukategooria vastavausse viidud summa ja lubatud summa.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="cc1cc-132">Kui vastendate kuluaruande kinnitatud reisitellimusega, ei saa tehingu summa olla suurem kui lubatud summa.</span><span class="sxs-lookup"><span data-stu-id="cc1cc-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]