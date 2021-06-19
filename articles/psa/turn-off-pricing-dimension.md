---
title: Hinnakujunduse dimensiooni väljalülitamine
description: Selles teemas kirjeldatakse, kuidas Project Service’i lahenduses seadistada hinnakujunduse dimensioone.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014291"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="615eb-103">Hinnakujunduse dimensiooni väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="615eb-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="615eb-104">Võimalik, et peate iga paari aasta tagant oma hinnakujunduse strateegia üle vaatama ja seda värskendama.</span><span class="sxs-lookup"><span data-stu-id="615eb-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="615eb-105">Teie tehtud värskendused võivad nõuda olemasoleva hinnakujunduse dimensiooni väljalülitamist ja uue loomist.</span><span class="sxs-lookup"><span data-stu-id="615eb-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="615eb-106">Näiteks võib juhtuda, et olete varem määranud hinna **Rolli** järgi, kuid nüüd olete otsustanud määrata hinna **Töökogemuse** järgi.</span><span class="sxs-lookup"><span data-stu-id="615eb-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="615eb-107">Võib juhtuda, et peate selleks **Rolli** hinnakujunduse dimensioonina välja lülitama ja looma **Töökogemuse** uue hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="615eb-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="615eb-108">Hinnakujunduse dimensiooni saab välja lülitada (olenemata sellest, kas see on valmis või kohandatud), kui seate hinnakujunduse dimensiooni väljade **Kehtib kulu kohta** ja **Kehtib müügi kohta** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="615eb-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="615eb-109">Seda tehes võidakse teile aga kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="615eb-109">However, when you do this, you might receive the following error message.</span></span>

![Äriprotsessi tõrge tõenäoliselt hinnakujunduse dimensiooni väljalülitamisest](media/Business-Process-Error.png)


<span data-ttu-id="615eb-111">See tõrketeade näitab, et on olemas hinnakirjed, mis on väljalülitatava dimensiooni jaoks juba varem seadistatud.</span><span class="sxs-lookup"><span data-stu-id="615eb-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="615eb-112">Enne kui dimensiooni kohaldatavust saab seada väärtusele **Ei**, tuleb kustutada kõik dimensioonile viitavad **Rolli hinna** ja **Rolli hinna hinnalisandi** kirjed.</span><span class="sxs-lookup"><span data-stu-id="615eb-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="615eb-113">See reegel kehtib nii valmishinnakujunduse dimensioonide kui ka kõigile teie loodud kohandatud hinnakujunduse dimensioonidele.</span><span class="sxs-lookup"><span data-stu-id="615eb-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="615eb-114">Selle valideerimise põhjuseks on asjaolu, et Project Service’il on piirang, mille järgi iga **Rolli hinna** kirjel peab olema kordumatu dimensioonide kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="615eb-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="615eb-115">Näiteks hinnakirjas **US Cost Rates 2018** (USA 2018. aasta kulumäärad) on teil olemas järgmised **Rolli hinna** read.</span><span class="sxs-lookup"><span data-stu-id="615eb-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="615eb-116">Standardpealkiri</span><span class="sxs-lookup"><span data-stu-id="615eb-116">Standard Title</span></span>         | <span data-ttu-id="615eb-117">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="615eb-117">Org Unit</span></span>    |<span data-ttu-id="615eb-118">Üksus</span><span class="sxs-lookup"><span data-stu-id="615eb-118">Unit</span></span>   |<span data-ttu-id="615eb-119">Hind</span><span class="sxs-lookup"><span data-stu-id="615eb-119">Price</span></span>  |<span data-ttu-id="615eb-120">Valuuta</span><span class="sxs-lookup"><span data-stu-id="615eb-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="615eb-121">Süsteemiinsener</span><span class="sxs-lookup"><span data-stu-id="615eb-121">Systems Engineer</span></span>|<span data-ttu-id="615eb-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="615eb-122">Contoso US</span></span>|<span data-ttu-id="615eb-123">tund</span><span class="sxs-lookup"><span data-stu-id="615eb-123">Hour</span></span>| <span data-ttu-id="615eb-124">100</span><span class="sxs-lookup"><span data-stu-id="615eb-124">100</span></span>|<span data-ttu-id="615eb-125">USD</span><span class="sxs-lookup"><span data-stu-id="615eb-125">USD</span></span>|
| <span data-ttu-id="615eb-126">Süsteemi vaneminsener</span><span class="sxs-lookup"><span data-stu-id="615eb-126">Senior Systems Engineer</span></span>|<span data-ttu-id="615eb-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="615eb-127">Contoso US</span></span>|<span data-ttu-id="615eb-128">tund</span><span class="sxs-lookup"><span data-stu-id="615eb-128">Hour</span></span>| <span data-ttu-id="615eb-129">150</span><span class="sxs-lookup"><span data-stu-id="615eb-129">150</span></span>| <span data-ttu-id="615eb-130">USD</span><span class="sxs-lookup"><span data-stu-id="615eb-130">USD</span></span>|


<span data-ttu-id="615eb-131">Kui lülitate **Standardpealkirja** hinnakujunduse dimensioonina välja ja Project Service’i mootor otsib hinda, kasutab see ainult **Org. üksuse** väärtust sisendi kontekstist.</span><span class="sxs-lookup"><span data-stu-id="615eb-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="615eb-132">Kui sisendkonteksti **Org. üksus** on „Contoso USA”, on tulemus mittedeterministlik, sest mõlemad read on ühesugused.</span><span class="sxs-lookup"><span data-stu-id="615eb-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="615eb-133">Selle stsenaariumi vältimiseks kontrollib Project Service, et **Rolli hinna** kirjete loomisel oleks dimensioonide kombinatsioon kordumatu.</span><span class="sxs-lookup"><span data-stu-id="615eb-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="615eb-134">Kui dimensioon lülitatakse pärast **Rolli hinna** kirjete loomist välja, saab seda piirangut rikkuda.</span><span class="sxs-lookup"><span data-stu-id="615eb-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="615eb-135">Seetõttu on nõutav, et enne dimensiooni väljalülitamist kustutaksite te ära kõik need **Rolli hinna** ja **Rolli hinna hinnalisandi** read, millel on dimensiooni väärtus täidetud.</span><span class="sxs-lookup"><span data-stu-id="615eb-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]