---
title: Ressursitaotluse esitamine
description: Selles teemas antakse teavet projekti ressursi taotluse esitamise kohta.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013166"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="7680c-103">Ressursitaotluse esitamine</span><span class="sxs-lookup"><span data-stu-id="7680c-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7680c-104">Saate loodud ressursinõude esitada ressursitaotlusena.</span><span class="sxs-lookup"><span data-stu-id="7680c-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="7680c-105">Taotlus saadetakse seejärel täitmiseks ressursihaldurile.</span><span class="sxs-lookup"><span data-stu-id="7680c-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="7680c-106">Broneeritavate ressursside loendi nägemiseks klõpsake Project Service Automation (PSA) lehel **Projektid** vahekaarti **Meeskond**.</span><span class="sxs-lookup"><span data-stu-id="7680c-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="7680c-107">Valige üldine ressurss, millel on olemas ressursinõue loendist, ja seejärel klõpsake valikut **Esita taotlus**.</span><span class="sxs-lookup"><span data-stu-id="7680c-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Ressursitaotluse esitamine](media/RM-how-to-18.png)

<span data-ttu-id="7680c-109">Üldise meeskonnaliikme taotluse olek muutub olekuks **Esitatud**.</span><span class="sxs-lookup"><span data-stu-id="7680c-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="7680c-110">Kui ressursihaldur on taotluse ära täitnud, asendatakse loodud ressurss nimega ressurssiga – seda juhul, kui ressursihaldur täidab nimega ressursi broneeringuga taotluse.</span><span class="sxs-lookup"><span data-stu-id="7680c-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="7680c-111">Muidu jääb meeskonnale üldine ressurss ja taotluse olekuks seatakse **Vajab ülevaatamist**, kui ressursihaldur on teinud nimega ressursi ettepaneku.</span><span class="sxs-lookup"><span data-stu-id="7680c-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]