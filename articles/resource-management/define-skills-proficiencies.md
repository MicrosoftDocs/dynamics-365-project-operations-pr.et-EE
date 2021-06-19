---
title: Oskuste ja pädevuste määratlemine
description: Selles teemas antakse teavet, kuidas häälestada ressursside hindamiseks oskustaseme mudelid.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015326"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="4a714-103">Oskuste ja pädevuste määratlemine</span><span class="sxs-lookup"><span data-stu-id="4a714-103">Define skills and proficiencies</span></span>

<span data-ttu-id="4a714-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="4a714-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4a714-105">Oskused on ressursi tunnused, mis on ühiskasutuses rakenduse Dynamics 365 Project Operations ja (kui on olemas) rakenduse Dynamics 365 Field Service vahel.</span><span class="sxs-lookup"><span data-stu-id="4a714-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="4a714-106">Oskuste hoidla säilitamiseks rakenduses Project Operations avage **Ressursid** \> **Ressursi oskused**.</span><span class="sxs-lookup"><span data-stu-id="4a714-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="4a714-107">Kasutage ressursside hindamiseks oskustaseme mudeleid</span><span class="sxs-lookup"><span data-stu-id="4a714-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="4a714-108">Ressursside oskusi hinnatakse oskustaseme mudelitega.</span><span class="sxs-lookup"><span data-stu-id="4a714-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="4a714-109">Individuaalsed hinnangud on oskustaseme mudelis.</span><span class="sxs-lookup"><span data-stu-id="4a714-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="4a714-110">Oskustaseme mudeli loomiseks tehke valikud **Ressursid** \> **Oskustaseme mudelid**, ja seejärel valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4a714-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="4a714-111">Määrake uues hindamismudelis minimaalne hinnangu väärtus, maksimaalne hinnangu väärtus ja hinnatav olem.</span><span class="sxs-lookup"><span data-stu-id="4a714-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="4a714-112">Andmeruudustikus **Hinnangu väärtused** saate määratleda erinevad hinnangu väärtused, minimaalsest maksimaalseni.</span><span class="sxs-lookup"><span data-stu-id="4a714-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="4a714-113">Need hinnangu väärtused kuvatakse filtrites **Ressursinõuded**, **Ajakavapaneel** ja **Ajakava abimees**.</span><span class="sxs-lookup"><span data-stu-id="4a714-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]