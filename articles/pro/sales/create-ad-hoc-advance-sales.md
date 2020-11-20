---
title: Lepingus sihtpärase advansi loomine – liht
description: See teema sisaldab teavet vastavalt vajadusele lepingus avansi loomist.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181357"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a><span data-ttu-id="82fbd-103">Lepingus sihtpärase advansi loomine – liht</span><span class="sxs-lookup"><span data-stu-id="82fbd-103">Creating an ad hoc advance on a contract - lite</span></span>

<span data-ttu-id="82fbd-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="82fbd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="82fbd-105">Microsoft Dynamics 365 Project Operations toetab arveldamisstsenaariumeid, mis hõlmavad eelmakseid ja avansse.</span><span class="sxs-lookup"><span data-stu-id="82fbd-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="82fbd-106">**Project Operationsis** suvandi **Avandsid** kasutamine sarnaneb **honorari** lepingutele.</span><span class="sxs-lookup"><span data-stu-id="82fbd-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="82fbd-107">Kliendile avansi eest arve esitamiseks tehke järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="82fbd-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="82fbd-108">Avage leht **Projektileping** ja valige vahekaart **Ettemaksed ja honorarid**.</span><span class="sxs-lookup"><span data-stu-id="82fbd-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="82fbd-109">Andmeruudustikus, mis loetleb kõik eelnevalt salvestatud avansid ja ettemaksed, valige **+ Uus projektilepingu honorar**.</span><span class="sxs-lookup"><span data-stu-id="82fbd-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="82fbd-110">Avaneb **kiirloomise** vorm ettemakse või avansi salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="82fbd-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="82fbd-111">Allolevas tabelis on loetletud avansi salvestamise väljad ja mida tuleks uute avansside loomisel meeles pidada.</span><span class="sxs-lookup"><span data-stu-id="82fbd-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="82fbd-112">Väli</span><span class="sxs-lookup"><span data-stu-id="82fbd-112">Field</span></span> | <span data-ttu-id="82fbd-113">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="82fbd-113">Description</span></span> | <span data-ttu-id="82fbd-114">Allavoolu mõjud</span><span class="sxs-lookup"><span data-stu-id="82fbd-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="82fbd-115">**Projektilepingu klient**</span><span class="sxs-lookup"><span data-stu-id="82fbd-115">**Project Contract Customer**</span></span> | <span data-ttu-id="82fbd-116">See väli näitab, millisele lepingu kliendile selle avansi eest arve esitatakse.</span><span class="sxs-lookup"><span data-stu-id="82fbd-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="82fbd-117">Kui teil on lepingus mitu klienti ja soovite esitada igale neist konkreetse honorari või avansi summa, looge avanss iga kliendi jaoks eraldi.</span><span class="sxs-lookup"><span data-stu-id="82fbd-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="82fbd-118">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="82fbd-118">**Description**</span></span> | <span data-ttu-id="82fbd-119">Avansi eesmärgi või ajastuse kirjeldus, et aidata avanssi tuvastada.</span><span class="sxs-lookup"><span data-stu-id="82fbd-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="82fbd-120">See kirjeldus kuvatakse selle avansi arvereal.</span><span class="sxs-lookup"><span data-stu-id="82fbd-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="82fbd-121">**Summa**</span><span class="sxs-lookup"><span data-stu-id="82fbd-121">**Amount**</span></span> | <span data-ttu-id="82fbd-122">Ettemakse või avansi summa.</span><span class="sxs-lookup"><span data-stu-id="82fbd-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="82fbd-123">See summa kuvatakse selle avansi arvereal.</span><span class="sxs-lookup"><span data-stu-id="82fbd-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="82fbd-124">**Arve kuupäev**</span><span class="sxs-lookup"><span data-stu-id="82fbd-124">**Invoice Date**</span></span> | <span data-ttu-id="82fbd-125">Kuupäev, millal selle avansi arve kliendile esitatakse.</span><span class="sxs-lookup"><span data-stu-id="82fbd-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="82fbd-126">See on automatiseeritud arve loomisprotsessi kuupäev, et luua selle avansi arverida.</span><span class="sxs-lookup"><span data-stu-id="82fbd-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="82fbd-127">**Arve olek**</span><span class="sxs-lookup"><span data-stu-id="82fbd-127">**Invoice Status**</span></span> | <span data-ttu-id="82fbd-128">See on suvandi säte, mis näitab, kas see avanss lisatakse selle kliendi arve mustandile.</span><span class="sxs-lookup"><span data-stu-id="82fbd-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="82fbd-129">Võimalikud väärtused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="82fbd-129">The possible values are:</span></span></br><span data-ttu-id="82fbd-130">- **Pole arveldamiseks valmis**</span><span class="sxs-lookup"><span data-stu-id="82fbd-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="82fbd-131">- **Arveldamiseks valmis**</span><span class="sxs-lookup"><span data-stu-id="82fbd-131">- **Ready to invoice**</span></span> | <span data-ttu-id="82fbd-132">Kui avanss või ettemaks on märgitud kui **Arveldamiseks valmis**, lisatakse see arve mustandile rea ajana.</span><span class="sxs-lookup"><span data-stu-id="82fbd-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="82fbd-133">Järgmise arveldusperioodi projektikulude vastavusse viimiseks saab kasutada ainult täielikult arveldatud ettemakset.</span><span class="sxs-lookup"><span data-stu-id="82fbd-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="82fbd-134">SelectAvansi või ettemakse salvestamiseks valige kiirloomise dialoogiboksis suvand **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="82fbd-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>
