---
title: Miks on tegeliku ajakulu vaikeväärtus null?
description: Tõrkeotsing, miks on tegeliku ajakulu vaikeväärtus 0.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3751069"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="be6b3-103">Miks on tegeliku ajakulu vaikeväärtus null?</span><span class="sxs-lookup"><span data-stu-id="be6b3-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="be6b3-104">See KKK kehtib sellise tegeliku kulu maksumuse puhul, mille kande liigiks on määratud Aeg ja kande tüübiks Kulu.</span><span class="sxs-lookup"><span data-stu-id="be6b3-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="be6b3-105">Alltoodud kolm kontrolli aitavad leida lahenduse, miks on tegeliku ajakulu vaikeväärtus 0.</span><span class="sxs-lookup"><span data-stu-id="be6b3-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="be6b3-106">1. kontroll: projekti omahinnakirja tuvastamine</span><span class="sxs-lookup"><span data-stu-id="be6b3-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="be6b3-107">Leidke projekt tegeliku näitaja projektiväljalt ja minge siis projekti lehele.</span><span class="sxs-lookup"><span data-stu-id="be6b3-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="be6b3-108">Klõpsake väljal lepingut sõlmiva üksuse linki.</span><span class="sxs-lookup"><span data-stu-id="be6b3-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="be6b3-109">Kontrollige lehel Lepingut sõlmiv üksus, kas lepingut sõlmival üksusel on omahinnakirjade ruudustikus hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="be6b3-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="be6b3-110">Kui seal on rohkem kui üks hinnakiri, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="be6b3-111">Project Service'is on ühe organisatsiooniüksuse kohta toetatud ainult üks hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="be6b3-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="be6b3-112">Eemaldage sellest olemist kõik hinnakirjad, kuni organisatsiooniüksuse omahinnakirjade ruudustikku jääb alles ainult üks manustatud hinnakiri.</span><span class="sxs-lookup"><span data-stu-id="be6b3-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="be6b3-113">Kui organisatsiooniüksusele pole manustatud ühtki hinnakirja, jätke meelde organisatsiooniüksuse valuuta.</span><span class="sxs-lookup"><span data-stu-id="be6b3-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="be6b3-114">Minge rakendusse Project Service, seejärel valige Parameetrid ja avage vahekaart Hinnakirjad. Kontrollige, kas mõne hinnakirja kontekstiväljaks on määratud Kulu ja kas valuuta kattub organisatsiooniüksuse valuutaga.</span><span class="sxs-lookup"><span data-stu-id="be6b3-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="be6b3-115">Kui ühtki sellisele kriteeriumile vastavat hinnakirja pole, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="be6b3-116">Veenduge, et teil oleks vähemalt üks hinnakiri, mille kontekstiks on määratud Kulu, ja valuuta kattuks organisatsiooniüksuse valuutaga.</span><span class="sxs-lookup"><span data-stu-id="be6b3-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="be6b3-117">Kui sellisele kriteeriumile vastab rohkem kui üks hinnakiri, jätkake dokumendi lugemist ja tehke järgmised kontrollid.</span><span class="sxs-lookup"><span data-stu-id="be6b3-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="be6b3-118">2. kontroll: kas mõni ülalpool tuvastatud hinnakirjadest kehtib tegeliku ajakulu kindlal kuupäeval?</span><span class="sxs-lookup"><span data-stu-id="be6b3-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="be6b3-119">Selleks et Project Service'is arvestataks hinnakiri hinna vaikeväärtuseks, peab see hinnakiri rakenduma tegeliku ajakulu kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="be6b3-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="be6b3-120">Kongtrollige järgmist, et näha, kas ülalpool tuvastatud hinnakiri(hinnakirjad) rakenduvad.</span><span class="sxs-lookup"><span data-stu-id="be6b3-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="be6b3-121">Kontrollige, kas lisatud hinnakirjade üldisel vahekaardil olev algus- ja lõppkuupäev on täidetud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="be6b3-122">Kui ülalpool tuvastatud hinnakirjade algus- ja lõppkuupäevad on tühjad, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="be6b3-123">Jätke meelde tegeliku ajakulu alguskuupäev ja kontrollige, kas mõni tuvastatud hinnakirjadest rakendub sellel päeval.</span><span class="sxs-lookup"><span data-stu-id="be6b3-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="be6b3-124">Näiteks peaks tegeliku ajakulu kuupäev jääma hinnakirja algus- ja lõppkuupäeva vahele.</span><span class="sxs-lookup"><span data-stu-id="be6b3-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="be6b3-125">Kui ükski hinnakiri ei kata tegeliku ajakulu seda kuupäeva, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="be6b3-126">Muutke hinnakirja algus- ja lõppkuupäeva tagamaks, et hinnakiri kataks tegeliku ajakulu kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="be6b3-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="be6b3-127">Kui rohkem kui üks hinnakiri katab tegeliku ajakulu seda kuupäeva, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="be6b3-128">Saate selle parandada, kui redigeerite hinnakirja(de) algus- ja lõppkuupäevi selliselt, et alles jääb ainult üks hinnakiri, mis katab tegeliku ajakulu kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="be6b3-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="be6b3-129">Kui on ainult üks hinnakiri, mis katab tegeliku ajakulu kuupäeva, liikuge edasi järgmise dokumendis toodud kontrolli juurde.</span><span class="sxs-lookup"><span data-stu-id="be6b3-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="be6b3-130">Kui olete vajalikud parandused teinud, looge ajakirje uuesti, kinnitage see ja veenduge, et tegelikus ajakulus kuvataks kehtiv hind.</span><span class="sxs-lookup"><span data-stu-id="be6b3-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="be6b3-131">3. kontroll: kas hinnakirjas on tegeliku ajakulu hinnadimensioonidel hind?</span><span class="sxs-lookup"><span data-stu-id="be6b3-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="be6b3-132">Kui olete edukalt lõpetanud 1. ja 2. kontrolli, peaks teil nüüd alles olema ainult üks projekti hinnakiri, mis rakendub tegeliku ajakulu kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="be6b3-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="be6b3-133">Avage see hinnakiri ja minge vahekaardile Rolli hinnad. Veenduge, et tegeliku ajakulu hinnadimensioonidel oleks ruudustikus rida.</span><span class="sxs-lookup"><span data-stu-id="be6b3-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="be6b3-134">Kui rolli hinna ruudustikus pole tegeliku ajakulu hinnadimensioonide jaoks ühtki rida, on probleem lahendatud.</span><span class="sxs-lookup"><span data-stu-id="be6b3-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="be6b3-135">Looge tegeliku ajakulu hinnadimensioonidele rida rolli hindade ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="be6b3-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="be6b3-136">Kui see on tehtud, looge ajakirje uuesti, kinnitage see ja veenduge, et tegelikus ajakulus kuvataks kehtiv hind.</span><span class="sxs-lookup"><span data-stu-id="be6b3-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="be6b3-137">Kui te pärast ülaltoodud kolme kontrolli ei näe tegeliku ajakulu kehtivat hinda, esitage tugiteenusepilet.</span><span class="sxs-lookup"><span data-stu-id="be6b3-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



