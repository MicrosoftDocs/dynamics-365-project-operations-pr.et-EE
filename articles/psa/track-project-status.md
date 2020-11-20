---
title: Projekti oleku jälgimine
description: Projekti oleku jälgimine Project Service’is
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 00b6d874b42a415fe567d17e49c0ea319d8952a0
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127828"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="77922-103">Projekti oleku jälgimine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="77922-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="77922-104">Kasutage funktsiooni [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] kliendi projekti edenemise jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="77922-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="77922-105">Tegevuste edenedes värskendatakse projekti etappe, kajastades tegevuste etappi.</span><span class="sxs-lookup"><span data-stu-id="77922-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="77922-106">**Uus**</span><span class="sxs-lookup"><span data-stu-id="77922-106">**New**</span></span>    | <span data-ttu-id="77922-107">Projekti loomisel määratakse etapiks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="77922-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="77922-108">Kui lõite projekti mallist, võib projektil olla selles staadiumis ajakava hinnanguid ja meeskonnaandmeid.</span><span class="sxs-lookup"><span data-stu-id="77922-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="77922-109">Vastasel korral on tegemist projekti struktuuriga ja ülejäänud projekti komponendid tuleb käsitsi sisestada.</span><span class="sxs-lookup"><span data-stu-id="77922-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="77922-110">**Hinnapakkumine**</span><span class="sxs-lookup"><span data-stu-id="77922-110">**Quote**</span></span>   |      <span data-ttu-id="77922-111">Kui seostate projekti hinnapakkumisega või loote selle hinnapakkumise põhjal, määratakse projekti etapiks **Hinnapakkumine** ning värskendatakse ka eeldatavaid algus- ja lõppkuupäevi.</span><span class="sxs-lookup"><span data-stu-id="77922-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="77922-112">Kui projekt on hinnapakkumise staadiumis, kuvatakse hinnapakkumise üksikasjad vahekaardil **Müük** lehel **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="77922-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="77922-113">**Plaan**</span><span class="sxs-lookup"><span data-stu-id="77922-113">**Plan**</span></span>   |                                     <span data-ttu-id="77922-114">Kui võidate projektiga seotud hinnapakkumise ja tegevused jõuavad lepingu etappi, määratakse projekti etapiks **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="77922-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="77922-115">Lepingu üksikasjad kuvatakse vahekaardil **Müük** lehel **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="77922-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="77922-116">**Lõpule viidud**</span><span class="sxs-lookup"><span data-stu-id="77922-116">**Complete**</span></span> |                    <span data-ttu-id="77922-117">Kui projekti töö on lõpetatud, saate määrata etapiks **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="77922-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="77922-118">Kui projekti etapiks on määratud Valmis, siis tähendab see, et töö on 100% valmis, kuid projekt hoitakse avatuna pooleliolevate aja- või kulukirjete registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="77922-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="77922-119">**Sule**</span><span class="sxs-lookup"><span data-stu-id="77922-119">**Close**</span></span>   |           <span data-ttu-id="77922-120">Kui kõik projekti toimingud on registreeritud ja neid pole enam vaja logida, võite märkida etapiks käsitsi **Sule**.</span><span class="sxs-lookup"><span data-stu-id="77922-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="77922-121">Kui projekti olekuks on määratud **Sule**, ei saa logida projekti rohkem kandeid ja projekt on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="77922-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="77922-122">Projekti oleku jälgimine</span><span class="sxs-lookup"><span data-stu-id="77922-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="77922-123">Minge jaotisse **Project Service > Projektid**.</span><span class="sxs-lookup"><span data-stu-id="77922-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="77922-124">Klõpsake projekti, millega soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="77922-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="77922-125">Valige kuva ülaosas asuvalt ribalt projekti nime kõrval olev allanool ja seejärel klõpsake suvandit **Projekti jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="77922-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="77922-126">Valige ülesannete loendi kohal olevast rippmenüüst **Panuse jälgimine** või **Kulude jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="77922-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="77922-127">Topeltklõpsake tööülesandel selle redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="77922-127">Double-click any task to edit it.</span></span> <span data-ttu-id="77922-128">Saate ka Gantti diagrammil tulpasid teisaldada või nende suurust muuta, et muuta ülesande aega ja edenemist.</span><span class="sxs-lookup"><span data-stu-id="77922-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="77922-129">Vt ka</span><span class="sxs-lookup"><span data-stu-id="77922-129">See Also</span></span>  
 [<span data-ttu-id="77922-130">Projektijuhi juhend</span><span class="sxs-lookup"><span data-stu-id="77922-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
