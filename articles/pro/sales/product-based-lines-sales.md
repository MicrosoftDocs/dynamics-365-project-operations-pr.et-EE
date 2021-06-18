---
title: Tootepõhise müügivõimaluse read – liht
description: Selles teemas antakse teavet tootepõhiste müügivõimaluste ridade kohta Project Operationsis.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994491"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="7c04d-103">Tootepõhise müügivõimaluse read – liht</span><span class="sxs-lookup"><span data-stu-id="7c04d-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="7c04d-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="7c04d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7c04d-105">Tootepõhised müügivõimaluse read on müügivõimaluse rea üksused.</span><span class="sxs-lookup"><span data-stu-id="7c04d-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="7c04d-106">Need spetsiaalsed reaüksused on lõplikul kliendile esitataval arvel.</span><span class="sxs-lookup"><span data-stu-id="7c04d-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="7c04d-107">Arve ei sisalda muid lisateenuseid.</span><span class="sxs-lookup"><span data-stu-id="7c04d-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="7c04d-108">Seostatud kulutamist ja tarbimist ei jälgita ühegi seostuva projekti tööülesannetes.</span><span class="sxs-lookup"><span data-stu-id="7c04d-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="7c04d-109">Tootepõhised read võivad olla kataloogiüksused või sisestatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="7c04d-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="7c04d-110">Enamik müügivõimaluse tootepõhistest funktsioonidest järgib rakenduse Dynamics 365 Sales antud funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="7c04d-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="7c04d-111">Lisateavet tootepõhiste müügivõimaluste ridade kohta leiate teemast [Toodete lisamine müügivõimalusse](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="7c04d-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="7c04d-112">**Kliendi eelarve** on mõiste, mis on seotud projektipõhise müügivõimaluse ridadega.</span><span class="sxs-lookup"><span data-stu-id="7c04d-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="7c04d-113">Väli **Kliendi eelarve** jälgib summat, mida klient on nõus üksuse eest tasuma.</span><span class="sxs-lookup"><span data-stu-id="7c04d-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="7c04d-114">Kui müügivõimaluse kokkuvõtte tulumeetod on **Süsteemi arvutatud**, siis summeeritakse kliendi eelarve väärtused kõigilt müügivõimaluse ridadelt, et arvutada prognoositav tulu.</span><span class="sxs-lookup"><span data-stu-id="7c04d-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]