---
title: Halda ressursse
description: Selles teemas antakse teavet ressursside haldamise kohta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997821"
---
# <a name="manage-resources"></a><span data-ttu-id="1299d-103">Halda ressursse</span><span class="sxs-lookup"><span data-stu-id="1299d-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1299d-104">Dynamics 365 Project Service Automation sisaldab ressursihalduri armatuurlauda, mis pakub visuaalset ülevaadet ressursi nõudlusest ja kasutamisest kogu ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="1299d-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="1299d-105">Armatuurlaua diagramme saate kasutada järgmise teabe visualiseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1299d-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="1299d-106">**Ressursi nõudlus** – **aktiivse ressursi taotluse** diagramm kuvab edastatud ressursid.</span><span class="sxs-lookup"><span data-stu-id="1299d-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="1299d-107">Ressursid on koondatud kas rolli või projekti kaudu.</span><span class="sxs-lookup"><span data-stu-id="1299d-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="1299d-108">**Esitamata ressursi nõudmised** – **määramata ressursi nõudluse** diagramm näitab kõiki ressursinõudeid, mida pole veel esitatud.</span><span class="sxs-lookup"><span data-stu-id="1299d-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="1299d-109">See aitab ressursihalduril vaadata nõudlust, mis pole kindel ja mida võidakse esitada ressursitaotluse kaudu.</span><span class="sxs-lookup"><span data-stu-id="1299d-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="1299d-110">**Viimase nädala tasustatav kasutamine** – **kasutuse roll** diagrammil näitab organisatsiooni tegeliku arvete kasutamise protsenti rolli poolt, mis on seotud selle sihtmärgiga.</span><span class="sxs-lookup"><span data-stu-id="1299d-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1299d-111">Selleks et teha **kasutuse rolli** diagramm saadavaks, looge töövoogu UpdateRoleUtilization käivitav töö.</span><span class="sxs-lookup"><span data-stu-id="1299d-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="1299d-112">Seda korduvat tööd käitatakse iga seitsme päeva järel, et arvutada viimase seitsme päeva jooksul tasustatav kasutamine.</span><span class="sxs-lookup"><span data-stu-id="1299d-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="1299d-113">Tulemused on koondatud rolli järgi.</span><span class="sxs-lookup"><span data-stu-id="1299d-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="1299d-114">Projekti meeskonnaliikmete haldamine</span><span class="sxs-lookup"><span data-stu-id="1299d-114">Manage project team members</span></span>

<span data-ttu-id="1299d-115">Projekti haldurid saavad kasutada ressursi halduri armatuurlauda, et hallata projektide ressursse.</span><span class="sxs-lookup"><span data-stu-id="1299d-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="1299d-116">Näiteks saavad nad lisada meeskonnaliikme otse projekti ja broneerida meeskonnaliikme, kes vastab üldise ressursi kogutud ressursinõuetele.</span><span class="sxs-lookup"><span data-stu-id="1299d-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="1299d-117">Meeskonnaliikme lisamine otse projektile</span><span class="sxs-lookup"><span data-stu-id="1299d-117">Add a team member directly to a project</span></span>

<span data-ttu-id="1299d-118">Meeskonnaliikme lisamiseks otse projektile valige lehel **Projektid** vahekaardil **Meeskond** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1299d-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="1299d-119">Kuvatakse dialoogiboks **Kiirloomine: projekti meeskonnaliige**.</span><span class="sxs-lookup"><span data-stu-id="1299d-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="1299d-120">Selles dialoogiboksis saate teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="1299d-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="1299d-121">**Broneerige nimega ressurss** – valige väljal **Broneeritav ressurss** ressursi nimi.</span><span class="sxs-lookup"><span data-stu-id="1299d-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="1299d-122">Seejärel valige roll, määrake periood ja valige jaotamise meetod.</span><span class="sxs-lookup"><span data-stu-id="1299d-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="1299d-123">Teie valitud nimega ressurss lisatakse projektile valitud jaotamise meetodi ja ressursside kalendri abil.</span><span class="sxs-lookup"><span data-stu-id="1299d-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="1299d-124">**Üldise ressursi lisamine** – jätke **Reserveeritava ressursi** väli tühjaks ja valige seejärel roll, määrake periood ja valige soovitud jaotuse meetod.</span><span class="sxs-lookup"><span data-stu-id="1299d-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="1299d-125">Üldine ressurss lisatakse meeskonda kohatäitena, et talletada nõudluse mudelit, mida kasutatakse meeskonnas nimega ressursside broneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1299d-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="1299d-126">Nõue esitatakse vastavalt projekti kalendrile.</span><span class="sxs-lookup"><span data-stu-id="1299d-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="1299d-127">**Nimega ressursi lisamine meeskonnale, rakendamata ressursi võimsust** – valige väljal **Broneeritav ressurss** ressurss.</span><span class="sxs-lookup"><span data-stu-id="1299d-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="1299d-128">Seejärel valige periood ja valige jaotamise meetodiks **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="1299d-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="1299d-129">Ressurss lisatakse meeskonda, kuid ressursi võimsust ei tarbita broneerimise kaudu.</span><span class="sxs-lookup"><span data-stu-id="1299d-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="1299d-130">Reserveerige meeskonnaliige, et täita ressursinõudeid üldise ressursi jaoks</span><span class="sxs-lookup"><span data-stu-id="1299d-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="1299d-131">Rakenduses PSA saate broneerida üldise ressursi projekti meeskonnas ning määrata rolli, nõutava võimsuse ja võimsuse jaotamise viisi.</span><span class="sxs-lookup"><span data-stu-id="1299d-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="1299d-132">Ressursinõudes saate määrata üldiste ressurssidega seotud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="1299d-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="1299d-133">Need atribuudid hõlmavad nõutavaid oskusi, eelistatud organisatsiooniüksust ja eelistatud ressursse.</span><span class="sxs-lookup"><span data-stu-id="1299d-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="1299d-134">Järgige neid juhiseid, et määrata arendaja jaoks üldise ressursi nõutavad oskused.</span><span class="sxs-lookup"><span data-stu-id="1299d-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="1299d-135">Valige lehel **Projektid** vahekaardil **Meeskond** käsk **Uus**, et broneerida üldine ressurss.</span><span class="sxs-lookup"><span data-stu-id="1299d-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Meeskonnas broneeritud üldine ressurss](media/Resource-Management-image9.png)

2. <span data-ttu-id="1299d-137">Valige vaates **Kõik meeskonnaliikmed** veerus **Ressursinõue** vastav link, et lisada üldisele ressursile nõutavad oskused.</span><span class="sxs-lookup"><span data-stu-id="1299d-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Nõude link](media/Resource-Management-image10.png)

3. <span data-ttu-id="1299d-139">Valige lehel **Ressursinõue**, mis kuvatakse **oskuste** ruudustikus, kolmikpunkt (**…**) ja seejärel valige **Lisa uus nõude omadus**, et lisada arendajale vajalikke oskusi.</span><span class="sxs-lookup"><span data-stu-id="1299d-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Uue nõude tunnuse käsu lisamine](media/Resource-Management-image11.png)

4. <span data-ttu-id="1299d-141">Valige dialoogiboksis **Kiirloomine: nõude tunnused** väljal **Tunnused** soovitud oskus.</span><span class="sxs-lookup"><span data-stu-id="1299d-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="1299d-142">Seejärel valige väljal **Hinnangu väärtus** selle oskuse jaoks oskuse tase.</span><span class="sxs-lookup"><span data-stu-id="1299d-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="1299d-143">Lõpuks määrake väljal **Ressursinõue** nõue, et ressursid pärineks organisatsiooniüksustest või isegi nimega ressurssidest.</span><span class="sxs-lookup"><span data-stu-id="1299d-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="1299d-144">Kui olete lõpetanud, valige **Save**.</span><span class="sxs-lookup"><span data-stu-id="1299d-144">When you've finished, select **Save**.</span></span>

    ![Kiirloomine: dialoogiboks Nõude tunnus](media/Resource-Management-image12.png)

5. <span data-ttu-id="1299d-146">Valige lehel **Ressursinõue** käsk **Broneeri**, et täita ressursinõue.</span><span class="sxs-lookup"><span data-stu-id="1299d-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Nupp Broneeri lehel Ressursinõue](media/Resource-Management-image13.png)

    <span data-ttu-id="1299d-148">Saate valida üldise ressursi ka ruudustikus **Kõik meeskonnaliikmed** ja seejärel valige **Reserveeri**.</span><span class="sxs-lookup"><span data-stu-id="1299d-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Nupp Broneeri kõigi meeskonnaliikmete ruudustiku kohal](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="1299d-150">Selles näites on 40 nõutavat tundi, kuid tegelikke broneeritud tunde ei kuvata, kuna üldistel ressurssidel pole reserveeringuid.</span><span class="sxs-lookup"><span data-stu-id="1299d-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="1299d-151">Lisaks pole määratud tunde, kuna üldine ressurss lisati otse meeskonnale.</span><span class="sxs-lookup"><span data-stu-id="1299d-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="1299d-152">Seda ei lisatud tööülesande määramise abil.</span><span class="sxs-lookup"><span data-stu-id="1299d-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="1299d-153">Lehel **Plaanimisabimees** saate saadaolevaid ressursse filtreerida ressursinõudes määratud nõuete järgi.</span><span class="sxs-lookup"><span data-stu-id="1299d-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="1299d-154">Ressursid sorditakse vastavalt ajakavapaneelil määratud sortimise parameetritele.</span><span class="sxs-lookup"><span data-stu-id="1299d-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Ajakavaabilise leht](media/Resource-Management-image15.png)

    <span data-ttu-id="1299d-156">Siin on mõned filtrid, mida kasutatakse sageli.</span><span class="sxs-lookup"><span data-stu-id="1299d-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="1299d-157">**Tunnused koos hinnanguga** – filtreerimine oskuste, sertifitseerimise ja muude ressursside omaduste alusel ning lisaks oskustaseme alusel.</span><span class="sxs-lookup"><span data-stu-id="1299d-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="1299d-158">**Rollid** – filtreeritakse vaikimisi kasutatavate rollide järgi, mis on määratud broneeritud ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="1299d-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="1299d-159">**Organisatsiooniüksused** – filtreerige arvestuslikke ressursse nende organisatsiooniüksuste järgi, kellele nad on määratud.</span><span class="sxs-lookup"><span data-stu-id="1299d-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="1299d-160">Kui te pole algse nõude otsingu tulemustega rahul, saate filtri kriteeriume muuta.</span><span class="sxs-lookup"><span data-stu-id="1299d-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="1299d-161">Laiendage vasakul olevat paani **Filtri vaade** ja seejärel valige **Otsi**, et leida täiendavaid ressursse.</span><span class="sxs-lookup"><span data-stu-id="1299d-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Filtri vaate paan](media/Resource-Management-image16.png)

7. <span data-ttu-id="1299d-163">Tulemuste sortimise muutmiseks valige **Sordi**.</span><span class="sxs-lookup"><span data-stu-id="1299d-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Sortimise käsk](media/Resource-Management-image17.png)

8. <span data-ttu-id="1299d-165">Valige ressursid vastavalt vajadusele määratud nõudmisele, nagu on näidatud ruudustiku ülaosas.</span><span class="sxs-lookup"><span data-stu-id="1299d-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="1299d-166">Saate tühjendada koordinaatvõrgus olevate lahtrite valiku ja jätta selle ressursi võimsuse avatuks.</span><span class="sxs-lookup"><span data-stu-id="1299d-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="1299d-167">Korraga saab valida ainult ühe ressursi.</span><span class="sxs-lookup"><span data-stu-id="1299d-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="1299d-168">Valige ressursi broneerimiseks **Broneeri** ja jätke ajakavapaneel avatuks, et saaksite valida täiendavad ressursid.</span><span class="sxs-lookup"><span data-stu-id="1299d-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="1299d-169">Võite ka valitud ressursi broneerimiseks ja ajakavapaneeli sulgemiseks valida **Broneeri ja välju**.</span><span class="sxs-lookup"><span data-stu-id="1299d-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ressursi reserveerimine](media/Resource-Management-image19.png)

    <span data-ttu-id="1299d-171">Teile kuvatakse teade broneeritud tundide kohta.</span><span class="sxs-lookup"><span data-stu-id="1299d-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="1299d-172">Nõudluse indikaatorid näitavad, kui palju broneerimisnõudeid on vaja täita ja kui palju on jäänud.</span><span class="sxs-lookup"><span data-stu-id="1299d-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="1299d-173">Samuti saate vaadata, kui palju valitud ressursi võimsust tarbitakse.</span><span class="sxs-lookup"><span data-stu-id="1299d-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="1299d-174">Ressursi reserveeringute üksikasjade vaatamiseks valige **Laienda**.</span><span class="sxs-lookup"><span data-stu-id="1299d-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="1299d-175">Naaske vaatesse **Kõik meeskonnaliikmed**.</span><span class="sxs-lookup"><span data-stu-id="1299d-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="1299d-176">Pange tähele, et üldine ressurss on asendatud nimega ressursiga ja 40 tundi on reserveeritud selle ressursi jaoks.</span><span class="sxs-lookup"><span data-stu-id="1299d-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Värskendatud kõigi meeskonnaliikmete ruudustik](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="1299d-178">Määratud tunde ei kuvata, kuna nad on otse meeskonnas broneeritud.</span><span class="sxs-lookup"><span data-stu-id="1299d-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="1299d-179">Neid ei broneeritud tööülesande määramise abil.</span><span class="sxs-lookup"><span data-stu-id="1299d-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="1299d-180">Üldiste ressursside määramine tööülesannetele ja ressursinõuete loomine</span><span class="sxs-lookup"><span data-stu-id="1299d-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="1299d-181">Rakenduses PSA saate luua tööülesandeid ja määrata neile üldiseid ressursse.</span><span class="sxs-lookup"><span data-stu-id="1299d-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="1299d-182">Sel viisil saab ressursi nõudluse esitada kohatäitena, kui hindate oma ajakava ja finantsnumbreid.</span><span class="sxs-lookup"><span data-stu-id="1299d-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="1299d-183">Seejärel saate luua ressursinõudeid üldistele ressurssidele ja need täita.</span><span class="sxs-lookup"><span data-stu-id="1299d-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="1299d-184">Tööülesande loomiseks valige lehel **Projektid** vahekaardil **Ajakava** **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1299d-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Uus tööülesanne loodud](media/Resource-Management-image21.png)

2. <span data-ttu-id="1299d-186">Valige väljal **Ressursid** sümbol **Ressursivalija**.</span><span class="sxs-lookup"><span data-stu-id="1299d-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="1299d-187">Kuvatakse ressursivalija, mis kuvab projekti jaoks olemasolevad meeskonnaliikmed.</span><span class="sxs-lookup"><span data-stu-id="1299d-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Ressursivalija](media/Resource-Management-image22.png)

3. <span data-ttu-id="1299d-189">Sisestage uue üldise ressursi nimi ja seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="1299d-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Sisestatud uue üldise ressursi nimi](media/Resource-Management-image23.png)

4. <span data-ttu-id="1299d-191">Valige kuvatavas dialoogiboksis **Kiirloomine: projekti meeskonnaliikmed** väljal **Roll** üldisele ressursile roll.</span><span class="sxs-lookup"><span data-stu-id="1299d-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="1299d-192">Valige väljalt **Ressursiühik** üldisele ressursile organisatsiooniüksus.</span><span class="sxs-lookup"><span data-stu-id="1299d-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="1299d-193">Seejärel tehke valik **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1299d-193">Then select **Save**.</span></span>

    ![Kiirloomine: dialoogiboks Projekti meeskonnaliige](media/Resource-Management-image24.png)

    <span data-ttu-id="1299d-195">Üldine meeskonnaliige on nüüd ülesandele määratud.</span><span class="sxs-lookup"><span data-stu-id="1299d-195">The generic team member is now assigned to the task.</span></span>

    ![Ülesandele määratud üldine meeskonnaliige](media/Resource-Management-image25.png)

    <span data-ttu-id="1299d-197">Vahekaardil **Meeskond** kuvatakse uus üldine meeskonnaliige.</span><span class="sxs-lookup"><span data-stu-id="1299d-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="1299d-198">Pange tähele, et sel on määratud ainult tunde.</span><span class="sxs-lookup"><span data-stu-id="1299d-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="1299d-199">Need tunnid on kõigi üldiste meeskonnaliikmete jaoks määratud ülesannete summa.</span><span class="sxs-lookup"><span data-stu-id="1299d-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="1299d-200">Üldisel meeskonnaliikmel pole veel nõutavaid tunde või ressursinõuet.</span><span class="sxs-lookup"><span data-stu-id="1299d-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Üldine meeskonnaliige vahekaardil Meeskond](media/Resource-Management-image26.png)

5. <span data-ttu-id="1299d-202">Nüüd saate määrata üldise meeskonnaliikme teistele ülesannetele, kasutades ressursivalijat.</span><span class="sxs-lookup"><span data-stu-id="1299d-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Üldine meeskonnaliige ressursivalijas](media/Resource-Management-image27.png)

    <span data-ttu-id="1299d-204">Kui olete üldise ressursi määramise ülesannetele lõpetanud, saate luua ressursinõude üldise ressursi jaoks.</span><span class="sxs-lookup"><span data-stu-id="1299d-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="1299d-205">Valige vahekaardil **Meeskond** üldine ressurss ja seejärel valige **Loo nõue**.</span><span class="sxs-lookup"><span data-stu-id="1299d-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Käsk Loo nõue](media/Resource-Management-image28.png)

    <span data-ttu-id="1299d-207">Kui nõue luuakse, on üldisel meeskonnaliikmel nõutavad tunnid ja link ressursinõudele.</span><span class="sxs-lookup"><span data-stu-id="1299d-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Ressursinõude link](media/Resource-Management-image29.png)

    <span data-ttu-id="1299d-209">Pärast nimega ressursi broneerimist eemaldatakse üldine ressurss meeskonnast ja asendatakse nimega ressursiga.</span><span class="sxs-lookup"><span data-stu-id="1299d-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Üldine ressurss on asendatud nimega ressursiga](media/Resource-Management-image30.png)

    <span data-ttu-id="1299d-211">Vahekaardil **Ajakava** eemaldatakse üldise ressursi määramised ja asendatakse nimega ressursiga.</span><span class="sxs-lookup"><span data-stu-id="1299d-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Vahekaardil Ajakava üldise ressursi määramised asendatud nimega ressursiga](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="1299d-213">See käitumine ilmneb ainult siis, kui nimega ressurss on täielikult broneeritud üldise ressursinõude jaoks.</span><span class="sxs-lookup"><span data-stu-id="1299d-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="1299d-214">Kui nimega ressurss asendab osaliselt üldise ressursinõude või mitu nimega ressurssi asendavad üldise ressursinõude, on üldine ressursinõue endiselt tööülesandele määratud.</span><span class="sxs-lookup"><span data-stu-id="1299d-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="1299d-215">Järgmisel illustratsioonil on 80-tunnise tööülesande kestuseks planeeritud viis päeva (16 tundi päevas üle viie päeva) ja määratud üldisele ressursile, mille nimi on **Funktsionaalne**.</span><span class="sxs-lookup"><span data-stu-id="1299d-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-Tunnine, viiepäevane ülesanne, mis on määratud funktsionaalsele üldisele ressursile](media/Resource-Management-image32.png)

    <span data-ttu-id="1299d-217">Nõude genereerimisel on see 80 tundi viie päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="1299d-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Nõue, mis on loodud 80 tunniks viie päeva jooksul](media/Resource-Management-image33.png)

    <span data-ttu-id="1299d-219">Kuna saadaolevad ressursid töötavad ainult kaheksa tundi päevas, on nõude täitmiseks vaja kahte ressurssi.</span><span class="sxs-lookup"><span data-stu-id="1299d-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Teine ressurss](media/Resource-Management-image35.png)

    <span data-ttu-id="1299d-221">Vahekaardil **Meeskond** saate nüüd vaadata, et üldisel ressursil pole nõutavaid tunde, kuid määratud tunnid kuvatakse endiselt koos kahe nimega ressursiga, mis moodustavad täitmise.</span><span class="sxs-lookup"><span data-stu-id="1299d-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Kaks nimega ressurssi vahekaardil Meeskond](media/Resource-Management-image36.png)

    <span data-ttu-id="1299d-223">Vahekaardil **Ajakava** on üldine ressurss endiselt tööülesande jaoks määratud.</span><span class="sxs-lookup"><span data-stu-id="1299d-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Üldised ressursid vahekaardil Ajakava](media/Resource-Management-image37.png)

<span data-ttu-id="1299d-225">PSA ei määra tööülesandele mõlemat ressurssi, kuna see käitumine tekitaks vähem prognoositavat ajakava.</span><span class="sxs-lookup"><span data-stu-id="1299d-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="1299d-226">Selles lihtsas näites on lihtne jagada tunde kahe ressursi vahel võrdselt.</span><span class="sxs-lookup"><span data-stu-id="1299d-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="1299d-227">Kuid keerukamate stsenaariumide korral, mis hõlmavad mitut tööülesannet ja mitut ressurssi, peab PSA tegema oletusi selle kohta, kuidas see peaks jaotama reserveeringud, mis on saadud mitme ressursi jaoks üle mitme toimingu.</span><span class="sxs-lookup"><span data-stu-id="1299d-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="1299d-228">Seega on neil juhtudel projektijuht vastutav mitme broneeringu sõelumise ja vajaduse korral määramise eest.</span><span class="sxs-lookup"><span data-stu-id="1299d-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="1299d-229">Broneeringute eraldamiseks määrab projektijuht tööülesanded üldistest ressurssidest nimega ressurssideks ja kasutab seejärel **vastavusseviimise** vaadet, et veenduda, kas eraldus töötab broneeringutega.</span><span class="sxs-lookup"><span data-stu-id="1299d-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="1299d-230">Ressursinõude redigeerimine</span><span class="sxs-lookup"><span data-stu-id="1299d-230">Edit a resource requirement</span></span>

<span data-ttu-id="1299d-231">Pärast seda, kui ressursinõue on loodud, võib projektijuht või ressursihaldur soovida redigeerida üksikasju, et täiustada otsingukriteeriumide järgimist ajakavapaneeli kasutamisel.</span><span class="sxs-lookup"><span data-stu-id="1299d-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="1299d-232">Ressursinõude redigeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1299d-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="1299d-233">Valige lehel **Projektid** vahekaardil **Meeskond** mis tahes üldise ressursi nõude link.</span><span class="sxs-lookup"><span data-stu-id="1299d-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="1299d-234">Kuvataval **Ressursinõude** lehel saate värskendada mitut atribuuti.</span><span class="sxs-lookup"><span data-stu-id="1299d-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="1299d-235">Järgmiselt on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="1299d-235">Here are some examples:</span></span>

    - <span data-ttu-id="1299d-236">Nimi</span><span class="sxs-lookup"><span data-stu-id="1299d-236">Name</span></span>
    - <span data-ttu-id="1299d-237">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="1299d-237">From Date</span></span>
    - <span data-ttu-id="1299d-238">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="1299d-238">To Date</span></span>
    - <span data-ttu-id="1299d-239">Kestus</span><span class="sxs-lookup"><span data-stu-id="1299d-239">Duration</span></span>
    - <span data-ttu-id="1299d-240">Ressursi tüüp</span><span class="sxs-lookup"><span data-stu-id="1299d-240">Resource Type</span></span>

<span data-ttu-id="1299d-241">**Ressursinõude** lehel saab projektijuht või ressursihaldur määratleda ka järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="1299d-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="1299d-242">Oskused</span><span class="sxs-lookup"><span data-stu-id="1299d-242">Skills</span></span>
- <span data-ttu-id="1299d-243">Rollid</span><span class="sxs-lookup"><span data-stu-id="1299d-243">Roles</span></span>
- <span data-ttu-id="1299d-244">Ressursieelistused</span><span class="sxs-lookup"><span data-stu-id="1299d-244">Resource preferences</span></span>
- <span data-ttu-id="1299d-245">Eelistatud organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="1299d-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="1299d-246">Pärast projekti broneerimist ressursi reserveeringute värskendamine</span><span class="sxs-lookup"><span data-stu-id="1299d-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="1299d-247">Pärast üldise või nimega ressursi lisamist projekti meeskonda saate ressursi reserveeringuid muuta.</span><span class="sxs-lookup"><span data-stu-id="1299d-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="1299d-248">Valige meeskonnaliige lehel **Projektid** vahekaardil **Meeskond** ja seejärel **Halda broneeringuid**.</span><span class="sxs-lookup"><span data-stu-id="1299d-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Valitud meeskonnaliikme jaoks avatud ajakavapaneel](media/Resource-Management-image40.png)

    <span data-ttu-id="1299d-250">Ilmub ajakavapaneel ja kuvatakse projekti meeskonnaliikme broneeringud.</span><span class="sxs-lookup"><span data-stu-id="1299d-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="1299d-251">Laiendage meeskonnaliikme kirjet, et vaadata selle projekti ja muude meeskonnaliikme võimsust tarbivate projektide suhtes broneeritud tunde.</span><span class="sxs-lookup"><span data-stu-id="1299d-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="1299d-252">Valige ja pukseerige broneering, et seda pikendada või lühendada.</span><span class="sxs-lookup"><span data-stu-id="1299d-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="1299d-253">Kuvatakse dialoogiboks **Ressursi reserveeringu loomine**, mis võimaldab teil reserveeringut muuta.</span><span class="sxs-lookup"><span data-stu-id="1299d-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Ressursi reserveeringu loomine](media/Resource-Management-image41.png)

3. <span data-ttu-id="1299d-255">Tehke broneeringul paremklõps.</span><span class="sxs-lookup"><span data-stu-id="1299d-255">Right-click the booking.</span></span> <span data-ttu-id="1299d-256">Seejärel saate kasutada otseteemenüüd järgmiste toimingute lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="1299d-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="1299d-257">Muutke broneeringu olekut.</span><span class="sxs-lookup"><span data-stu-id="1299d-257">Change the booking status.</span></span>
    - <span data-ttu-id="1299d-258">Redigeerige broneeringut.</span><span class="sxs-lookup"><span data-stu-id="1299d-258">Edit the booking.</span></span>
    - <span data-ttu-id="1299d-259">Asendage ressurss projekti meeskonnas.</span><span class="sxs-lookup"><span data-stu-id="1299d-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="1299d-260">Broneeringu oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="1299d-260">Change the booking status</span></span>

<span data-ttu-id="1299d-261">Saate muuta mis tahes vaike- või kohandatud broneeringu olekut.</span><span class="sxs-lookup"><span data-stu-id="1299d-261">You can change any default or custom booking status.</span></span>

![Käsk Muuda olekut](media/Resource-Management-image42.png)

<span data-ttu-id="1299d-263">PSA-s on järgmised olekud</span><span class="sxs-lookup"><span data-stu-id="1299d-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="1299d-264">**Tühistatud** – see olek tühistab ressursi reserveeringu ja vabastab ressursi võimsuse.</span><span class="sxs-lookup"><span data-stu-id="1299d-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="1299d-265">**Fikseeritud reserveering** – see olek kasutab ressursi võimsust.</span><span class="sxs-lookup"><span data-stu-id="1299d-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="1299d-266">Broneerimisel on tavaliselt see olek, kui avate lehel **Projektid** ruudustikust **Kõik meeskonnaliikmed** valiku **Halda broneeringuid**.</span><span class="sxs-lookup"><span data-stu-id="1299d-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="1299d-267">**Esialgne reserveerimine** – see olek lisab ressursi meeskonnale, kuid ei tarbi ressursi võimsust.</span><span class="sxs-lookup"><span data-stu-id="1299d-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="1299d-268">See näitab, et ressurss on reserveeritud potentsiaalsele tööle, kuid sellel on siiski vaba aega, kui seda on vaja teistel töödel.</span><span class="sxs-lookup"><span data-stu-id="1299d-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="1299d-269">Ressursside üldise kättesaadavuse vaates on esialgsetes reserveeringutes teistsugune olek kui fikseeritud reserveeringutes.</span><span class="sxs-lookup"><span data-stu-id="1299d-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="1299d-270">**Pakutud** – see olek esindab ressursi juhi või projektijuhi ettepanekut ressursi kohta.</span><span class="sxs-lookup"><span data-stu-id="1299d-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="1299d-271">Ettepanekud ei tarbi ressursi võimsust ja ressurssi ei lisata projekti meeskonda.</span><span class="sxs-lookup"><span data-stu-id="1299d-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="1299d-272">Ressursi fikseeritult reserveerimiseks meeskonda, peab projektijuht ettepaneku vastu võtma.</span><span class="sxs-lookup"><span data-stu-id="1299d-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="1299d-273">Ressursitaotluste esitamine</span><span class="sxs-lookup"><span data-stu-id="1299d-273">Submit resource requests</span></span>

<span data-ttu-id="1299d-274">Ressursi taotlusi kasutatakse nõudluse (ressursinõue) täitmiseks, mille peab täitma ressursihaldur.</span><span class="sxs-lookup"><span data-stu-id="1299d-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="1299d-275">Üldise ressursi jaoks, mis on juba meeskonnas, saate esitada ressursi taotluse otse.</span><span class="sxs-lookup"><span data-stu-id="1299d-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="1299d-276">Ressursi taotluse saab täita kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="1299d-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="1299d-277">Ressursihaldur täidab taotluse otse.</span><span class="sxs-lookup"><span data-stu-id="1299d-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="1299d-278">Sellisel juhul asendatakse üldine ressurss fikseeritud reserveeringuga, millel on nimega ressurss.</span><span class="sxs-lookup"><span data-stu-id="1299d-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="1299d-279">Ressursihaldur soovitab ressursi projektijuhti ja projektijuht kinnitab või hülgab pakutud ressursi.</span><span class="sxs-lookup"><span data-stu-id="1299d-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="1299d-280">Ressursi taotluse otsene täitmine</span><span class="sxs-lookup"><span data-stu-id="1299d-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="1299d-281">Ressursinõude loomisel saab projektijuht esitada ressursi taotluse üldise ressursi jaoks, valides ressursi ja valides seejärel valiku **Esita taotlus**.</span><span class="sxs-lookup"><span data-stu-id="1299d-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Nupp Taotluse esitamine](media/Resource-Management-image45.png)

<span data-ttu-id="1299d-283">Ressursi kohta leiate teavet selle ressursi haldurilt, kes seda taotlust täidab.</span><span class="sxs-lookup"><span data-stu-id="1299d-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="1299d-284">Pärast taotluse esitamist muudetakse meeskonnaliikme väli **Olek** väärtusele **Esitatud**.</span><span class="sxs-lookup"><span data-stu-id="1299d-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Valikuliste kommentaaride sisestamine](media/Resource-Management-image46.png)

<span data-ttu-id="1299d-286">Kui ressursihaldur vastab taotlusele, asendatakse üldine meeskonnaliige nimega ressursiga ruudustikus **Kõik meeskonnaliikmed**.</span><span class="sxs-lookup"><span data-stu-id="1299d-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Nimega ressursiga asendatud üldine meeskonnaliige ruudustikus Kõik meeskonnaliikmed](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="1299d-288">Ressursi soovituse kasutamine ressursi taotlemisel</span><span class="sxs-lookup"><span data-stu-id="1299d-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="1299d-289">Ressursi taotlusele ressursi otse broneerimise asemel, saab ressursihaldur teha ressursi ettepaneku projekti juhile.</span><span class="sxs-lookup"><span data-stu-id="1299d-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="1299d-290">Ressursihaldur võib seda suvandit kasutada juhul, kui nõuete täpne vaste pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="1299d-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="1299d-291">Kui ressursihaldur pakub ressurssi, näeb projektijuht, et üldise meeskonnaliikme väli **Olek** on muudetud väärtusele **Vaja läbivaatamist**.</span><span class="sxs-lookup"><span data-stu-id="1299d-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Üldise meeskonnaliikme olek muudetud väärtusele Vaja läbivaatamist](media/Resource-Management-image48.png)

<span data-ttu-id="1299d-293">Kui soovite vaadata pakutud ressurssi koos soovituse reserveeringu efektiga, topeltklõpsake meeskonnaliiget, kellel on olek **Vaja läbivaatamist**.</span><span class="sxs-lookup"><span data-stu-id="1299d-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="1299d-294">Seejärel valige vahekaart **Pakutavad ressursid**.</span><span class="sxs-lookup"><span data-stu-id="1299d-294">Then select the **Proposed Resources** tab.</span></span>

![Pakutavad ressursid](media/Resource-Management-image49.png)

<span data-ttu-id="1299d-296">Valige **Aktsepteeri kõik ettepanekud**, et nõustuda kõigi pakutud ressurssidega või **Hülga kõik ettepanekud** nende tagasilükkamiseks.</span><span class="sxs-lookup"><span data-stu-id="1299d-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="1299d-297">Kui nõustute pakutavate ressurssidega, on nad projektis meeskonnaliikmena fikseeritult reserveeritud ja asendavad üldiseid ressursse.</span><span class="sxs-lookup"><span data-stu-id="1299d-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="1299d-298">Kõik pakutavad ressursid tuleb kas aktsepteerida või hüljata.</span><span class="sxs-lookup"><span data-stu-id="1299d-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="1299d-299">Neid ei saa osaliselt aktsepteerida või hüljata.</span><span class="sxs-lookup"><span data-stu-id="1299d-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="1299d-300">Asendage ressurss projekti meeskonnas</span><span class="sxs-lookup"><span data-stu-id="1299d-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="1299d-301">Vahel peab projektijuht asendama broneeritud meeskonnaliikme projektis.</span><span class="sxs-lookup"><span data-stu-id="1299d-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="1299d-302">Valige lehel **Projektid** vahekaardil **Meeskond** soovitud ressurss, mis vajab asendamist, ja seejärel valige käsk **Halda reserveeringud**.</span><span class="sxs-lookup"><span data-stu-id="1299d-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="1299d-303">Laiendage ressurssi, et kuvada neile määratud projekte.</span><span class="sxs-lookup"><span data-stu-id="1299d-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Ressurss on laiendatud, et kuvada määratud projekte](media/Resource-Management-image50.png)

3. <span data-ttu-id="1299d-305">Paremklõpsake projekti ja seejärel valige käsk **Asenda ressurss**.</span><span class="sxs-lookup"><span data-stu-id="1299d-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="1299d-306">Kui teate ressurssi, mida soovite praeguse ressursi jaoks asendada, valige või tippige nimi ja seejärel valige **Uuesti määramine**.</span><span class="sxs-lookup"><span data-stu-id="1299d-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Asendava ressursi määramine](media/Resource-Management-image51.png)

    <span data-ttu-id="1299d-308">Ressursi otsimiseks tehke ka järgmist.</span><span class="sxs-lookup"><span data-stu-id="1299d-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="1299d-309">Valige **Leia asendus**.</span><span class="sxs-lookup"><span data-stu-id="1299d-309">Select **Find Substitution**.</span></span>

        ![Asendava ressursi otsimine](media/Resource-Management-image52.png)

        <span data-ttu-id="1299d-311">Ajakava abimees tagastab saadaolevate asendajate loendi.</span><span class="sxs-lookup"><span data-stu-id="1299d-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="1299d-312">Ajakava abimehes saate kättesaadavaid ressursse täiendavalt filtreerida sobiva asenduse leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="1299d-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Saadaolevate näidiste loend](media/Resource-Management-image53.png)

    2. <span data-ttu-id="1299d-314">Ressursi asendamiseks valige ressurss, mida te soovite, ja seejärel valige **Asenda**.</span><span class="sxs-lookup"><span data-stu-id="1299d-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Asendusressurss valitud](media/Resource-Management-image54.png)

    <span data-ttu-id="1299d-316">Broneeringud ja määramised asendatakse uue ressursiga.</span><span class="sxs-lookup"><span data-stu-id="1299d-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Broneeringud ja määramised asendatakse uue ressursiga](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="1299d-318">Meeskonnaliikmete broneeringute ja määramiste vastavusse viimine</span><span class="sxs-lookup"><span data-stu-id="1299d-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="1299d-319">Meeskonnaliikmete puhul on broneeringud ja tööülesanded lõdvalt ühendatud.</span><span class="sxs-lookup"><span data-stu-id="1299d-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="1299d-320">Teisisõnu, ressurssidel võivad olla määramised, kuid ei mingeid broneeringuid, või neil võib olla broneeringuid, kuid mitte määramisi.</span><span class="sxs-lookup"><span data-stu-id="1299d-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="1299d-321">Ideaalis tuleks reserveeringud ja ülesanded viia vastavusse, nii et ressursid on toime pannud võimsuse täitmiseks tööülesandeid.</span><span class="sxs-lookup"><span data-stu-id="1299d-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="1299d-322">Kuid broneeringud võivad põhineda saadavusel ja tööülesande ajastused võivad projekti jätkudes muutuda.</span><span class="sxs-lookup"><span data-stu-id="1299d-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="1299d-323">Seega pakub broneeringute ja ülesannete vaba ühendamine paindlikkust.</span><span class="sxs-lookup"><span data-stu-id="1299d-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="1299d-324">PSA-l on vahekaart **Vastavusseviimine**, mis võimaldab projekti juhtidel ühitada meeskonnaliikmete reserveeringud ja nende määramised projekti meeskondadele.</span><span class="sxs-lookup"><span data-stu-id="1299d-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Vahekaart Vastavusseviimine](media/Resource-Management-image56.png)

<span data-ttu-id="1299d-326">Vahekaardil **Vastavusseviimine** on kuvatud reserveeringud ja ülesanded, mis on seotud iga meeskonnaliikme tööülesande määramise tasemega.</span><span class="sxs-lookup"><span data-stu-id="1299d-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="1299d-327">See näitab tunde lahtrites, mis esindavad ajavahemikke kuude ja päevade kaupa.</span><span class="sxs-lookup"><span data-stu-id="1299d-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="1299d-328">Vahekaardil kuvatakse ka projekti üldine neto kogusumma koos veeruga kokku.</span><span class="sxs-lookup"><span data-stu-id="1299d-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="1299d-329">Iga ressursi puhul arvutab vahekaart meeskonnaliikme reserveeringute ja meeskonnaliikme tööülesannete määramise vahe.</span><span class="sxs-lookup"><span data-stu-id="1299d-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="1299d-330">Ideaalis peaks see erinevus olema 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1299d-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="1299d-331">Teisisõnu ei tohiks broneeringute ja ülesannete vahel olla vahet.</span><span class="sxs-lookup"><span data-stu-id="1299d-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="1299d-332">Erinevused on värvitud ja varjutatud, et juhtida tähelepanu kahele tingimusele.</span><span class="sxs-lookup"><span data-stu-id="1299d-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="1299d-333">**Broneeringu puudujääk** – broneeringu puudujääk ilmneb siis, kui ressursil on rohkem määramisi kui broneeringuid.</span><span class="sxs-lookup"><span data-stu-id="1299d-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="1299d-334">Kuna seda võimsust pole reserveeritud, võib projektijuht soovida selle tingimuse parandamist, pikendades ressursi reserveeringud puudujäägi katteks.</span><span class="sxs-lookup"><span data-stu-id="1299d-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="1299d-335">**Liigsed broneeringud** – üleliigsed broneeringud ilmnevad, kui ressurss on projektile broneeritud, kuid seda pole ülesannetele määratud.</span><span class="sxs-lookup"><span data-stu-id="1299d-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="1299d-336">See tingimus võib olla vastuvõetav juhul, kui ressurss oli projektile broneeritud enne tööülesande määramise toimumist.</span><span class="sxs-lookup"><span data-stu-id="1299d-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="1299d-337">Kuid teistel juhtudel ressurssi ei kavandata tööülesannetele määrata.</span><span class="sxs-lookup"><span data-stu-id="1299d-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="1299d-338">Sellisel juhul peaks projektijuht kaaluma ressursi broneeringute tühistamist, et võimsust saaks kasutada mõne muu projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="1299d-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="1299d-339">Mõnel juhul, kui te vaatate aega kõrgemal tasemel kui päeva tasemel (näiteks kuu tasand), võidakse kuvada ressursi neto erinevus (teisisõnu, broneerimine = määramine).</span><span class="sxs-lookup"><span data-stu-id="1299d-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="1299d-340">Kuid kui te vaatate aega nädala tasemel, võite näha, et seal on määramised null tundi ja broneeringud 40 tundi esimesel nädalal, kuid määramine 40 tundi ja broneerimine null tundi teisel nädalal.</span><span class="sxs-lookup"><span data-stu-id="1299d-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="1299d-341">Kokkuvõttes lepitakse reserveeringud ja määramised kokku, kuid nad erinevad ühe nädala jooksul järgmisena.</span><span class="sxs-lookup"><span data-stu-id="1299d-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="1299d-342">Kui vaatate aega kõrgemal tasemel, on vahekaardil **Vastavusseviimine** määratud lahtrite indikaator, mis teatab, et madalamatel tasanditel on erinevusi.</span><span class="sxs-lookup"><span data-stu-id="1299d-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="1299d-343">Lahtrit topeltklõpsates saate erinevuse vaatamiseks suumida.</span><span class="sxs-lookup"><span data-stu-id="1299d-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="1299d-344">Seejärel saate väljasuumimiseks paremklõpsu teha. Valides ressursi ja kasutades seejärel ruudustiku tööriistaribal juhtelementi **Järgmine erinevus**, saate minna järgmisele erinevusele selle ressursi reserveeringute ja ülesannete vahel.</span><span class="sxs-lookup"><span data-stu-id="1299d-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="1299d-345">Seejärel saate tagasiminemiseks kasutada juhtelementi **Eelmine erinevus**.</span><span class="sxs-lookup"><span data-stu-id="1299d-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="1299d-346">Samuti saate suvandi **Sätted** kaudu erinevuste indikaatori ja navigeerimise käitumise välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="1299d-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Erinevuse indikaator](media/Resource-Management-image57.png)

<span data-ttu-id="1299d-348">Kui teil on ressursi jaoks tööülesanded, kuid ei mingeid broneeringuid,valige lehel **Projektid** vahekaardil **Vastavusseviimine** broneeringu puudujääk, seejärel valige käsk **Pikenda reserveeringut**.</span><span class="sxs-lookup"><span data-stu-id="1299d-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="1299d-349">Kuvatakse dialoogiboks **Pikenda reserveeringut** ja kuvatakse broneering, mis on vajalik ressursi puudujäägi lahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="1299d-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="1299d-350">See näitab ka ressursi olemasolevaid broneeringuid kõigis projektides või muudes kavandatud üksustes.</span><span class="sxs-lookup"><span data-stu-id="1299d-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="1299d-351">Kui valite ressursi reserveeringu loomiseks valiku **OK**, võite selle ressursi saadavusest olenemata põhjustada ülebroneeringu.</span><span class="sxs-lookup"><span data-stu-id="1299d-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialoogiboks Pikenda reserveeringut](media/Resource-Management-image58.png)

<span data-ttu-id="1299d-353">Projektijuht või ressursihaldur saab seejärel kasutada ajakavapaneeli, et hallata mis tahes olukordi, kus ressurss on üle broneeritud.</span><span class="sxs-lookup"><span data-stu-id="1299d-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]