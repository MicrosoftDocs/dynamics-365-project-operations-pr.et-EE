---
title: Juurutamise tüübi määratlemine
description: Selles teemas antakse teavet, et aidata teha kindlaks oma ettevõtte projektitoimingute õige juurutamistüüp.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 715b117cae5418fc743ea870772278450fff5ae9
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663589"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="8cf3e-103">Juurutamise tüübi määratlemine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-103">Determine your deployment type</span></span>

<span data-ttu-id="8cf3e-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cf3e-105">Pärast litsentsi ostmist alustage siit, et määrata parim Dynamics 365 Project Operationsi juurutamise mudel kasutades [Juhendatud paigalduse voogu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="8cf3e-106">Pärast juhendatud installimisvoo lõpetamist suunatakse teid õigesse haldusportaali, et saaksite oma installimise lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="8cf3e-107">Installimise lõpuleviimiseks lugege juurutuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="8cf3e-108">Dynamicsi olemasolevad kliendid, kes kasutavad rakendust Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8cf3e-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="8cf3e-109">Project Operations sisaldab võimalusi, mis tarnitakse koos rakendusega Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="8cf3e-110">2021. aasta väljalaske 1. laine klientidele väljastatakse versiooniuuenduse tee.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="8cf3e-111">Rakenduse Dynamics 365 Finance olemasolevad kliendid, kes kasutavad projektihaldust ja raamatupidamist</span><span class="sxs-lookup"><span data-stu-id="8cf3e-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="8cf3e-112">Rakenduse Finance olemasolevad kliendid, kes kasutavad projektihalduse ja raamatupidamise funktsiooni, saavad jätkata selle endisel kujul kasutamist.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="8cf3e-113">Vaadake teemat [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="8cf3e-114">Juurutamise piirkonnad</span><span class="sxs-lookup"><span data-stu-id="8cf3e-114">Deployment regions</span></span>
<span data-ttu-id="8cf3e-115">Project Operationsi juurutust toetavate piirkondade määratlemiseks vaadake teemat [Dynamics 365-e ja Power Platformi aruande geograafiline kättesaadavus](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="8cf3e-116">Valige **Kuva aruanne** ja laiendage **Dynamics 365 > Operationsi rakendused > Dynamics 365 Project Operations**, et vaadata toetatud piirkondi.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="8cf3e-117">Juurutustüübid</span><span class="sxs-lookup"><span data-stu-id="8cf3e-117">Deployment types</span></span>
<span data-ttu-id="8cf3e-118">Project Operations toetab teie vajadustele vastamiseks mitut juurutamise võimalust.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="8cf3e-119">Olenemata sellest, kas olete rakenduse Dynamics 365 uus või juba aktiivne klient, Project Operations saab teie vajadusi toetada.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="8cf3e-120">Meie [juurutuse küsimustik](https://aka.ms/provisionprojectoperations) aitab teil teha kindlaks õige juurutuse.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="8cf3e-121">Tulemused suunavad teid ühe järgmiste juurutustüübi juurde.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="8cf3e-122">Lihtjuurutamine – tehing fiktiivsele arveldusele</span><span class="sxs-lookup"><span data-stu-id="8cf3e-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="8cf3e-123">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="8cf3e-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="8cf3e-124">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="8cf3e-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="8cf3e-125">Project Operations toetab juriidilise olemi tasemel konfguratsioonide kaudu samas keskkonnas ladustatavat/tootmistellimuste stsenaariumeid ja mitteladustatavaid/ressursipõhiseid stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="8cf3e-126">Näiteks saab Contoso kasutada laopõhiseid/tootmistellimuste võimalusi oma USA tootmisüksuses (juriidiline isik = Contoso Manufacturing, Ameerika Ühendriigid).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="8cf3e-127">Contoso saab kasutada mittelaopõhiseid/ressursipõhiseid võimalusi oma ettevõtte Contoso Robotics Arms teenindusüksuses Ühendkuningriigis (juriidiline isik = Contoso Robotics, Ühendkuningriik).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="8cf3e-128">Lihtjuurutamine – tehing näidisarveldusele</span><span class="sxs-lookup"><span data-stu-id="8cf3e-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="8cf3e-129">Lite’i juurutus sisaldab järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="8cf3e-130">Rakenduse Dynamics 365 Sales kogemusi ületavate projektide müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="8cf3e-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="8cf3e-131">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="8cf3e-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="8cf3e-132">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="8cf3e-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="8cf3e-133">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="8cf3e-133">Unified resource management</span></span>
- <span data-ttu-id="8cf3e-134">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-134">Time tracking</span></span>
- <span data-ttu-id="8cf3e-135">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="8cf3e-135">Basic expense</span></span>
- <span data-ttu-id="8cf3e-136">Näidisarveldus projektijuhi läbivaatuseks ja redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="8cf3e-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="8cf3e-137">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="8cf3e-137">Deployment steps</span></span>
<span data-ttu-id="8cf3e-138">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="8cf3e-139">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](lite-preview-subscription-sign-up.md) ja [Uue keskkonna ettevalmistamine](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="8cf3e-140">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="8cf3e-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="8cf3e-141">Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks hõlmavad järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="8cf3e-142">Rakenduse Dynamics 365 Sales ületavate projektide müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="8cf3e-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="8cf3e-143">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="8cf3e-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="8cf3e-144">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="8cf3e-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="8cf3e-145">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="8cf3e-145">Unified resource management</span></span>
- <span data-ttu-id="8cf3e-146">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-146">Time tracking</span></span>
- <span data-ttu-id="8cf3e-147">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="8cf3e-147">Basic expense</span></span>
- <span data-ttu-id="8cf3e-148">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="8cf3e-148">Full expense</span></span>
- <span data-ttu-id="8cf3e-149">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="8cf3e-149">Receipt OCR</span></span>
- <span data-ttu-id="8cf3e-150">Näidisarvedamine ja ja kliendile suunatud arveldamine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="8cf3e-151">Projektide tulude kajastamine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="8cf3e-152">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="8cf3e-152">Deployment steps</span></span>
<span data-ttu-id="8cf3e-153">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="8cf3e-154">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](resource-sign-up-preview-subscription.md) ja [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="8cf3e-155">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="8cf3e-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="8cf3e-156">Projekti kavandamise WBS-i kasutades</span><span class="sxs-lookup"><span data-stu-id="8cf3e-156">Project planning using WBS</span></span>
- <span data-ttu-id="8cf3e-157">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="8cf3e-157">Resource management</span></span>
- <span data-ttu-id="8cf3e-158">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-158">Time tracking</span></span>
- <span data-ttu-id="8cf3e-159">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="8cf3e-159">Full expense</span></span>
- <span data-ttu-id="8cf3e-160">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="8cf3e-160">Receipt OCR</span></span>
- <span data-ttu-id="8cf3e-161">Täisarveldus</span><span class="sxs-lookup"><span data-stu-id="8cf3e-161">Full invoicing</span></span>
- <span data-ttu-id="8cf3e-162">Tulu kajastamine</span><span class="sxs-lookup"><span data-stu-id="8cf3e-162">Revenue recognition</span></span>
- <span data-ttu-id="8cf3e-163">Tootmistellimused</span><span class="sxs-lookup"><span data-stu-id="8cf3e-163">Production orders</span></span>
- <span data-ttu-id="8cf3e-164">Laopõhiste materjalide tugi koos varudega</span><span class="sxs-lookup"><span data-stu-id="8cf3e-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="8cf3e-165">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="8cf3e-165">Deployment steps</span></span>
<span data-ttu-id="8cf3e-166">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="8cf3e-167">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uue keskkonna ettevalmistamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-167">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
