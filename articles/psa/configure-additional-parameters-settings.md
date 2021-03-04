---
title: Täiendavate parameetrisätete konfigureerimine
description: Project Service'i täiendavate parameetrisätete konfigureerimine
author: JohnPBurrows
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151563"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="5378d-103">Täiendavate parameetrisätete konfigureerimine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="5378d-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5378d-104">Kui olete eelmistes teemades nimetatud üksused konfigureerinud, peate määrama täiendavad projektiparameetrid, mida oma projektide puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="5378d-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="5378d-105">Funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] installimisel lõite parameetrisätte, et luua esmalt kõik funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kasutamiseks vajalikud kirjed.</span><span class="sxs-lookup"><span data-stu-id="5378d-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="5378d-106">Nüüd on aeg minna tagasi ja konfigureerida nende seadete lisaväljad.</span><span class="sxs-lookup"><span data-stu-id="5378d-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="5378d-107">Peate konfigureerima järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="5378d-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="5378d-108">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="5378d-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="5378d-109">Arve sagedus</span><span class="sxs-lookup"><span data-stu-id="5378d-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="5378d-110">Töötundide mall</span><span class="sxs-lookup"><span data-stu-id="5378d-110">Work hours template</span></span>  
  
-   <span data-ttu-id="5378d-111">Hinnakiri</span><span class="sxs-lookup"><span data-stu-id="5378d-111">Price list</span></span>  
 
<span data-ttu-id="5378d-112">Selles etapis näitate ka seda, millist tüüpi ressursieraldist soovite.</span><span class="sxs-lookup"><span data-stu-id="5378d-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="5378d-113">**Keskne**.</span><span class="sxs-lookup"><span data-stu-id="5378d-113">**Central**.</span></span> <span data-ttu-id="5378d-114">Projektidele saavad ressursse eraldada ainult ressursihaldurid.</span><span class="sxs-lookup"><span data-stu-id="5378d-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="5378d-115">**Hübriid**.</span><span class="sxs-lookup"><span data-stu-id="5378d-115">**Hybrid**.</span></span> <span data-ttu-id="5378d-116">Projektidele saavad ressursse määrata ressursihaldurid, projektijuhid ja kontohaldurid.</span><span class="sxs-lookup"><span data-stu-id="5378d-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="5378d-117">Projektiparameetrite määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="5378d-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="5378d-118">Minge jaotisse **Project Service > Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5378d-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="5378d-119">Klõpsake parameetrisättel, mida soovite konfigureerida (see, mille lõite funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] installimisel), või klõpsake uue loomiseks valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5378d-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="5378d-120">Määrake alal **Üldine** oma projektiparameetrite jaoks kõik suvandid.</span><span class="sxs-lookup"><span data-stu-id="5378d-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="5378d-121">Klõpsake alal **Hinnakiri** nuppu **+**, et lisada hinnakiri, valige hinnakiri ripploendist **Projektiparameetri hinnakiri** ja seejärel klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5378d-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="5378d-122">Klõpsake ekraani paremas alanurgas nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5378d-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="5378d-123">Projekti parameetri kirje peab Project Service'i õigeks töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="5378d-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="5378d-124">Seda kirjet ei tohiks kustutada.</span><span class="sxs-lookup"><span data-stu-id="5378d-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="5378d-125">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5378d-125">See Also</span></span>  
 [<span data-ttu-id="5378d-126">Ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="5378d-126">Set up resources</span></span>](../psa/set-up-resources.md)
