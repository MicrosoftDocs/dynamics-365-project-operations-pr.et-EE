---
title: Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks
description: Selles teemas kirjeldatakse, kuidas luua kohandatud hinnakujunduse jaoks lahendusi.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278413"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="500b3-103">Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks</span><span class="sxs-lookup"><span data-stu-id="500b3-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="500b3-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="500b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="500b3-105">Kõik kohandatud hinnakujunduse dimensiooni muudatused peaksid olema eraldi lahenduses.</span><span class="sxs-lookup"><span data-stu-id="500b3-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="500b3-106">See oluline hea tava võimaldab paindlikkust värskendada või eemaldada vastavalt vajadusele muudatusi, aitab teid oma töö uuesti kasutamisel ja muudab lihtsamaks teisedada need muudatused teistesse eksemplaridesse.</span><span class="sxs-lookup"><span data-stu-id="500b3-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="500b3-107">Pärast vajalike muudatuste tegemist eksportige see lahendus kui **Hallatud** lahendus ja importige seejärel muudesse eksemplaridesse, et uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="500b3-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="500b3-108">Lahenduse loomine kohandatud hinnakujunduse dimensioonide jaoks</span><span class="sxs-lookup"><span data-stu-id="500b3-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="500b3-109">Valige **Sätted** > **Lahendused** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="500b3-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="500b3-110">Sisestage lahenduse nimi, organisatsiooni *<your organization name> hinnakujunduse dimensioonid*.</span><span class="sxs-lookup"><span data-stu-id="500b3-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="500b3-111">Sisestage ülejäänud nõutav teave ja calige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="500b3-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Kohandatud hinnakujunduse dimensiooni lahenduse loomine](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="500b3-113">Lisage kõik nõutavad olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse</span><span class="sxs-lookup"><span data-stu-id="500b3-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="500b3-114">Lisage oma hinnakujunduse lahendusele järgmised teenuse Project Service olemid, et teha oma hinnakujunduse lahenduses olulised skeemi muudatused.</span><span class="sxs-lookup"><span data-stu-id="500b3-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="500b3-115">Pärast selle toimingu lõpetamist tuvastavad olemid uue hinnakujunduse dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="500b3-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="500b3-116">Valige **Sätted** > **Lahendused** ja topeltklõpsake seejärel valikut **organisatsiooni <*teie organisatsiooni nimi*> hinnakujunduse dimendioonid**.</span><span class="sxs-lookup"><span data-stu-id="500b3-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="500b3-117">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="500b3-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="500b3-118">Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.</span><span class="sxs-lookup"><span data-stu-id="500b3-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="500b3-119">**Tegelik**</span><span class="sxs-lookup"><span data-stu-id="500b3-119">**Actual**</span></span>
   - <span data-ttu-id="500b3-120">**Broneeritav ressurss**</span><span class="sxs-lookup"><span data-stu-id="500b3-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="500b3-121">**Prognoosi rida**</span><span class="sxs-lookup"><span data-stu-id="500b3-121">**Estimate Line**</span></span>
   - <span data-ttu-id="500b3-122">**Projekti ülesanne**</span><span class="sxs-lookup"><span data-stu-id="500b3-122">**Project Task**</span></span>
   - <span data-ttu-id="500b3-123">**Arve rea üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="500b3-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="500b3-124">**Töölehe rida**</span><span class="sxs-lookup"><span data-stu-id="500b3-124">**Journal Line**</span></span>
   - <span data-ttu-id="500b3-125">**Projekti lepingurea üksikasi**</span><span class="sxs-lookup"><span data-stu-id="500b3-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="500b3-126">**Projektimeeskonna liige**</span><span class="sxs-lookup"><span data-stu-id="500b3-126">**Project Team Member**</span></span>
   - <span data-ttu-id="500b3-127">**Hinnapakkumise rea üksikasi**</span><span class="sxs-lookup"><span data-stu-id="500b3-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="500b3-128">**Rolli hinna hinnalisand**</span><span class="sxs-lookup"><span data-stu-id="500b3-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="500b3-129">**Rolli hind**</span><span class="sxs-lookup"><span data-stu-id="500b3-129">**Role Price**</span></span>
   - <span data-ttu-id="500b3-130">**Ajakirje**</span><span class="sxs-lookup"><span data-stu-id="500b3-130">**Time Entry**</span></span>
 
   ![Olemasolevate olemite kohandatud hinnakujunduse dimensiooni lahenduse lisamine](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="500b3-132">Vaadake iga olemi kohta lisatavaid komponente ja iga olemi kohta olemi varade lõplikku loendit.</span><span class="sxs-lookup"><span data-stu-id="500b3-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="500b3-133">Kaasake iga valitud olemite jaoks kõik vormid ja vaated.</span><span class="sxs-lookup"><span data-stu-id="500b3-133">Include all forms and views for each of the selected entities.</span></span>

  ![Lisatud olemid](./media/solution-component-selection.png)


5.  <span data-ttu-id="500b3-135">Kui teil palutakse lisada valitud olemite jaoks mis tahes sõltuvaid olemeid, valige suvand **Ei, ära kaasa nõutavaid komponente.**</span><span class="sxs-lookup"><span data-stu-id="500b3-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Kaasab sõltuvad olemid](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]