---
title: Kataloogitoodete oma- ja müügihindade seadistamine – liht
description: Selles teemas kirjeldatakse tootekataloogi üksuste kulude ja müügihindade seadistamist.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176696"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="2ae6e-103">Kataloogitoodete oma- ja müügihindade seadistamine – liht</span><span class="sxs-lookup"><span data-stu-id="2ae6e-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="2ae6e-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="2ae6e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2ae6e-105">Tootekataloogi üksuste hinnakujunduse seadistamine Dynamics 365 Project Operationsis on sama, mis Dynamics 365 Salesis.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="2ae6e-106">Kuna tooteid ei saa prognoosida ega kasutada Project Operationsi projektides, ei pea seadistama tootekataloogi hindu hinnapakkumiste ja lepingute projekti hinnakirjadele.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="2ae6e-107">Tootekataloogi hinnad tuleks seadistada hinnapakkumise, lepingu või konto väljal **Toote hind**.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="2ae6e-108">Ärge seadistage tootekataloogi hindu nende olemite projekti hinnakirjades.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="2ae6e-109">Projekti hinnakirjad on eksklusiivsed Project Operationsile.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="2ae6e-110">Seal on rakendusele omane äriloogika, mis kopeerib hinnakirjad hinnapakkumisest lepingule.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="2ae6e-111">Tulemuseks on lepingupõhine projekti hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="2ae6e-112">Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="2ae6e-113">Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="2ae6e-114">See tähendab, et toodete hinnakiri ei mõjuta hinnapakkumise võitmise protsessi tulemuslikkust.</span><span class="sxs-lookup"><span data-stu-id="2ae6e-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
