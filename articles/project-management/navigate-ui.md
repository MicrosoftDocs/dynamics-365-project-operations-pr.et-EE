---
title: Kasutajaliidese navigeerimine
description: Selles teemas antakse teavet projektihaldusest Dynamics 365 Projecti toimingutes.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961851"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="e2c6a-103">Kasutajaliidese navigeerimine</span><span class="sxs-lookup"><span data-stu-id="e2c6a-103">Navigating the user interface</span></span>

<span data-ttu-id="e2c6a-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="e2c6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="e2c6a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e2c6a-105">Overview</span></span>

<span data-ttu-id="e2c6a-106">Peamine projekti vorm on eraldatud mitmele vahekaardile.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="e2c6a-107">Iga vahekaart esindab projektis erinevat üksikasjalikku teavet.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="e2c6a-108">**Kokkuvõte**: kirjeldab projekti ja koondab nii planeeritud kui ka tegeliku projekti tulemuslikkuse.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Kokkuvõtte vahekaart ja väljad](media/navigation7.png)

- <span data-ttu-id="e2c6a-110">**Tööülesanded**: kirjeldatakse tööjaotuse struktuuri üksikasju, mida esindab ruudustiku vaade, lai vaade ja Gantti diagramm.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Ülesande vahekaart ja väljad](media/navigation8.png)

- <span data-ttu-id="e2c6a-112">**Meeskond**: pakub üksikasju projekti osaliste kohta.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="e2c6a-113">Ka iga meeskonnaliikme määratud panus on samuti selles vaates kokku võetud.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Meeskonna vahekaart ja väljad](media/navigation9.png)

- <span data-ttu-id="e2c6a-115">**Ressursi määramised**: annab ajafaasiga vaate iga projekti ressursi panusest.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Ressursi määramiste vahekaart ja väljad](media/navigation10.png)

- <span data-ttu-id="e2c6a-117">**Ressursi vastavusseviimine**: annab ajafaasiga vaate iga nimetatud ressursi ja selle broneeringu määramiste erinevuste kohta.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Ressursi vastavusseviimise vahekaart ja väljad](media/navigation11.png)

- <span data-ttu-id="e2c6a-119">**Prognoosid**: annab ajafaasiga vaate projekti kulude ja müügi prognoosidest.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Prognooside vahekaart ja väljad](media/navigation12.png)

- <span data-ttu-id="e2c6a-121">**Jälgimine**: annab vaate, mis kuvab tööülesannete edenemist panuse, kulude ja müügi tööjaotuse struktuuris.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Jälgimise vahekaart ja väljad](media/navigation13.png)

- <span data-ttu-id="e2c6a-123">**Müük**: annab süvalinke projektiga seotud hinnapakkumistele ja lepingutele.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="e2c6a-124">**Kuluprognoosid**: annab ruudustiku, mis määratleb projekti kulud vastavalt ettevõtte kulukategooriatele.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Kuluprognooside vahekaart ja väljad](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="e2c6a-126">Ruudustiku juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="e2c6a-126">Grid controls</span></span>

<span data-ttu-id="e2c6a-127">Järgnev on lühike ülevaade erinevatelt projekti kavandamise vahekaartidelt leitud tüüpilistest juhtelementidest.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="e2c6a-128">Värskendamine</span><span class="sxs-lookup"><span data-stu-id="e2c6a-128">Refresh</span></span>

<span data-ttu-id="e2c6a-129">**Värskenda**: toob serverist uusimad andmed, kui pärast ruudustikku laadimist on toimunud muudatusi.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Nupp Värskenda](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="e2c6a-131">Rühmitusalus:</span><span class="sxs-lookup"><span data-stu-id="e2c6a-131">Group by</span></span>

<span data-ttu-id="e2c6a-132">**Rühmitamine**: värskendab ruudustiku ridade rühmitamist, et kajastada kas ressursse, rolle või kategooriaid vastavalt kasutaja vajadustele.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Rühmitamise nupp](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="e2c6a-134">Eelmine/järgmine</span><span class="sxs-lookup"><span data-stu-id="e2c6a-134">Previous/Next</span></span>

<span data-ttu-id="e2c6a-135">**Eelmine**/**Järgmine**: ajafaasiga ruudustiku nähtavate ajaperioodide värskendamine.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Nupud Eelmine ja Järgmine](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="e2c6a-137">Ajaskaala</span><span class="sxs-lookup"><span data-stu-id="e2c6a-137">Timescale</span></span>

<span data-ttu-id="e2c6a-138">**Ajaskaala**: ajafaasiliste andmete koondamise muutmine päevade, nädalate, kuude ja aastate vahel.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Nupp Ajaskaala](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="e2c6a-140">Laienda</span><span class="sxs-lookup"><span data-stu-id="e2c6a-140">Expand</span></span>

<span data-ttu-id="e2c6a-141">**Laienda**: nähtava ruudustiku renderdamine täisekraanile, võimaldades näha täiendavaid rolle.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Nupp Laienda](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="e2c6a-143">Ajafaasi alus</span><span class="sxs-lookup"><span data-stu-id="e2c6a-143">Time-phase by</span></span>

<span data-ttu-id="e2c6a-144">**Ajafaasi alus**: ruudustiku ridade rühmitamise uuendamine, et see kajastaks müügiprognooside kuluprognoose.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="e2c6a-145">See juhtelement kehtib ka prognoosi skripti ja jälgimise ruudustiku kohta.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Nupp ajafaasi alus](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="e2c6a-147">Lisa veerg</span><span class="sxs-lookup"><span data-stu-id="e2c6a-147">Add column</span></span>

<span data-ttu-id="e2c6a-148">**Veeru lisamine**: võimaldab kasutajal määratleda ruudustikus nähtavaid veerge.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="e2c6a-149">Vormi **Projekti kavandamine** ruudustikele saab lisada ainult valmiskujul veergusid.</span><span class="sxs-lookup"><span data-stu-id="e2c6a-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Nupp Lisa veerg](media/navigation5.png)
