---
title: Esialgse broneerimise nõuded
description: Selles teemas kirjeldatakse esialgse broneerimise nõudeid.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997911"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="e2277-103">Esialgse broneerimise nõuded</span><span class="sxs-lookup"><span data-stu-id="e2277-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e2277-104">Ressursinõuet saab fikseeritult broneerida.</span><span class="sxs-lookup"><span data-stu-id="e2277-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="e2277-105">Fikseeritud broneering loob pakkumise, mis kasutab ressursi võimsust.</span><span class="sxs-lookup"><span data-stu-id="e2277-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="e2277-106">Seejärel saadetakse pakkumine kinnitamiseks tagasi taotlejale.</span><span class="sxs-lookup"><span data-stu-id="e2277-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="e2277-107">Esialgne broneering lisab ressursi ebalevalt projektimeeskonda ja sellel on ajakavapaneelil teistsugune olek, kuid see ei tarbi ressursi võimsust.</span><span class="sxs-lookup"><span data-stu-id="e2277-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="e2277-108">Ressursi esialgseks broneerimiseks ajakavapaneelilt määrake väli **Broneerimise olek** väärtusele **Esialgne**.</span><span class="sxs-lookup"><span data-stu-id="e2277-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Broneeringu olekuks on määratud Esialgne](media/Resource-Management-image77.png)

<span data-ttu-id="e2277-110">Kui vahekaart **Meeskond** on vaates **Nimega meeskonnaliikmed**, kuvatakse ressurss seal.</span><span class="sxs-lookup"><span data-stu-id="e2277-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="e2277-111">Esialgselt broneeritud tunnid esitatakse veerus **Esialgselt broneeritud tunnid**.</span><span class="sxs-lookup"><span data-stu-id="e2277-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Esialgselt broneeritud tunnid nimega meeskonnaliikmete vaates](media/Resource-Management-image78.png)

<span data-ttu-id="e2277-113">Esialgselt broneeritud meeskonnaliikmeid saab määrata ülesannetele.</span><span class="sxs-lookup"><span data-stu-id="e2277-113">Soft-booked team members can be assigned to tasks.</span></span>

![Ülesandele määratud esialgselt broneeritud meeskonnaliige](media/Resource-Management-image79.png)

<span data-ttu-id="e2277-115">Vahekaardil **Vastavusseviimine** ei kuvata esialgselt broneeritud ressursile ühtegi broneeringut, kuna vahekaart **Vastavusseviimine** arvestab ainult fikseeritud broneeringutega.</span><span class="sxs-lookup"><span data-stu-id="e2277-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Broneeringuteta esialgselt broneeritud ressurss vahekaardil Vastavusseviimine](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="e2277-117">Te ei saa ressurssi esialgselt broneerida nõudest, mis loodi üldisest meeskonnaliikmest.</span><span class="sxs-lookup"><span data-stu-id="e2277-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="e2277-118">Ressursi esialgse broneerimise jaoks kasutatakse ajakavapaneelil erinevat värvi.</span><span class="sxs-lookup"><span data-stu-id="e2277-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Esialgsed broneeringud ajakavapaneelil](media/Resource-Management-image81.png)

<span data-ttu-id="e2277-120">Esialgse broneeringu teisendamiseks fikseeritud broneeringuks paremklõpsake ajakavapaneelil esialgset broneeringut ja seejärel tehke valikud **Muuda olekut** \> **Fikseeritud broneering** \> **Fikseeritud**.</span><span class="sxs-lookup"><span data-stu-id="e2277-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Broneeringu oleku muutmine fikseerituks](media/Resource-Management-image82.png)

<span data-ttu-id="e2277-122">Broneeringut muudetakse ja olekut muudetakse ajakavapaneelil.</span><span class="sxs-lookup"><span data-stu-id="e2277-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="e2277-123">Kuna broneeringu olekuks on nüüd **Fikseeritud**, kuvatakse ressurss broneerituna ja selle võimsust ning saadavust reguleeritakse.</span><span class="sxs-lookup"><span data-stu-id="e2277-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="e2277-124">Sama meetodit saate kasutada ka fikseeritud või esialgse broneeringu ajakavapaneelilt tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="e2277-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="e2277-125">Esialgselt broneeritud ressursi teisendamiseks fikseeritud broneeringuks projekti vahekaardil **Meeskond**, valige ressurss ja seejärel tehke valik **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="e2277-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Käsk Kinnita](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]