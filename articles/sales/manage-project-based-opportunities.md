---
title: Projektipõhiste müügivõimaluste haldamine
description: Selles teemas antakse teave projektidega seotud müügivõimalustega töötamise kohta.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d1f9b29e0e9516ff78517e47694a2385c083ec7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277828"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="d4b41-103">Projektipõhiste müügivõimaluste haldamine</span><span class="sxs-lookup"><span data-stu-id="d4b41-103">Manage project-based opportunities</span></span>

<span data-ttu-id="d4b41-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="d4b41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4b41-105">Projektipõhiste ettevõtetel on tarne toimingud tavaliselt hajutatud mitmesse riiki ja geograafilisse piirkonda.</span><span class="sxs-lookup"><span data-stu-id="d4b41-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="d4b41-106">Projekti täitmise ja tarnimise kulu võib varieeruda vastavalt sellele, milline geograafiline piirkond või allüksustel tarnet haldab.</span><span class="sxs-lookup"><span data-stu-id="d4b41-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="d4b41-107">See võib omakorda mõjutada tehingu marginaale.</span><span class="sxs-lookup"><span data-stu-id="d4b41-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="d4b41-108">Projektipõhiste teenuste tarne tähendab tavaliselt suurt hulka inimressursi aega, märkimisväärseid kulusid reisidele, materiaalseid kulusid ja muid kulusid.</span><span class="sxs-lookup"><span data-stu-id="d4b41-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="d4b41-109">Projektipõhised müügivõimalused rakenduses Dynamics 365 Project Operations on kujundatud laiendustega rakendusele Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d4b41-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="d4b41-110">Teemas antakse teavet erinevate väljade ja äriloogikate kohta, mis sisaldub täiendavas funktsionaalsuses, mida projektipõhised ettevõtted vajavad projektipõhiste müügivõimaluste haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="d4b41-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="d4b41-111">Kõigi projektipõhiste müügivõimaluste vaatamine</span><span class="sxs-lookup"><span data-stu-id="d4b41-111">View all project-based opportunities</span></span>

<span data-ttu-id="d4b41-112">Kõigi projektipõhiste müügivõimaluste loend kuvatakse lehel **Müügivõimalused**.</span><span class="sxs-lookup"><span data-stu-id="d4b41-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="d4b41-113">Minge jaotisse **Müük** > **Müügivõimalused**.</span><span class="sxs-lookup"><span data-stu-id="d4b41-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="d4b41-114">Kasutage suvandit **Vaate vahetaja**, et valida müügivõimaluste jaoks teine filtreeritud vaade.</span><span class="sxs-lookup"><span data-stu-id="d4b41-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="d4b41-115">Nende vaadete ja navigeerimisvalikute konfigureerimiseks saate luua oma vaated kohandatud filtrikriteeriumidega.</span><span class="sxs-lookup"><span data-stu-id="d4b41-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="d4b41-116">Projekti müügivõimalusi saab luua või kustutada selle loendi lehelt või üksikasjade lehelt.</span><span class="sxs-lookup"><span data-stu-id="d4b41-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="d4b41-117">Projektipõhiste tehingute äriprotsessi voog</span><span class="sxs-lookup"><span data-stu-id="d4b41-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="d4b41-118">Project Operationsi projektipõhistes tehingutes toetatakse järgmisi äriprotsessi voogusid.</span><span class="sxs-lookup"><span data-stu-id="d4b41-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="d4b41-119">Müügivihjest müügivõimaluseni äriprotsess</span><span class="sxs-lookup"><span data-stu-id="d4b41-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="d4b41-120">Müügivõimaluse müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="d4b41-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="d4b41-121">Müügivihjest müügivõimaluseni äriprotsess</span><span class="sxs-lookup"><span data-stu-id="d4b41-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="d4b41-122">Müügivihjest müügivõimaluseni äriprotsess toetab järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="d4b41-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="d4b41-123">Etapp</span><span class="sxs-lookup"><span data-stu-id="d4b41-123">Stage</span></span> | <span data-ttu-id="d4b41-124">Vastendatud olem</span><span class="sxs-lookup"><span data-stu-id="d4b41-124">Mapped entity</span></span> | <span data-ttu-id="d4b41-125">Funktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="d4b41-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d4b41-126">Sobivaks kinnitamine</span><span class="sxs-lookup"><span data-stu-id="d4b41-126">Qualify</span></span> | <span data-ttu-id="d4b41-127">Müügivihje</span><span class="sxs-lookup"><span data-stu-id="d4b41-127">Lead</span></span> | <span data-ttu-id="d4b41-128">Konto, kontakti ja müügivõimaluse loomiseks müügivihje kvalifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="d4b41-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="d4b41-129">Arendage</span><span class="sxs-lookup"><span data-stu-id="d4b41-129">Develop</span></span> | <span data-ttu-id="d4b41-130">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="d4b41-130">Opportunity</span></span> | <span data-ttu-id="d4b41-131">Müügivõimaluse arendamine, et lisada lisateavet seotud töö, peamiste sidusrühmade ja konkurentide kohta.</span><span class="sxs-lookup"><span data-stu-id="d4b41-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="d4b41-132">Soovita</span><span class="sxs-lookup"><span data-stu-id="d4b41-132">Propose</span></span> | <span data-ttu-id="d4b41-133">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="d4b41-133">Opportunity</span></span> | <span data-ttu-id="d4b41-134">Ettepaneku väljaarendamine ja sisemise läbivaatuse meeskonnalt heakskiidu saamine.</span><span class="sxs-lookup"><span data-stu-id="d4b41-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="d4b41-135">Saate dialoogiakna sulgeda</span><span class="sxs-lookup"><span data-stu-id="d4b41-135">Close</span></span> | <span data-ttu-id="d4b41-136">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="d4b41-136">Opportunity</span></span> | <span data-ttu-id="d4b41-137">Tehingu sulgemiseks müügivõimaluse võitmine.</span><span class="sxs-lookup"><span data-stu-id="d4b41-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="d4b41-138">Müügivõimaluse müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="d4b41-138">Opportunity sales process</span></span>
<span data-ttu-id="d4b41-139">Project Operationsi müügivõimaluse müügiprotsess on müügivõimaluse müügiprotsessi ärivoo laiendus rakenduses Sales.</span><span class="sxs-lookup"><span data-stu-id="d4b41-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="d4b41-140">See äriprotsess on loodud valmislahendusena, et toetada projektipõhise müügivõimaluse järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="d4b41-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="d4b41-141">Etapp</span><span class="sxs-lookup"><span data-stu-id="d4b41-141">Stage</span></span> | <span data-ttu-id="d4b41-142">Vastendatud olem</span><span class="sxs-lookup"><span data-stu-id="d4b41-142">Mapped entity</span></span> | <span data-ttu-id="d4b41-143">Funktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="d4b41-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d4b41-144">Sobivaks kinnitamine</span><span class="sxs-lookup"><span data-stu-id="d4b41-144">Qualify</span></span> | <span data-ttu-id="d4b41-145">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="d4b41-145">Opportunity</span></span> | <span data-ttu-id="d4b41-146">Konto, kontakti ja müügivõimaluse loomiseks müügivihje kvalifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="d4b41-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="d4b41-147">Soovita</span><span class="sxs-lookup"><span data-stu-id="d4b41-147">Propose</span></span> | <span data-ttu-id="d4b41-148">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="d4b41-148">Quote</span></span> | <span data-ttu-id="d4b41-149">Ettepaneku väljaarendamine projekti hinnapakkumist kasutades ja sisemise läbivaatuse meeskonnalt heakskiidu saamine.</span><span class="sxs-lookup"><span data-stu-id="d4b41-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="d4b41-150">Leping</span><span class="sxs-lookup"><span data-stu-id="d4b41-150">Contract</span></span> | <span data-ttu-id="d4b41-151">Projekti leping</span><span class="sxs-lookup"><span data-stu-id="d4b41-151">Project Contract</span></span> | <span data-ttu-id="d4b41-152">Hinnapakkumise võitmiseks looge leping ja alustage projekti täitmist ja tarnimist.</span><span class="sxs-lookup"><span data-stu-id="d4b41-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="d4b41-153">Saate dialoogiakna sulgeda</span><span class="sxs-lookup"><span data-stu-id="d4b41-153">Close</span></span> | <span data-ttu-id="d4b41-154">Projekti leping</span><span class="sxs-lookup"><span data-stu-id="d4b41-154">Project Contract</span></span> | <span data-ttu-id="d4b41-155">Lõpetage töö edukalt ja sulgege projekti leping.</span><span class="sxs-lookup"><span data-stu-id="d4b41-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="d4b41-156">Kui teie projektipõhine tehing algas müügivihjega, on müügivihjest müügivõimaluseks äriprotsess tähtsam.</span><span class="sxs-lookup"><span data-stu-id="d4b41-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="d4b41-157">Kui teie projektipõhine tehing algas müügivõimalusega, on müügivõimaluse müügiprotsess tähtsam.</span><span class="sxs-lookup"><span data-stu-id="d4b41-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="d4b41-158">Saate toote äriprotsessi voog redigeerida või luua oma äriprotsessi voogusid, et vajaduse kohaselt müügiprotsessi jälgida.</span><span class="sxs-lookup"><span data-stu-id="d4b41-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="d4b41-159">Lisateavet äriprotsessi voo kohta leiate jaotisest [Äriprotsessi voogude ülevaade](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="d4b41-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]