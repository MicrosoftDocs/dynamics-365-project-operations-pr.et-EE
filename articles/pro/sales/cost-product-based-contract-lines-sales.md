---
title: Tootepõhiste lepinguridade kulu – liht
description: Selles teemas antakse teavet loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177236"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="98b01-103">Tootepõhiste lepinguridade kulu – liht</span><span class="sxs-lookup"><span data-stu-id="98b01-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="98b01-104">_**Kohaldub:** lihtjuurutus – tehing näidisarvelusega_</span><span class="sxs-lookup"><span data-stu-id="98b01-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="98b01-105">Dynamics 365 Project Operationsi tootepõhised lepinguread sisaldavad välja **Omahind**, mis salvestab toote omahinna tootmisahela järgmise etapi kasumi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="98b01-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="98b01-106">Kui kataloogitoote jaoks on loodud projektipõhine lepingurida, võetakse projektipõhise lepingurea kulu vaikimisi tootekataloogi väljalt **Standardne kulu**.</span><span class="sxs-lookup"><span data-stu-id="98b01-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="98b01-107">Tootekataloogi väli **Standardkulu** seadistatakse organisatsiooni põhivaluutas.</span><span class="sxs-lookup"><span data-stu-id="98b01-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="98b01-108">Kui ühiku omahind on lepingureal vaikimisi määratud, teisendatakse see lepingus toodud müügivaluutaks.</span><span class="sxs-lookup"><span data-stu-id="98b01-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="98b01-109">Tootepõhise lepingurea ühiku omahind</span><span class="sxs-lookup"><span data-stu-id="98b01-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="98b01-110">Tootepõhise lepingurea ühiku omahind võimaldada iga ühiku müügi jaoks erineva toote omahinna.</span><span class="sxs-lookup"><span data-stu-id="98b01-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="98b01-111">Kuigi see ei ole alati vajalik, on olemas teatud stsenaariumid, mille korral tarnija teeb toote omahinna osas kliendile allahindluse.</span><span class="sxs-lookup"><span data-stu-id="98b01-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="98b01-112">Siin on ühe võimaliku stsenaariumi näide.</span><span class="sxs-lookup"><span data-stu-id="98b01-112">Consider the following scenario:</span></span>

<span data-ttu-id="98b01-113">Fabrikami robootika installib ettevõtte Adatum Corporation koosteliinidele robotõlgasid.</span><span class="sxs-lookup"><span data-stu-id="98b01-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="98b01-114">Fabrikami pakub paigaldusteenused, kuid robotõlgade tootja on Trey Research.</span><span class="sxs-lookup"><span data-stu-id="98b01-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="98b01-115">Kui ettevõtte Adatum Corporation poolt paigaldatavad robotõlad avavad ettevõtte Trey Research jaoks uue tööstusharu, võib Trey anda Fabrikamile selle kokkuleppe jaoks eriallahindluse.</span><span class="sxs-lookup"><span data-stu-id="98b01-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="98b01-116">Sel juhul loob Fabrikam tootepõhise lepingurea robotõlgadele ja sisenditele, mis on seotud selle lepingu ühe ühiku omahinnaga, mis erineb robotõlgade jaoks määratud standardsest omahinnast Trey Researchis.</span><span class="sxs-lookup"><span data-stu-id="98b01-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
