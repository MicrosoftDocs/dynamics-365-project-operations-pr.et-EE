---
title: Hinnakujunduse dimensiooni väljalülitamine
description: Selles teemas kirjeldatakse, kuidas lülitada hinnakujunduse dimensioone välja.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274723"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="8cb28-103">Hinnakujunduse dimensiooni väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="8cb28-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="8cb28-104">_**Rakendub:** Project Operationsi ressurssipõhiste/mitteaktsiapõhiste stsenaariumide korral,  Lihtjuurutamine - tehing fiktiivsele arveldusele_</span><span class="sxs-lookup"><span data-stu-id="8cb28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8cb28-105">Võimalik, et peate iga paari aasta tagant oma hinnakujunduse strateegia üle vaatama ja seda värskendama.</span><span class="sxs-lookup"><span data-stu-id="8cb28-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="8cb28-106">Teie tehtud värskendused võivad nõuda olemasoleva hinnakujunduse dimensiooni väljalülitamist ja uue loomist.</span><span class="sxs-lookup"><span data-stu-id="8cb28-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="8cb28-107">Näiteks võib juhtuda, et olete varem määranud hinna **Rolli** järgi, kuid nüüd olete otsustanud määrata hinna **Töökogemuse** järgi.</span><span class="sxs-lookup"><span data-stu-id="8cb28-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="8cb28-108">Võib juhtuda, et peate selleks **Rolli** hinnakujunduse dimensioonina välja lülitama ja looma **Töökogemuse** uue hinnakujunduse dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="8cb28-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="8cb28-109">Hinnakujunduse dimensiooni saab välja lülitada (olenemata sellest, kas see on valmis või kohandatud), kui seate hinnakujunduse dimensiooni väljade **Kehtib kulu kohta** ja **Kehtib müügi kohta** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="8cb28-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="8cb28-110">Kuid seda tehes võidakse kuvada tõrketeade, **Hinnakujunduse dimensiooni ei saa värskendada ega kustutada, kui seostuvad hinnakirjad on olemas.**</span><span class="sxs-lookup"><span data-stu-id="8cb28-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Äriprotsessi tõrge tõenäoliselt hinnakujunduse dimensiooni väljalülitamisest](media/Business-Process-Error.png)

<span data-ttu-id="8cb28-112">See tõrketeade näitab, et on olemas hinnakirjed, mis on väljalülitatava dimensiooni jaoks juba varem seadistatud.</span><span class="sxs-lookup"><span data-stu-id="8cb28-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="8cb28-113">Enne kui dimensiooni kohaldatavust saab seada väärtusele **Ei**, tuleb kustutada kõik dimensioonile viitavad **Rolli hinna** ja **Rolli hinna hinnalisandi** kirjed.</span><span class="sxs-lookup"><span data-stu-id="8cb28-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="8cb28-114">See reegel kehtib nii valmishinnakujunduse dimensioonide kui ka kõigile teie loodud kohandatud hinnakujunduse dimensioonidele.</span><span class="sxs-lookup"><span data-stu-id="8cb28-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="8cb28-115">Selle valideerimise põhjuseks on asjaolu, et igal **Rolli hinna** kirjel peab olema kordumatu dimensioonide kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="8cb28-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="8cb28-116">Näiteks hinnakirjas **US Cost Rates 2018** (USA 2018. aasta kulumäärad) on teil olemas järgmised **Rolli hinna** read.</span><span class="sxs-lookup"><span data-stu-id="8cb28-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="8cb28-117">Standardpealkiri</span><span class="sxs-lookup"><span data-stu-id="8cb28-117">Standard Title</span></span>         | <span data-ttu-id="8cb28-118">Organisatsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="8cb28-118">Org Unit</span></span>    |<span data-ttu-id="8cb28-119">Ühik</span><span class="sxs-lookup"><span data-stu-id="8cb28-119">Unit</span></span>   |<span data-ttu-id="8cb28-120">Hind</span><span class="sxs-lookup"><span data-stu-id="8cb28-120">Price</span></span>  |<span data-ttu-id="8cb28-121">Valuuta</span><span class="sxs-lookup"><span data-stu-id="8cb28-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="8cb28-122">Süsteemiinsener</span><span class="sxs-lookup"><span data-stu-id="8cb28-122">Systems Engineer</span></span>|<span data-ttu-id="8cb28-123">Jõgi US</span><span class="sxs-lookup"><span data-stu-id="8cb28-123">Contoso US</span></span>|<span data-ttu-id="8cb28-124">Hour</span><span class="sxs-lookup"><span data-stu-id="8cb28-124">Hour</span></span>| <span data-ttu-id="8cb28-125">100</span><span class="sxs-lookup"><span data-stu-id="8cb28-125">100</span></span>|<span data-ttu-id="8cb28-126">USD</span><span class="sxs-lookup"><span data-stu-id="8cb28-126">USD</span></span>|
| <span data-ttu-id="8cb28-127">Süsteemi vaneminsener</span><span class="sxs-lookup"><span data-stu-id="8cb28-127">Senior Systems Engineer</span></span>|<span data-ttu-id="8cb28-128">Jõgi US</span><span class="sxs-lookup"><span data-stu-id="8cb28-128">Contoso US</span></span>|<span data-ttu-id="8cb28-129">Hour</span><span class="sxs-lookup"><span data-stu-id="8cb28-129">Hour</span></span>| <span data-ttu-id="8cb28-130">150</span><span class="sxs-lookup"><span data-stu-id="8cb28-130">150</span></span>| <span data-ttu-id="8cb28-131">USD</span><span class="sxs-lookup"><span data-stu-id="8cb28-131">USD</span></span>|


<span data-ttu-id="8cb28-132">Kui lülitate **Standardpealkirja** hinnakujunduse dimensioonina välja ja hinnakujunduse mootor otsib hinda, kasutab see ainult **Org. üksuse** väärtust sisendi kontekstist.</span><span class="sxs-lookup"><span data-stu-id="8cb28-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="8cb28-133">Kui sisendi konteksti **Org. üksus** on „Jõgi US”, on tulemus mittedeterministlik, sest mõlemad read on ühesugused.</span><span class="sxs-lookup"><span data-stu-id="8cb28-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="8cb28-134">Selle stsenaariumi vältimiseks kontrollib süsteem, et **Rolli hinna** kirjete loomisel oleks dimensioonide kombinatsioon kordumatu.</span><span class="sxs-lookup"><span data-stu-id="8cb28-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="8cb28-135">Kui dimensioon lülitatakse pärast **Rolli hinna** kirjete loomist välja, saab seda piirangut rikkuda.</span><span class="sxs-lookup"><span data-stu-id="8cb28-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="8cb28-136">Seetõttu on nõutav, et enne dimensiooni väljalülitamist kustutaksite te ära kõik need **Rolli hinna** ja **Rolli hinna hinnalisandi** read, millel on dimensiooni väärtus täidetud.</span><span class="sxs-lookup"><span data-stu-id="8cb28-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]