---
title: Juurutamise tüübi määratlemine
description: Selles teemas antakse teavet, et aidata teha kindlaks oma ettevõtte projektitoimingute õige juurutamistüüp.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401213"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="4ba83-103">Juurutamise tüübi määratlemine</span><span class="sxs-lookup"><span data-stu-id="4ba83-103">Determine your deployment type</span></span>

<span data-ttu-id="4ba83-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4ba83-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ba83-105">Pärast litsentsi ostmist alustage siit, et määratleda rakenduse Dynamics 365 Project Operations jaoks parim juurutuse mudel, kasutades [juhendatavat installimisvoogu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="4ba83-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="4ba83-106">Pärast juhendatud installimisvoo lõpetamist suunatakse teid õigesse haldusportaali, et saaksite oma installimise lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="4ba83-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="4ba83-107">Installimise lõpuleviimiseks lugege juurutuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4ba83-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="4ba83-108">Dynamicsi olemasolevad kliendid, kes kasutavad rakendust Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4ba83-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="4ba83-109">Project Operations sisaldab võimalusi, mis tarnitakse koos rakendusega Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4ba83-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="4ba83-110">2021. aasta väljalaske 1. laine klientidele väljastatakse versiooniuuenduse tee.</span><span class="sxs-lookup"><span data-stu-id="4ba83-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="4ba83-111">Rakenduse Dynamics 365 Finance olemasolevad kliendid, kes kasutavad projektihaldust ja raamatupidamist</span><span class="sxs-lookup"><span data-stu-id="4ba83-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="4ba83-112">Rakenduse Finance olemasolevad kliendid, kes kasutavad projektihalduse ja raamatupidamise funktsiooni, saavad jätkata selle endisel kujul kasutamist.</span><span class="sxs-lookup"><span data-stu-id="4ba83-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="4ba83-113">Vaadake teemat [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma).</span><span class="sxs-lookup"><span data-stu-id="4ba83-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="4ba83-114">Juurutustüübid</span><span class="sxs-lookup"><span data-stu-id="4ba83-114">Deployment types</span></span>
<span data-ttu-id="4ba83-115">Project Operations toetab teie vajadustele vastamiseks mitut juurutamise võimalust.</span><span class="sxs-lookup"><span data-stu-id="4ba83-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="4ba83-116">Olenemata sellest, kas olete rakenduse Dynamics 365 uus või juba aktiivne klient, Project Operations saab teie vajadusi toetada.</span><span class="sxs-lookup"><span data-stu-id="4ba83-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="4ba83-117">Meie [juurutuse küsimustik](https://aka.ms/provisionprojectoperations) aitab teil teha kindlaks õige juurutuse.</span><span class="sxs-lookup"><span data-stu-id="4ba83-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="4ba83-118">Tulemused suunavad teid ühe järgmiste juurutustüübi juurde.</span><span class="sxs-lookup"><span data-stu-id="4ba83-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="4ba83-119">Lihtjuurutamine – tehing fiktiivsele arveldusele</span><span class="sxs-lookup"><span data-stu-id="4ba83-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="4ba83-120">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="4ba83-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="4ba83-121">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="4ba83-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="4ba83-122">Project Operations toetab juriidilise olemi tasemel konfguratsioonide kaudu samas keskkonnas ladustatavat/tootmistellimuste stsenaariumeid ja mitteladustatavaid/ressursipõhiseid stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="4ba83-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="4ba83-123">Näiteks saab Contoso kasutada ladustatud/tootmistellimuse võimalusi oma USA tootmisettevõttes (juriidiline olem = Contoso tootmine Ameerika Ühendriikides).</span><span class="sxs-lookup"><span data-stu-id="4ba83-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="4ba83-124">Contoso saab kasutada ladustatud/tootmistellimuse võimalusi oma Contoso robotõlgade hooldamise asutuses Ühendkuningriigis (juriidiline olem = Contoso robootika Ühendkuningriigis).</span><span class="sxs-lookup"><span data-stu-id="4ba83-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="4ba83-125">Lihtjuurutamine – tehing näidisarveldusele</span><span class="sxs-lookup"><span data-stu-id="4ba83-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="4ba83-126">Lite’i juurutus sisaldab järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="4ba83-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="4ba83-127">Rakenduse Dynamics 365 Sales kogemusi ületavate projektide müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="4ba83-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="4ba83-128">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="4ba83-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="4ba83-129">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="4ba83-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="4ba83-130">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="4ba83-130">Unified resource management</span></span>
- <span data-ttu-id="4ba83-131">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="4ba83-131">Time tracking</span></span>
- <span data-ttu-id="4ba83-132">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="4ba83-132">Basic expense</span></span>
- <span data-ttu-id="4ba83-133">Näidisarvedamine ja ja kliendile suunatud arveldamine</span><span class="sxs-lookup"><span data-stu-id="4ba83-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="4ba83-134">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="4ba83-134">Deployment steps</span></span>
<span data-ttu-id="4ba83-135">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="4ba83-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4ba83-136">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](lite-preview-subscription-sign-up.md) ja [Uue keskkonna ettevalmistamine](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="4ba83-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="4ba83-137">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="4ba83-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="4ba83-138">Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks hõlmavad järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="4ba83-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="4ba83-139">Rakenduse Dynamics 365 Sales ületavate projektide müügiprotsess</span><span class="sxs-lookup"><span data-stu-id="4ba83-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="4ba83-140">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="4ba83-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="4ba83-141">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="4ba83-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="4ba83-142">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="4ba83-142">Unified resource management</span></span>
- <span data-ttu-id="4ba83-143">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="4ba83-143">Time tracking</span></span>
- <span data-ttu-id="4ba83-144">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="4ba83-144">Basic expense</span></span>
- <span data-ttu-id="4ba83-145">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="4ba83-145">Full expense</span></span>
- <span data-ttu-id="4ba83-146">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="4ba83-146">Receipt OCR</span></span>
- <span data-ttu-id="4ba83-147">Näidisarvedamine ja ja kliendile suunatud arveldamine</span><span class="sxs-lookup"><span data-stu-id="4ba83-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="4ba83-148">Projektide tulude kajastamine</span><span class="sxs-lookup"><span data-stu-id="4ba83-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4ba83-149">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="4ba83-149">Deployment steps</span></span>
<span data-ttu-id="4ba83-150">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="4ba83-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4ba83-151">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](resource-sign-up-preview-subscription.md) ja [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4ba83-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="4ba83-152">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="4ba83-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="4ba83-153">Projekti kavandamise WBS-i kasutades</span><span class="sxs-lookup"><span data-stu-id="4ba83-153">Project planning using WBS</span></span>
- <span data-ttu-id="4ba83-154">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="4ba83-154">Resource Management</span></span>
- <span data-ttu-id="4ba83-155">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="4ba83-155">Time Tracking</span></span>
- <span data-ttu-id="4ba83-156">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="4ba83-156">Full Expense</span></span>
- <span data-ttu-id="4ba83-157">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="4ba83-157">Receipt OCR</span></span>
- <span data-ttu-id="4ba83-158">Täisarveldus</span><span class="sxs-lookup"><span data-stu-id="4ba83-158">Full Invoicing</span></span>
- <span data-ttu-id="4ba83-159">Tulu kajastamine</span><span class="sxs-lookup"><span data-stu-id="4ba83-159">Revenue Recognition</span></span>
- <span data-ttu-id="4ba83-160">Tootmistellimused</span><span class="sxs-lookup"><span data-stu-id="4ba83-160">Production Orders</span></span>
- <span data-ttu-id="4ba83-161">Materjalide tugi</span><span class="sxs-lookup"><span data-stu-id="4ba83-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="4ba83-162">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="4ba83-162">Deployment steps</span></span>
<span data-ttu-id="4ba83-163">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="4ba83-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="4ba83-164">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uue keskkonna ettevalmistamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="4ba83-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

