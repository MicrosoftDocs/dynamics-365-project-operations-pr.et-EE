---
title: Ressursi prognoosid
description: See teema sisaldab teavet selle kohta, kuidas Project Operationsis ressursiprognoose arvutatakse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286513"
---
# <a name="resource-estimates"></a><span data-ttu-id="63bd8-103">Ressursi prognoosid</span><span class="sxs-lookup"><span data-stu-id="63bd8-103">Resource estimates</span></span>

<span data-ttu-id="63bd8-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="63bd8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63bd8-105">Ressursiprognoosid pärinevad ajafaasiga jõupingutustest, mis on määratletud tööjaotuse struktuuris koos kohaldatavate hinnakujunduse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="63bd8-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="63bd8-106">Tavaliselt on arvutuseks **kiirus/hr iga rolli jaoks x tunnid.**</span><span class="sxs-lookup"><span data-stu-id="63bd8-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="63bd8-107">Iga ressursi ajafaasiga jõupingutus salvestatakse ressursi määramise kirjesse.</span><span class="sxs-lookup"><span data-stu-id="63bd8-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="63bd8-108">Hinnastus salvestatakse eelmääratletud hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="63bd8-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="63bd8-109">Ühiku teisendust rakendatakse vastavalt kehtivale hinnakirjale.</span><span class="sxs-lookup"><span data-stu-id="63bd8-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ressursi prognoosid](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="63bd8-111">Vaikimisi omahinna ja kulu valuuta</span><span class="sxs-lookup"><span data-stu-id="63bd8-111">Default cost price and cost currency</span></span>

<span data-ttu-id="63bd8-112">Omahinna vaikeväärtused määratakse organisatsiooni üksusest.</span><span class="sxs-lookup"><span data-stu-id="63bd8-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="63bd8-113">Arvelduskulu ja müügivaluuta vaikeväärtused</span><span class="sxs-lookup"><span data-stu-id="63bd8-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="63bd8-114">Müügihindu rakendatakse üks kord tehingu kohta.</span><span class="sxs-lookup"><span data-stu-id="63bd8-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="63bd8-115">Müügihinna loendi vaikesätete hierarhia on järgmine.</span><span class="sxs-lookup"><span data-stu-id="63bd8-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="63bd8-116">Organisatsioon</span><span class="sxs-lookup"><span data-stu-id="63bd8-116">Organization</span></span>
2. <span data-ttu-id="63bd8-117">Klient</span><span class="sxs-lookup"><span data-stu-id="63bd8-117">Customer</span></span>
3. <span data-ttu-id="63bd8-118">Hinnapakkumine/leping</span><span class="sxs-lookup"><span data-stu-id="63bd8-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]