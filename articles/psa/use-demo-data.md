---
title: Demoandmetega katsetamine
description: Kuidas Project Service Automation demoandmeid alla laadida ja nendega katsetada?
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
ms.openlocfilehash: e1f3ebf8d0cd6c8e25fcab6775cd92d544867af8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151113"
---
# <a name="experiment-with-demo-data-project-service"></a><span data-ttu-id="0f3cc-103">Demoandmetega katsetamine (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0f3cc-103">Experiment with demo data (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0f3cc-104">Rakenduse Dynamics 365 Project Service Automation võimalustega tutvumiseks on hea, kui teil on eelnevalt konfigureeritud keskkond, mida uurida.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-104">To become familiar with Dynamics 365 Project Service Automation, it’s useful to have a pre-configured environment to explore.</span></span> <span data-ttu-id="0f3cc-105">Selleks otstarbeks oleme loonud eraldi näidisandmete installipaketi (hetkel ainult inglise keeles), mille abil on neid lahendusi lihtsam õppida.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-105">For this purpose, we’ve created a separate sample data installation package (English-language only at this time) that makes it easier to learn about these solutions.</span></span> 

<span data-ttu-id="0f3cc-106">Installipakett on saadaval [Microsofti allalaadimiskeskuses](https://go.microsoft.com/fwlink/?linkid=859966).</span><span class="sxs-lookup"><span data-stu-id="0f3cc-106">The installation package is available on the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966).</span></span>  

<span data-ttu-id="0f3cc-107">Package Deployer installi käivitamine teeb järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-107">Running the Package Deployer install performs the following actions:</span></span> 
  
-   <span data-ttu-id="0f3cc-108">Loob või määrab väärtused, mis ajendavad Project Service'i käitumist</span><span class="sxs-lookup"><span data-stu-id="0f3cc-108">Creates or sets default parameters that drive behavior of Project Service</span></span>  
  
-   <span data-ttu-id="0f3cc-109">Impordib näidisandmed, nagu broneeritavad ressursid, rollid, müügi ja omahinna hinnakirjad, organisatsiooniüksused, asjakohased müügiprotsessi kirjed, töökorraldused ja projektid</span><span class="sxs-lookup"><span data-stu-id="0f3cc-109">Imports sample data such as Bookable Resources, Roles, Sales and Cost Price lists, Organizational Units, relevant sales process records, Work Orders and Projects</span></span>    
  
> [!IMPORTANT]
> <span data-ttu-id="0f3cc-110">**Demoandmeid ei saa ühelgi moel desinstallida.**</span><span class="sxs-lookup"><span data-stu-id="0f3cc-110">**There is no way to un-install the demo data.**</span></span> <span data-ttu-id="0f3cc-111">Seetõttu kasutage seda paketti ainult süsteemide demonstreerimiseks, hindamiseks, koolitamiseks ja testimiseks.</span><span class="sxs-lookup"><span data-stu-id="0f3cc-111">Therefore, you should only use this package on demonstration, evaluation, training and test systems.</span></span>

<span data-ttu-id="0f3cc-112">Lisateabe saamiseks vt seda [blogi](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span><span class="sxs-lookup"><span data-stu-id="0f3cc-112">For more information, see this [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span></span>





  
### <a name="see-also"></a><span data-ttu-id="0f3cc-113">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0f3cc-113">See Also</span></span>  
 <span data-ttu-id="0f3cc-114">[Administraatori juhend](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f3cc-114">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="0f3cc-115">[Kontohalduri juhend](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f3cc-115">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="0f3cc-116">[Projektijuhi juhend](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f3cc-116">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="0f3cc-117">[Ressursihalduri juhend](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0f3cc-117">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="0f3cc-118">Aja-, kulu- ja koostööjuhend</span><span class="sxs-lookup"><span data-stu-id="0f3cc-118">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
