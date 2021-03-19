---
title: Ressursikalendrite määratlemine
description: Selles teemas kirjeldatakse, kuidas määratleda rakenduses Project Operations ressusrsside tööajakalendrid.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279808"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="5aeb5-103">Ressursikalendrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="5aeb5-103">Define resource calendars</span></span>

<span data-ttu-id="5aeb5-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="5aeb5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5aeb5-105">Igal projektiga töötaval ressursil peab olema tööajakalender, et määratleda oma kättesaadavus.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="5aeb5-106">Ressursi tööaega saab määratleda kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="5aeb5-107">Ressursi jaoks üksikute kalendri reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="5aeb5-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="5aeb5-108">Ressursi jaoks olemasoleva kalendrimalli rakendamine</span><span class="sxs-lookup"><span data-stu-id="5aeb5-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="5aeb5-109">Ressursi tööajaga määratlemine</span><span class="sxs-lookup"><span data-stu-id="5aeb5-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="5aeb5-110">Valige menüüs **Ressursid** suvand **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5aeb5-111">Valige ruudustiku vaates vastav **Broneeritav ressurss**.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="5aeb5-112">Lehel **Ressursi üksikasjad** valige vahekaart **Tööaeg**. Vaikimisi läheb broneeritava ressursi kalender vaikimisi tööajamalli tööajale, mis on organisatsiooni jaoks määratletud.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="5aeb5-113">Tööaja uuendamiseks paremklõpsake määratletava esitatud kalendri reegli alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="5aeb5-114">Kasutage kalendri reegli menüüd, et määratleda kalendri reegel konkreetse päeva, ülejäänud seeria või kogu kalendri jaoks.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="5aeb5-115">Pärast suvandi valimist saate määratleda järgmist.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="5aeb5-116">Nädalapäev, millele tööaega rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="5aeb5-117">Tööaeg iga päeva jaoks.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-117">The working times within each day.</span></span>
    - <span data-ttu-id="5aeb5-118">Kalendrireegli ajavöönd.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="5aeb5-119">Vajaduse korral saab reegli jaoks määrata ka mitte-tööaja.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="5aeb5-120">Ressursile kalendri malli rakendamine</span><span class="sxs-lookup"><span data-stu-id="5aeb5-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="5aeb5-121">Valige menüüs **Ressursid** suvand **Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5aeb5-122">Valige ruudustiku vaatest värskendamiseks kuni 25 **Broneeritavat ressurssi**.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="5aeb5-123">Valige suvand **Määra kalender** ja kuvatakse dialoog saadaolevate tööajamallide loendiga.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="5aeb5-124">Valige mall, mida soovite kasutada, ja valige seejärel **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="5aeb5-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]