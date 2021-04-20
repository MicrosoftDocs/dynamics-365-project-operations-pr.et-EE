---
title: Hinnakirjade inaktiveerimine
description: Selles teemas kirjeldatakse, kuidas kasutamata või vanad hinnakirjad inaktiveerida või eemaldada.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701924"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="e7e27-103">Hinnakirjade inaktiveerimine</span><span class="sxs-lookup"><span data-stu-id="e7e27-103">Deactivate price lists</span></span> 

<span data-ttu-id="e7e27-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="e7e27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7e27-105">Vanade või kasutamata hinnakirjade rakendusest Dynamics 365 Project Operations eemaldamiseks peate läbima kaks etappi.</span><span class="sxs-lookup"><span data-stu-id="e7e27-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="e7e27-106">Eemaldage või kustutage hinnakiri konkreetsetelt lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="e7e27-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="e7e27-107">Inaktiveerige või kustutage hinnakiri lehe **Hinnakirjad** aktiivsete hinnakirjade seast.</span><span class="sxs-lookup"><span data-stu-id="e7e27-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="e7e27-108">Hinnakirja täielikuks eemaldamiseks peate läbima mõlemad toimingud.</span><span class="sxs-lookup"><span data-stu-id="e7e27-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="e7e27-109">Ainult 2. etapi läbimisel, mis on mõeldud hinnakirja vaates Aktiivsed hinnakirjad otseseks kustutamiseks või inaktiveerimiseks, pole piisav.</span><span class="sxs-lookup"><span data-stu-id="e7e27-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="e7e27-110">Peate kustutama ka kõik selle hinnakirja seosed kõikide 1. etapis mainitud kohtadest.</span><span class="sxs-lookup"><span data-stu-id="e7e27-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="e7e27-111">Hinnakirja kustutamine konkreetsetel saitidel</span><span class="sxs-lookup"><span data-stu-id="e7e27-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="e7e27-112">Hinnakirja kustutamiseks Project Operationsist minge järgmistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="e7e27-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="e7e27-113">Leht **Projekti parameetrid** > vahekaart **Hinnakirjad**</span><span class="sxs-lookup"><span data-stu-id="e7e27-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="e7e27-114">Leht **Organisatsiooniüksus** > ruudustik **Hinnakirjad**</span><span class="sxs-lookup"><span data-stu-id="e7e27-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="e7e27-115">Leht **Konto** > ruudustik **Projekti hinnakirjad**</span><span class="sxs-lookup"><span data-stu-id="e7e27-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="e7e27-116">Leht **Projekti hinnapakkumised** > ruudustik **Projekti hinnakirjad**: see rakendub kõikidele aktiivsetele projekti hinnapakkumistele.</span><span class="sxs-lookup"><span data-stu-id="e7e27-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="e7e27-117">Leht **Projektilepingud** > ruudustik **Projekti hinnakirjad**: see rakendub kõikidele aktiivsetele projektilepingutele.</span><span class="sxs-lookup"><span data-stu-id="e7e27-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="e7e27-118">Peate iga lehe jaoks valima hinnakirja, mille soovite kustutada, ja seejärel valima nupu **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="e7e27-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="e7e27-119">Hinnakirja kustutamine või inaktiveerimine lehel Hinnakirjad</span><span class="sxs-lookup"><span data-stu-id="e7e27-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="e7e27-120">Hinnakirja kustutamiseks aktiivsete hinnakirjade seast, avage **Müük** > **Kohandatud** > **Hinnakirjad**.</span><span class="sxs-lookup"><span data-stu-id="e7e27-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="e7e27-121">Valige hinnakiri, mille soovite kustutada, ja seejärel valima nupu **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="e7e27-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="e7e27-122">Kui hinnakiri viitab mis tahes olemasolevale tehingule, ei saa te seda kustutada.</span><span class="sxs-lookup"><span data-stu-id="e7e27-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="e7e27-123">Kui nii juhtub, saate hinnakirja inaktiveerida, et seda ei kuvataks üheski vaates.</span><span class="sxs-lookup"><span data-stu-id="e7e27-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="e7e27-124">Hinnakirja inaktiveerimiseks valige hinnakiri uuesti ja valige seejärel **Inaktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="e7e27-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
