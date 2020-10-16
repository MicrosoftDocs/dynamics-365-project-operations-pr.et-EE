---
title: Juurutustüübid
description: Selles teemas antakse teavet, et aidata teha kindlaks oma ettevõtte projektitoimingute õige juurutamistüüp.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948828"
---
# <a name="deployment-types"></a><span data-ttu-id="a279c-103">Juurutustüübid</span><span class="sxs-lookup"><span data-stu-id="a279c-103">Deployment types</span></span>

<span data-ttu-id="a279c-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="a279c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a279c-105">Pärast litsentsi ostmist alustage siit, et määratleda rakenduse Dynamics 365 Project Operations jaoks parim juurutuse mudel, kasutades [juhendatavat installimisvoogu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a279c-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="a279c-106">Pärast juhendatud installimisvoo lõpetamist suunatakse teid õigesse haldusportaali, et saaksite oma installimise lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="a279c-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="a279c-107">Installimise lõpuleviimiseks lugege allolevaid juurutuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a279c-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="a279c-108">Dynamicsi olemasolevad kliendid, kes kasutavad rakendust Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a279c-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="a279c-109">Project Operations sisaldab võimalusi, mis tarnitakse koos rakendusega Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a279c-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="a279c-110">Tulevikus antakse nendele klientidele välja versiooniuuenduse tee.</span><span class="sxs-lookup"><span data-stu-id="a279c-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="a279c-111">Rakenduse Dynamics 365 Finance olemasolevad kliendid, kes kasutavad projektihaldust ja raamatupidamist</span><span class="sxs-lookup"><span data-stu-id="a279c-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="a279c-112">Rakenduse Finance olemasolevad kliendid, kes kasutavad projektihalduse ja raamatupidamise funktsiooni, saavad jätkata selle kasutamist samal kujul.</span><span class="sxs-lookup"><span data-stu-id="a279c-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="a279c-113">Vaadake teemat [Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks](#pma).</span><span class="sxs-lookup"><span data-stu-id="a279c-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="a279c-114">Project Operations toetab teie vajadustele vastamiseks mitut juurutamise võimalust.</span><span class="sxs-lookup"><span data-stu-id="a279c-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="a279c-115">Olenemata sellest, kas olete rakenduse Dynamics 365 uus või juba aktiivne klient, Project Operations saab teie vajadusi toetada.</span><span class="sxs-lookup"><span data-stu-id="a279c-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="a279c-116">Meie [juurutuse küsimustik](https://aka.ms/provisionprojectoperations) aitab teil teha kindlaks õige juurutuse.</span><span class="sxs-lookup"><span data-stu-id="a279c-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="a279c-117">Tulemused suunavad teid ühe järgmiste juurutustüübi juurde.</span><span class="sxs-lookup"><span data-stu-id="a279c-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="a279c-118">Lihtjuurutamine – tehing fiktiivsele arveldusele</span><span class="sxs-lookup"><span data-stu-id="a279c-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="a279c-119">Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="a279c-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="a279c-120">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="a279c-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="a279c-121">Project Operations toetab juriidilise olemi tasemel konfguratsioonide kaudu samas keskkonnas ladustatavat/tootmistellimuste stsenaariumeid ja mitteladustatavaid/ressursipõhiseid stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="a279c-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="a279c-122">Näiteks saab Contoso võimendada ladustatud/tootmistellimuse võimalusi oma USA tootmisettevõttes (juriidiline olem = Contoso tootmine Ameerika Ühendriikides) ja mitteladustatavaid/ressursipõhiseid võimalusi oma Contoso robotõlgade hooldamise asutuses Suurbritannias (juriidiline olem = Contoso robootika Ühendkuningriigis).</span><span class="sxs-lookup"><span data-stu-id="a279c-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="a279c-123"><a name="lite"><a/>Lihtjuurutamine – tehing näidisarveldusele</span><span class="sxs-lookup"><span data-stu-id="a279c-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="a279c-124">Lite’i juurutus sisaldab järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="a279c-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="a279c-125">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="a279c-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a279c-126">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="a279c-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a279c-127">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="a279c-127">Unified Resource Management</span></span>
- <span data-ttu-id="a279c-128">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="a279c-128">Time Tracking</span></span>
- <span data-ttu-id="a279c-129">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="a279c-129">Basic Expense</span></span>
- <span data-ttu-id="a279c-130">Arvesoovitus</span><span class="sxs-lookup"><span data-stu-id="a279c-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="a279c-131">Juurutamise sammud.</span><span class="sxs-lookup"><span data-stu-id="a279c-131">Deployment steps:</span></span>
<span data-ttu-id="a279c-132">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="a279c-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a279c-133">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](lite-preview-subscription-sign-up.md) ja [Uue keskkonna ettevalmistamine](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="a279c-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="a279c-134"><a name="integrated"><a/>Project Operations ressursi/mitteaktsia stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="a279c-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="a279c-135">Project Operations ressursipõhiste/mitteladustatavate stsenaariumite jaoks hõlmavad järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="a279c-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="a279c-136">Projekti planeerimine Microsoft Pro veebirakendust kasutades</span><span class="sxs-lookup"><span data-stu-id="a279c-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a279c-137">Mitmedimensiooniline hinnakujundus</span><span class="sxs-lookup"><span data-stu-id="a279c-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a279c-138">Ühtne ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="a279c-138">Unified Resource Management</span></span>
- <span data-ttu-id="a279c-139">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="a279c-139">Time Tracking</span></span>
- <span data-ttu-id="a279c-140">Põhikulu</span><span class="sxs-lookup"><span data-stu-id="a279c-140">Basic Expense</span></span>
- <span data-ttu-id="a279c-141">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="a279c-141">Full Expense</span></span>
- <span data-ttu-id="a279c-142">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="a279c-142">Receipt OCR</span></span>
- <span data-ttu-id="a279c-143">Täisarveldus</span><span class="sxs-lookup"><span data-stu-id="a279c-143">Full Invoicing</span></span>
- <span data-ttu-id="a279c-144">Tulu kajastamine</span><span class="sxs-lookup"><span data-stu-id="a279c-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="a279c-145">Juurutamise sammud.</span><span class="sxs-lookup"><span data-stu-id="a279c-145">Deployment steps:</span></span>
<span data-ttu-id="a279c-146">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="a279c-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a279c-147">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](resource-sign-up-preview-subscription.md) ja [Uue keskkonna ettevalmistamine](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a279c-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="a279c-148">Project Operations ressursi/tootmise tellimuste stsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="a279c-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="a279c-149">Projekti kavandamise WBS-i kasutades</span><span class="sxs-lookup"><span data-stu-id="a279c-149">Project planning using WBS</span></span>
- <span data-ttu-id="a279c-150">Ressursihaldus</span><span class="sxs-lookup"><span data-stu-id="a279c-150">Resource Management</span></span>
- <span data-ttu-id="a279c-151">Aja jälgimine</span><span class="sxs-lookup"><span data-stu-id="a279c-151">Time Tracking</span></span>
- <span data-ttu-id="a279c-152">Täiskulu</span><span class="sxs-lookup"><span data-stu-id="a279c-152">Full Expense</span></span>
- <span data-ttu-id="a279c-153">Kviitungi OCR</span><span class="sxs-lookup"><span data-stu-id="a279c-153">Receipt OCR</span></span>
- <span data-ttu-id="a279c-154">Täisarveldus</span><span class="sxs-lookup"><span data-stu-id="a279c-154">Full Invoicing</span></span>
- <span data-ttu-id="a279c-155">Tulu kajastamine</span><span class="sxs-lookup"><span data-stu-id="a279c-155">Revenue Recognition</span></span>
- <span data-ttu-id="a279c-156">Tootmistellimused</span><span class="sxs-lookup"><span data-stu-id="a279c-156">Production Orders</span></span>
- <span data-ttu-id="a279c-157">Materjalide tugi</span><span class="sxs-lookup"><span data-stu-id="a279c-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="a279c-158">Juurutamise sammud.</span><span class="sxs-lookup"><span data-stu-id="a279c-158">Deployment steps:</span></span>
<span data-ttu-id="a279c-159">Tehke [juurutamise küsimustiku](https://aka.ms/provisionprojectoperations) abil kindlaks rakenduse Project Operations jaoks parim juurutamise mudel.</span><span class="sxs-lookup"><span data-stu-id="a279c-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a279c-160">Selle juurutuse kohta leiate teavet teemadest [Eelversiooni kordustellimuseks registreerumine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ja [Uue keskkonna ettevalmistamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a279c-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



