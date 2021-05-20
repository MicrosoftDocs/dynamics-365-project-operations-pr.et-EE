---
title: Tootepõhise müügivõimaluse read – liht
description: Selles teemas antakse teavet tootepõhiste müügivõimaluste ridade kohta Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949539"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="14e01-103">Tootepõhise müügivõimaluse read – liht</span><span class="sxs-lookup"><span data-stu-id="14e01-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="14e01-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="14e01-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="14e01-105">Tootepõhised müügivõimaluse read on müügivõimaluse rea üksused.</span><span class="sxs-lookup"><span data-stu-id="14e01-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="14e01-106">Need spetsiaalsed reaüksused on lõplikul kliendile esitataval arvel.</span><span class="sxs-lookup"><span data-stu-id="14e01-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="14e01-107">Arve ei sisalda muid lisateenuseid.</span><span class="sxs-lookup"><span data-stu-id="14e01-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="14e01-108">Seostatud kulutamist ja tarbimist ei jälgita ühegi seostuva projekti tööülesannetes.</span><span class="sxs-lookup"><span data-stu-id="14e01-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="14e01-109">Tootepõhised read võivad olla kataloogiüksused või sisestatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="14e01-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="14e01-110">Enamik müügivõimaluse tootepõhistest funktsioonidest järgib rakenduse Dynamics 365 Sales antud funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="14e01-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="14e01-111">Lisateavet tootepõhiste müügivõimaluste ridade kohta leiate teemast [Toodete lisamine müügivõimalusse](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="14e01-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="14e01-112">**Kliendi eelarve** on mõiste, mis on seotud projektipõhise müügivõimaluse ridadega.</span><span class="sxs-lookup"><span data-stu-id="14e01-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="14e01-113">Väli **Kliendi eelarve** jälgib summat, mida klient on nõus üksuse eest tasuma.</span><span class="sxs-lookup"><span data-stu-id="14e01-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="14e01-114">Kui müügivõimaluse kokkuvõtte tulumeetod on **Süsteemi arvutatud**, siis summeeritakse kliendi eelarve väärtused kõigilt müügivõimaluse ridadelt, et arvutada prognoositav tulu.</span><span class="sxs-lookup"><span data-stu-id="14e01-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]