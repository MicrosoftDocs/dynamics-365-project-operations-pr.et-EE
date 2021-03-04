---
title: Hinnakirja loomine
description: Hinnakirja loomine Project Service'is
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18f6e7a7a96f374acc85ee1027c5252cbf7ab5f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149448"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="5a4bc-103">Hinnakirja loomine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="5a4bc-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5a4bc-104">Hinnakirjad annavad malli, mille abil saavad teie kontohaldurid luua hinnapakkumisi ja projekte ning teha kindlaks projekti kulusid.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="5a4bc-105">Need pakuvad reaüksuse rollide ja kulude loendi ning igaühe hinna.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="5a4bc-106">Saate luua mitu hinnakirja, et hallata erinevate müügipiirkondade või müügikanalite puhul eraldi hinnastruktuure.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="5a4bc-107">Arukas on luua vähemalt üks hinnakiri iga valuuta kohta, milles kavatsete oma klientidele arveid esitada.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="5a4bc-108">Edastatava töö finantsprognooside loomiseks veenduge, et igal projektil oleks aluseks olev kulu- ja müügihinnakiri.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="5a4bc-109">Seadistage kulu ja müügi vaikehinnakiri, mis kehtib kõigi teie organisatsioonis loodud projektide puhul.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="5a4bc-110">Hinnakirjad tuginevad rollidele ja kulukategooriatele, seega enne hinnakirja loomist veenduge, et oleksite konfigureerinud rollid ja kulukategooriad, mida soovite hinnakirja loomise kasutada.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="5a4bc-111">Minge jaotisse **Project Service > Hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="5a4bc-112">Klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="5a4bc-113">Valige jaotises **Kontekst**, kas hinnakirja tüüp on **Kulu**, **Ost** või **Müük**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="5a4bc-114">Sisestage väljale **Nimi** hinnakirja nimi.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="5a4bc-115">Valige väljal **Valuuta** arveldamiseks või omahinna arvutamiseks kasutatav valuuta.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="5a4bc-116">Määrake väljal **Ajaühik** hinna kehtimise ajaperiood, nagu päev või tund.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="5a4bc-117">Vajaduse korral täitke väljad **Alguskuupäev**, **Lõppkuupäev** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="5a4bc-118">Klõpsake kirje loomiseks käsku **Salvesta**, seejärel saate selle redigeerimist jätkata.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="5a4bc-119">Hinnakirjale rollihinna lisamiseks klõpsake jaotises **Rollihinnad** nuppu **+**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="5a4bc-120">Sisestage üksikasjad paanil **Rolli hind** ja seejärel klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="5a4bc-121">Jätkake rollihindade lisamisega vajadust mööda.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="5a4bc-122">Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="5a4bc-123">Hinnakirjale kulukategooria lisamiseks klõpsake jaotises **Kategooriahinnad** nuppu **+**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="5a4bc-124">Sisestage üksikasjad paanil **Tehingukategooria hind** ja seejärel klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="5a4bc-125">Jätkake kategooriahindade lisamisega vajadust mööda.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="5a4bc-126">Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="5a4bc-127">Hinnakirjale hinnakirjaüksuste lisamiseks klõpsake jaotises **Hinnakirjaüksused** nuppu **+**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="5a4bc-128">Sisestage üksikasjad paanil **Hinnakirjaüksus** ja seejärel klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="5a4bc-129">Jätkake hinnakirjaüksuste lisamisega vajadust mööda.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="5a4bc-130">Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="5a4bc-131">Hinnakirjale piirkonnaseoste lisamiseks klõpsake jaotises **Piirkonnaseosed** nuppu **+**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="5a4bc-132">Sisestage üksikasjad aknas **Uus ühendus** ja seejärel klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="5a4bc-133">Jätkake piirkonnaseoste lisamisega vajadust mööda.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="5a4bc-134">Kui olete lõpetanud, klõpsake kuva paremas alanurgas käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5a4bc-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5a4bc-135">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5a4bc-135">See Also</span></span>  
 [<span data-ttu-id="5a4bc-136">Project Service Automation konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5a4bc-136">Configure Project Service Automation</span></span>](../psa/configure.md)
