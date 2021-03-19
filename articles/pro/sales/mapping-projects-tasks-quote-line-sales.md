---
title: Projektide ja ülesannete vastendamine projektipõhise hinnapakkumise reaga
description: Selles teemas kirjeldatakse projektide ja tööülesannete vastendamist projektipõhise tööülesande reaga.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272743"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="0fa98-103">Projektide ja ülesannete vastendamine projektipõhise hinnapakkumise reaga</span><span class="sxs-lookup"><span data-stu-id="0fa98-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="0fa98-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="0fa98-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0fa98-105">Projektipõhistel hinnapakkumiste ridadel saate vastendada juba hinnapakkumise reaga seostatud projekti konkreetsed ülesanded.</span><span class="sxs-lookup"><span data-stu-id="0fa98-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="0fa98-106">Kui vastendate tööülesanded hinnapakkumise reaga, rakendatakse järgmisi hinnapakkumise real määratletud üksusi ainult nendele ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="0fa98-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="0fa98-107">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="0fa98-107">Billing method</span></span>
- <span data-ttu-id="0fa98-108">Arveldatavuse valikud</span><span class="sxs-lookup"><span data-stu-id="0fa98-108">Chargeability options</span></span>
- <span data-ttu-id="0fa98-109">Mitteületatavad limiidid</span><span class="sxs-lookup"><span data-stu-id="0fa98-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="0fa98-110">Kliendid</span><span class="sxs-lookup"><span data-stu-id="0fa98-110">Customers</span></span>

<span data-ttu-id="0fa98-111">Näiteks võib teil olla projekt, kus üks etapp on fikseeritud hinnaga ja kõik ülejäänud etapid on aja ja materjalide põhjal.</span><span class="sxs-lookup"><span data-stu-id="0fa98-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="0fa98-112">Sel juhul saate seostada esimese etapi ja kõik selle alluvad tööülesanded selle etapi hinnapakkumise rea fikseeritud arveldusmeetodiga.</span><span class="sxs-lookup"><span data-stu-id="0fa98-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="0fa98-113">Seejärel saate kõik muud etapid seostada aja- ja materjalidepõhise hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="0fa98-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="0fa98-114">Projektipõhiste hinnapakkumise ridadega ülesannete seostamine</span><span class="sxs-lookup"><span data-stu-id="0fa98-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="0fa98-115">Saate tööülesanded seostada hinnapakkumiste ridadega järgmistest asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="0fa98-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="0fa98-116">Leht **Projekt** > vahekaart **Ülesande arveldus** (optimaalne)</span><span class="sxs-lookup"><span data-stu-id="0fa98-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="0fa98-117">Leht **Hinnapakkumise rida** vahekaart > **Arveldatavad ülesanded**</span><span class="sxs-lookup"><span data-stu-id="0fa98-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="0fa98-118">Projekti lehelt</span><span class="sxs-lookup"><span data-stu-id="0fa98-118">From the Project page</span></span>

<span data-ttu-id="0fa98-119">Leht **Projekt** pakub optimaalset kogemust ülesannete seostamiseks hinnapakkumise ridadega.</span><span class="sxs-lookup"><span data-stu-id="0fa98-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="0fa98-120">Sellel lehel saate valida mitu tööülesannet ja seostada kõik need ning nende alluvad tööülesanded valitud hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="0fa98-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="0fa98-121">Kontrollige, et projektipõhise hinnapakkumise rea vahekaardil **Üldine** olekt täidetud väli **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="0fa98-122">Valige väljal **Kaasatud tööülesanded** valik **Ainult valitud tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="0fa98-123">Salvestage projektipõhine hinnapakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="0fa98-123">Save the project-based quote line.</span></span> <span data-ttu-id="0fa98-124">Vormi värskendamisel kuvatakse vahekaarti **Arveldatavad tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="0fa98-125">Valige vahekaardil **Üldine** projektile link väljalt **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="0fa98-126">Valige lehel **Projektid** vahekaart **Ülesande arveldus**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="0fa98-127">Valige teisest ruudustikust, mis puudutab ülesandepõhise arvelduse seadistamist, üks või rohkem ülesannet ja seejärel valige suvand **Seosta hinnapakkumise read**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="0fa98-128">Valige kuvatavas dialoogis hinnapakkumise rida, kus kuvatakse hinnapakkumisel projektipõhiseid hinnapakkumise ridu.</span><span class="sxs-lookup"><span data-stu-id="0fa98-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="0fa98-129">Märkige väljal **Arvelduse tüüp**, kas need toimingud on arveldatavad või mitte.</span><span class="sxs-lookup"><span data-stu-id="0fa98-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="0fa98-130">Märkige ruut, kui soovite, et ühing peaks kaasama valitud tööülesannete alluvad tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="0fa98-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="0fa98-131">Kasti märkimine seostab valitud ülesannete tütarülesanded hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="0fa98-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="0fa98-132">Valige dialoogi sulgemiseks nupp **Ok**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="0fa98-133">Hinnapakkumise rea lehelt</span><span class="sxs-lookup"><span data-stu-id="0fa98-133">From the Quote line page</span></span>

<span data-ttu-id="0fa98-134">Projekti tööülesanded saate seostada hinnapakkumise ridadega vahekaardil **Arveldatavad ülesanded** lehel **Hinnapakkumise rida**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="0fa98-135">Optimaalne koht projekti ülesannete seostamiseks hinnapakkumiste ridadega on vahekaart **Ülesande arveldus** lehel **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="0fa98-136">Kui seostate tööülesanded vahekaardilt **Arveldatavad ülesanded** lehelt **Hinnapakkumise rida**, peate iga projekti käsitsi seostama.</span><span class="sxs-lookup"><span data-stu-id="0fa98-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="0fa98-137">Kontrollige, et projektipõhise hinnapakkumise rea vahekaardil **Üldine** oleks väljal **Projekt** projekt valitud.</span><span class="sxs-lookup"><span data-stu-id="0fa98-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="0fa98-138">Valige väljal **Kaasatud tööülesanded** valik **Ainult valitud tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="0fa98-139">Salvestage projektipõhine hinnapakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="0fa98-139">Save the project-based quote line.</span></span> <span data-ttu-id="0fa98-140">Vormi värskendamisel kuvatakse vahekaarti **Arveldatavad tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="0fa98-141">Valige vahekaardil **Arveldatavad ülesanded** suvand **Lisa hinnapakkumise rea tööülesanne**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="0fa98-142">Valige lehe **Hinnapakkumise rea ülesanne** väljal **Ülesanded** ülesanne ja valige väljal **Arvelduse tüüp** käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="0fa98-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0fa98-143">Close the page.</span></span> <span data-ttu-id="0fa98-144">Valitud tööülesanne on nüüd seotud hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="0fa98-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="0fa98-145">Ülesannete projektipõhiste hinnapakkumiste ridadest lahti sidumine</span><span class="sxs-lookup"><span data-stu-id="0fa98-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="0fa98-146">Projekti lehelt</span><span class="sxs-lookup"><span data-stu-id="0fa98-146">From the Project page</span></span>

<span data-ttu-id="0fa98-147">See meetod pakub kõige optimaalsemat kogemust ülesannete hinnapakkumiste ridadest lahti sidumiseks.</span><span class="sxs-lookup"><span data-stu-id="0fa98-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="0fa98-148">Saate valida mitu tööülesannet ja siduda valitud hinnapakkumise reast lahti kõik need ning nende alluvad tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="0fa98-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="0fa98-149">Valige projekti link projektipõhise hinnapakkumise rea vahekaardilt **Üldine** väljal **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="0fa98-150">Valige lehel **Projektid** vahekaart **Ülesande arveldus**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="0fa98-151">Valige teisest ruudustikust, mis puudutab ülesandepõhise arvelduse seadistamist, üks või rohkem ülesannet ja seejärel valige suvand **Hinnapakkumise ridade lahti sidumine**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="0fa98-152">Valige kuvatavas dialoogiboksis hinnapakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="0fa98-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="0fa98-153">Märkige ruut, et näidata, kas soovite, et seotus tuleks eemaldada ka valitud ülesannete tütarülesannetelt.</span><span class="sxs-lookup"><span data-stu-id="0fa98-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="0fa98-154">Kasti märkimine seob hinnapakkumise reast lahti seob lahti ka tütarülesanded.</span><span class="sxs-lookup"><span data-stu-id="0fa98-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="0fa98-155">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-155">Select **OK**.</span></span> <span data-ttu-id="0fa98-156">Hoiatusteade hoiatab teid, et kui eemaldate selle seose, võidakse kõik varem toimingule salvestatud tegelikud näitajad tagasi pöörata.</span><span class="sxs-lookup"><span data-stu-id="0fa98-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="0fa98-157">Valige **OK**, et jätkata ja eemaldada seos ülesande ja projektipõhise hinnapakkumise rea vahel.</span><span class="sxs-lookup"><span data-stu-id="0fa98-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="0fa98-158">Hinnapakkumise rea lehelt</span><span class="sxs-lookup"><span data-stu-id="0fa98-158">From the Quote line page</span></span>

<span data-ttu-id="0fa98-159">Projekti tööülesanded saate hinnapakkumise ridadest lahti siduda ka vahekaardil **Arveldatavad ülesanded** lehel **Hinnapakkumise rida**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="0fa98-160">Valige vahekaardil **Arveldatavad ülesanded** suvand **Tühista hinnapakkumise rea tööülesanne**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="0fa98-161">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fa98-161">Select **OK**.</span></span> <span data-ttu-id="0fa98-162">Hoiatusteade hoiatab teid, et kui eemaldate selle seose, võidakse kõik varem toimingule salvestatud tegelikud näitajad tagasi pöörata.</span><span class="sxs-lookup"><span data-stu-id="0fa98-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="0fa98-163">Valige **OK**, et jätkata ja eemaldada seos ülesande ja projektipõhise hinnapakkumise rea vahel.</span><span class="sxs-lookup"><span data-stu-id="0fa98-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="0fa98-164">See toiming ei kustuta tööülesannet projektist.</span><span class="sxs-lookup"><span data-stu-id="0fa98-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="0fa98-165">See eemaldab ainult tööülesande seose projektipõhiselt hinnapakkumise realt.</span><span class="sxs-lookup"><span data-stu-id="0fa98-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]