---
title: Kataloogitoodete oma- ja müügihindade seadistamine – liht
description: Selles teemas kirjeldatakse tootekataloogi üksuste kulude ja müügihindade seadistamist.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764545"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="7fdb0-103">Kataloogitoodete oma- ja müügihindade seadistamine – liht</span><span class="sxs-lookup"><span data-stu-id="7fdb0-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="7fdb0-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="7fdb0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7fdb0-105">Tootekataloogi üksuste hinnakujunduse seadistamine rakenduses Dynamics 365 Project Operations on sama nagu rakenduses Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="7fdb0-106">Project Operationsis ei saa tooteid hinnata ega projektides kasutada, seega ei pea tootekataloogi hindasid hinnapakkumiste ja lepingute jaoks projekti hinnakirjades seadistama.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="7fdb0-107">Tootekataloogi hindade seadistamiseks kasutage hinnapakkumise, lepingu või konto välja **Toote hind**.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="7fdb0-108">Ärge seadistage tootekataloogi hindasid projekti hinnakirjades.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="7fdb0-109">Projekti hinnakirjad on eksklusiivsed Project Operationsile.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="7fdb0-110">Rakendusepõhine äriloogika kopeerib hinnakirjad hinnapakkumisest lepingusse.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="7fdb0-111">Tulemuseks on lepingupõhine projekti hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="7fdb0-112">Kopeerimistoiming võib lükata edasi hinnapakkumise võitmise protsessi, kui projekti hinnakiri hinnapakkumisel läheb liiga suureks.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="7fdb0-113">Toodete hinnakirja ei kopeerita lepingutele kohandatud hinnakirjade loomiseks.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="7fdb0-114">Kuna kopeerimist pole kasutatud, siis hinnapakkumise protsessi jõudlust see ei mõjuta.</span><span class="sxs-lookup"><span data-stu-id="7fdb0-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
