---
title: Projekti tööprognooside esitamine müügiprotsessi käigus
description: Project Service'i projekti tööprognooside esitamine müügiprotsessi käigus
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075006"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="de2b7-103">Projekti tööprognooside esitamine müügiprotsessi käigus (Project Service)</span><span class="sxs-lookup"><span data-stu-id="de2b7-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="de2b7-104">Saate müügiprotsessi käigus müügiprognoosid hinnapakkumise ridade abil algusest peale välja töötada.</span><span class="sxs-lookup"><span data-stu-id="de2b7-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="de2b7-105">Funktsiooni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rakenduses [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] võimalused pakuvad teaduslikumat ja ettemääratumat viisi müügiprognoosidega väljatulemiseks, liigendades tööüksusi ja seostades asjakohaseid atribuute, mis panustavad projekti prognoosidesse tööjaotuse struktuuris.</span><span class="sxs-lookup"><span data-stu-id="de2b7-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="de2b7-106">Kui olete müügi võitnud, saate kasutada oma projektiplaani seostatud tööjaotuse struktuuri, seda projekti edukaks täitmiseks vajaduse korral kitsamalt määratledes.</span><span class="sxs-lookup"><span data-stu-id="de2b7-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="de2b7-107">Projekti linkimine hinnapakkumise reaga</span><span class="sxs-lookup"><span data-stu-id="de2b7-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="de2b7-108">Projektipõhise hinnapakkumise rea loomisel saate luua uue projekti hinnapakkumise realt.</span><span class="sxs-lookup"><span data-stu-id="de2b7-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="de2b7-109">Seejärel saate kasutada projektimalle, mis on kas teie organisatsioonile ühised eelkonfigureeritud standardsed projektiplaanid ja finantsprognoosid või projektiplaani koopia ja prognoosid viimasest projektist.</span><span class="sxs-lookup"><span data-stu-id="de2b7-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="de2b7-110">Projekti loomisel pakub projektimalli valimine aluse projektiplaani, prognooside ja rollinõuete täpsustamiseks.</span><span class="sxs-lookup"><span data-stu-id="de2b7-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="de2b7-111">Kui loote projekti hinnapakkumisest, seostatakse projekt automaatselt hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="de2b7-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="de2b7-112">Projektiprognoosi komponendid</span><span class="sxs-lookup"><span data-stu-id="de2b7-112">Project estimate components</span></span>  
 <span data-ttu-id="de2b7-113">Projekti tööjaotuse struktuur võimaldab jaotada töö ülesanneteks, hallata ülesannete hierarhiat ja määrata iga ülesande täitmiseks vajaliku pingutusprognoosi.</span><span class="sxs-lookup"><span data-stu-id="de2b7-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="de2b7-114">Saate ülesandega seostada ka rolle, et näidata ülesande ja ajakava täitmiseks vajalikku hinnangulist ressursitüüpi.</span><span class="sxs-lookup"><span data-stu-id="de2b7-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="de2b7-115">Tööjaotuse struktuur aitab teil välja selgitada tööpingutuse ja ajakava prognoosi.</span><span class="sxs-lookup"><span data-stu-id="de2b7-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="de2b7-116">Vaikimisi kasutab projekt vaikehinnakirju, mille olete varem määratlenud.</span><span class="sxs-lookup"><span data-stu-id="de2b7-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="de2b7-117">Hinnakirjades määratletud kulu- ja müügihinnad aitavad välja selgitada projekti tööjaotuse finantsprognoosi.</span><span class="sxs-lookup"><span data-stu-id="de2b7-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="de2b7-118">Kui teie projekt on seostatud hinnapakkumisega ja hinnapakkumisel on mõni muu hinnakiri kui vaikimisi, kasutatakse finantsprognooside puhul hinnapakkumise hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="de2b7-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="de2b7-119">Prognooside importimine projektist hinnapakkumisse</span><span class="sxs-lookup"><span data-stu-id="de2b7-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="de2b7-120">Kui teil on projektis projektiprognoosid olemas, saate need importida hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="de2b7-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="de2b7-121">Klõpsake jaotises **Hinnapakkumise rea üksikasjad** käsku **Impordi prognoosidest**.</span><span class="sxs-lookup"><span data-stu-id="de2b7-121">In **Quote Line Details** , click **Import from estimates**.</span></span> 

-   <span data-ttu-id="de2b7-122">Valige, kas importida projekti prognoosid summeerituna kande tüübi, rolli või tööjaotuse struktuuri sõlmetaseme järgi.</span><span class="sxs-lookup"><span data-stu-id="de2b7-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="de2b7-123">Vt ka</span><span class="sxs-lookup"><span data-stu-id="de2b7-123">See Also</span></span>  
 [<span data-ttu-id="de2b7-124">Projektijuhi juhend</span><span class="sxs-lookup"><span data-stu-id="de2b7-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
