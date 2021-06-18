---
title: Projektide ja ülesannete vastendamine projektipõhise hinnapakkumise reaga
description: Selles teemas kirjeldatakse projektide ja tööülesannete vastendamist projektipõhise tööülesande reaga.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994581"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="53715-103">Projektide ja ülesannete vastendamine projektipõhise hinnapakkumise reaga</span><span class="sxs-lookup"><span data-stu-id="53715-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="53715-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="53715-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="53715-105">Projektipõhistel hinnapakkumiste ridadel saate vastendada juba hinnapakkumise reaga seostatud projekti konkreetsed ülesanded.</span><span class="sxs-lookup"><span data-stu-id="53715-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="53715-106">Kui vastendate tööülesanded hinnapakkumise reaga, rakendatakse järgmisi hinnapakkumise real määratletud üksusi ainult nendele ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="53715-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="53715-107">Arveldusmeetod</span><span class="sxs-lookup"><span data-stu-id="53715-107">Billing method</span></span>
- <span data-ttu-id="53715-108">Arveldatavuse valikud</span><span class="sxs-lookup"><span data-stu-id="53715-108">Chargeability options</span></span>
- <span data-ttu-id="53715-109">Mitteületatavad limiidid</span><span class="sxs-lookup"><span data-stu-id="53715-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="53715-110">Kliendid</span><span class="sxs-lookup"><span data-stu-id="53715-110">Customers</span></span>

<span data-ttu-id="53715-111">Näiteks võib teil olla projekt, kus üks etapp on fikseeritud hinnaga ja kõik ülejäänud etapid on aja ja materjalide põhjal.</span><span class="sxs-lookup"><span data-stu-id="53715-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="53715-112">Sel juhul saate seostada esimese etapi ja kõik selle alluvad tööülesanded selle etapi hinnapakkumise rea fikseeritud arveldusmeetodiga.</span><span class="sxs-lookup"><span data-stu-id="53715-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="53715-113">Seejärel saate kõik muud etapid seostada aja- ja materjalidepõhise hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="53715-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="53715-114">Projektipõhiste hinnapakkumise ridadega ülesannete seostamine</span><span class="sxs-lookup"><span data-stu-id="53715-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="53715-115">Saate tööülesanded seostada hinnapakkumiste ridadega järgmistest asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="53715-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="53715-116">Leht **Projekt** > vahekaart **Ülesande arveldus** (optimaalne)</span><span class="sxs-lookup"><span data-stu-id="53715-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="53715-117">Leht **Hinnapakkumise rida** vahekaart > **Arveldatavad ülesanded**</span><span class="sxs-lookup"><span data-stu-id="53715-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="53715-118">Projekti lehelt</span><span class="sxs-lookup"><span data-stu-id="53715-118">From the Project page</span></span>

<span data-ttu-id="53715-119">Leht **Projekt** pakub optimaalset kogemust ülesannete seostamiseks hinnapakkumise ridadega.</span><span class="sxs-lookup"><span data-stu-id="53715-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="53715-120">Sellel lehel saate valida mitu tööülesannet ja seostada kõik need ning nende alluvad tööülesanded valitud hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="53715-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="53715-121">Kontrollige, et projektipõhise hinnapakkumise rea vahekaardil **Üldine** olekt täidetud väli **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="53715-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="53715-122">Valige väljal **Kaasatud tööülesanded** valik **Ainult valitud tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="53715-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="53715-123">Salvestage projektipõhine hinnapakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="53715-123">Save the project-based quote line.</span></span> <span data-ttu-id="53715-124">Vormi värskendamisel kuvatakse vahekaarti **Arveldatavad tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="53715-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="53715-125">Valige vahekaardil **Üldine** projektile link väljalt **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="53715-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="53715-126">Valige lehel **Projektid** vahekaart **Ülesande arveldus**.</span><span class="sxs-lookup"><span data-stu-id="53715-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="53715-127">Valige teisest ruudustikust, mis puudutab ülesandepõhise arvelduse seadistamist, üks või rohkem ülesannet ja seejärel valige suvand **Seosta hinnapakkumise read**.</span><span class="sxs-lookup"><span data-stu-id="53715-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="53715-128">Valige kuvatavas dialoogis hinnapakkumise rida, kus kuvatakse hinnapakkumisel projektipõhiseid hinnapakkumise ridu.</span><span class="sxs-lookup"><span data-stu-id="53715-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="53715-129">Märkige väljal **Arvelduse tüüp**, kas need toimingud on arveldatavad või mitte.</span><span class="sxs-lookup"><span data-stu-id="53715-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="53715-130">Märkige ruut, kui soovite, et ühing peaks kaasama valitud tööülesannete alluvad tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="53715-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="53715-131">Kasti märkimine seostab valitud ülesannete tütarülesanded hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="53715-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="53715-132">Valige dialoogi sulgemiseks nupp **Ok**.</span><span class="sxs-lookup"><span data-stu-id="53715-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="53715-133">Hinnapakkumise rea lehelt</span><span class="sxs-lookup"><span data-stu-id="53715-133">From the Quote line page</span></span>

<span data-ttu-id="53715-134">Projekti tööülesanded saate seostada hinnapakkumise ridadega vahekaardil **Arveldatavad ülesanded** lehel **Hinnapakkumise rida**.</span><span class="sxs-lookup"><span data-stu-id="53715-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="53715-135">Optimaalne koht projekti ülesannete seostamiseks hinnapakkumiste ridadega on vahekaart **Ülesande arveldus** lehel **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="53715-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="53715-136">Kui seostate tööülesanded vahekaardilt **Arveldatavad ülesanded** lehelt **Hinnapakkumise rida**, peate iga projekti käsitsi seostama.</span><span class="sxs-lookup"><span data-stu-id="53715-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="53715-137">Kontrollige, et projektipõhise hinnapakkumise rea vahekaardil **Üldine** oleks väljal **Projekt** projekt valitud.</span><span class="sxs-lookup"><span data-stu-id="53715-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="53715-138">Valige väljal **Kaasatud tööülesanded** valik **Ainult valitud tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="53715-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="53715-139">Salvestage projektipõhine hinnapakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="53715-139">Save the project-based quote line.</span></span> <span data-ttu-id="53715-140">Vormi värskendamisel kuvatakse vahekaarti **Arveldatavad tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="53715-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="53715-141">Valige vahekaardil **Arveldatavad ülesanded** suvand **Lisa hinnapakkumise rea tööülesanne**.</span><span class="sxs-lookup"><span data-stu-id="53715-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="53715-142">Valige lehe **Hinnapakkumise rea ülesanne** väljal **Ülesanded** ülesanne ja valige väljal **Arvelduse tüüp** käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="53715-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="53715-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="53715-143">Close the page.</span></span> <span data-ttu-id="53715-144">Valitud tööülesanne on nüüd seotud hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="53715-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="53715-145">Ülesannete projektipõhiste hinnapakkumiste ridadest lahti sidumine</span><span class="sxs-lookup"><span data-stu-id="53715-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="53715-146">Projekti lehelt</span><span class="sxs-lookup"><span data-stu-id="53715-146">From the Project page</span></span>

<span data-ttu-id="53715-147">See meetod pakub kõige optimaalsemat kogemust ülesannete hinnapakkumiste ridadest lahti sidumiseks.</span><span class="sxs-lookup"><span data-stu-id="53715-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="53715-148">Saate valida mitu tööülesannet ja siduda valitud hinnapakkumise reast lahti kõik need ning nende alluvad tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="53715-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="53715-149">Valige projekti link projektipõhise hinnapakkumise rea vahekaardilt **Üldine** väljal **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="53715-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="53715-150">Valige lehel **Projektid** vahekaart **Ülesande arveldus**.</span><span class="sxs-lookup"><span data-stu-id="53715-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="53715-151">Valige teisest ruudustikust, mis puudutab ülesandepõhise arvelduse seadistamist, üks või rohkem ülesannet ja seejärel valige suvand **Hinnapakkumise ridade lahti sidumine**.</span><span class="sxs-lookup"><span data-stu-id="53715-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="53715-152">Valige kuvatavas dialoogiboksis hinnapakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="53715-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="53715-153">Märkige ruut, et näidata, kas soovite, et seotus tuleks eemaldada ka valitud ülesannete tütarülesannetelt.</span><span class="sxs-lookup"><span data-stu-id="53715-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="53715-154">Kasti märkimine seob hinnapakkumise reast lahti seob lahti ka tütarülesanded.</span><span class="sxs-lookup"><span data-stu-id="53715-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="53715-155">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="53715-155">Select **OK**.</span></span> <span data-ttu-id="53715-156">Hoiatusteade hoiatab teid, et kui eemaldate selle seose, võidakse kõik varem toimingule salvestatud tegelikud näitajad tagasi pöörata.</span><span class="sxs-lookup"><span data-stu-id="53715-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="53715-157">Valige **OK**, et jätkata ja eemaldada seos ülesande ja projektipõhise hinnapakkumise rea vahel.</span><span class="sxs-lookup"><span data-stu-id="53715-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="53715-158">Hinnapakkumise rea lehelt</span><span class="sxs-lookup"><span data-stu-id="53715-158">From the Quote line page</span></span>

<span data-ttu-id="53715-159">Projekti tööülesanded saate hinnapakkumise ridadest lahti siduda ka vahekaardil **Arveldatavad ülesanded** lehel **Hinnapakkumise rida**.</span><span class="sxs-lookup"><span data-stu-id="53715-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="53715-160">Valige vahekaardil **Arveldatavad ülesanded** suvand **Tühista hinnapakkumise rea tööülesanne**.</span><span class="sxs-lookup"><span data-stu-id="53715-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="53715-161">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="53715-161">Select **OK**.</span></span> <span data-ttu-id="53715-162">Hoiatusteade hoiatab teid, et kui eemaldate selle seose, võidakse kõik varem toimingule salvestatud tegelikud näitajad tagasi pöörata.</span><span class="sxs-lookup"><span data-stu-id="53715-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="53715-163">Valige **OK**, et jätkata ja eemaldada seos ülesande ja projektipõhise hinnapakkumise rea vahel.</span><span class="sxs-lookup"><span data-stu-id="53715-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="53715-164">See toiming ei kustuta tööülesannet projektist.</span><span class="sxs-lookup"><span data-stu-id="53715-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="53715-165">See eemaldab ainult tööülesande seose projektipõhiselt hinnapakkumise realt.</span><span class="sxs-lookup"><span data-stu-id="53715-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]