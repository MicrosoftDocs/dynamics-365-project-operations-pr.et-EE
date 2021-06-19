---
title: Hankija maksete kinnipidamise tingimuste loomine ja rakendamine
description: Selles teemas antakse teavet, kuidas seadistada ja hallata hankija maksete kinnipidamise tingimusi.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006316"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="88106-103">Hankija maksete kinnipidamise tingimuste loomine ja rakendamine</span><span class="sxs-lookup"><span data-stu-id="88106-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="88106-104">Projekti jaoks hankija maksete kinnipidamise tingimuste seadistamine on kasulik juhul, kui teie organisatsioon soovib säilitada osa hankijale tehtud maksetest.</span><span class="sxs-lookup"><span data-stu-id="88106-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="88106-105">Näiteks juhul, kui soovite hankija maksed ootele panna, kuni tarnitud tooted teie ootustele vastavad.</span><span class="sxs-lookup"><span data-stu-id="88106-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="88106-106">Hankija maksete kinnipidamise tingimusi saab määrata hankijaga lepingu läbirääkimisi pidades.</span><span class="sxs-lookup"><span data-stu-id="88106-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="88106-107">Hankija maksete kinnipidamise tingimuste loomine</span><span class="sxs-lookup"><span data-stu-id="88106-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="88106-108">Saate sisestada hankija maksete kinnipidamise protsendi ja varasemalt kinnipeetud summade, mis vabastatakse, protsendi.</span><span class="sxs-lookup"><span data-stu-id="88106-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="88106-109">Summad peetakse automaatselt hankija arvetel kinni, kuni leping jõuab määratud olekuni.</span><span class="sxs-lookup"><span data-stu-id="88106-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="88106-110">Pärast kinnipidamise tingimuste seadistamist saate need rakendada selle hankija mis tahes projektile.</span><span class="sxs-lookup"><span data-stu-id="88106-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="88106-111">Kasutage järgmisi juhiseid hankija maksete kinnipidamise tingimuste seadistamiseks ja haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="88106-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="88106-112">Minge jaotisse **Projektihaldus ja raamatupidamine** > **Kinnipidamine** > **Hankija maksete kinnipidamise tingimused**.</span><span class="sxs-lookup"><span data-stu-id="88106-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="88106-113">Valige **Uus**, et lisada uus hankija kinnipidamise tingimus.</span><span class="sxs-lookup"><span data-stu-id="88106-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="88106-114">Uue tingimuse väärtus **Reegli ID** sisestatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="88106-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="88106-115">Sisestage lühikirjeldus väljale **Kirjeldus** ja valige seejärel FastTabilt **Tingimused** ja seejärel **Lisa rida**, et sisestada järgmisele tingimuse väärtused.</span><span class="sxs-lookup"><span data-stu-id="88106-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="88106-116">**Tarnitud ühikute protsent**: sisestage tingimuse täitmise protsent.</span><span class="sxs-lookup"><span data-stu-id="88106-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="88106-117">Summad peetakse automaatselt hankija arvetel kinni, kuni projekti valmisoleku etapp võrdub määratud protsendiga.</span><span class="sxs-lookup"><span data-stu-id="88106-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="88106-118">Näiteks kui sisestate 50,00, peetakse summad kinni, kuni projekt on 50 protsendi ulatuses valmis.</span><span class="sxs-lookup"><span data-stu-id="88106-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="88106-119">**Kinnipeetav protsent** : sisestage hankija arvelt kinnipeetava summa protsent.</span><span class="sxs-lookup"><span data-stu-id="88106-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="88106-120">Näiteks juhul, kui sisestate 10,00, peetakse 10 protsenti hankija arve summast kinni seni, kuni projekt saavutab protsendi, mis on seatud väljal **Välja tarnitud ühikute protsent**.</span><span class="sxs-lookup"><span data-stu-id="88106-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="88106-121">**Vabastatav protsent**: valige suvand **Lisa rida**, et sisestada protsent varem kinnipeetud summadest, mis tuleb vabastada valitud projekti taseme saavutamisel.</span><span class="sxs-lookup"><span data-stu-id="88106-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="88106-122">Kui teil on projekti täitmise erinevatel tasemetel rohkem kui üks vahe-eesmärk, sisestage iga kinnipidamise tingimuse jaoks eraldi tarnija kinnipidamise tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="88106-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="88106-123">Iga rida saab määrata erineva kinnipidamise protsendi ja iga määratud taseme projekti lõpuleviimiseks erineva vabastamise protsendi.</span><span class="sxs-lookup"><span data-stu-id="88106-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="88106-124">Pärast hankijale hankija kinnipidamise tingimuste loomist saate need tingimused projektile rakendada.</span><span class="sxs-lookup"><span data-stu-id="88106-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="88106-125">Hankija kinnipidamise tingimuste rakendamine projektile</span><span class="sxs-lookup"><span data-stu-id="88106-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="88106-126">Minge jaotisesse **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja avage projektiloendi lehelt projekt.</span><span class="sxs-lookup"><span data-stu-id="88106-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="88106-127">Valige kiirvahekaardil **Hankija lepingud** käsk **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="88106-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="88106-128">Valige **Konto koodi väljal** üks järgmistest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="88106-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="88106-129">**Tabel**: hankija kinnipidamise tingimused rakenduvad ühele hankijale.</span><span class="sxs-lookup"><span data-stu-id="88106-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="88106-130">**Rühm**: hankija kinnipidamise tingimused rakenduvad kõigile hankijarühma hankijatele.</span><span class="sxs-lookup"><span data-stu-id="88106-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="88106-131">**Kõik**: hankija kinnipidamise tingimused rakenduvad kõikidele hankijatele.</span><span class="sxs-lookup"><span data-stu-id="88106-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="88106-132">Valige **Hankija/hankijarühma väljalt** hankija või hankijarühm, mille jaoks hankija kinnipidamise tingimusi rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="88106-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="88106-133">Kui valisite eelmises etapis suvandi **Kõik**, pole see väli saadaval.</span><span class="sxs-lookup"><span data-stu-id="88106-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="88106-134">Valige väljal **Hankija kinnipidamise tingimused** eelmises protseduuris loodud kinnipidamise tingimused.</span><span class="sxs-lookup"><span data-stu-id="88106-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="88106-135">Kui projektil on ka hankija jaoks seadistatud tasulised (PWP) tingimused, sisestage projekti läviprotsent väljale **PWP läviprotsent**.</span><span class="sxs-lookup"><span data-stu-id="88106-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="88106-136">Hankija kinnipidamise tingimused kuvatakse ka ostutellimustel, mille olete hankija jaoks loonud.</span><span class="sxs-lookup"><span data-stu-id="88106-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]