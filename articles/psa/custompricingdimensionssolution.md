---
title: Kohandatud lahenduste loomine hinnakujunduse dimensioonide jaoks
description: Selles teemas selgitatakse, kuidas luua kohandatud hinnakujunduse dimensioonide loomise ajal kohandatud lahendus.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144634"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="be09f-103">Kohandatud lahenduste loomine hinnakujunduse dimensioonide jaoks</span><span class="sxs-lookup"><span data-stu-id="be09f-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="be09f-104">Kõik kohandatud hinnakujunduse dimensiooni muudatused peaksid olema eraldi lahenduses.</span><span class="sxs-lookup"><span data-stu-id="be09f-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="be09f-105">See oluline hea tava annab tulevikus paindlikkuse muudatuste värskendamiseks või eemaldamiseks vastavalt vajadusele, aitab teie tööd uuesti kasutada ja muudab nende muudatuste teisaldamise teistele eksemplaridele hõlpsamaks.</span><span class="sxs-lookup"><span data-stu-id="be09f-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="be09f-106">Kui teete vajalikke muudatusi, eksportige see lahendus kui **Hallatud lahendus** ja importige see muudesse eksemplaridesse, et saaksite oma hinnakujunduse seadistust uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="be09f-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="be09f-107">Valige **Sätted** > **Lahendused** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="be09f-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="be09f-108">Pange lahendusele nimi **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**, sisestage ülejäänud nõutav teave ja valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="be09f-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Kohandatud lahenduse loomine hinnakujunduse dimensioonide jaoks](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="be09f-110">Lisage kõik nõutavad olemid ja seotud komponendid hinnakujunduse dimensiooni lahendusse</span><span class="sxs-lookup"><span data-stu-id="be09f-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="be09f-111">Hinnakujunduse lahendusele tuleb lisada järgmised Project Service’i olemid.</span><span class="sxs-lookup"><span data-stu-id="be09f-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="be09f-112">Läbige selle protseduuri etapid, et muuta hinnakujunduse lahenduses teatud olulisi skeeme, et olemid oleksid uutest hinnakujunduse dimensioonidest teadlikud.</span><span class="sxs-lookup"><span data-stu-id="be09f-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="be09f-113">Valige **Sätted** > **Lahendused** ja topeltklõpsake seejärel suvandit **Organisatsiooni \<your organization name> hinnakujunduse dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="be09f-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="be09f-114">Valige rakenduses Solution Explorer vasakul navigeerimispaanil suvandid **Lisa olemasolev** > **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="be09f-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="be09f-115">Valige dialoogiboksis **Lahenduse komponendid** järgmised olemid.</span><span class="sxs-lookup"><span data-stu-id="be09f-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="be09f-116">Tegelik</span><span class="sxs-lookup"><span data-stu-id="be09f-116">Actual</span></span>
- <span data-ttu-id="be09f-117">Broneeritav ressurss</span><span class="sxs-lookup"><span data-stu-id="be09f-117">Bookable Resource</span></span>
- <span data-ttu-id="be09f-118">Prognoosi rida</span><span class="sxs-lookup"><span data-stu-id="be09f-118">Estimate Line</span></span>
- <span data-ttu-id="be09f-119">Projekti ülesanne</span><span class="sxs-lookup"><span data-stu-id="be09f-119">Project Task</span></span>
- <span data-ttu-id="be09f-120">Arve rea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="be09f-120">Invoice Line Detail</span></span>
- <span data-ttu-id="be09f-121">Töölehe rida</span><span class="sxs-lookup"><span data-stu-id="be09f-121">Journal Line</span></span>
- <span data-ttu-id="be09f-122">Projekti lepingurea üksikasi</span><span class="sxs-lookup"><span data-stu-id="be09f-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="be09f-123">Projektimeeskonna liige</span><span class="sxs-lookup"><span data-stu-id="be09f-123">Project Team Member</span></span>
- <span data-ttu-id="be09f-124">Hinnapakkumise rea üksikasi</span><span class="sxs-lookup"><span data-stu-id="be09f-124">Quote Line Detail</span></span>
- <span data-ttu-id="be09f-125">Rolli hinna hinnalisand</span><span class="sxs-lookup"><span data-stu-id="be09f-125">Role Price Markup</span></span>
- <span data-ttu-id="be09f-126">Rolli hind</span><span class="sxs-lookup"><span data-stu-id="be09f-126">Role Price</span></span> 
- <span data-ttu-id="be09f-127">Ajakirje</span><span class="sxs-lookup"><span data-stu-id="be09f-127">Time Entry</span></span> 

> ![Olemasolevate olemite lisamine hinnakujunduse dimensioonide lahendusse](media/Existing-entities-to-PD-solution.png)

> ![Lahenduse komponentide valimine](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="be09f-130">Veenduge, et kõigi valitud olemite jaoks kaasatakse kõik vormid ja vaated.</span><span class="sxs-lookup"><span data-stu-id="be09f-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="be09f-131">Kui teil palutakse kaasata valitud olemite jaoks kõik sõltuvad olemid, valige **Ei**.</span><span class="sxs-lookup"><span data-stu-id="be09f-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Ära kaasa kõiki seotud komponente](media/Do-not-include-required.png)


