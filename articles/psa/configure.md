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
ms.openlocfilehash: fd02611b5b3133e097b2818a725b6c5d667e5ac0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075065"
---
# <a name="configure-project-service"></a><span data-ttu-id="0f5d2-103">Project Service'i konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0f5d2-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0f5d2-104">Enne kui saate kasutada oma ettevõtete, projektide ja ressursside haldamiseks lahenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatiseerimisvõimalusi [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]-is, peate läbima mõne konfiguratsioonietapi, et tagada lahenduse [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vastavus teie organisatsiooni vajadustele.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="0f5d2-105">Etapid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-105">These steps include:</span></span>  
  
-   <span data-ttu-id="0f5d2-106">[Ajaühikute seadistamine](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="0f5d2-107">Ajaühikute konfigureerimine tootekataloogis, mida kasutate oma projektide planeerimise ja arveldamise alusena.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="0f5d2-108">[Valuutade ja vahetuskursside seadistamine](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="0f5d2-109">Projektide jaoks kasutatavate valuutade seadistamine.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="0f5d2-110">[Organisatsiooniüksuste loomine](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="0f5d2-111">Rühmade seadistamine, mida teie ettevõte kasutab äriliseks jaotamiseks – kas geograafia, ärifunktsiooni või muu loogilise jaotuse alusel.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="0f5d2-112">[Arve sageduste seadistamine](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="0f5d2-113">Ajaperioodide seadistamine, mida soovite oma klientidega arveldamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="0f5d2-114">[Tehingukategooriate konfigureerimine](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="0f5d2-115">Tehingukategooriate seadistamine, mida teie nõustajad saavad oma arveldatavate ja mittearveldatavate kulude jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="0f5d2-116">[Kulukategooriate konfigureerimine](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="0f5d2-117">Kategooriate seadistamine, mida teie nõustajad saavad oma arveldatavate ja mittearveldatavate kulude jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="0f5d2-118">[Tootekataloogi üksuste loomine](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="0f5d2-119">Müüdavate toodete, nt tarkvaralitsentside, lisamine tootekataloogi.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="0f5d2-120">[Hinnakirja loomine](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="0f5d2-121">Erinevate hinnakirjade konfigureerimine olenevalt sellest, kui palju soovite oma klientidelt tasu küsida iga rolli eest, mida nende projekt nõuab.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="0f5d2-122">[Ressursside seadistamine](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="0f5d2-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="0f5d2-123">Oskuste, pädevuste, ressursirollide ja muu oma projektide jaoks vajaliku ressursiteabe lisamine.</span><span class="sxs-lookup"><span data-stu-id="0f5d2-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0f5d2-124">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0f5d2-124">See Also</span></span>  
 <span data-ttu-id="0f5d2-125">[Project Service Automation ülevaade](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="0f5d2-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="0f5d2-126">[Project Service Automation konfigureerimine](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="0f5d2-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="0f5d2-127">[Kontohalduri juhend](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f5d2-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="0f5d2-128">[Projektijuhi juhend](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f5d2-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="0f5d2-129">[Ressursihalduri juhend](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f5d2-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="0f5d2-130">Aja-, kulu- ja koostööjuhend</span><span class="sxs-lookup"><span data-stu-id="0f5d2-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
