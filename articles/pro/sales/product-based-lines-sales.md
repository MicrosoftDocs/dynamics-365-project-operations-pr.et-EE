---
title: Tootepõhised müügivõimaluse read
description: Selles teemas antakse teavet tootepõhiste müügivõimaluste ridade kohta Project Operationsis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074882"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="30965-103">Tootepõhised müügivõimaluse read</span><span class="sxs-lookup"><span data-stu-id="30965-103">Product-based opportunity lines</span></span>

<span data-ttu-id="30965-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="30965-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="30965-105">Tootepõhised müügivõimaluse read on müügivõimaluse rea üksused.</span><span class="sxs-lookup"><span data-stu-id="30965-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="30965-106">Need read toimetatakse kliendile konkreetsete reaüksustena lõplikul arvel ilma muude lisandväärtustega teenusteta.</span><span class="sxs-lookup"><span data-stu-id="30965-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="30965-107">Seostatud kulutamist ja tarbimist ei jälgita ühegi seostuva projekti tööülesannetes.</span><span class="sxs-lookup"><span data-stu-id="30965-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="30965-108">Tootepõhised read võivad olla kataloogiüksused või sisestatavad tooted.</span><span class="sxs-lookup"><span data-stu-id="30965-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="30965-109">Enamik müügivõimaluse tootepõhistest funktsioonidest järgib rakenduse Dynamics 365 Sales antud funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="30965-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="30965-110">Lisateavet tootepõhiste müügivõimaluste ridade kohta leiate teemast [Toodete lisamine müügivõimalusse](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="30965-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="30965-111">Üks kontseptsioon tootepõhiste müügivõimaluse ridade kohta, mis on seotud projektipõhiste müügivõimalustega, on **Kliendi eelarve**.</span><span class="sxs-lookup"><span data-stu-id="30965-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="30965-112">Selle välja abil saate jälgida summat, mille klient on valmis selle reaüksuse eest maksma.</span><span class="sxs-lookup"><span data-stu-id="30965-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="30965-113">Kui müügivõimaluse kokkuvõtte tulu meetodi väärtuseks on seatud **Süsteemi arvutatud** , summeeritakse prognoositava tulu arvutamiseks kõik toote-ja projekti-põhistes ridades olevad kliendi eelarve väärtused.</span><span class="sxs-lookup"><span data-stu-id="30965-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
