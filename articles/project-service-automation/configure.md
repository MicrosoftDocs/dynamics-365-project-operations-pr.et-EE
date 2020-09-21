---
title: Project Service Automation konfigureerimine
description: Project Service'i konfigureerimistoimingud
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750948"
---
# <a name="configure-project-service"></a><span data-ttu-id="d367e-103">Project Service'i konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d367e-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d367e-104">Enne kui saate kasutada oma ettevõtete, projektide ja ressursside haldamiseks lahenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatiseerimisvõimalusi [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]-is, peate läbima mõne konfiguratsioonietapi, et tagada lahenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vastavus teie organisatsiooni vajadustele.</span><span class="sxs-lookup"><span data-stu-id="d367e-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="d367e-105">Etapid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="d367e-105">These steps include:</span></span>  
  
-   <span data-ttu-id="d367e-106">[Ajaühikute seadistamine](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="d367e-107">Ajaühikute konfigureerimine tootekataloogis, mida kasutate oma projektide planeerimise ja arveldamise alusena.</span><span class="sxs-lookup"><span data-stu-id="d367e-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="d367e-108">[Valuutade ja vahetuskursside seadistamine](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="d367e-109">Projektide jaoks kasutatavate valuutade seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d367e-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="d367e-110">[Organisatsiooniüksuste loomine](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="d367e-111">Rühmade seadistamine, mida teie ettevõte kasutab äriliseks jaotamiseks – kas geograafia, ärifunktsiooni või muu loogilise jaotuse alusel.</span><span class="sxs-lookup"><span data-stu-id="d367e-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="d367e-112">[Arve sageduste seadistamine](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="d367e-113">Ajaperioodide seadistamine, mida soovite oma klientidega arveldamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="d367e-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="d367e-114">[Tehingukategooriate konfigureerimine](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="d367e-115">Tehingukategooriate seadistamine, mida teie nõustajad saavad oma arveldatavate ja mittearveldatavate kulude jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="d367e-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="d367e-116">[Kulukategooriate konfigureerimine](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="d367e-117">Kategooriate seadistamine, mida teie nõustajad saavad oma arveldatavate ja mittearveldatavate kulude jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="d367e-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="d367e-118">[Tootekataloogi üksuste loomine](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="d367e-119">Müüdavate toodete, nt tarkvaralitsentside, lisamine tootekataloogi.</span><span class="sxs-lookup"><span data-stu-id="d367e-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="d367e-120">[Hinnakirja loomine](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="d367e-121">Erinevate hinnakirjade konfigureerimine olenevalt sellest, kui palju soovite oma klientidelt tasu küsida iga rolli eest, mida nende projekt nõuab.</span><span class="sxs-lookup"><span data-stu-id="d367e-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="d367e-122">[Ressursside seadistamine](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d367e-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="d367e-123">Oskuste, pädevuste, ressursirollide ja muu oma projektide jaoks vajaliku ressursiteabe lisamine.</span><span class="sxs-lookup"><span data-stu-id="d367e-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d367e-124">Vt ka</span><span class="sxs-lookup"><span data-stu-id="d367e-124">See Also</span></span>  
 <span data-ttu-id="d367e-125">[Project Service Automation ülevaade](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="d367e-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="d367e-126">[Project Service Automation konfigureerimine](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="d367e-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="d367e-127">[Kontohalduri juhend](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d367e-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="d367e-128">[Projektijuhi juhend](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d367e-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="d367e-129">[Ressursihalduri juhend](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d367e-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="d367e-130">Aja-, kulu- ja koostööjuhend</span><span class="sxs-lookup"><span data-stu-id="d367e-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
