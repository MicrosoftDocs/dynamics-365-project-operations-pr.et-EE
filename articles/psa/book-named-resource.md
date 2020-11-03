---
title: Broneeri nimega ressursid ressursinõuetest
description: Selles teemas antakse teavet üldise ressursi nõudega seotud nimega ressursside broneerimise kohta.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075161"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="90412-103">Broneeri nimega ressursid ressursinõuetest</span><span class="sxs-lookup"><span data-stu-id="90412-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90412-104">Nimega ressursi saate broneerida ressursi nõutava üldressursi asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="90412-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="90412-105">Klõpsake rakenduses Project Service Automation (PSA) lehel **Projektid** vahekaarti **Meeskond**.</span><span class="sxs-lookup"><span data-stu-id="90412-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="90412-106">Valige loendist ressursinõudega üldine ressurss ja klõpsake seejärel suvandit **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="90412-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="90412-107">Või avage ressursinõue ja seejärel klõpsake suvandit **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="90412-107">Or, open the resource requirement and then click **Book**.</span></span>


![Üldise meeskonnaliikme broneerimine](media/RM-how-to-14.png)


3. <span data-ttu-id="90412-109">Valige lehel **Ajastamise abimees** nimega ressurss, mille soovite oma projekti meeskonnale broneerida, seejärel klõpsake suvandit **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="90412-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Üldise meeskonnaliikme broneerimine ajastamise abimehe abil](media/RM-how-to-15.png)

<span data-ttu-id="90412-111">Kui broneering on valmis ja täidetud nimega ressursi poolt, asendatakse üldine ressurss nimega ressurss.</span><span class="sxs-lookup"><span data-stu-id="90412-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Nimega meeskonnaliikme, kes asendab üldise meeskonnaliikme](media/RM-how-to-16.png)

<span data-ttu-id="90412-113">Ajakavas olevad määrangud värskendatakse ka nimega ressursiga.</span><span class="sxs-lookup"><span data-stu-id="90412-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Projekti tööülesannetele määratud nimega meeskonnaliige](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="90412-115">Üldise ressursi täitmine mitme nimega ressurssidega</span><span class="sxs-lookup"><span data-stu-id="90412-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="90412-116">Mitme nimega ressurssi sisaldava üldressursi nõude täitmine on sarnane ühe nimega ressursi määramisega.</span><span class="sxs-lookup"><span data-stu-id="90412-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="90412-117">Näiteks on tööülesanne kestusega viis päeva ja 120 tundi pingutust.</span><span class="sxs-lookup"><span data-stu-id="90412-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="90412-118">Seda tööülesannet ei saa lõpule viia üks ressurss, mis töötab viis päeva nädalas tüüpilise 8-tunnise päevaga.</span><span class="sxs-lookup"><span data-stu-id="90412-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Toiming, mis vajab 5 päeva jooksul 120 tundi pingutust](media/RM-how-to-21.png)

<span data-ttu-id="90412-120">Nõue on 120 tundi robootika inseneri üle viie päeva, mis on 24 tundi päevas.</span><span class="sxs-lookup"><span data-stu-id="90412-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Päevane nõue](media/RM-how-to-22.png)

<span data-ttu-id="90412-122">See on näide sellest, kui üldiste ressursside taotluse täitmiseks on vaja mitut nimega ressurssi.</span><span class="sxs-lookup"><span data-stu-id="90412-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="90412-123">Nõude täitmiseks on vaja broneerida mitu ressurssi.</span><span class="sxs-lookup"><span data-stu-id="90412-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Mitme ressursi broneerimine nõude täitmiseks](media/RM-how-to-23.png)

<span data-ttu-id="90412-125">Peamine erinevus selle stsenaariumi puhul seisneb selles, et üldine ressurss jääb tööülesandele määratud meeskonnale ja broneeritud nimega ressursi meeskonnaliikmeid ei määrata positsiooni osana.</span><span class="sxs-lookup"><span data-stu-id="90412-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="90412-126">Projektijuht saab määrata tööd vastavalt vajadusele nimega ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="90412-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="90412-127">Vaade **Sobitamine** võib aidata projektijuhti broneeringute jaotamisel üle mitmete ressursside vahel määrangute tegemisel.</span><span class="sxs-lookup"><span data-stu-id="90412-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="90412-128">Seda ei tehta automaatselt, kuna mis tahes stsenaariumi korral, mis on keerulisem kui ülaltoodud lihtne näide, näiteks juhul, kui teil on nõude komplekt ülesandeid, peab süsteem eeldama, kuidas projektijuht soovib seda määrata.</span><span class="sxs-lookup"><span data-stu-id="90412-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="90412-129">Kuna süsteem ei saa kavatsusest aru, on võimalik, et eeldused on teistsugused kui ette nähtud ja juhtub vale või ettearvamatu tulemus.</span><span class="sxs-lookup"><span data-stu-id="90412-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="90412-130">Prognoositav tulemus on, et üldine ressurss jääb alles, kuni projektijuht tahtlikult vaate **Sobitamine** abil määrangu loob.</span><span class="sxs-lookup"><span data-stu-id="90412-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


