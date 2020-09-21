---
title: Demoandmetega katsetamine
description: Kuidas Project Service Automation demoandmeid alla laadida ja nendega katsetada?
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b195e5c8-63bc-4e90-914c-f29b8d565942
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 76dd5ff14cbafbfc5341885f0469a6e3e71dd66f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750998"
---
# <a name="experiment-with-demo-data-project-service"></a><span data-ttu-id="69b15-103">Demoandmetega katsetamine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="69b15-103">Experiment with demo data (Project Service)</span></span>

<span data-ttu-id="69b15-104">Rakenduse Dynamics 365 Project Service Automation võimalustega tutvumiseks on hea, kui teil on eelnevalt konfigureeritud keskkond, mida uurida.</span><span class="sxs-lookup"><span data-stu-id="69b15-104">To become familiar with Dynamics 365 Project Service Automation, it’s useful to have a pre-configured environment to explore.</span></span> <span data-ttu-id="69b15-105">Selleks otstarbeks oleme loonud eraldi näidisandmete installipaketi (hetkel ainult inglise keeles), mille abil on neid lahendusi lihtsam õppida.</span><span class="sxs-lookup"><span data-stu-id="69b15-105">For this purpose, we’ve created a separate sample data installation package (English-language only at this time) that makes it easier to learn about these solutions.</span></span> 

<span data-ttu-id="69b15-106">Installipakett on saadaval [Microsofti allalaadimiskeskuses](https://go.microsoft.com/fwlink/?linkid=859966).</span><span class="sxs-lookup"><span data-stu-id="69b15-106">The installation package is available on the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966).</span></span>  

<span data-ttu-id="69b15-107">Package Deployer installi käivitamine teeb järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="69b15-107">Running the Package Deployer install performs the following actions:</span></span> 
  
-   <span data-ttu-id="69b15-108">Loob või määrab väärtused, mis ajendavad Project Service'i käitumist</span><span class="sxs-lookup"><span data-stu-id="69b15-108">Creates or sets default parameters that drive behavior of Project Service</span></span>  
  
-   <span data-ttu-id="69b15-109">Impordib näidisandmed, nagu broneeritavad ressursid, rollid, müügi ja omahinna hinnakirjad, organisatsiooniüksused, asjakohased müügiprotsessi kirjed, töökorraldused ja projektid</span><span class="sxs-lookup"><span data-stu-id="69b15-109">Imports sample data such as Bookable Resources, Roles, Sales and Cost Price lists, Organizational Units, relevant sales process records, Work Orders and Projects</span></span>    
  
> [!IMPORTANT]
> <span data-ttu-id="69b15-110">**Demoandmeid ei saa ühelgi moel desinstallida.**</span><span class="sxs-lookup"><span data-stu-id="69b15-110">**There is no way to un-install the demo data.**</span></span> <span data-ttu-id="69b15-111">Seetõttu kasutage seda paketti ainult süsteemide demonstreerimiseks, hindamiseks, koolitamiseks ja testimiseks.</span><span class="sxs-lookup"><span data-stu-id="69b15-111">Therefore, you should only use this package on demonstration, evaluation, training and test systems.</span></span>

<span data-ttu-id="69b15-112">Lisateabe saamiseks vt seda [blogi](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span><span class="sxs-lookup"><span data-stu-id="69b15-112">For more information, see this [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span></span>





  
### <a name="see-also"></a><span data-ttu-id="69b15-113">Vt ka</span><span class="sxs-lookup"><span data-stu-id="69b15-113">See Also</span></span>  
 <span data-ttu-id="69b15-114">[Administraatori juhend](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="69b15-114">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="69b15-115">[Kontohalduri juhend](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="69b15-115">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="69b15-116">[Projektijuhi juhend](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="69b15-116">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="69b15-117">[Ressursihalduri juhend](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="69b15-117">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="69b15-118">Aja-, kulu- ja koostööjuhend</span><span class="sxs-lookup"><span data-stu-id="69b15-118">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
