---
title: Üldine ressursinõude täitmine
description: Selles teemas antakse teavet üldise ressursi nõudega seotud nimega ressursside broneerimise kohta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279583"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="7defb-103">Üldine ressursinõude täitmine</span><span class="sxs-lookup"><span data-stu-id="7defb-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="7defb-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="7defb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7defb-105">Nimega ressursi saate broneerida ressursi nõutava üldressursi asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="7defb-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="7defb-106">Lehel **Projektid** valige vahekaart **Meeskond**.</span><span class="sxs-lookup"><span data-stu-id="7defb-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="7defb-107">Valige loendist pärineva ressursinõudega üldine ressurss ja valige seejärel **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="7defb-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="7defb-108">Või avage ressursinõue ja valige seejärel **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="7defb-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="7defb-109">Valige lehel **Ajakava abimees** nimega ressurss, mille soovite oma projekti meeskonnale broneerida, seejärel klõpsake suvandit **Broneeri**.</span><span class="sxs-lookup"><span data-stu-id="7defb-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="7defb-110">Kui broneering on valmis ja täidetud nimega ressursi poolt, asendatakse üldine ressurss nimega ressurss.</span><span class="sxs-lookup"><span data-stu-id="7defb-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="7defb-111">Ajakavas olevad määrangud värskendatakse ka nimega ressursiga.</span><span class="sxs-lookup"><span data-stu-id="7defb-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="7defb-112">Üldise ressursi täitmine mitme nimega ressurssidega</span><span class="sxs-lookup"><span data-stu-id="7defb-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="7defb-113">Mitme nimega ressurssi sisaldava üldressursi nõude täitmine on sarnane ühe nimega ressursi määramisega.</span><span class="sxs-lookup"><span data-stu-id="7defb-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="7defb-114">Näiteks on tööülesanne kestusega viis päeva ja 120 tundi pingutust.</span><span class="sxs-lookup"><span data-stu-id="7defb-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="7defb-115">Seda tööülesannet ei saa lõpule viia üks ressurss, mis töötab viis päeva nädalas ja tavaliselt kaheksa tundi päevas.</span><span class="sxs-lookup"><span data-stu-id="7defb-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="7defb-116">Nõue on 120 tundi robootika inseneri üle viie päeva, mis on 24 tundi päevas.</span><span class="sxs-lookup"><span data-stu-id="7defb-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="7defb-117">See on näide sellest, kui üldiste ressursside taotluse täitmiseks on vaja mitut nimega ressurssi.</span><span class="sxs-lookup"><span data-stu-id="7defb-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="7defb-118">Nõude täitmiseks on vaja broneerida mitu ressurssi.</span><span class="sxs-lookup"><span data-stu-id="7defb-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="7defb-119">Peamine erinevus selle stsenaariumi puhul seisneb selles, et üldine ressurss jääb tööülesandele määratud meeskonnale ja broneeritud nimega ressursi meeskonnaliikmeid ei määrata positsiooni osana.</span><span class="sxs-lookup"><span data-stu-id="7defb-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="7defb-120">Projektijuht saab määrata tööd vastavalt vajadusele nimega ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="7defb-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="7defb-121">Vaade **Sobitamine** võib aidata projektijuhti broneeringute jaotamisel üle mitmete ressursside vahel määrangute tegemisel.</span><span class="sxs-lookup"><span data-stu-id="7defb-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="7defb-122">Seda ei tehta automaatselt, kuna mis tahes stsenaariumi korral, mis on keerulisem kui ülaltoodud lihtne näide, näiteks juhul, kui teil on nõude komplekt ülesandeid või peab süsteem eeldama, kuidas projektijuht soovib seda määrata.</span><span class="sxs-lookup"><span data-stu-id="7defb-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="7defb-123">Kuna aga süsteem ei saa kavatsusest aru, siis need eeldused suure tõenäosusega erinevad sellest, mida tegelikult teha sooviti, ning seetõttu kuvatakse vale ja ettearvamatu tulemus.</span><span class="sxs-lookup"><span data-stu-id="7defb-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="7defb-124">Prognoositav tulemus on, et üldine ressurss jääb alles, kuni projektijuht tahtlikult vaate **Sobitamine** abil määrangu loob.</span><span class="sxs-lookup"><span data-stu-id="7defb-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]