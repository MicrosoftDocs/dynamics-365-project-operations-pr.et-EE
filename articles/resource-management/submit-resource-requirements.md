---
title: Ressursitaotluse esitamine
description: Saate loodud ressursinõude esitada ressursitaotlusena. Taotlus saadetakse seejärel täitmiseks ressursihaldurile.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014021"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="e6d6b-104">Ressursitaotluse esitamine</span><span class="sxs-lookup"><span data-stu-id="e6d6b-104">Submit a resource request</span></span>

<span data-ttu-id="e6d6b-105">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="e6d6b-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6d6b-106">Saate loodud ressursinõude esitada ressursitaotlusena.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="e6d6b-107">Taotlus saadetakse seejärel täitmiseks ressursihaldurile.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="e6d6b-108">Broneeritavate ressursside loendi nägemiseks rakenduses Dynamics 365 Project Operations valige lehel **Projektid** vahekaart **Meeskond**.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="e6d6b-109">Valige üldine ressurss, millel on olemas ressursinõue loendist, ja seejärel klõpsake valikut **Esita taotlus**.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="e6d6b-110">Üldise meeskonnaliikme taotluse olek muutub olekuks **Esitatud**.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="e6d6b-111">Kui taotlus on täidetud, asendatakse loodud ressurss nimega ressurssiga – seda juhul, kui ressursihaldur täidab nimega ressursi broneeringuga taotluse.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="e6d6b-112">Muidu, kui ressursihaldur on teinud nimega ressursi ettepaneku, jääb meeskonnale üldine ressurss ja taotluse olekuks seatakse **Vajab ülevaatamist**.</span><span class="sxs-lookup"><span data-stu-id="e6d6b-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]