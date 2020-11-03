---
title: Juurutamise tüübi määratlemine
description: Selles teemas antakse teavet, et aidata teha kindlaks oma ettevõtte projektitoimingute õige juurutamistüüp.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074960"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="6aa8a-103">Juurutamise tüübi määratlemine</span><span class="sxs-lookup"><span data-stu-id="6aa8a-103">Determine your deployment type</span></span>

<span data-ttu-id="6aa8a-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="6aa8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6aa8a-105">Pärast litsentsi ostmist alustage siit, et määratleda rakenduse Dynamics 365 Project Operations jaoks parim juurutuse mudel, kasutades [juhendatavat installimisvoogu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6aa8a-106">Pärast juhendatud installimisvoo lõpetamist suunatakse teid õigesse haldusportaali, et saaksite oma installimise lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6aa8a-107">Installimise lõpuleviimiseks lugege juurutuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6aa8a-108">Dynamicsi olemasolevad kliendid, kes kasutavad rakendust Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6aa8a-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6aa8a-109">Project Operations sisaldab võimalusi, mis tarnitakse koos rakendusega Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6aa8a-110">Tulevikus antakse nendele klientidele välja versiooniuuenduse tee.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6aa8a-111">Rakenduse Dynamics 365 Finance olemasolevad kliendid, kes kasutavad projektihaldust ja raamatupidamist</span><span class="sxs-lookup"><span data-stu-id="6aa8a-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6aa8a-112">Rakenduse Finance olemasolevad kliendid, kes kasutavad projektihalduse ja raamatupidamise funktsiooni, saavad jätkata selle kasutamist samal kujul.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="6aa8a-113">Vaadake teemat [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="6aa8a-114">Juurutustüübid</span><span class="sxs-lookup"><span data-stu-id="6aa8a-114">Deployment types</span></span>
<span data-ttu-id="6aa8a-115">Project Operations toetab teie vajadustele vastamiseks mitut juurutamise võimalust.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6aa8a-116">Olenemata sellest, kas olete rakenduse Dynamics 365 uus või juba aktiivne klient, Project Operations saab teie vajadusi toetada.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6aa8a-117">Meie [juurutuse küsimustik](https://aka.ms/provisionprojectoperations) aitab teil teha kindlaks õige juurutuse.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6aa8a-118">Tulemused suunavad teid ühe järgmiste juurutustüübi juurde.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6aa8a-119">Lihtjuurutamine – tehing fiktiivsele arveldusele</span><span class="sxs-lookup"><span data-stu-id="6aa8a-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6aa8a-120">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="6aa8a-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6aa8a-121">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="6aa8a-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6aa8a-122">Project Operations toetab juriidilise olemi tasemel konfguratsioonide kaudu samas keskkonnas ladustatavat/tootmistellimuste stsenaariumeid ja mitteladustatavaid/ressursipõhiseid stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6aa8a-123">Näiteks saab Contoso kasutada ladustatud/tootmistellimuse võimalusi oma USA tootmisettevõttes (juriidiline olem = Contoso tootmine Ameerika Ühendriikides).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="6aa8a-124">Contoso saab kasutada ladustatud/tootmistellimuse võimalusi oma Contoso robotõlgade hooldamise asutuses Ühendkuningriigis (juriidiline olem = Contoso robootika Ühendkuningriigis).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="6aa8a-125">Lihtjuurutamine – tehing näidisarveldusele</span><span class="sxs-lookup"><span data-stu-id="6aa8a-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="6aa8a-126">Lite’i juurutus sisaldab järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6aa8a-127">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="6aa8a-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6aa8a-128">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6aa8a-129">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-129">Unified Resource Management</span></span>
- <span data-ttu-id="6aa8a-130">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="6aa8a-130">Time Tracking</span></span>
- <span data-ttu-id="6aa8a-131">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="6aa8a-131">Basic Expense</span></span>
- <span data-ttu-id="6aa8a-132">Arvesoovitus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6aa8a-133">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="6aa8a-133">Deployment steps</span></span>
<span data-ttu-id="6aa8a-134">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6aa8a-135">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](lite-preview-subscription-sign-up.md) ja [Uue keskkonna ettevalmistamine](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="6aa8a-136">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="6aa8a-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6aa8a-137">Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks hõlmavad järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6aa8a-138">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="6aa8a-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6aa8a-139">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6aa8a-140">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-140">Unified Resource Management</span></span>
- <span data-ttu-id="6aa8a-141">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="6aa8a-141">Time Tracking</span></span>
- <span data-ttu-id="6aa8a-142">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="6aa8a-142">Basic Expense</span></span>
- <span data-ttu-id="6aa8a-143">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="6aa8a-143">Full Expense</span></span>
- <span data-ttu-id="6aa8a-144">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="6aa8a-144">Receipt OCR</span></span>
- <span data-ttu-id="6aa8a-145">Täisarveldus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-145">Full Invoicing</span></span>
- <span data-ttu-id="6aa8a-146">Tulu kajastamine</span><span class="sxs-lookup"><span data-stu-id="6aa8a-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6aa8a-147">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="6aa8a-147">Deployment steps</span></span>
<span data-ttu-id="6aa8a-148">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6aa8a-149">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](resource-sign-up-preview-subscription.md) ja [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6aa8a-150">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="6aa8a-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6aa8a-151">Projekti kavandamise WBS-i kasutades</span><span class="sxs-lookup"><span data-stu-id="6aa8a-151">Project planning using WBS</span></span>
- <span data-ttu-id="6aa8a-152">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-152">Resource Management</span></span>
- <span data-ttu-id="6aa8a-153">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="6aa8a-153">Time Tracking</span></span>
- <span data-ttu-id="6aa8a-154">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="6aa8a-154">Full Expense</span></span>
- <span data-ttu-id="6aa8a-155">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="6aa8a-155">Receipt OCR</span></span>
- <span data-ttu-id="6aa8a-156">Täisarveldus</span><span class="sxs-lookup"><span data-stu-id="6aa8a-156">Full Invoicing</span></span>
- <span data-ttu-id="6aa8a-157">Tulu kajastamine</span><span class="sxs-lookup"><span data-stu-id="6aa8a-157">Revenue Recognition</span></span>
- <span data-ttu-id="6aa8a-158">Tootmistellimused</span><span class="sxs-lookup"><span data-stu-id="6aa8a-158">Production Orders</span></span>
- <span data-ttu-id="6aa8a-159">Materjalide tugi</span><span class="sxs-lookup"><span data-stu-id="6aa8a-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6aa8a-160">Juurutamise sammud</span><span class="sxs-lookup"><span data-stu-id="6aa8a-160">Deployment steps</span></span>
<span data-ttu-id="6aa8a-161">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="6aa8a-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6aa8a-162">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uue keskkonna ettevalmistamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6aa8a-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

