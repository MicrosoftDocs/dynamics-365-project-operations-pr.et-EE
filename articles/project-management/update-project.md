---
title: Projekti värskendamine
description: Selles teemas kirjeldatakse Project Operationsis projektide värskendamist.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131428"
---
# <a name="update-a-project"></a><span data-ttu-id="a578b-103">Projekti värskendamine</span><span class="sxs-lookup"><span data-stu-id="a578b-103">Update a project</span></span>

<span data-ttu-id="a578b-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="a578b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a578b-105">Allpool on kokkuvõte väljadest, mida saab projektis värskendada pärast selle loomist ja mis tahes värskendustega seotud tagajärgedest.</span><span class="sxs-lookup"><span data-stu-id="a578b-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="a578b-106">Projekti üksikasjade väljad</span><span class="sxs-lookup"><span data-stu-id="a578b-106">Project detail fields</span></span>

- <span data-ttu-id="a578b-107">**Nimi**: Projekti pealkiri.</span><span class="sxs-lookup"><span data-stu-id="a578b-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="a578b-108">**Kirjeldus**: Projekti ülevaade.</span><span class="sxs-lookup"><span data-stu-id="a578b-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="a578b-109">**Klient**: ettevõte, kellele projekt toimetatakse.</span><span class="sxs-lookup"><span data-stu-id="a578b-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="a578b-110">**Kalendri Mall**: projekti tööaeg.</span><span class="sxs-lookup"><span data-stu-id="a578b-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="a578b-111">Pärast välja muutmist arvutatakse kogu ajakava ümber.</span><span class="sxs-lookup"><span data-stu-id="a578b-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="a578b-112">**Valuuta**: projekti valuuta.</span><span class="sxs-lookup"><span data-stu-id="a578b-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="a578b-113">See väli vaikeväärtus põhineb lepingut sõlmiva üksuse määratletud valuutal.</span><span class="sxs-lookup"><span data-stu-id="a578b-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="a578b-114">Kui lepingut sõlmivat üksust värskendatakse, värskendatakse ka seda välja.</span><span class="sxs-lookup"><span data-stu-id="a578b-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="a578b-115">**Lepingut sõlmiv üksus**: organisatsiooniüksus, mis esindab ettevõtte rühma või allüksust, kes vastutab peamiselt müügi võitmise eest ja tööde ning teenuste kliendile pakkumise eest.</span><span class="sxs-lookup"><span data-stu-id="a578b-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="a578b-116">**Projektijuht**: projekti meeskonnaliige, kellel on õigus ajakirjeid ja kulusid üle vaadata ning kinnitada.</span><span class="sxs-lookup"><span data-stu-id="a578b-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="a578b-117">Väljade prognoosimine</span><span class="sxs-lookup"><span data-stu-id="a578b-117">Estimate fields</span></span>

- <span data-ttu-id="a578b-118">**Prognoositav alguskuupäev**: projekti alustamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a578b-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="a578b-119">Kui see väli on värskendatud, teisaldatakse projekti kõik tööülesanded proportsionaalselt uue alguskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="a578b-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="a578b-120">**Lõppkuupäev**: kuupäev, millele on kavandatud projekti lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="a578b-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="a578b-121">**Tööpanus**: projekti prognoositav panus.</span><span class="sxs-lookup"><span data-stu-id="a578b-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="a578b-122">Kui projektile lisatakse tööülesanded, siis seda välja enam muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="a578b-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="a578b-123">**Eeldatav tööjõukulu**: projekti eeldatav tööjõukulu.</span><span class="sxs-lookup"><span data-stu-id="a578b-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="a578b-124">Kui projektile lisatakse tööjõukulud, siis seda välja enam muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="a578b-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="a578b-125">**Prognoositavad kulud**: projekti prognoositavad kulud.</span><span class="sxs-lookup"><span data-stu-id="a578b-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="a578b-126">Kui projektile lisatakse kulud, siis seda välja enam muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="a578b-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="a578b-127">Projekti tegelike näitajate väljad</span><span class="sxs-lookup"><span data-stu-id="a578b-127">Project actual fields</span></span>
- <span data-ttu-id="a578b-128">**Tegelik algus**: projekti käivitamise päev.</span><span class="sxs-lookup"><span data-stu-id="a578b-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="a578b-129">**Tegelik lõpp**: värskendatakse projekti lõpetamisel.</span><span class="sxs-lookup"><span data-stu-id="a578b-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="a578b-130">Projekti oleku väljad</span><span class="sxs-lookup"><span data-stu-id="a578b-130">Project status fields</span></span>

- <span data-ttu-id="a578b-131">**Projekti üldine olek**: projektijuhi antud üldine projekti tervis.</span><span class="sxs-lookup"><span data-stu-id="a578b-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="a578b-132">**Kommentaarid**: projektijuhi antud narratiiv projekti praeguse tervise kohta.</span><span class="sxs-lookup"><span data-stu-id="a578b-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

