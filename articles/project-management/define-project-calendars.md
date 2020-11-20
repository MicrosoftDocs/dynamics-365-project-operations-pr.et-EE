---
title: Projektikalendrite määratlemine
description: Selles teemas leiate teavet projekti kalendri kasutamise kohta, et jälgida projekti ajakava.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131653"
---
# <a name="define-project-calendars"></a><span data-ttu-id="479ef-103">Projektikalendrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="479ef-103">Define project calendars</span></span>

<span data-ttu-id="479ef-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="479ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="479ef-105">Projekti ajakava loomiseks peate looma projektikalendri malli, mis määratleb töötundide arvu päevas ja kõik äri lõpetamised.</span><span class="sxs-lookup"><span data-stu-id="479ef-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="479ef-106">Projektikalendri malli loomiseks seostage projekti väljaga **Kalendrimall** töömall.</span><span class="sxs-lookup"><span data-stu-id="479ef-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="479ef-107">Töömalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="479ef-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="479ef-108">Valige vasakpoolsel navigatsioonipaanil **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="479ef-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="479ef-109">Avage loendilehel **Ressursid** kasutajakirje ja seejärel tehke valik **Kuva töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="479ef-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="479ef-110">Veenduge, et brauseriaknas oleks hüpikaknad lubatud.</span><span class="sxs-lookup"><span data-stu-id="479ef-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="479ef-111">Nii saate vaadata ressursi jaoks määratud töötunde.</span><span class="sxs-lookup"><span data-stu-id="479ef-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="479ef-112">Valige vahekaardil **Kuuvaade** suvand **Seadista**.</span><span class="sxs-lookup"><span data-stu-id="479ef-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="479ef-113">Kuvatakse kolme suvandiga loend.</span><span class="sxs-lookup"><span data-stu-id="479ef-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="479ef-114">Uus nädalagraafik</span><span class="sxs-lookup"><span data-stu-id="479ef-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="479ef-115">Ühe päeva töögraafik</span><span class="sxs-lookup"><span data-stu-id="479ef-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="479ef-116">Eemalolekuaeg</span><span class="sxs-lookup"><span data-stu-id="479ef-116">Time Off</span></span>

4. <span data-ttu-id="479ef-117">Tehke valik **Uus nädalagraafik** ja seejärel määrake selle ressurside ajakava suvandid.</span><span class="sxs-lookup"><span data-stu-id="479ef-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="479ef-118">Saate määrata korduva nädalagraafiku, iga päeva tunniparameetrid, äri lõpetamised ja muud.</span><span class="sxs-lookup"><span data-stu-id="479ef-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="479ef-119">Määrake kuupäevavahemik, valige **Salvesta** ja valige seejärel **Sule**.</span><span class="sxs-lookup"><span data-stu-id="479ef-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="479ef-120">Minge tagasi loendilehele **Ressursid** ja valige ressurss, mille jaoks töötunde määrate.</span><span class="sxs-lookup"><span data-stu-id="479ef-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="479ef-121">Töömalli määramiseks tehke valik **Seadista kalender nimega**.</span><span class="sxs-lookup"><span data-stu-id="479ef-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="479ef-122">Sisestage dialoogiboksis **Töömall** töömalli nimi ja seejärel tehke valik **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="479ef-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="479ef-123">Nüüd saate seostada töömalli projektikalendri malliga.</span><span class="sxs-lookup"><span data-stu-id="479ef-123">You can now associate the work template with a project calendar template.</span></span>
