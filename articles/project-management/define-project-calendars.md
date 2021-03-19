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
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286963"
---
# <a name="define-project-calendars"></a><span data-ttu-id="eb72c-103">Projektikalendrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="eb72c-103">Define project calendars</span></span>

<span data-ttu-id="eb72c-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="eb72c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb72c-105">Projekti ajakava loomiseks peate looma projektikalendri malli, mis määratleb töötundide arvu päevas ja kõik äri lõpetamised.</span><span class="sxs-lookup"><span data-stu-id="eb72c-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="eb72c-106">Projektikalendri malli loomiseks seostage projekti väljaga **Kalendrimall** töömall.</span><span class="sxs-lookup"><span data-stu-id="eb72c-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="eb72c-107">Töömalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eb72c-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="eb72c-108">Valige vasakpoolsel navigatsioonipaanil **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="eb72c-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="eb72c-109">Avage loendilehel **Ressursid** kasutajakirje ja seejärel tehke valik **Kuva töötunnid**.</span><span class="sxs-lookup"><span data-stu-id="eb72c-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="eb72c-110">Veenduge, et brauseriaknas oleks hüpikaknad lubatud.</span><span class="sxs-lookup"><span data-stu-id="eb72c-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="eb72c-111">Nii saate vaadata ressursi jaoks määratud töötunde.</span><span class="sxs-lookup"><span data-stu-id="eb72c-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="eb72c-112">Valige vahekaardil **Kuuvaade** suvand **Seadista**.</span><span class="sxs-lookup"><span data-stu-id="eb72c-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="eb72c-113">Kuvatakse kolme suvandiga loend.</span><span class="sxs-lookup"><span data-stu-id="eb72c-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="eb72c-114">Uus nädalagraafik</span><span class="sxs-lookup"><span data-stu-id="eb72c-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="eb72c-115">Ühe päeva töögraafik</span><span class="sxs-lookup"><span data-stu-id="eb72c-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="eb72c-116">Eemalolekuaeg</span><span class="sxs-lookup"><span data-stu-id="eb72c-116">Time Off</span></span>

4. <span data-ttu-id="eb72c-117">Tehke valik **Uus nädalagraafik** ja seejärel määrake selle ressurside ajakava suvandid.</span><span class="sxs-lookup"><span data-stu-id="eb72c-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="eb72c-118">Saate määrata korduva nädalagraafiku, iga päeva tunniparameetrid, äri lõpetamised ja muud.</span><span class="sxs-lookup"><span data-stu-id="eb72c-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="eb72c-119">Määrake kuupäevavahemik, valige **Salvesta** ja valige seejärel **Sule**.</span><span class="sxs-lookup"><span data-stu-id="eb72c-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="eb72c-120">Minge tagasi loendilehele **Ressursid** ja valige ressurss, mille jaoks töötunde määrate.</span><span class="sxs-lookup"><span data-stu-id="eb72c-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="eb72c-121">Töömalli määramiseks tehke valik **Seadista kalender nimega**.</span><span class="sxs-lookup"><span data-stu-id="eb72c-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="eb72c-122">Sisestage dialoogiboksis **Töömall** töömalli nimi ja seejärel tehke valik **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="eb72c-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="eb72c-123">Nüüd saate seostada töömalli projektikalendri malliga.</span><span class="sxs-lookup"><span data-stu-id="eb72c-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]