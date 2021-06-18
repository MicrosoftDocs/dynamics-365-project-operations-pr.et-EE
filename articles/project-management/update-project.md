---
title: Projekti värskendamine
description: Selles teemas kirjeldatakse Project Operationsis projektide värskendamist.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993366"
---
# <a name="update-a-project"></a><span data-ttu-id="88688-103">Projekti värskendamine</span><span class="sxs-lookup"><span data-stu-id="88688-103">Update a project</span></span>

<span data-ttu-id="88688-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="88688-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="88688-105">Allpool on kokkuvõte väljadest, mida saab projektis värskendada pärast selle loomist ja mis tahes värskendustega seotud tagajärgedest.</span><span class="sxs-lookup"><span data-stu-id="88688-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="88688-106">Projekti üksikasjade väljad</span><span class="sxs-lookup"><span data-stu-id="88688-106">Project detail fields</span></span>

- <span data-ttu-id="88688-107">**Nimi**: Projekti pealkiri.</span><span class="sxs-lookup"><span data-stu-id="88688-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="88688-108">**Kirjeldus**: Projekti ülevaade.</span><span class="sxs-lookup"><span data-stu-id="88688-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="88688-109">**Klient**: ettevõte, kellele projekt toimetatakse.</span><span class="sxs-lookup"><span data-stu-id="88688-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="88688-110">**Kalendri Mall**: projekti tööaeg.</span><span class="sxs-lookup"><span data-stu-id="88688-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="88688-111">Pärast välja muutmist arvutatakse kogu ajakava ümber.</span><span class="sxs-lookup"><span data-stu-id="88688-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="88688-112">**Valuuta**: projekti valuuta.</span><span class="sxs-lookup"><span data-stu-id="88688-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="88688-113">See väli vaikeväärtus põhineb lepingut sõlmiva üksuse määratletud valuutal.</span><span class="sxs-lookup"><span data-stu-id="88688-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="88688-114">Kui lepingut sõlmivat üksust värskendatakse, värskendatakse ka seda välja.</span><span class="sxs-lookup"><span data-stu-id="88688-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="88688-115">**Lepingut sõlmiv üksus**: organisatsiooniüksus, mis esindab ettevõtte rühma või allüksust, kes vastutab peamiselt müügi võitmise eest ja tööde ning teenuste kliendile pakkumise eest.</span><span class="sxs-lookup"><span data-stu-id="88688-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="88688-116">**Projektijuht**: projekti meeskonnaliige, kellel on õigus ajakirjeid ja kulusid üle vaadata ning kinnitada.</span><span class="sxs-lookup"><span data-stu-id="88688-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="88688-117">Väljade prognoosimine</span><span class="sxs-lookup"><span data-stu-id="88688-117">Estimate fields</span></span>

- <span data-ttu-id="88688-118">**Prognoositav alguskuupäev**: projekti alustamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="88688-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="88688-119">Kui see väli on värskendatud, teisaldatakse projekti kõik tööülesanded proportsionaalselt uue alguskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="88688-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="88688-120">**Lõppkuupäev**: kuupäev, millele on kavandatud projekti lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="88688-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="88688-121">**Tööpanus**: projekti prognoositav panus.</span><span class="sxs-lookup"><span data-stu-id="88688-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="88688-122">Kui projektile lisatakse tööülesanded, siis seda välja enam muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="88688-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="88688-123">**Eeldatav tööjõukulu**: projekti eeldatav tööjõukulu.</span><span class="sxs-lookup"><span data-stu-id="88688-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="88688-124">Kui projektile lisatakse tööjõukulud, siis seda välja enam muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="88688-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="88688-125">**Prognoositavad kulud**: projekti prognoositavad kulud.</span><span class="sxs-lookup"><span data-stu-id="88688-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="88688-126">Kui projektile lisatakse kulud, siis seda välja enam muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="88688-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="88688-127">Projekti tegelike näitajate väljad</span><span class="sxs-lookup"><span data-stu-id="88688-127">Project actual fields</span></span>
- <span data-ttu-id="88688-128">**Tegelik algus**: projekti käivitamise päev.</span><span class="sxs-lookup"><span data-stu-id="88688-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="88688-129">**Tegelik lõpp**: värskendatakse projekti lõpetamisel.</span><span class="sxs-lookup"><span data-stu-id="88688-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="88688-130">Projekti oleku väljad</span><span class="sxs-lookup"><span data-stu-id="88688-130">Project status fields</span></span>

- <span data-ttu-id="88688-131">**Projekti üldine olek**: projektijuhi antud üldine projekti tervis.</span><span class="sxs-lookup"><span data-stu-id="88688-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="88688-132">**Kommentaarid**: projektijuhi antud narratiiv projekti praeguse tervise kohta.</span><span class="sxs-lookup"><span data-stu-id="88688-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]