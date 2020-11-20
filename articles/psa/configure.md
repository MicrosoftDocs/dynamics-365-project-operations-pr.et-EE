---
title: Project Service Automation konfigureerimine
description: Project Service'i konfigureerimistoimingud
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129178"
---
# <a name="configure-project-service"></a><span data-ttu-id="e44bc-103">Project Service'i konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e44bc-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e44bc-104">Enne kui saate kasutada oma ettevõtete, projektide ja ressursside haldamiseks lahenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatiseerimisvõimalusi [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]-is, peate läbima mõne konfiguratsioonietapi, et tagada lahenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vastavus teie organisatsiooni vajadustele.</span><span class="sxs-lookup"><span data-stu-id="e44bc-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="e44bc-105">Etapid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="e44bc-105">These steps include:</span></span>  
  
-   <span data-ttu-id="e44bc-106">[Ajaühikute seadistamine](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="e44bc-107">Ajaühikute konfigureerimine tootekataloogis, mida kasutate oma projektide planeerimise ja arveldamise alusena.</span><span class="sxs-lookup"><span data-stu-id="e44bc-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="e44bc-108">[Valuutade ja vahetuskursside seadistamine](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="e44bc-109">Projektide jaoks kasutatavate valuutade seadistamine.</span><span class="sxs-lookup"><span data-stu-id="e44bc-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="e44bc-110">[Organisatsiooniüksuste loomine](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="e44bc-111">Rühmade seadistamine, mida teie ettevõte kasutab äriliseks jaotamiseks – kas geograafia, ärifunktsiooni või muu loogilise jaotuse alusel.</span><span class="sxs-lookup"><span data-stu-id="e44bc-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="e44bc-112">[Arve sageduste seadistamine](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="e44bc-113">Ajaperioodide seadistamine, mida soovite oma klientidega arveldamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="e44bc-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="e44bc-114">[Tehingukategooriate konfigureerimine](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="e44bc-115">Tehingukategooriate seadistamine, mida teie nõustajad saavad oma arveldatavate ja mittearveldatavate kulude jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="e44bc-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="e44bc-116">[Kulukategooriate konfigureerimine](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="e44bc-117">Kategooriate seadistamine, mida teie nõustajad saavad oma arveldatavate ja mittearveldatavate kulude jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="e44bc-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="e44bc-118">[Tootekataloogi üksuste loomine](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="e44bc-119">Müüdavate toodete, nt tarkvaralitsentside, lisamine tootekataloogi.</span><span class="sxs-lookup"><span data-stu-id="e44bc-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="e44bc-120">[Hinnakirja loomine](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="e44bc-121">Erinevate hinnakirjade konfigureerimine olenevalt sellest, kui palju soovite oma klientidelt tasu küsida iga rolli eest, mida nende projekt nõuab.</span><span class="sxs-lookup"><span data-stu-id="e44bc-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="e44bc-122">[Ressursside seadistamine](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="e44bc-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="e44bc-123">Oskuste, pädevuste, ressursirollide ja muu oma projektide jaoks vajaliku ressursiteabe lisamine.</span><span class="sxs-lookup"><span data-stu-id="e44bc-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e44bc-124">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e44bc-124">See Also</span></span>  
 <span data-ttu-id="e44bc-125">[Project Service Automation ülevaade](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="e44bc-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="e44bc-126">[Project Service Automation konfigureerimine](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="e44bc-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="e44bc-127">[Kontohalduri juhend](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e44bc-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="e44bc-128">[Projektijuhi juhend](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e44bc-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="e44bc-129">[Ressursihalduri juhend](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="e44bc-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="e44bc-130">Aja-, kulu- ja koostööjuhend</span><span class="sxs-lookup"><span data-stu-id="e44bc-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
