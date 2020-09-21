---
title: Täiendavate parameetrisätete konfigureerimine
description: Project Service'i täiendavate parameetrisätete konfigureerimine
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751058"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="126d2-103">Täiendavate parameetrisätete konfigureerimine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="126d2-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="126d2-104">Kui olete eelmistes teemades nimetatud üksused konfigureerinud, peate määrama täiendavad projektiparameetrid, mida oma projektide puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="126d2-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="126d2-105">Funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] installimisel lõite parameetrisätte, et luua esmalt kõik funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kasutamiseks vajalikud kirjed.</span><span class="sxs-lookup"><span data-stu-id="126d2-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="126d2-106">Nüüd on aeg minna tagasi ja konfigureerida nende seadete lisaväljad.</span><span class="sxs-lookup"><span data-stu-id="126d2-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="126d2-107">Peate konfigureerima järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="126d2-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="126d2-108">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="126d2-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="126d2-109">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="126d2-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="126d2-110">Töötundide mall</span><span class="sxs-lookup"><span data-stu-id="126d2-110">Work hours template</span></span>  
  
-   <span data-ttu-id="126d2-111">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="126d2-111">Price list</span></span>  
 
<span data-ttu-id="126d2-112">Selles etapis näitate ka seda, millist tüüpi ressursieraldist soovite.</span><span class="sxs-lookup"><span data-stu-id="126d2-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="126d2-113">**Keskne**.</span><span class="sxs-lookup"><span data-stu-id="126d2-113">**Central**.</span></span> <span data-ttu-id="126d2-114">Projektidele saavad ressursse eraldada ainult ressursihaldurid.</span><span class="sxs-lookup"><span data-stu-id="126d2-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="126d2-115">**Hübriid**.</span><span class="sxs-lookup"><span data-stu-id="126d2-115">**Hybrid**.</span></span> <span data-ttu-id="126d2-116">Projektidele saavad ressursse määrata ressursihaldurid, projektijuhid ja kontohaldurid.</span><span class="sxs-lookup"><span data-stu-id="126d2-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="126d2-117">Projektiparameetrite määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="126d2-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="126d2-118">Minge jaotisse **Project Service > Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="126d2-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="126d2-119">Klõpsake parameetrisättel, mida soovite konfigureerida (see, mille lõite funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] installimisel), või klõpsake uue loomiseks valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="126d2-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="126d2-120">Määrake alal **Üldine** oma projektiparameetrite jaoks kõik suvandid.</span><span class="sxs-lookup"><span data-stu-id="126d2-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="126d2-121">Klõpsake alal **Hinnakiri** nuppu **+**, et lisada hinnakiri, valige hinnakiri ripploendist **Projektiparameetri hinnakiri** ja seejärel klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="126d2-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="126d2-122">Klõpsake ekraani paremas alanurgas nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="126d2-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="126d2-123">Projekti parameetri kirje peab Project Service'i õigeks töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="126d2-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="126d2-124">Seda kirjet ei tohiks kustutada.</span><span class="sxs-lookup"><span data-stu-id="126d2-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="126d2-125">Vt ka</span><span class="sxs-lookup"><span data-stu-id="126d2-125">See Also</span></span>  
 [<span data-ttu-id="126d2-126">Ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="126d2-126">Set up resources</span></span>](../project-service/set-up-resources.md)
