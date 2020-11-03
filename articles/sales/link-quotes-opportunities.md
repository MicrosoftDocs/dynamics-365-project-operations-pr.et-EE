---
title: Projekti hinnapakkumiste loomine müügivõimalustest
description: Selles teemas antakse teavet müügivõimalusest projekti hinnapakkumise loomise kohta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074868"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="3031b-103">Projekti hinnapakkumiste loomine müügivõimalustest</span><span class="sxs-lookup"><span data-stu-id="3031b-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="3031b-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="3031b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3031b-105">Hinnapakkumisi saab luua projekti müügivõimalustest järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="3031b-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="3031b-106">Lehe **Projekti müügivõimalus** vahekaardilt **Hinnapakkumised**</span><span class="sxs-lookup"><span data-stu-id="3031b-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="3031b-107">Müügivõimaluse müügiprotsessi voost</span><span class="sxs-lookup"><span data-stu-id="3031b-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="3031b-108">Olemasoleva hinnapakkumise müügivõimaluse viidet värskendades</span><span class="sxs-lookup"><span data-stu-id="3031b-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="3031b-109">Projekti müügivõimaluse lehe vahekaardilt Hinnapakkumised</span><span class="sxs-lookup"><span data-stu-id="3031b-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="3031b-110">Müügivõimalusest projekti hinnapakkumise loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3031b-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="3031b-111">Avage leht **Projekti müügivõimalus** ja valige vahekaart **Hinnapakkumised**.</span><span class="sxs-lookup"><span data-stu-id="3031b-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="3031b-112">Valige andmeruudustikus **Hinnapakkumised** suvand **+** , et luua müügivõimaluse põhjal uus projekti hinnapakkumine.</span><span class="sxs-lookup"><span data-stu-id="3031b-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="3031b-113">Kõik müügivõimaluste read ja seotud projekti hinnakirjad kopeeritakse müügivõimalusest uude hinnapakkumisesse.</span><span class="sxs-lookup"><span data-stu-id="3031b-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="3031b-114">Müügivõimaluse müügiprotsessi voost</span><span class="sxs-lookup"><span data-stu-id="3031b-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="3031b-115">Müügivõimalusest müügiprotsessi voost hinnapakkumise loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3031b-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="3031b-116">Avage müügivõimaluse müügiprotsessi voos müügivõimalus.</span><span class="sxs-lookup"><span data-stu-id="3031b-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="3031b-117">Valige etapp **Kinnita sobivaks**.</span><span class="sxs-lookup"><span data-stu-id="3031b-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="3031b-118">Valige **Järgmine** ja valige seejärel **+ Loo** , et luua uus hinnapakkumine.</span><span class="sxs-lookup"><span data-stu-id="3031b-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="3031b-119">Enamus selle uue hinnapakkumise vahekaardil **Kokkuvõte** olevast teabest pärineb vaikimisi müügivõimalusest.</span><span class="sxs-lookup"><span data-stu-id="3031b-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="3031b-120">Sisestage kogu nõutud teave, mis puudub, või värskendage vastavalt vajadusele vahekaardil **Kokkuvõte** vaikimisi väärtused.</span><span class="sxs-lookup"><span data-stu-id="3031b-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="3031b-121">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3031b-121">Select **Save**.</span></span> <span data-ttu-id="3031b-122">Uus hinnapakkumine luuakse ja seostatakse müügivõimalusega.</span><span class="sxs-lookup"><span data-stu-id="3031b-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="3031b-123">Nüüd saate vaadata hinnapakkumise teavet lehe **Müügivõimalus** vahekaardil **Hinnapakkumised**.</span><span class="sxs-lookup"><span data-stu-id="3031b-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="3031b-124">Müügivõimaluse müügiprotsess liigub järgmisse etappi, **Soovitus**.</span><span class="sxs-lookup"><span data-stu-id="3031b-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="3031b-125">Olemasoleva hinnapakkumise müügivõimaluse viidet värskendades</span><span class="sxs-lookup"><span data-stu-id="3031b-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="3031b-126">Olemasoleva hinnapakkumise saab siduda müügivõimalusega.</span><span class="sxs-lookup"><span data-stu-id="3031b-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="3031b-127">Olemasoleva hinnapakkumise müügivõimaluse teabe värskendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3031b-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="3031b-128">Avage leht **Hinnapakkumine** ja valige vahekaart **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="3031b-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="3031b-129">Väljal **Müügivõimalus** valige müügivõimalus, mille soovite hinnapakkumisega siduda.</span><span class="sxs-lookup"><span data-stu-id="3031b-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="3031b-130">Hinnapakkumist saate vaadata müügivõimaluse ruudustikus **Hinnapakkumine**.</span><span class="sxs-lookup"><span data-stu-id="3031b-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="3031b-131">Müügivõimaluse müügiprotsessi kasutamisel saab müügivõimaluse teisaldada järgmisse etappi, **Soovitus**.</span><span class="sxs-lookup"><span data-stu-id="3031b-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="3031b-132">Kui teisaldate müügivõimaluse sellesse etappi, saate selle hinnapakkumise valida selle müügivõimalusega seostatud hinnapakkumiste loendist.</span><span class="sxs-lookup"><span data-stu-id="3031b-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="3031b-133">Selle hinnapakkumise valimine näitab, et liigute sellega edasi.</span><span class="sxs-lookup"><span data-stu-id="3031b-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="3031b-134">Kõik teised müügivõimalusega seotud hinnapakkumised on endiselt saadaval ja aktiivsed, kuni üks neist on võidetud.</span><span class="sxs-lookup"><span data-stu-id="3031b-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="3031b-135">Saate liigutada müügiprotsessi tagasi eelmisesse etappi ( **Kinnita sobivakd** ) ja valida mõne muu hinnapakkumise sellega edasi liikumiseks.</span><span class="sxs-lookup"><span data-stu-id="3031b-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
