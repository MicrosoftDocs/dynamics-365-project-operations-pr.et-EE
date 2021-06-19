---
title: Oskuste ja oskustaseme mudelid
description: Selles teemas antakse teavet oskuste ja oskustaseme mudelite kasutamise kohta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008666"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="5925b-103">Oskuste ja oskustaseme mudelid</span><span class="sxs-lookup"><span data-stu-id="5925b-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5925b-104">Oskused on ressursi tunnused, mis on ühiskasutuses rakenduse Dynamics 365 Project Service Automation ja (kui on olemas) rakenduse Dynamics 365 Field Service vahel.</span><span class="sxs-lookup"><span data-stu-id="5925b-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="5925b-105">Oskuste hoidla säilitamiseks rakenduses Project Service Automation tehke valikud **Ressursid** \> **Ressursi oskused**.</span><span class="sxs-lookup"><span data-stu-id="5925b-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Ressursi oskused](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="5925b-107">Kasutage ressursside hindamiseks oskustaseme mudeleid</span><span class="sxs-lookup"><span data-stu-id="5925b-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="5925b-108">Ressursside oskusi hinnatakse oskustaseme mudelitega.</span><span class="sxs-lookup"><span data-stu-id="5925b-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="5925b-109">Individuaalsed hinnangud on oskustaseme mudelis.</span><span class="sxs-lookup"><span data-stu-id="5925b-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="5925b-110">Oskustaseme mudeli loomiseks tehke valikud **Ressursid** \> **Oskustaseme mudelid**, ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5925b-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="5925b-111">Määrake uues hindamismudelis minimaalne hinnangu väärtus, maksimaalne hinnangu väärtus ja hinnatav olem.</span><span class="sxs-lookup"><span data-stu-id="5925b-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="5925b-112">Andmeruudustikus **Hinnangu väärtused** saate määratleda erinevad hinnangu väärtused, minimaalsest maksimaalseni.</span><span class="sxs-lookup"><span data-stu-id="5925b-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimaalsed ja maksimaalsed hinnangud on määratletud](media/Resource-Management-image85.png)

<span data-ttu-id="5925b-114">Need hinnangu väärtused kuvatakse filtrites **Ressursinõuded**, **Ajakavapaneel** ja **Ajakava abimees**.</span><span class="sxs-lookup"><span data-stu-id="5925b-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]