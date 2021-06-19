---
title: Müügi hinnakirja seadistamine
description: Selles teemas antakse teavet projekti hinnakujunduse müügi hinnakirjade kohta.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004886"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="9960b-103">Müügi hinnakirja seadistamine</span><span class="sxs-lookup"><span data-stu-id="9960b-103">Set up a sales price list</span></span>

<span data-ttu-id="9960b-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="9960b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9960b-105">Projekti hinnapakkumiste ja lepingute puhul on projekti hinnakirjas teistsugune hinna alistamise muster kui toodete hinnakirjas.</span><span class="sxs-lookup"><span data-stu-id="9960b-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="9960b-106">Tootekataloogil põhineval hinnapakkumise real saate hinna alistada rollidele ja kategooriatele otse pakkumise real, sest iga hinnapakkumise rida osutab täpselt ühele kataloogiüksusele.</span><span class="sxs-lookup"><span data-stu-id="9960b-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="9960b-107">Projektil põhineva hinnapakkumise ei saa te siiski otse hinnapakkumiste real olevate rollide ja kategooriate hinda alistada.</span><span class="sxs-lookup"><span data-stu-id="9960b-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="9960b-108">Võite kasutada projekti hinnakirja, et töötada kahe erineva alistamise mustriga.</span><span class="sxs-lookup"><span data-stu-id="9960b-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="9960b-109">Soovitame, et teil oleks oma projekti ressursside ja kataloogiüksuste jaoks eraldi hinnakiri nende kahe käitumise erinevuste tõttu, kui te alistate hinnakujunduse.</span><span class="sxs-lookup"><span data-stu-id="9960b-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="9960b-110">Kõigil järgmistest olemitest võib projekti hinnakujunduseks olla üks või mitu seotud müügi hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="9960b-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="9960b-111">Klient (konto)</span><span class="sxs-lookup"><span data-stu-id="9960b-111">Customer (account)</span></span> 
- <span data-ttu-id="9960b-112">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="9960b-112">Opportunity</span></span> 
- <span data-ttu-id="9960b-113">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="9960b-113">Quote</span></span> 
- <span data-ttu-id="9960b-114">Projektileping</span><span class="sxs-lookup"><span data-stu-id="9960b-114">Project Contract</span></span>

<span data-ttu-id="9960b-115">Nende olemite seotust hinnakirjaga näitavad projekti hinnakirjad.</span><span class="sxs-lookup"><span data-stu-id="9960b-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="9960b-116">Saate seostada ühe või mitu hinnakirja kliendi, müügivõimaluse, hinnapakkumise ja projekti lepingu müügi olemitega.</span><span class="sxs-lookup"><span data-stu-id="9960b-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="9960b-117">Vaikimisi projekti hinnakirja ei sisestata kliendi kirjesse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="9960b-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="9960b-118">Siiski saate projekti hinnakirja käsitsi manustada kliendi kirjele.</span><span class="sxs-lookup"><span data-stu-id="9960b-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="9960b-119">Sellegipoolest peaksite projekti hinnakirja käsitsi lisama ainult siis, kui teil on kliendiga kohandatud hinnakujunduse leping.</span><span class="sxs-lookup"><span data-stu-id="9960b-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="9960b-120">Kui projekti hinnakiri on seotud müügiesindaja, valideeritakse järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="9960b-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="9960b-121">Hinnakirjal on kontekst **Müük**.</span><span class="sxs-lookup"><span data-stu-id="9960b-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="9960b-122">Hinnakirja valuuta ühtima kliendi valuutaga.</span><span class="sxs-lookup"><span data-stu-id="9960b-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="9960b-123">Projekti lepingu järgmist järjestuss kasutatakse selleks, et seada seotud projekti hinnakiri automaatselt.</span><span class="sxs-lookup"><span data-stu-id="9960b-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="9960b-124">Hinnapakkumine</span><span class="sxs-lookup"><span data-stu-id="9960b-124">Quote</span></span>
2. <span data-ttu-id="9960b-125">Müügivõimalus</span><span class="sxs-lookup"><span data-stu-id="9960b-125">Opportunity</span></span>
3. <span data-ttu-id="9960b-126">Klient</span><span class="sxs-lookup"><span data-stu-id="9960b-126">Customer</span></span> 
4. <span data-ttu-id="9960b-127">Globaalsätted</span><span class="sxs-lookup"><span data-stu-id="9960b-127">Global settings</span></span> 

<span data-ttu-id="9960b-128">Kui projekti hinnakiri on vaikimisi sisestatud, kinnitab süsteem, et valuuta vastab kliendi valuutale ja et vaikimisi määratud hinnakirjad sisaldavad konteksti **Müük**.</span><span class="sxs-lookup"><span data-stu-id="9960b-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="9960b-129">Saate seostada mitu projekti hinnakirja kliendi, müügivõimaluse, hinnapakkumise ja projekti lepingu olemitega.</span><span class="sxs-lookup"><span data-stu-id="9960b-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="9960b-130">See võimalus toetab kuupäevapõhiseid vaikimisi hindu pikaajalise projektilepingu jaoks, mille puhul võib inflatsiooni tõttu tekkivate hinnavärskenduste arvestamiseks vajada mitut hinnakirja.</span><span class="sxs-lookup"><span data-stu-id="9960b-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="9960b-131">Kui aga kliendi, müügivõimaluse, hinnapakkumise või projekti lepingu olemiga seostatud hinnakiri sisaldab kattuvat jõustumiskuupäeva, võivad vaikimisi hinnad valed olla.</span><span class="sxs-lookup"><span data-stu-id="9960b-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="9960b-132">Seetõttu peaksite veenduma, et projekti hinnakiri, millel on kattuvad jõustumiskuupäevad, pole nende olemitega seostatud.</span><span class="sxs-lookup"><span data-stu-id="9960b-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]