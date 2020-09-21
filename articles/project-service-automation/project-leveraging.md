---
title: Müügiprognoosid ja projektid
description: See teema pakub teavet selle kohta, kuidas müügiprotsessis ajakava ja prognoose ära kasutada.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750943"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="ad053-103">Müügiprognoosid ja projektid</span><span class="sxs-lookup"><span data-stu-id="ad053-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ad053-104">Müügiprotsessi käigus saate luua müügiprognoose, kui seostate projekti müügipakkumisega.</span><span class="sxs-lookup"><span data-stu-id="ad053-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="ad053-105">Sel viisil saab müügiprotsessi ajal toimuda kindel prognoos, et saaksite ära kasutada projekti ajastamise ja prognoosimise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="ad053-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="ad053-106">Kui müük toimub, saab müügiprognoosi eesmärkidel kasutatud ajakava kasutada projektiplaani edasiseks täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="ad053-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="ad053-107">Projekti linkimine hinnapakkumise reaga</span><span class="sxs-lookup"><span data-stu-id="ad053-107">Linking a project to a quote line</span></span>

<span data-ttu-id="ad053-108">Projektipõhise hinnapakkumise rea loomisel saate luua uue projekti või seostada olemasoleva projekti lehel **Hinnapakkumise rida**.</span><span class="sxs-lookup"><span data-stu-id="ad053-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Hinnapakkumise rea vorm](media/project-8.png)
 
<span data-ttu-id="ad053-110">Kui loote hinnapakkumise rea üksikasjadest uue projekti, võite ära kasutada projekti malle.</span><span class="sxs-lookup"><span data-stu-id="ad053-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="ad053-111">Projektimallid on mudelprojektid, mis esindavad standardseid projektiplaane ja organisatsioonile tüüpilisi finantskalkulatsioone.</span><span class="sxs-lookup"><span data-stu-id="ad053-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="ad053-112">Need võivad esindada ka projektiplaanide koopiaid ja varasemate projektide prognoose.</span><span class="sxs-lookup"><span data-stu-id="ad053-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Hinnapakkumise rea üksikasjad](media/project-9.png)
  
<span data-ttu-id="ad053-114">Kui loote hinnapakkumisest projekti, seostatakse projekt automaatselt hinnapakkumise reaga.</span><span class="sxs-lookup"><span data-stu-id="ad053-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="ad053-115">Projekti prognooside komponendid</span><span class="sxs-lookup"><span data-stu-id="ad053-115">Components of estimates in a project</span></span>

<span data-ttu-id="ad053-116">Ajakava abil saate töö jaotada ülesanneteks, hallata ülesannete hierarhiat, otsustada, milliseid ressursse on ülesande lõpule viimiseks vaja ja määrata ülesande lõpule viimiseks vajaliku panuse prognoosi.</span><span class="sxs-lookup"><span data-stu-id="ad053-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="ad053-117">Saate määrata töökoormuse ja ajastada prognoose, kui kasutate lehe **Projekt** vahekaardil **Ajakava** olevaid välju.</span><span class="sxs-lookup"><span data-stu-id="ad053-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="ad053-118">Kuna hinnakiri on projektiga seotud, arvutatakse finantskalkulatsioonid hinnakirjas määratletud omahindade ja müügihindade alusel.</span><span class="sxs-lookup"><span data-stu-id="ad053-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="ad053-119">Prognooside importimine projektist hinnapakkumisse</span><span class="sxs-lookup"><span data-stu-id="ad053-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="ad053-120">Pärast projekti prognooside määramist saate need importida hinnapakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="ad053-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="ad053-121">Projekti prognooside summeerimiseks kande tüübi, rolli või ülesande taseme järgi tehke lehe **Hinnapakkumise rea üksikasjad** ribal valik **Impordi prognoosidest**.</span><span class="sxs-lookup"><span data-stu-id="ad053-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
